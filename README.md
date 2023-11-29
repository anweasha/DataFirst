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
