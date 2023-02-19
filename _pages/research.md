---
layout: page
permalink: /research/
title: research 
description: 
nav: true
nav_order: 5
---

___

## Research projects:

---

## Project: Improve robustness of DNN for ECG signal classification

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/icmla.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/cbm.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


- Motivation:

    - Electrocardiogram (ECG) is often the first step for the diagnosis of heart conditions before using expensive cardiac medical imaging.
    - Researchers have been developing machine learning-based ECG signal analysis methods for decades. Deep learning have demonstrated superior performance in a wide range of applications and were successfully applied for automatic ECG signal diagnosis. However, DNNs are known to be vulnerable to adversarial noises.
    - To our best knowledge, this is the first work to improve DNN robustness against adversarial attacks for ECG classification.

- Brief description of our work:

    -	We proposed a regularization method to improve the deep-learning-based electrocardiogram automatic diagnosis for better robustness. 
    -	We designed a multiple-layer perceptron (MLP) model for electrocardiogram data classification (from PhysionNet’s MIT-BIH dataset), whose prediction accuracy is 92%.                    
    -	We designed and implemented a CNN model for a variant-length 12-lead electrocardiogram classification task (from the China Physiological Signal Challenge 2018) via Python, Pytorch, Pandas, Scikit-learn, etc., which achieved top performance in the challenge.       
    -   We evaluated the robustness of the models under PGD100, SAP and uniform white noises. 
    -   We did ablation study to show how sensitive this method is sensitive to the hyperparameters. 
    -   We defined a criterion for hyperparameter selection.

-   Please read our papers ([1](https://www.sciencedirect.com/science/article/pii/S0010482522001378), [2](https://ieeexplore.ieee.org/abstract/document/9356227), [3](https://arxiv.org/abs/2005.09134)) for details.

___

## Project: Increasing-margin adversarial (IMA) training to improve adversarial robustness of neural networks
 {% include figure.html path="assets/img/ima.png" title="example image" class="img-fluid rounded z-depth-1" %}    

- Motivation:
    - To improve the adversarial robustness of a DNN model, adversarial training is the most general strategy. However, training a model by adversarielly will significantly harm the model's accuracy.
    - Our study aims to lift the trade off between adversarial robustness and standard accuracy: alleviate (or even avoid) the reduction in standard accuracy while improving adversarial robustness.

- Brief description of our work: 
    - Proposed a training method via increasing margin ideas to improve the neural networks for better robustness.
    - Evaluated the proposed method with residual net classifiers on image datasets, PathMnist and Cifar10, and real-world medical images, Covid-19 CT.
    - Mitigate this method to medical image segmentation tasks.
    - The proposed method significantly improved the model’s robustness against adversarial noises with minimal accuracy degradation.
- Please read our [paper](https://arxiv.org/abs/2005.09147) for details. 

---  

## Project: Improving Adversarial Robustness of Deep Neural Networks Via Adaptive Margin Evolution
 {% include figure.html path="assets/img/ame.png" title="example image" class="img-fluid rounded z-depth-1" %}  
- Motivation:
    - Adversarial training is the most popular and general strategy to improve Deep Neural Network (DNN) robustness against adversarial noises. Many adversarial training methods have been proposed in the past few years. However, most of these methods are highly susceptible to hyperparameters, especially the training noise upper bound. Tuning these hyperparameters is expensive and difficult for people not in the adversarial robustness research domain, which prevents adversarial training techniques from being used in many application fields. 
    - We wanted to propose a hyperparamter-free adversarial training method.

- Brief description of our work:                  
    - We proposed a hyperparameter-free adversarial training method.
    - We proved the existence of the optimal convergence state.
    - We evaluated the proposed method with residual net classifiers on public image datasets, CIFAR10, TinyImageNet and SVHN.
- Please read our [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4342066) for details.

---            

### Adaptive Adversarial Training to Improve Adversarial Robustness of DNNs for Medical Image Segmentation and Detection

{% include figure.html path="assets/img/amat.png" title="example image" class="img-fluid rounded z-depth-1" %}

- Motivation:
    -   Deep Neural Networks are vulnerable to adversarial noises and variant defense methods have been proposed recently. However, most of the methods are proposed under the assumption of classification situation. Although there are similarities between classification tasks and other tasks, e.g., regression, there are still gaps between them, e.g, some defense methods uses misclassification creteria, which is well-defined in classification but not in regression. As a result, the defense methods proposed for classification may not be derectly applied to other tasks. On the other hand, in medical image application domain, non-classification tasks, e.g., segmentaion, location and detection, are more often seen than classification of a whole image. As a result, we wanted to propose a defense method that can be applied to variant types of deep learning-based tasks. 
    -   Vanilla adversarial training is a simple but effective defense method. Also, it can be applied to almost all kinds of tasks. However, Vanilla adversarial training has its inner drawbacks: it is higly sensitive to its fixed and unified training noise upper bound. A unsuitable training noise upper bound may either reduce the model's accuracy significantly or make the adversarial-trained models not robust enough. As a result, we wanted to propose an adaptive adversarail training method that can adapt the training noise upper bound during the training process.

- Brief description of our work:
    -	We proposed a general adaptive adversarial training to improve the deep learning applications.
    -   We evaluated this methods in variant medical image application tasks:
        -	Unet-based model (nnUnet) for Heart, Hippocampus and Prostate MRI images segmentation.
        -	Multi-task Unet-based model for cephalometric landmark detection.
        -	YOLO V5 for blood cell detection.
    -	The experiments were conducted on Tesla V100 GPU and the results show that our proposed methods are effective in variant medical image application tasks.

-   Please read our [paper](https://arxiv.org/abs/2206.01736) for details.

___

## Diversity driven adaptive test generation for concurrent data structures

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/ATG1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/ATG2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

- Motivation:
    - Testing concurrent data structures remains a notoriously challenging task, due to the nondeterminism of multi-threaded tests and the exponential explosion on the number of thread schedules.
    - Testing a concurrent data structure may raise more challenges than testing a concurrent program because a concurrent data structure cannot run on its own. A test case of a concurrent data structure is a multi-threaded program that makes simultaneous accesses to the concurrent data structure. Obviously, the test case space is infinite in general. Therefore, it gives rise to a fundamental problem on the automated generation of effective multi-threaded test cases (i.e., concurrent programs) for concurrent data structures.

- Brief description of our work:
    -	We designed and developed a C++ generator via Python and C\C++ to automatically parse the C++ class (the concurrent data structure implemented with the pthread library) and to generate test cases that invoke the class. 
    -	We proposed two two diversity metrics and three adaptive algorithms to improve the C++ test case generation.
    -   The proposed methods discovered up to 6% more potential concurrent errors and reduced the time cost by up to 10%, than the baseline method.

-   Please read our [paper](https://www.sciencedirect.com/science/article/pii/S0950584918301356) for details.

 ___

## Reviewer Experience:
-	1 paper in International Conference on Machine Learning 2022 (ICML2022) – AI top conference
-	3 papers in Neural Information Processing Systems 2022 (NeurIPS 2022) – AI top conference
-	1 paper in Scientific Programming – A peer-reviewed journal in software engineering
-	1 paper in IEEE Journal of Biomedical and Health Informatics (JBHI)– A peer-reviewed journal in biomedical informatics
-	4 papers in Expert Systems with Applications (ESWA) – A peer-reviewed journal in intelligent systems applications
-	1 paper in Artificial Intelligence (AI)– A peer-reviewed journal in AI
-	1 paper in Computers in Biology and Medicine (CIBM) – A peer-reviewed journal in biomedical informatics
-	2 papers in Computer Systems Science and Engineering (CSSE) – A peer-reviewed journal in computer systems science
-	1 paper in Computers, Materials & Continua (CMC)–  A peer-reviewed journal in computational materials science and engineering


