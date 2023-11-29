 <p align="center">
	<h1 align="center">  Understanding the Relation between Noise and Bias in Annotated Datasets  </h1>
</p>

## Motivation
- **Bias in Annotation**: Annotator differences in <em>subjective tasks</em> introduce <em>bias in their annotations</em>, especially in sensitive domains like hate speech recognition, stemming from diverse backgrounds and perspectives.
- **Misinterpretation of Bias as Noise**: Minority votes are often considered <em>outliers</em> by models. This causes models to perceive them as noise, leading to biased predictions favoring <em>majority vote</em>.
- In this project, we'll explore if <em>perspectivist classification models</em> effectively utilize valuable insights from instances labeled as noisy by noise-detection techniques.


## Problem Statement


## Datasets
-
-
-
-


## Methodology
- **Data Cartography** summarizes training dynamics for all samples as
<ul>
  <li> **Confidence**: Mean of probabilities for gold label across epochs.</li>
  <li> **Variability**: Standard Deviation of probabilities for gold label across epochs.</li>
</ul>
- **Multi annotator models** leverages the diverse viewpoints brought by different annotators. They learn to *predict the labels each annotator would provide* for each instance in the dataset. These models get an instance id and an annotator id as input. 



## Results


## References
