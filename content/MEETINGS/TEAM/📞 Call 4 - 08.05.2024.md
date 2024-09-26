**General:**

Chcemy zminimalizować tradeoff performance vs fairness

Czy możemy powiedzieć right reasons = fairness?

Debiasingiem może być unlearning konceptu

**Use case:**

- Mamy potężne modele i nie opłaca się uczyć od nowa - optymalizujemy hajs
- Regulacje prawne dlatego muszą się oduczyć i wystawić tego certyfikat
    - Wytłumaczenie że postaraliśmy się zweryfikować fairness
    - Toolkit as a service do oduczania

**High-level idea use case:**

### **AutoFair**

**Value:**

1. Chcemy zapewnić fairness w modelach
2. Osiągamy fairness poprzez minimalizację szkodliwości tradeoffu performance-fairness/przy jak najmniejszym spadku performance

**Pomysł**:

1. Zbudować bibliotekę/software, który wykorzysta ileś istniejących metod i wybierze rezultat, który osiąga najlepsze wyniki na predefniowanych miarach jakości i fairness
2. Ideowo, chcemy aby dało się wrzucić dowolny model z PyTorcha/TensorFlow do naszej biblioteki, a my zoptymalizujemy performance-fairness w sposób automatyczny — ewentualnie z wyborem wag przez użytkownika appropo kryteriów

**Badawczo**:

1. Chcemy zacząć od przeprowadzenia szerokiego benchmarku metod intra-processing (i.e., unlearning) oraz post-processing — naszą roboczą hipotezą jest, że unlearning będzie prowadzić do zysku na performance-fairness curve względem post-processing.
2. Zbudować system do automatycznego zapewniania fairness
3. Zbadać transferowalność zapewniania fairness na jakimś open-source datasecie i tego czy rzeczywiście to fairness jest zachowane na oryginalnym datasecie modelu - **transfer unlearning 4 fairness - badanie ood unlearning (unlearning na danych z rozkładu, sprawdzamy generalizację tego processu na ood data (zewnetrzny zbiór)).**
4. Zbadać na toy-toy datasecie czy oduczenie się konceptu pozwoli na transferowalność tego konceptu na dataset o lekko innym rozkładzie (tj. nasz lokalny dataset → dataset prywatny klienta). Teza jest taka, że post-hoc się nie generalizują, a unlearning owszem.

**Plan działania:**

1. Chcemy zbudować benchamark ala samek, gdzie dodamy kilka kolumn fairness, dodamy kilka metod post-hoc fairness i intra-unlearning
2. Przenalizować unlearning vs post-hoc i zobaczyc jakie są relacje pomiędzy performance a fairness

Tentative deadline:

- AAAI’25 Demonstration Track ~15 september —> 2 page short paper + video

---

**Hot takes:**

Metryki wewnatrz notion of fairness (group, individual, etc.) niekoniecznie muszą być ortogonalne, przeciwne. Wiemy o tym ze istnieje tradeoff group vs indivitual:

[A clarification of the nuances in the fairness metrics landscape](https://www.nature.com/articles/s41598-022-07939-1#Sec23)

**Fair Enough: Searching for Sufficient Measures of Fairness**

[https://arxiv.org/pdf/2110.13029](https://arxiv.org/pdf/2110.13029)

- There are many spurious fairness metrics; i.e. metrics that measure very similar things.-
- To simplify fairness testing, just (a) determine what type of fairness is desirable (for a list of types, see Table 4 and Table 5 ); then (b) look up those types in our clusters; then (c) just test for one item per cluster.
- While this approach does not completely remove all issues with fairness testing, it does reduce a very complex problem of (say) 30 metrics to a much smaller and manageable set.

**To the Fairness Frontier and Beyond: Identifying, Quantifying, and Optimizing the Fairness-Accuracy Pareto Frontier**

[https://arxiv.org/pdf/2206.00074](https://arxiv.org/pdf/2206.00074)

Tradeoffs between accuracy vs fairnesss

![[Pasted image 20240904231248.png]]

**Algorithmic fairness datasets: the story so far**

[https://doi.org/10.1007/s10618-022-00854-z](https://doi.org/10.1007/s10618-022-00854-z)