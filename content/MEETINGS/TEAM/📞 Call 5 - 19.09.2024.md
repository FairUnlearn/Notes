Intra-processing Debiasing, Neural Networks, Vision, Fairness

### Agenda 
1. Jaka struktura kodu do naszego toola jest najlepsza? Czy znamy jakieś paczki, które robią coś podobnego co my?
	1. [Dalex](https://dalex.drwhy.ai/python-dalex-fairness.html)
		1. Ale on jest Scikit-learn based
		2. Ma tylko 3 opcje bias mitigation
	2. Fairlearn
		1. To samo, scikit-learn based
		2. Ma tylko 3 opcje bias mitigation
		3. Jest używany w Azure! (Potencjał dla naszej paczki jeśli będzie FOSS)
	3. Przydała by się paczka która wchodzi w kod Pytorch / Keras
2. Chyba post processing nie ma sensu, trzeba się wziąć z low-hanging fruit - zapuścić RRClarck i sprawdzić fairness
### Surveys 
1. Przeczytane
	1. A Survey of Machine Unlearning
	2. A Survey on Bias and Fairness in Machine Learning (dużo o biasach)
	3. Bias and Fairness in Large Language Models: A Survey (dobre visuals i podział)
	4. Machine Unlearning: A Survey (Takie trochę taxonomy)
	5. Fairness in Machine Learning: A Survey (ogólnie o Fairness, dobra motywacja)
2. Do czytania
	1. [Survey of Social Bias in Vision-Language Models](https://arxiv.org/pdf/2309.14381) - [[@Lukasz]]
	2. [Fairness and Bias Mitigation in Computer Vision: A Survey](https://arxiv.org/abs/2408.02464) - [[@Ignacy]]
	3. [Fairness in Deep Learning: A Survey on Vision and Language Research](https://dl.acm.org/doi/pdf/10.1145/3637549) -[[@Michal]]

### Papiery 
1. Przeczytane
	1. Intra-Processing Methods for Debiasing Neural Networks - [[@Ignacy]]
	2. Unlearning Bias in Language Models by Partitioning Gradients - [[@Lukasz]]
	3. [[Fast Model Debias with Machine Unlearning]] - [[@Lukasz]]
	4. From Hope to Safety: Unlearning Biases of Deep Models via Gradient Penalization in Latent Space (**RR-Clarck**) - [[@Michal]]
2. Do czytania - znaleźć impelmentacje
	1. Reveal to Revise: An Explainable AI Life Cycle for Iterative Bias Correction of Deep Models - [[@Ignacy]] 
	2. Reactive Model Correction: Mitigating Harm to Task-Relevant Features via Conditional Bias Suppression - [[@Michal]] 

