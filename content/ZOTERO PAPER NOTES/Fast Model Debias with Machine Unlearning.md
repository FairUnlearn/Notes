---
tags:
  - zotero
  - literature-note
  - 

title: Fast Model Debias with Machine Unlearning 
authors: Ruizhe Chen, Jianfei Yang, Huimin Xiong, Jianhong Bai, Tianxiang Hu, Jin Hao, Yang Feng, Joey Tianyi Zhou, Jian Wu, Zuozhu Liu 
year: 2023 
keywords: [Computer Science - Machine Learning]
citekey: chenFastModelDebias2023
---

> [!info]+ Metadata [Zotero](zotero://select/library/items/4L6VNQ6F) | [PDF](zotero://open-pdf/library/items/L3Z6R3C7) | [URL](http://arxiv.org/abs/2310.12560)
> 
> **Bibiography:** Chen, Ruizhe, Jianfei Yang, Huimin Xiong, Jianhong Bai, Tianxiang Hu, Jin Hao, Yang Feng, Joey Tianyi Zhou, Jian Wu, and Zuozhu Liu. “Fast Model Debias with Machine Unlearning.” arXiv, November 3, 2023. [http://arxiv.org/abs/2310.12560](http://arxiv.org/abs/2310.12560).
> 
> **Authors:**  [[Ruizhe Chen]],  [[Jianfei Yang]],  [[Huimin Xiong]],  [[Jianhong Bai]],  [[Tianxiang Hu]],  [[Jin Hao]],  [[Yang Feng]],  [[Joey Tianyi Zhou]],  [[Jian Wu]],  [[Zuozhu Liu]]
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
> Recent discoveries have revealed that deep neural networks might behave in a biased manner in many real-world scenarios. For instance, deep networks trained on a large-scale face recognition dataset CelebA tend to predict blonde hair for females and black hair for males. Such biases not only jeopardize the robustness of models but also perpetuate and amplify social biases, which is especially concerning for automated decision-making processes in healthcare, recruitment, etc., as they could exacerbate unfair economic and social inequalities among different groups. Existing debiasing methods suffer from high costs in bias labeling or model re-training, while also exhibiting a deficiency in terms of elucidating the origins of biases within the model. To this respect, we propose a fast model debiasing framework (FMD) which offers an efficient approach to identify, evaluate and remove biases inherent in trained models. The FMD identifies biased attributes through an explicit counterfactual concept and quantifies the influence of data samples with influence functions. Moreover, we design a machine unlearning-based strategy to efficiently and effectively remove the bias in a trained model with a small counterfactual dataset. Experiments on the Colored MNIST, CelebA, and Adult Income datasets along with experiments with large language models demonstrate that our method achieves superior or competing accuracies compared with state-of-the-art methods while attaining significantly fewer biases and requiring much less debiasing cost. Notably, our method requires only a small external dataset and updating a minimal amount of model parameters, without the requirement of access to training data that may be too large or unavailable in practice.
> 

### Notes
%% begin notes %%


%% end notes %%

## Highlights


*Imported: 2024-09-05 13:50*

### ⭕ Very important or questionable

> [!quote|red]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=QZW3TSLB))
> although there is no causal relationship between hair color and gender [9] 

> [!quote|red]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=XL36424T))
> they do not provide explicit illustrations on whether the decisionmaking is based on sensitive/protected attributes 

> [!quote|red]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=WMETXLBL))
> The influence function [64] provides an approximation on the updates to parameters if zk were removed from Dtr with a small coefficient ε. 

> [!quote|red]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=89JP9SHT))
> we can construct the same modification to the protected attribute on external samples 

### ❄Future Implications & Research Ideas

> [!quote|blue]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=K42DU3DC))
> (CNNs) might favor texture over shape for object classification [6] 

> [!quote|blue]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=P6UY4P2C))
> identify whether a sample is helpful or harmful for model predictions 
> - **Label noise?**

> [!quote|blue]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=5CTWMF2A))
> We employ an external dataset Dex 

> [!quote|blue]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=Y45P38WH))
> while keeping xi unchanged 

> [!quote|blue]+ Note ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=P6GR3FIG))
> - **Maths**

> [!quote|blue]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=WR6G5KR3))
> θnew = ˆ θ+ K X k=1 H −1 ˆ θ ∇ˆ θL(zk, ˆ θ), 

> [!quote|blue]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=HSVKD4LG))
> we have observed that the harmful samples heavily lead to biased/error correlations (i.e., bias-aligned) while the helpful samples behave oppositely (i.e., bias-conflicting) 

> [!quote|blue]+ Highlight ([page. 7](zotero://open-pdf/library/items/L3Z6R3C7?page=7&annotation=7R9XHGCH))
> he same target labels but the opposite protected attribute 

> [!quote|blue]+ Image ([page. 9](zotero://open-pdf/library/items/L3Z6R3C7?page=9&annotation=JKUZXZIA))
> ![[Shared_Obsidian/ASSETS/IMAGES/chenFastModelDebias2023/image-chenFastModelDebias2023-9-x283-y509.png]]

> [!quote|blue]+ Highlight ([page. 10](zotero://open-pdf/library/items/L3Z6R3C7?page=10&annotation=5SFIAYJF))
> more analysis on model fairness from different perspectives, which will be in our future plan 

### ✅ Supporting claims

> [!quote|green]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=XQ9Q2XMS))
> preference for specific individuals or groups based on irrelevant attributes (error correlations) 

> [!quote|green]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=PAPTQVH4))
> most methods assume that the biased attributes were known, while a generalized debiasing framework should be able to verify whether an attribute (e.g. shape, texture, and color in an image classification task) is biased or not as well 

> [!quote|green]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=6BPL6USG))
> biased-effect evaluation phase 

> [!quote|green]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=HUYVBAT6))
> Counterfactual Fairness. 

> [!quote|green]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=Q7PZKCSQ))
> fˆ θ is fair on A 

> [!quote|green]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=GZDBUBCJ))
> the latter part calculates the impact of removing on the parameters. 

> [!quote|green]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=PMJAV7BL))
> select the top-K harmful samples 

> [!quote|green]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=UPAWIQXR))
> However, in practice, the training set might be too large or even unavailable in the unlearning phase. 

> [!quote|green]+ Highlight ([page. 7](zotero://open-pdf/library/items/L3Z6R3C7?page=7&annotation=ZR8YLUXM))
> Adult dataset, we flip the protected attribute to the opposite 

> [!quote|green]+ Highlight ([page. 8](zotero://open-pdf/library/items/L3Z6R3C7?page=8&annotation=YTJPTWN5))
> anilla method performed the best in accuracy on both tasks 

### 🟣 Conclusions

> [!quote|purple]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=4F8UE4M6))
> tend to predict a female person to be with blonde hair, and a male to be with black hair 

> [!quote|purple]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=NPUBDPGF))
> extend the theory of influence functions [32] 

> [!quote|purple]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=SPFYZ63J))
> identifying bias from different predictions with counterfactual samples 

> [!quote|purple]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=LM9SUU9R))
> recently extended to characterize the contribution of a given training sample to predictions 

> [!quote|purple]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=IL937LFK))
> The former part corresponds to the derivative of bias with respect to parameters, assessing how changes in parameters affect the bias 

> [!quote|purple]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=KIZJH232))
> where  ̄ zk denotes the bias-conflicting sample of zk 

> [!quote|purple]+ Highlight ([page. 8](zotero://open-pdf/library/items/L3Z6R3C7?page=8&annotation=ABVLY5QX))
> in the real-world dataset, race and gender are biased w.r.t income in both training and test set 

> [!quote|purple]+ Highlight ([page. 10](zotero://open-pdf/library/items/L3Z6R3C7?page=10&annotation=NCLM8EI2))
> our method is not applicable to black-box models, which are of high interest in real-world scenarios 

### ⭐Summary, Definitions, Concepts

> [!quote|yellow]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=EDL9MP4J))
> iases not only jeopardize the robustness of models but also perpetuate and amplify social biases 

> [!quote|yellow]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=VF6TTJZH))
> does not learn the correct classification strategy 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=Y75WLRAM))
> Existing debiasing mechanisms could be categorized into three types depending on when debiasing is conducted: pre-processing, in-processing, and post-processing 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=P68JUGJI))
> feature-level data augmentation or adversarial training 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=WGQL8YI3))
> ensure group fairness by alternating predictions of some selected samples 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=P58EMBLK))
> all-inclusive framework 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=BE8JRZJH))
> bias identification, biased-effect evaluation, and bias removal 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=MDUGVG2S))
> leverages only a small external dataset, 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=37BLHD5B))
> minimal number of parameters, such as the top MLP layers of pre-trained deep networks 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=T3VAF3XK))
> first step is to ascertain whether and to what extent the model exhibits bias towards the attribute 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=MDYQCX5M))
> model’s predictions change with the attribute variations 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=JKLS87M6))
> employing it to estimate the impact of perturbing a biased attribute within the training data 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=7YXH828Y))
> Newton step 

> [!quote|yellow]+ Highlight ([page. 2](zotero://open-pdf/library/items/L3Z6R3C7?page=2&annotation=Z2J7QRFG))
> We further design an alternative strategy to unlearn biases with the counterfactual external dataset 

> [!quote|yellow]+ Highlight ([page. 3](zotero://open-pdf/library/items/L3Z6R3C7?page=3&annotation=UXMU94WQ))
> group fairness) could be intuitively unfair at the individual level 

> [!quote|yellow]+ Highlight ([page. 3](zotero://open-pdf/library/items/L3Z6R3C7?page=3&annotation=KDRH4K5P))
> counterfactual fairness 

> [!quote|yellow]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=GJNCBW4Q))
> attribute a is highly correlated but wrongly correlated to the prediction 

> [!quote|yellow]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=KBCLAV7F))
> attainable by 

> [!quote|yellow]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=8WP3XB9B))
> Refer to Appendix A for the derivation 

> [!quote|yellow]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=PEF7N6T6))
> After quantifying how biases are learned by the model from harmful samples, the next question is how to remove such biases. 

> [!quote|yellow]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=XDXFUD9U))
> Newton update step 

> [!quote|yellow]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=NRFB3YJ6))
> generalization of the bias function B(ˆ θ) 

> [!quote|yellow]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=3G5ASGGY))
> empirically demonstrate the effectiveness of FMD in deep models 

> [!quote|yellow]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=Z23EK8SC))
> can be precalculated and applied to different ∇ˆ θB(ˆ θ) 

> [!quote|yellow]+ Highlight ([page. 7](zotero://open-pdf/library/items/L3Z6R3C7?page=7&annotation=GPE2WSSP))
> we randomly add another color on the same digit image as the counterfactual sample 

> [!quote|yellow]+ Image ([page. 10](zotero://open-pdf/library/items/L3Z6R3C7?page=10&annotation=ZH9NAZDB))
> ![[Shared_Obsidian/ASSETS/IMAGES/chenFastModelDebias2023/image-chenFastModelDebias2023-10-x352-y323.png]]

> [!quote|yellow]+ Highlight ([page. 10](zotero://open-pdf/library/items/L3Z6R3C7?page=10&annotation=NCRHC629))
> Research on fairness with few/no attribute labels is still in the infant stage [93], and we will further explore it 

### 🍊Important, Interesting, Confusing

> [!quote|orange]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=LM8YY5RY))
> exhibiting a deficiency in terms of elucidating the origins of biases within the model 
> - **Usually the data?**

> [!quote|orange]+ Highlight ([page. 1](zotero://open-pdf/library/items/L3Z6R3C7?page=1&annotation=ZZJENK7E))
> This is because the number of <blonder hair, female> and <black hair, male> image pairs is significantly higher than others 

> [!quote|orange]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=TX4PFW4B))
> research on how such bias is learned from training samples is limited 

> [!quote|orange]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=P54V6ICX))
> difference in predictions 

> [!quote|orange]+ Highlight ([page. 4](zotero://open-pdf/library/items/L3Z6R3C7?page=4&annotation=H3JAY9PK))
> average of individual counterfactual biases 

> [!quote|orange]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=SU9DBCTS))
> bias threshold δ 

### 🔗 References

> [!quote|grey]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=H8KZCCM2))
> Hence, this equation quantifies the influence of removing on the bias. 

### 📅 Vocabulary, Names, Dates, Definitions

> [!quote|magenta]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=H2JVNGYF))
> how each training point zk in the training set Dtr contributes to B(ˆ θ) 

> [!quote|magenta]+ Highlight ([page. 5](zotero://open-pdf/library/items/L3Z6R3C7?page=5&annotation=IETK9SV4))
> first rank the influence Iup,bias(zk, B(ˆ θ)) of every training sample zk in Dtr 

> [!quote|magenta]+ Highlight ([page. 6](zotero://open-pdf/library/items/L3Z6R3C7?page=6&annotation=95EX2RTB))
> corresponding counterfactual sample  ̄ zk 

%% Import Date: 2024-09-05T13:50:44.911+02:00 %%
