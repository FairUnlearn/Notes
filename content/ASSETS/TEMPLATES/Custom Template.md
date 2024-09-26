---
tags:
  - zotero
  - literature-note
  - {{publicationTitle}}

title: {{ title }} 
authors: {{ authors }} 
year: {{ date | format("YYYY") }} 
keywords: [{{ allTags }}]
citekey: {{citekey}}
---

> [!example]+ Metadata [Zotero]({{desktopURI}}) | {%- for attachment in attachments | filterby("path", "endswith", ".pdf") %} [PDF](zotero://open-pdf/library/items/{{attachment.itemKey}}){%- endfor %}{% if DOI %} | [DOI:{{DOI}}](http://doi.org/{{DOI}}){% elif ISBN %} | ISBN: {{ISBN}}{% endif %}{%if url %} | [URL]({{url}}){% endif %}
> 
> **Bibiography:** {{bibliography}}
> 
> **Authors:** {% for a in creators %} [[{{a.firstName}} {{a.lastName}}]]{% if not loop.last %}, {% endif %}{% endfor %}
> 
>{% if itemType %}**ItemType**: {{itemType}}{% endif %}  
> 
>{% if itemType == "journalArticle" %}**Journal**: _{{publicationTitle}}_{% endif %}
>
> {% if itemType == "bookSection" %}**Book**: {{publicationTitle}} {% endif %}
> 
> **Related**: {% for relation in relations %} {% if relation.citekey %} [[{{relation.citekey}}]], {% endif %} {% endfor %}


> [!abstract]- 
> {% if abstractNote %} 
> {{abstractNote|replace("\n"," ")}}
> {% endif %}

{% persist "notes" %}

> [!attention]- Skim Notes
> **What this paper introduce?**
>  - 
> 
> **Is this novel concept?**
>  - 
> 
> **How they approached it?**
>  - 
> 
> **What are the results?**
>  - 
> 
> **What are the implcations?**
>  - 

> [!note]- Deep Notes
> **What this paper introduce?**
>  - 
> 
> **Is this novel concept?**
>  - 
> 
> **How they approached it?**
>  - 
> 
> **What are the results?**
>  - 
> 
> **What are the implcations?**
>  - 

{% endpersist %}
## Highlights

{%-
    set zoteroColors = {
	    "#2ea8e5": "blue",
        "#5fb236": "green",
        "#a28ae5": "purple",
        "#ff6666": "red",
        "#ffd400": "yellow",
        "#f19837": "orange",
        "#aaaaaa": "grey",
        "#e56eee": "magenta"
    }
-%}

{%-
   set colorHeading = {
		"red": "⭕ Very important or questionable",
		"blue": "❄Future Implications & Research Ideas",
		"green": "✅ Supporting claims",
		"purple": "🟣 Conclusions",
		"yellow": "⭐Summary, Definitions, Concepts",
		"orange": "🍊Important, Interesting, Confusing",
		"grey": "🔗 References",
		"magenta": "📅 Vocabulary, Names, Dates, Definitions"
   }
-%}

{%- macro calloutHeader(type) -%}
    {%- switch type -%}
        {%- case "highlight" -%}
        Highlight
        {%- case "image" -%}
        Image
        {%- default -%}
        Note
    {%- endswitch -%}
{%- endmacro %}

{%- set newAnnot = [] -%}
{%- set newAnnotations = [] -%}
{%- set annotations = annotations | filterby("date", "dateafter", lastImportDate) %}

{% if annotations.length > 0 %}
*Imported: {{importDate | format("YYYY-MM-DD HH:mm")}}*

{%- for annot in annotations -%}

    {%- if annot.color in zoteroColors -%}
        {%- set customColor = zoteroColors[annot.color] -%}
    {%- elif annot.colorCategory|lower in colorHeading -%}
    	{%- set customColor = annot.colorCategory|lower -%}
    {%- else -%}
	    {%- set customColor = "other" -%}
    {%- endif -%}

    {%- set newAnnotations = (newAnnotations.push({"annotation": annot, "customColor": customColor}), newAnnotations) -%}

{%- endfor -%}

{#- INSERT ANNOTATIONS -#}
{#- Loops through each of the available colors and only inserts matching annotations -#}
{#- This is a workaround for inserting categories in a predefined order (instead of using groupby & the order in which they appear in the PDF) -#}

{%- for color, heading in colorHeading -%}
{%- for entry in newAnnotations | filterby ("customColor", "startswith", color) -%}
{%- set annot = entry.annotation -%}

{%- if entry and loop.first %}

### {{colorHeading[color]}}
{%- endif %}

> [!quote{{"|" + color if color != "other"}}]+ {{calloutHeader(annot.type)}} ([page. {{annot.pageLabel}}](zotero://open-pdf/library/items/{{annot.attachment.itemKey}}?page={{annot.pageLabel}}&annotation={{annot.id}}))

{%- if annot.annotatedText %}
> {{annot.annotatedText|nl2br}} {% if annot.hashTags %}{{annot.hashTags}}{% endif -%}
{%- endif %}

{%- if annot.imageRelativePath %}
> ![[{{annot.imageRelativePath}}]]
{%- endif %}

{%- if annot.ocrText %}
> {{annot.ocrText}}
{%- endif %}

{%- if annot.comment %}
> - **{{annot.comment|nl2br}}**
{%- endif -%}

{%- endfor -%}
{%- endfor -%}
{% endif %}