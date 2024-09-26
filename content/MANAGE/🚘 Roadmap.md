Dostęp do compute

Może z TAILOR?

Na poniedziałek

- Chcemy robić Samka adaptację do Fairness jako short term goal
- Chcemy operować na zdjęciach i datasetach które mają etykiety cech
- Musimy znaleźć dataset (y)

Teoretycznie co robimy

- Uczymy model klasyfikacji czegoś np zawodu człowieka na zdjęciu. Np resnet mały i uczymy lokalnie. Na samym końcu najwyżej przerzucimy się na duży duży model pod paper I finał eksperymenty.
- Teraz liczymy jakieś accuracy i metrykę fairness. Potencjalnie znaleźć binarne koncepty które są unfair. Czy biały jest lepiej klasyfikowany niż Asian jako gitarzysta? — tworzymy matrix fairness np biały czarny vs wykrywa nie wykrywa Y i patrzymy czy jest bias
- Ogarnąć który sposób oduczania będziemy używać

Znaleźć dataset

- Pogrupować koncepty I wyodrębnić koncepty które uważamy że są unfair
- Robimy sami labele w taki sposób że bierzemy klasyfikator do np koloru skóry i tworzymy grupy labelowanych konceptów których będziemy potencjalnie chcieli się oduczać. Możemy to zrobić w dwóch wersjach czyli kompletnie auto i auto + ręczny filtering false positive. Ewaluacją FACETEM. To co uczymy nasz główny model klasyfikować musi się pokrywać z jakimiś labelami z FACETA

Btw CycleGANem transfer koloru skóry na tym samym zdjęciu żeby były identyczne obrazki do testowania biasu

TODO:

- wszyscy: papiery do przeczytania z xyz-clarc
- Michał -
- Ignacy
- Łukasz