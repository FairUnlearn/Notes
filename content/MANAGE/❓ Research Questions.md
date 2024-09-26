
**Premise:**

- Modele używają biased conceptów do klasyfikacji, co należy wykazać

**RQ0:** Can we investigate what concepts are actually being used for classification? In an automatic fashion.

- I’m not sure how to formulate this RQ correctly. The main idea is to divide concepts into:
    - Sparse concepts - incorporate some relevancy testing
    - Localized concepts - use YOLO to segment obejcts, then investigate how much CRP do they accumulate inside the rectangle of some detected object

**RQ1:** Can we use LRP-based unlearning methods to effectively unlearn protected (or harmful) concepts in Deep Learning models? (measured by group fairness metrics)

- See literature for fariness in images

**RQ2:** How does the LRP-based concept unlearning influence the model performance (accuracy-wise)? Does bias-accuracy tradeoff, widely known in fairness ML literature, holds for visual concepts unlearning?

**RQ3:** How do LRP-based unlearning methods compare to other post-hoc fairness methods? Do we gain anything by using this framework?

---
**Goal 1: Harmful concept detection - upewnić się że nie ma zadnych publikacji**

We want to investigate if harmful concepts are being used for classification. We prepare a list o harmful concepts and provide an unpaired sets of images with and without that concept present in the photo. We distinguish two types of concepts:

1. Sparse - which correspond to some descriptive features or elements in the image that are not particularly possible to directly pinpoint. Examples of such concepts are: haristyle, age, gender etc.
2. Localized - correspond to objects or attributes that can be located in the image. These are: face, tie, shoes, etc.

We believe that we should be able to automatically detect if concepts that we predefine to be harmful are being used for classification. To do that, we propose to investigate whether the following approach will facilitate that:

1. For sparse concepts: use TCAV testing on the last layer before classification head and verify if images with concept A lead to higher activations than images without concept A.
2. For localized concepts:
    1. Also use TCAVs
    2. Use YOLO (or related) to perform instance segmentation (object detection + labels), then if some of the detected objects have labels that correspond to our set of harmful concepts, we want to verify how much of the network’s attention is directed at this object. To do that, we will do CRP to obtain a concept relevancy map over the input image. After that we should be able to quantify “how much” relevancy does this particular object captures.

**Goal 2: Unlearning harmful concepts**

After detecting that some harmful concepts are being used for image classification, we want to unlearn them. We want to use RR-CLARC (and other clarcs) to unlearn these concepts after the model is already trained (post-hoc). Things that we want to see here are:

1. Whether unlearning leads to actual concept removal from the decision process. So essentially use methods from Goal 1 again to verify if we eliminated those concepts.
2. Calculate before/after metrics for group fairness and accuracy (and other related to both performance and fairness) and see what is the impact of application of our method.

**Goal 3: Fairness**

We need to verify the effectiveness of the proposed approach with comparison to other existing fairness methods that also do not interfere with the data or the main training process of the model. This work is not being done in a vacuum, so we want to show that our method can lead to some gains from the stakeholder perspective. We need to justify why someone would want to use our method compared to just post-hoc equalization of odds.

1. Show fairness metrics of our method and juxtapose them with methods from post-hoc fairness literature
2. Potentially: show that classical post-hoc fairness is just a band-aid over a bleeding wound. Because it still utilizes harmful concepts, but tries to make sure that at the global level they don’t cause discrimination. We believe that these concepts should be eliminated from the decision process completely and not just by some mitigation strategies.
    1. Subtask is to find literature on post-hoc fairness and understand the field so that we can justify our approach well