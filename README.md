 <p align="center">
	<h1 align="center"> Understanding the Relation between Noise and Bias <br />
	in Annotated Datasets </h1>
</p>

## Motivation
- **Bias in Annotation**: Annotator differences in <em>subjective tasks</em> introduce <em>bias in their annotations</em>, especially in sensitive domains like hate speech recognition, stemming from diverse backgrounds and perspectives.
- **Misinterpretation of Bias as Noise**: Minority votes are often considered <em>outliers</em> by models. This causes models to perceive them as noise, leading to biased predictions favoring <em>majority vote</em>.
- In this project, we'll explore if <em>perspectivist classification models</em> effectively utilize valuable insights from instances labeled as noisy by noise-detection techniques.


![annotations emoji image](Annotations_image_emoji.png)


## Problem Statement
In the evolving landscape of machine learning, the reliability and fairness of models hinge on the quality of annotated data. However, the presence of bias, particularly in subjective tasks, has become a critical concern. This is especially prominent in sensitive domains like hate speech recognition, where annotators, stemming from diverse backgrounds and perspectives, might introduce bias in their annotations.

## Datasets

<table>  
  <tr>
    <td rowspan="2"></td>
    <th colspan="3" scope="colgroup">Toxicity and Hate Speech</th>
    <th colspan="1" scope="colgroup">Emotion</th>
  </tr>
  <tr>
    <th scope="col">Attitudes <br /> [1]</th>
    <th scope="col">Agree to Disagree <br /> [3]</th>
    <th scope="col">Kennedy <br /> [4]</th>
    <th scope="col">SemEval <br /> [2] </th>
  </tr>
  <tr>
    <th scope="row" style="text-align: left"># Annotators</th>
    <td style="text-align: center">184</td>
    <td style="text-align: center">819</td>
    <td style="text-align: center">7,912</td>
    <td style="text-align: center">183</td>
  </tr>
  <tr>
    <th scope="row" style="text-align: left"># Annotations per annotator</th>
    <td style="text-align: center">18.8±25.6</td>
    <td style="text-align: center">63.7±139</td>
    <td style="text-align: center">17.1±3.8</td>
    <td style="text-align: center">476.4±1079</td>
  </tr>
  <tr>
    <th scope="row" style="text-align: left"># Unique texts</th>
    <td style="text-align: center">627</td>
    <td style="text-align: center">10,440</td>
    <td style="text-align: center">39,565</td>
    <td style="text-align: center">11,090</td>
  </tr>
  <tr>
    <th scope="row" style="text-align: left"># Annotations per text</th>
    <td style="text-align: center">5.5±0.8</td>
    <td style="text-align: center">5</td>
    <td style="text-align: center">2.3±1.0</td>
    <td style="text-align: center">7.8±3.0</td>
  </tr>
</table>



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

> **DATASET CARTOGRAPHY**

<img src="plots_agree_to_disagree/conf_vs_var_color_correctness.png" alt="agree to disagree" height="400px" width="500px">
<img src="plots_kennedy/conf_vs_var_color_correctness.png" alt="kennedy" height="400px" width="500px">
<img src="plots_sbic/conf_vs_var_color_correctness.png" alt="sbic" height="400px" width="500px">
<br>

### AGREE TO DISAGREE
> **MAJORITY VOTE LABEL**

<img src="plots_agree_to_disagree/agr_factor_vs_conf_hue.png" alt="agr factor vs conf" height="350px" width="500px">

> **MULTI ANNOTATOR**

<br>&nbsp;&nbsp;&nbsp;<img src="plots_agree_to_disagree/disagree_vs_conf.png" alt="disagree vs conf" height="350px" width="350px">
<br>&nbsp;&nbsp;&nbsp;<img src="plots_agree_to_disagree/low_conf_mjr_disagree_vs_conf.png" alt="low conf mjr disagree vs conf" height="350px" width="350px">
<br>&nbsp;&nbsp;&nbsp;<img src="plots_agree_to_disagree/group_count.png" alt="group count]" height="350px" width="400px">
<br>

### KENNEDY
> **MAJORITY VOTE LABEL**

<br>&nbsp;&nbsp;&nbsp;<img src="plots_kennedy/agr_factor_vs_conf_hue.png" alt="agr factor vs conf" height="350px" width="500px">
 
> **MULTI ANNOTATOR**

<br>&nbsp;&nbsp;&nbsp;<img src="plots_kennedy/disagree_vs_conf.png" alt="disagree vs conf" height="350px" width="350px">
<!--<br>![disagree vs conf](plots_kennedy/disagree_vs_conf.png)-->
<br>&nbsp;&nbsp;&nbsp;<img src="plots_kennedy/low_conf_mjr_disagree_vs_conf.png" alt="low conf mjr disagree vs conf" height="350px" width="350px">
<!--<br>![low conf mjr disagree vs conf](plots_kennedy/low_conf_mjr_disagree_vs_conf.png)-->
<br>&nbsp;&nbsp;&nbsp;<img src="plots_kennedy/group_count.png" alt="group count" height="350px" width="400 px">
<!--<br>![group count](plots_kennedy/group_count.png)-->
<br>

### SBIC
> **MAJORITY VOTE LABEL**

<br>&nbsp;&nbsp;&nbsp;<img src="plots_sbic/agr_factor_vs_conf_hue.png" alt="agr factor vs conf" height="350px" width="500px">
<!--<br>![agr factor vs conf](plots_sbic/agr_factor_vs_conf_hue.png)-->

> **MULTI ANNOTATOR**

<br>&nbsp;&nbsp;&nbsp;<img src="plots_sbic/disagree_vs_conf.png" alt="disagree vs conf" height="350px" width="350px">
<!--<br>![disagree vs conf](plots_sbic/disagree_vs_conf.png)-->
<br>&nbsp;&nbsp;&nbsp;<img src="plots_sbic/low_conf_mjr_disagree_vs_conf.png" alt="low conf mjr disagree vs conf" height="350px" width="350px">
<!--<br>![low conf mjr disagree vs conf](plots_sbic/low_conf_mjr_disagree_vs_conf.png)-->
<br>&nbsp;&nbsp;&nbsp;<img src="plots_sbic/group_count.png" alt="group count" height="350px" width="400px">
<!--<br>![group count](plots_sbic/group_count.png)-->
<br>

## FINDINGS

Focusing on the correlation between human agreement and the model’s confidence over the instances we observe:
- We see significant correlation between agreement between annotators and model confidence in all the datasets, with the confidence decreasing with more disagreement between the annotators on the label.

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
