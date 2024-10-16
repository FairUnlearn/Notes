 Paper: [Achtibat et al. 2023 - "From attribution maps to human-understandable explanations through Concept Relevance Propagation"](https://www.nature.com/articles/s42256-023-00711-8)
 
As a reminder layer-wise relevance propagation (LRP) goes as follows
Math for the forward pass in neural network (nothing fancy, just a classic forward pass)  
$$
z_{ij} = a_iw_{ij}
$$
$$
z_j = \sum_i z_{ij}
$$
$$
a_j = \sigma(z_j)
$$

Layerwise relevance propagation:  
$$
R_{i~\leftarrow~j} = \frac{z_{ij}}{z_j}R_j
$$
Conditional relevance of a given sample x to some class y (meaning per-class):  
$$
R(x|y)
$$
Concept relevance propagation (CRP) just propagates per-class conditional relevance, so the modification in LRP is that we zero-out all the neurons in the last output layer $L$ and propagate the relevance back from class $y$.     
$$
R_j^L(x|y) = \delta_{iy}{f_j^L(x)}
$$
or maybe that's just conditional relevance...? Nonetheless, we can go even further with constraining the relevancy flow to the concepts we care about. So we can not only be per-class relevant, but also propagate the relevancy through neurons that we believe are important for concepts we care about.  

So, let's define $\theta$ as a set of conditions $c_l$ bound to concepts in layer $l$. What does it exactly mean? hard to tell, but I assume its something like TCAV, so a condition is that layer $l$ (or filter) has to be sensitive to some concept in TCAV terms  

$$
R_{i~\leftarrow~j}^{(l-1,l)} (x|\theta~\cup~\theta_l) = \frac{z_{ij}}{z_j} \sum_{c_l \in \theta_l} \delta_{j~c_l} R_j^l(x|\theta)
$$
It looks complicated, but it's we're just zeroing-out (via Kronecker delta) the relevance coming from the upstream layer $j$ to not propagate it back.    
	*I think it loses the relevance conservation property, no?*


**How to constrain the flow**  
In the paper they were selecting some channels that were relevant (via LRP) to a given class

Notation explained:

![[signal-2024-10-16-102432.jpeg]]
