### Resume
- Compute (FERS) -> jesteśmy zawieszeni do prawdopodobnie połowy listopada
- Setup techniczny -> Łukasz opis

### Cele
- Najbliższy: poster na ML in PL
	- Na poziomie filozoficznym stawiamy tezę, że oduczanie u źródła, tj. z sieci neuronowej jest znacznie lepsze niż post-hoc kalibracje, ponieważ pozbywa się konceptu z procesu wnioskowania, pozwalając klasyfikatorowi przykładać więcej wagi do reprezentacji poprawnych konceptów. 
	- Celem pierwszej części pracy jest empiryczna weryfikacja czy postawiona teza ma oparcie w rzeczywistości 
	- Na syntetycznym zbiorze danym `coloredMNIST` testować będziemy sensowność naszych pomysłów, tak aby mieć kontrolowane środowisko, w którym będziemy mogli dokładnie zbadać wpływ naszego oduczania. 
	- Znając i kontrolując proces generowania danych jesteśmy w stanie wprowadzać biasy skorelowane z odpowiednimi klasami. 
	- W pierwszej fazie badań wprowadzimy dwa biasy testujące dwa lekko inne problemy
		- `Zlokalizowane`, w formie kolorowego kwadracika w rogu zdjęcia skorelowanego z wybraną klasą
		- `Niezlokalizowane`, w formie kolorowania liczby na kolor czerwony z pewnym prawdopodobieństwem pokolorowania. Konkretnie, dla każdego zdjęcia z każdej klasy będziemy losować czy zostanie ono pokolorowane na czerwono z prawdopodobieństwem `p`. Zdjęcia z jednej z klas, będą posiadać wyższe prawdopodobieństwo pokolorowania `p + epsilon` co efektywnie powinno wprowadzić bias
	- Na początku, używając znanych nam biasów będziemy testować, czy jesteśmy w stanie zlokalizować / wykryć różnicę w aktywacjach pomiędzy zdjęciami z konceptem koloru czerwonego, a bez niego
	- Intuicyjnie: $$ neuron\_biasedness = \frac{\sum{LRP(D_{biased})}}{N_{biased}} - \frac{\sum{LRP(D_{unbiased})}}{N_{unbiased}}$$
	- Kolejno, jeśli uda się znaleźć w powyższym pewien sygnał, będziemy chcieli użyć go do oduczania i badać poprawę na różnych miarach group fairness, accuracy, fairness na logitach

### MVP Inżynierki
Minimalny produkt, który chcemy dostarczyć to open-source biblioteka do zapewniania fairness przy użyciu technik oduczania
	- Skupiamy się tylko na `group fairness`, w tym np. na `statistical parity` (equality of rate of positive predictions) i `equalized odds` (fp = fn). Docelowo to użytkownik decyduje jaka miara go interesuje
		- As in Buyl and De Bie 2024 "Inherent limitations of AI fairness" paper, paraphrasing, there is no universal fairness definition and the choice of mathematical proxy has to carefully selected. Also, "Technical tools for AI fairness should be flexible in how fairness is formalized [...]"
	- Przygotowujemy zestaw otagowanych datasetów, tak aby mieć możliwość dzielenia zdjęć na grupy zawierające dany koncept, jak i te bez niego
		- Datasety to np. CelebA gdzie dostęp jest do wielu atrybutów dotyczących twarzy
	- Biblioteka ma umożliwić włożenie modelu w PyTorchu i automatyczne oduczenie wybranych konceptów przy użyciu (otagowanych) zbiorów danych zebranych przez nas
