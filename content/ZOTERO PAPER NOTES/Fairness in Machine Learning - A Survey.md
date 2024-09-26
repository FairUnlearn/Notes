---
tags:
  - zotero
  - literature-note
title: "Fairness in Machine Learning: A Survey"
authors: Simon Caton, Christian Haas
year: 2020
keywords:
  - Computer Science - Machine Learning
  - Statistics - Machine Learning
citekey: catonFairnessMachineLearning2020
---

> [!info]+ Metadata [Zotero](zotero://select/groups/5331428/items/3WFGH37U) | [PDF](zotero://open-pdf/library/items/AQTRKSLR) | [DOI:10.48550/arXiv.2010.04053](http://doi.org/10.48550/arXiv.2010.04053) | [URL](http://arxiv.org/abs/2010.04053)
> 
> **Bibiography:** Caton, Simon, and Christian Haas. “Fairness in Machine Learning: A Survey.” arXiv, October 4, 2020. [https://doi.org/10.48550/arXiv.2010.04053](https://doi.org/10.48550/arXiv.2010.04053).
> 
> **Authors:**  [[Simon Caton]],  [[Christian Haas]]
> 
>**ItemType**: preprint  
> 
>
>
> 
> 
> **Related**: 


> [!abstract]- 
>  
> As Machine Learning technologies become increasingly used in contexts that affect citizens, companies as well as researchers need to be confident that their application of these methods will not have unexpected social implications, such as bias towards gender, ethnicity, and/or people with disabilities. There is significant literature on approaches to mitigate bias and promote fairness, yet the area is complex and hard to penetrate for newcomers to the domain. This article seeks to provide an overview of the different schools of thought and approaches to mitigating (social) biases and increase fairness in the Machine Learning literature. It organises approaches into the widely accepted framework of pre-processing, in-processing, and post-processing methods, subcategorizing into a further 11 method areas. Although much of the literature emphasizes binary classification, a discussion of fairness in regression, recommender systems, unsupervised learning, and natural language processing is also provided along with a selection of currently available open source libraries. The article concludes by summarising open challenges articulated as four dilemmas for fairness research.
> 

### Notes
%% begin notes %%


%% end notes %%

## Highlights


*Imported: 2024-09-05 15:06*

### ⭐Summary, Definitions, Concepts

> [!quote|yellow]+ Highlight ([page. 1](zotero://open-pdf/library/items/AQTRKSLR?page=1&annotation=93B4YJAZ))
> Although much of the literature emphasizes 

> [!quote|yellow]+ Highlight ([page. 4](zotero://open-pdf/library/items/AQTRKSLR?page=4&annotation=WKC8AN8V))
> Thus, pre-processing approaches tend to alter the sample distributions of protected variables, or more generally perform specific transformations on the data with the aim to remove discrimination from the training data [155] 

> [!quote|yellow]+ Highlight ([page. 4](zotero://open-pdf/library/items/AQTRKSLR?page=4&annotation=WRQVLW2W))
> In-processing approaches tackle this by often incorporating one or more fairness metrics into the model optimization functions in a bid to converge towards a model parameterization that maximizes performance and fairness. 

> [!quote|yellow]+ Highlight ([page. 4](zotero://open-pdf/library/items/AQTRKSLR?page=4&annotation=4UPV77FU))
> Thus, post-processing approaches tend to apply transformations to model output to improve prediction fairness. Post-processing is one of the most flexible approaches as 

> [!quote|yellow]+ Highlight ([page. 5](zotero://open-pdf/library/items/AQTRKSLR?page=5&annotation=JNJC78VC))
> t only needs access to the predictions and sensitive attribute information, without requiring access to the actual algorithms and ML models 

> [!quote|yellow]+ Highlight ([page. 18](zotero://open-pdf/library/items/AQTRKSLR?page=18&annotation=TPJXIM6S))
> However, when implementing fairness measures, we must emphasize either fairness or model performance as improving one can often detriment the other [27, 87, 73, 129, 296, 54, 124]. [96] do, however, note that a reduction in accuracy may in fact be the desired result, if it was discrimination in the first place that raised accuracy 

%% Import Date: 2024-09-05T15:06:14.270+02:00 %%
