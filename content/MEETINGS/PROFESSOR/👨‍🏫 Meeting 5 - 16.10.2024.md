
Uwagi strukturalne:
1. **Motywacja** - Focused ML - wymieniamy pewne wyzwania współczesnych systemów uczenia maszynowego (językowe, wizyjne, etc.), nie zajmujemy się aspektami prawnymi ale pokazujemy toy examples jak działa fairness w różnych kontekstach - do motywacji - nie lać wody na samym początku, dać sensowne intro, koło tego trzeba zacząć mówić o wyzwaniach w systemach wizyjnych (identify knowledge gap), że są braki w wiedzy/dziedzinie.
   TLDR; przeprowadzamy spójny wywód logiczny, zarysowujemy dziedzinę uczenia moszynowego, identyfikujemy knowledge gap i uderzamy do meritum z problemem który rozwiązujemy.
2. **Aim & Scope of work** - tutaj musimy odwołać się do zidentyfikowanego knowledge gap i opisać w jaki sposób chcemy go załatać konkretnymi zadaniami - realizacja pomysłow stąd jest medium do zasypania knowledge gap. Scope zakończony jest outline’em pracy/oszukane contributions (praca składa się z rozdziałów xyz…) i opisem gdzie w pracy pracy znajdują się najważniejsze/najciekawsze rzeczy.
3. **Literature Review** - do backround należy dorzucić literaturę z unlearning. W części gdzie rozmawiamy o related software piszemy że nie robi on tego co my idealnie chcemy osiągnąć klasyczne biblioteki nie spełniają wszystkich wymagań, zgrubna analiza, dobrze byłoby dorzucić tutaj kilka screenshotów/filmów z related software.
   - [polskojęzyczna książka rekomendowana jako źródło](https://helion.pl/ksiazki/sztuczna-inteligencja-dla-inzynierow-metody-ogolne-mieczyslaw-muraszkiewicz-robert-nowak,e_2p52.htm?srsltid=AfmBOoonfvnPWyzJa0954V8Rb-yc_p3cXmFj3yDrq2I62_SpO7mJN3KD)
4. **Our methods** - przemyśleć tą sekcję, może być potencjalnie zbyt obszerna i trzeba będzie ją podzielić - naszą metodę dać do sekcji którą nazwiemy tak jak ta metoda, etc. Dane same z siebie mogą wymagać opisu (oddzielny rozdział na dane???).
5. **Experiment results**- brak większych uwag.
6. **Use cases and examples** - może mogą być to podrozdziały w experimental results - rekomendowana zmiana nazwy sekcji na practical scenarrios/usage case study.
7. **Conclusions** - brak większych uwag.

Uwagi do Milestones:
1. Przenieść częściowo rzeczy z end of the year na listopad (ICLR Tiny) - tam powinniśmy już próbować przenieść bardziej rozwinięte datasety
2. Zacząć pisać rozdziały listopad/grudzień
3. Dopisać przygotowanie scenariusza (Hypothesis, Research Questions etc.) w listopadzie na eksperymenty

Pomniejsze uwagi:
1. Trzeba będzie napisać streszczenie pracy po polsku.
2. 4. The $F_\beta$ score with $\beta > 1$ is better than the $F_1$ score.




TODO asap:
1. Wymyślić tytuł pracy w języku polskim i w angielskim - 25.10 deadline
2. Zerknąć dokładniej na:
	1. Miary fairness - rekomandowane 6, 3 są już zaimplementowane w Fairlearn
	2. Miary performance - zainspirować się imbalanced data, odezwać się do profesora o artykuł/survey który je zawiera
	3. Loss uczonej sieci - według nas nie jest ważny i metoda powinna być na to agnostic
	4. Loss do oduczania
3. Dać raport o postępach na koniec przyszłego tygodnia (25.10)
4. Zrobić minimal reproduction LRP/CRP



