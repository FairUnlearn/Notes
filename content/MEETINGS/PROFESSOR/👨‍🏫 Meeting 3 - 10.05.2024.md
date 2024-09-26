# Problem statement

Rozpatrujemy problem gdzie chcemy zapewnić optymalny **tradeoff fairness vs performance** w przypadku użycia metod **post-hoc i intra-processing** do debiasingu modeli wizyjnych których uczenie od nowa byloby zbyt kosztowne. Przykładem byłoby zachowanie group fairness w przypadku klasyfikacji zdjęć znamion w celu diagnozy nowotworu. My proponujemy na początku **stworzenie toolkitu do takiego problemu i benchmarking powyższych metod**. Następnie na tej bazie możemy pracować ze zdefiniowanymi przez nas problemami badawczymi z transferowalności oduczania jednego datasetu na inne datasety.

## Gdzie mamy novelty

- samo zastosowanie machine unlearning do fairness
- toolkit sam w sobie jako agregacja metod
- benchmark jest przydatny i publikowalny
- badanie generalizacji/transferu oduczania na dataset klienta
- ocenianie datasetu pod kątem transferu KONCEPTÓW, concept prototypes?

## Pro tips

- Możemy się zwracać po radę do prof. Brzezińskiego jeśli chodzi o imbalance i fariness
- Zgłaszać się na konferencje które są w Polsce
- Spojrzeć na klaster politechniczny w przyszłości (oszacować ile compute i storage potrzebujemy)
- prof. Biecek stwierdził ze najwiecej cytowań ma właśnie z toolkitów publikowanych w softwarewych journalach
- Jeśli dobrze to napiszemy to ten toolkit może być dobrą pracą konferencyjną

## Do zrobienia

Ogólne:

- [ ] Uporządkować całą wiedzę w jeden duzy dokument/blogposty/wiki
- [ ] Zrobić harmonogram
- [ ] Znaleźć journale akceptujące rozwiązania softowe

Infra:

- [x] GitHub
- [ ] External storage dla zbiorów danych
- [ ] Experiment tracking (Lukasz poleca ClearML)

Benchmarking:

- [ ] Wyselekcjonować metody, mogą one zapewniać fairness w różnych ujęciach (nasz interesuje group fairness)
- [ ] Dobrać zbiory do fairness w CV (mogą nam wystarczyć niefairnessowe zbiory), pamiętać o diversity tych zbiorów pod kątem tasków, można wziąć z artykułów prof. Samka
- [x] Dobrać metody CV na których będziemy przeprowadzali debiasing @completed(2024-09-06T16:19:03+02:00)
- [ ] Dobrać miary fairness - niekoniecznie ściśle ortogonalne, mogą być niekompatybilne wewnątrz klastrów (które trzeba doczytać, są wobec nich wątpliwości) [citation Ignacy]
- [ ] Spojrzeć na miary oceny z AutoML

Badanie transferowalności

- [ ] Przemyśleć scenariusz rzeczywisty (case z nowotworem skóry)
    - Może dozwolimy jakieś funkcje oceniające i porównujące dystrybucje i przydatność datasetów?
- [ ] Czy koncepty będą się pokrywały między datasetem użytym do oduczenia a docelowym, użytkowym?
- [ ] Stworzyć globalną charakterystykę konceptów, **prototypy konceptów z fariness**
- [ ] Funkcje opisujące dataset klienta i potencjalnie oceniajace możliwość zapewnienia fairness używając naszych in-house datasetów #DONE