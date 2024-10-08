
### Milestones
1. ML in PL (7.11) deadline na 31.10
	- #todo 
2. ICLR Tiny (9.12) załóżmy 30.11
	- #todo
3. Facct (22.01) załóżmy 15.01
	- #todo 
4. Inżynierka 15.01
	- #todo 
5. ECML (main track w marcu, demo koniec kwietnia)
	- #todo 


###  Roadmap
1. Identify some methodological gap in machine learning practices
2. Literature review (fairness as a whole, unlearning, debiasing)
3. Ideate initial hypotheses
4. Preliminary experiments design
5. Technical environment design and setup
6. Preliminary experiments verifying soundness of posed hypotheses
7. Design comprehensive experiments
8. Create a robust codebase for experiment running
9. Analyze results and draw conclusions about hypotheses

### Structure
1. Motivation
	1. Talk about ML 
	2. Talk about fairness problems
	3. Talk about the possibility of ensuring fairness and that the existing methods have many flaws
	4. Talk about our idea and motivation on why unlearning is better
2. Aim & Scope of work 
	1. What exactly are we going to do here
3. Literature review
	1. Background
		1. Machine learning (classification, learning)
		2. Deep learning (neural networks, training)
		3. Computer vision (CNNs, architectures, detection & classification tasks)
		4. Fairness (metrics, biases, social concerns)
	2. Methods
		1. Explainable AI in images
			1. CAVs (TCAV paper)
			2. Sailency maps (GradCAM, kilka innych, LRP)
			3. CRP
		2. Pre-in-post processing taxonomy
			1. Pre-processing
				1. `TODO`
			2. In-processing
				1. Ross et al "Right for the Right Reasons: Training Differentiable Models by Constraining their Explanations" 
				2. #todo 
			3. Post-processing
				1. #todo 
		3. Debiasing (intra-processing)
			1. Intra-processing 
				1. Savani et al"Intra-Processing Methods for Debiasing Neural Networks"
				2. Chen et al "Fast model debias"
				3. #todo 
			2. Class Artifact Compensation (CLARC)
				1. P-CLARC
				2. Pat-CLARC
				3. A-CLARC
				4. RR-CLARC
	3. Related software ([AIF360](https://github.com/Trusted-AI/AIF360), [Fairlearn](https://github.com/fairlearn/fairlearn), [Aequitas](https://github.com/dssg/aequitas))
4. Our methods (methods section)
	1. Extension of method / our method
	2. Proposed software
	3. Project structure
	4. Datasets
5. Experiment results
6. Use cases and examples
7. Conclusions


## Next steps / TASKS  

***Łukasz***
- Tools for our `coloredMNIST`
- Uzupełnienie lit review  

***Ignacy*** 
- Uzupełnienie lit review
- LRP z backpropem
- Dodać notatkę z BUYL AND DE BIE "Inherent Limitations of AI Fairness"

***Michał***
- LRP z nnsight
- Roadmap
- Setup overleafa

**TODO na później**
- Napisać math z debiasingu i metod, które będziemy robić