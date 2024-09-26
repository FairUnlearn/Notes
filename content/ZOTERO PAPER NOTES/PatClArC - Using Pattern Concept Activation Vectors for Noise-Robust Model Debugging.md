---
tags:
  - zotero
  - literature-note
title:PatClArC: Using Pattern Concept Activation Vectors for Noise-Robust Model Debugging 
authors: Frederik Pahde, Leander Weber, Christopher J. Anders, Wojciech Samek, Sebastian Lapuschkin 
year: 2022 
keywords: [Computer Science - Machine Learning, Computer Science - Artificial Intelligence, Computer Science - Computer Vision and Pattern Recognition]
citekey: pahdePatClArCUsingPattern2022
---

> [!info]+ Metadata [Zotero](zotero://select/groups/5331428/items/MIR29B29) | [PDF](zotero://open-pdf/library/items/W5B425ZH) | [URL](http://arxiv.org/abs/2202.03482)
> 
> **Bibiography:** Pahde, Frederik, Leander Weber, Christopher J. Anders, Wojciech Samek, and Sebastian Lapuschkin. “PatClArC: Using Pattern Concept Activation Vectors for Noise-Robust Model Debugging.” arXiv, February 7, 2022. [http://arxiv.org/abs/2202.03482](http://arxiv.org/abs/2202.03482).
> 
> **Authors:**  [[Frederik Pahde]],  [[Leander Weber]],  [[Christopher J. Anders]],  [[Wojciech Samek]],  [[Sebastian Lapuschkin]]
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
> State-of-the-art machine learning models are commonly (pre-)trained on large benchmark datasets. These often contain biases, artifacts, or errors that have remained unnoticed in the data collection process and therefore fail in representing the real world truthfully. This can cause models trained on these datasets to learn undesired behavior based upon spurious correlations, e.g., the existence of a copyright tag in an image. Concept Activation Vectors (CAV) have been proposed as a tool to model known concepts in latent space and have been used for concept sensitivity testing and model correction. Specifically, class artifact compensation (ClArC) corrects models using CAVs to represent data artifacts in feature space linearly. Modeling CAVs with filters of linear models, however, causes a significant influence of the noise portion within the data, as recent work proposes the unsuitability of linear model filters to find the signal direction in the input, which can be avoided by instead using patterns. In this paper we propose Pattern Concept Activation Vectors (PCAV) for noise-robust concept representations in latent space. We demonstrate that pattern-based artifact modeling has beneficial effects on the application of CAVs as a means to remove influence of confounding features from models via the ClArC framework.
> 

### Notes
%% begin notes %%


%% end notes %%

## Highlights


*Imported: 2024-09-05 15:07*

### ⭕ Very important or questionable

> [!quote|red]+ Highlight ([page. 3](zotero://open-pdf/library/items/W5B425ZH?page=3&annotation=IVESMTC6))
> also a distractor part, e.g., from noise in the data 

### ⭐Summary, Definitions, Concepts

> [!quote|yellow]+ Highlight ([page. 3](zotero://open-pdf/library/items/W5B425ZH?page=3&annotation=4Y68FN87))
> Artifact Removal and Model Debugging Due to the increased awareness of Clever Hans artifacts in training sets, several approaches have been developed that aim at unlearning specified model behavior. Simply removing affected samples is commonly not desirable, as these samples can still contain valuable features, particularly in the low data regime. eXplanatory Interactive Learning uses a human-in-the-loop, who provides feedback on local explanations by replacing Clever Hans artifacts in training samples with noise [Teso and Kersting, 2019]. Learning not to Learn was introduced as a regularization algorithm in which an artifact detector is added to the network and artifactual features are unlearned by minimizing shared information between embedded features and target biases [Kim et al., 2019]. Ross et al. [2017] guide the model training by penalizing attribution scores in undesired regions by appending an additional attribution-based regularization term to the loss function. Similarly, Rieger et al. [2020] introduced Contextual Decomposition Explanation Penalization, a method leveraging local explanations and domain knowledge to add an explanation error term to the optimization objective. Note that the latter two approaches require sample-wise ground-truth explanations, which are expensive and often infeasible to obtain. ClArC [Anders et al., 2022] is a framework that uses CAVs to represent artifacts in latent space to unlearn the model behavior directly caused by artifacts. Practically, the model is corrected either by fine-tuning on a dataset where samples from all classes are augmented with the artifact using the CAV, or by removing the artifact direction (i.e., CAV direction) from samples by a projection in feature space at test time. Our method extends the ClArC framework by introducing a more noise-robust PCAV. 
> - **Unlearning specified model behavior. DOBRA MOTYWACJA**

%% Import Date: 2024-09-05T15:08:02.238+02:00 %%
