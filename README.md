 <p align="center">
	<h1 align="center"> Understanding the Relation between Noise and Bias <br />
	in Annotated Datasets </h1>
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
<ul>
	<li> <b>Data Cartography</b> summarizes training dynamics for all samples as: </li>
		<ul>
  			<li> <b>Confidence</b>: Mean of probabilities for gold label across epochs.</li>
  			<li> <b>Variability</b>: Standard Deviation of probabilities for gold label across epochs.</li>
		</ul>
	<li> <b>Multi annotator models</b> leverages the diverse viewpoints brought by different annotators. They learn to <em>predict the labels each annotator would provide</em> for each instance in the dataset. These models get an instance id and an annotator id as input. </li>
</ul>



## Results


## References

[1] [Annotators with Attitudes: How Annotator Beliefs And Identities Bias Toxic Language Detection](https://aclanthology.org/2022.naacl-main.431) (Sap et al., NAACL 2022)

[2] [SemEval-2018 Task 1: Affect in Tweets](https://aclanthology.org/S18-1001) (Mohammad et al., SemEval 2018)

[3] [Agreeing to Disagree: Annotating Offensive Language Datasets with Annotators’ Disagreement](https://aclanthology.org/2021.emnlp-main.822) (Leonardelli et al., EMNLP 2021)

[4] [Constructing interval variables via faceted Rasch measurement and multitask deep learning: a hate speech application](https://arxiv.org/abs/2009.10277) (Kennedy et al., 2020)

[5] [Dataset Cartography: Mapping and Diagnosing Datasets with Training Dynamics](https://aclanthology.org/2020.emnlp-main.746) (Swayamdipta et al., EMNLP 2020)

[6] [Dealing with Disagreements: Looking Beyond the Majority Vote in Subjective Annotations](https://aclanthology.org/2022.tacl-1.6) (Mostafazadeh Davani et al., TACL 2022)


## About the Team

<table>
<tr align="center">
	
<td>
Abhishek Anand
<p align="center"> MS in Computer Science </p>
</td>

<td>
Anweasha Saha
<p align="center"> MS in Computer Science </p>
</td>

<td>
Prathyusha Naresh Kumar
<p align="center"> MS in Computer Science </p>
</td>

<td>
Negar Mokhberian
<p align="center"> PhD in Computer Science </p>
</td>

<td>
Ashwin Rao
<p align="center"> PhD in Computer Science </p>
</td>

<td>
Zihao He
<p align="center"> PhD in Computer Science </p>
</td>

</tr>
  </table>
