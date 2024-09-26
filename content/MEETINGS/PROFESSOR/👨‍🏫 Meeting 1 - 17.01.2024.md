
## Omówienie 3 głównych motywacji oduczania [[@Lukasz]]

Źródło: [Nguyen et al., “A Survey of Machine Unlearning.”]

- _**Bezpieczeństwo**_: odporność na ataki
    - Przykład: Wystrzykiwanie niebezpiecznych danych do generowania błędnych predykcji. Model nauczył się na niebezpiecznych danych i teraz musimy oduczyć go błędnych zachowań.
- _**Prywatność**_: chcemy uniemożliwić wyciągnięcie konkretnego przykładu/osoby z danych stojących za modelem
- _**Right to be forgotten**_: ktoś żąda, aby usunąć jego dane i nie trenować na nim modeli
    - Samo usunięcie z danych i nauczenie od nowa może być podatne na ekstrakcję danych poprzez porównanie modelu starego i nowego [Chen et al., “When Machine Unlearning Jeopardizes Privacy.”]
- Survey wymienia też mniej popularne motywacje takie jak:
    - Wierność (ang. Fidelity) - przeciwdziałanie niechcianej stronniczości modelu (praktycznie to samo co Fairness)
    - Użyteczność (ang. Usability) - zmiana preferencji użytkownika (użytkownik nie chce, żeby model do rekomendacji używał konkretnej cechy użytkownika) [Cao and Yang, “Towards Making Systems Forget with Machine Unlearning.”]

Tematy uważane za manipulację danych a nie oduczanie:

- _**Differential privacy**_: techniki ograniczajace wpływ danej uczącej na przykład przez zaszumianie rozkładem Laplace’a
- _**Statistical query learning**_: uczenie się na zagregowanych informacjach a nie na pojedynczych danych
- **Data Masking / Obfuscation**: ukrywanie danych poprzez ich dosłowną manipulację

Oduczanie, systematyczne podejścia:

- **Kwantyzowanie**:
    - Bazowa idea: np kmeans dyskretyzacja/rzutowanie centroidów co iterację poprzez rzutowanie na kratę.
    - Sprawdzamy czy usuwany przykład był wpływowy na rzutowanie w danej iteracji. Jeśli nie, nie musimy nic zmieniać, jeśli tak, trzeba trenować na nowo.
- **SISA**: (popularniejsze)
    - W uproszczeniu - zespoły modeli uczone na różnych podzbiorach danych. Dzięki temu, jeśli ktoś prosi o usunięcie, to możemy nauczyć od nowa tylko te silosy, które tą daną zawierały.

Przeważającym tematem jest right to be forgotten. Wydaje się, że temat wokół SISA jest dość nieskomplikowany i jest pole do proponowania swojej metody.


![[Pasted image 20240904230035.png]]
**ClArC - Class Artifact Compensation Workflow (CLARC)**

- Trzy stopniowe rozwiązanie, które ma poprawić jakość modelu
- Szukamy artefaktu, którego chcemy się pozbyć
- Usuwamy go/niwelujemy wpływ
    - **A-ClArC - Augumentative** - wycinanie artefaktu i dodawanie do wszystkich innych przykładów w celu sprawienia aby ten artefakt nie miał wpływu na klasyfikację. Zakłada dalsze dotrenowanie modelu z takimi próbkami.
    - **P-ClArC - Projective** - projekcja danch na płaszczyznę w punkcie będącym średnią próbek bez artefaktow do której wektor konceptu jest normalny, co eliminuje wpływ artefaktu. Problemem jest znalezienie w sieci odpowiedniego miejsca takiej projekcji, nie przewiduje ona dalszego trenowania.

**PatClArC** - używa PCAV zamiast CAV (Parrern Concept Activation Vectors)

**RR-ClArC** - Right Reason - penalizacja gradientu w kierunku danego konceptu. Pozwala na dobranie per przykład nieporządanych konceptów

**Ignacy**

**Fairness datasets in CV**

**Object-level annotations:**

- MS-COCO
- Open Images

**Person-level annotations:**

- Open Images More Inclusive People Annotations (MIAP)
    - What is labelled: perceived gender and age group
    - Labels are not particularly diverse
- CelebA
    - What is labelled: many person-level attributes including a lot of subjective and potentially harmful, like, attractive, big lips, chubby etc…
- UTK-Faces
- FACET - Fairness in Computer Vision Evaluation Benchmark (2023 meta ai)
    - [https://arxiv.org/pdf/2309.00035.pdf](https://arxiv.org/pdf/2309.00035.pdf)
    - Large-scale evaluation on a lot of labels
    - 13 person attributes like skin tone, hair type, perceived age group
    - 52 person classes like hairdresser or reporter
    - _FACET is an evaluation-only benchmark. Using any of the annotations for training is strictly prohibited._

**Questions / Potential Problems**

1. Are models better at classifying people as skateboarder when their perceived gender has more stereotypically male attributes?
2. Do standard detection models struggle to detect people whenever their skin tone is darker?

**How is fairness solved in deep learning**

- Adding fairness constraints to optimization / learning
- Data Operations like over-sampling minority groups, re-weighting
- Removing sensitive features from numerical data

**Granty:**

- Potencjalnie zapytać Mateusza o młodą kadrę
    - Potencjalnie 2 zpytać Piotrka o młodą kadrę
- Preludium?
- Potencjalnie dopisanie się do OPUS prof. Krawca

**MLowe konferencje**

_ECML_: Marzec 15

_ECAI_ : Kwiecien 28

_SIGKDD_: Sierpien 1

_AAAI_: Sierpien 15

_ICLR_: Połowa września

**Computer Vision**

_ECCV_: Marzec 7

_CVPR_: Listopad