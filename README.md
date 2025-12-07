# Project overview

This project aims to analyze OCD patients' data to answer different questions about Obsessive-compulsive disorder using different tools.

## Current Project idea summary and main challenges

Studying the  Comorbid Anxiety and Depression in OCD patients, and I aim to use simple EDA as well as ML to predict comorbidity.

## Problem Statement

Obsessive–compulsive disorder (OCD) frequently co-occurs with other psychological conditions, particularly anxiety and depression. These comorbid symptoms may influence treatment response and contribute to poorer long-term outcomes.
This project aims to investigate whether early life stress, obsessive–compulsive symptom patterns, experiential avoidance, and coping styles differ across OCD patients with anxiety symptoms only, and those with both anxiety and depression symptoms.
Understanding these differences is crucial for identifying risk profiles, elucidating underlying mechanisms, and tailoring interventions to meet patient needs.

## Main research question

How do early life dress, obsessive compulsive symptoms, experiential avoidance, and coping style differ between  OCD patients with anxiety symptoms only and patients with both anxiety and depression symptoms?

The co-occurring mental problems in this research are only anxiety and depression

## Project objectives and main points

**one**: using HADS (to measure anxiety and depression) with a threshold of 8 classify people to:

* anxiety symptoms only
* depression and anxiety symptoms

**Two**: study the differences between the above categories and other problems like childhood trauma and coping style, as well as OCD severity and other symptom dimensions.

**Three**: build an ML model to predict the above classes based on things like CATS score (Child abuse and trauma scale), Coping style (active coping and planing) from the COPE scale, experiential avoidance scale as well as OCD symptoms severity and type.

## Data used

please refer to [this link](https://datashare.ed.ac.uk/handle/10283/8698#:~:text=Participants%20were%20also%20asked%20to,was%20also%20recorded) that has the original data used in this project from the university of Edinburgh data share under this License [Creative Commons License: Attribution 4.0 International](https://datashare.ed.ac.uk/bitstream/handle/10283/8698/license_text?sequence=5&isAllowed=y)

### Data Citation

Kirkham, Elizabeth; Król, Martyna; Cao, Yintao. (2024). Associations between obsessive-compulsive disorder, early life stress, psychological variables and treatment resistance, [dataset]. University of Edinburgh. [https://doi.org/10.7488/ds/7661](https://doi.org/10.7488/ds/7661)

### Data Description

This dataset was collected using an online survey between May and July 2022. People with and without obsessive-compulsive disorder (OCD; n = 390) were asked to complete a survey which included the following questionnaires: Obsessive-Compulsive Inventory Revised (OCI-R); Child Abuse and Trauma Scale (CATS; Sanders & Becker-Lausen, 1995); Brief Experiential Avoidance Questionnaire (BEAQ; Gamez et al., 2014); Hospital Anxiety and Depression Scale (HADS; Zigmond & Snaith, 1983); and the "Planning" and "Active Coping" subscales of the Coping Orientation to Problems Experienced (COPE) questionnaire (Carver, 1989). Participants were also asked to provide information on whether they had OCD (and if it was self- or professionally- diagnosed) and what treatment they had received for OCD. Brief demographic information (age, gender, ethnicity, university attendance) was also recorded.

### Important notes

1. the description of the original data under the `Data Description` heading above was copied from the website.
2. in my project I edited and cleaned the data and I will provide a description and data dictionary for the edited and cleaned data, lines of code used will also be provided as much as possible.

**NOTE**: adjustments could be made as the project is evolving

### Personal learning goals

* Reinforce data science knowledge.

* Apply machine learning

### To Easily navigate the repository

* domain knowledge related resources [can be found here](0_domain_study/links.md)

* to find the data the raw and cleaned data and data dictionaries [in this folder](data)

* to find the notebooks that are used to clean data [in this folder](cleaning_notebooks)

* [data analysis notebooks](data_exploration_and_analysis)

## Tha analysis (Part one)

for more details visit the [data exploration and analysis notebook](data_exploration_and_analysis/data_exploration_and_analysis_three.ipynb)

### research question answer

### 1. Coping (active coping strategy)

If you to give these statements higher scores such as a 3 or 4, you will score highly as using Active Coping as one of your coping strategies. If you scored low giving these statements a 1 or 2 then Active Coping would not be one of your core coping strategies.

this scale measures weather an individual use active coping strategy to deal with problems, it has 4 statements to measure that.
[for more information about the scale](https://positivepsychology.com/coping-scales-brief-cope-inventory/#:~:text=The%20Brief%20COPE%20Inventory%20consists,University%20of%20California%2C%20San%20Francisco.).

#### active coping statement 1 (I concentrate my efforts on doing something about it)

![plot1_anx/dep](plots/ac1_anx_and_dep.png)

![plot1_anx](plots/ac1_anx_only.png)

generally category of patients with anxiety symptoms only has less individuals choosing 1 or 2 (low scores), compared to the category of patients with both anxiety and depression symptoms

#### active coping statement 2 (I take additional action to try to get rid of the problem.)

![plot2_anx/dep](plots/ac2_anx_and_dep.png)

![plot2_anx](plots/ac2_anx_only.png)
in both categories most people answered (3 or 4) (considered high)

#### active coping statement 3 (I take direct action to get around the problem.)

![plot3_anx/dep](plots/ac3_anx_and_dep.png)

![plot3_anx](plots/ac3_anx_only.png)

in both categories individuals who chose (1 or 2), are almost equal to individuals who chose (3 or 4)

#### active coping statement 4 (I do what has to be done, one step at a time.)

![plot4_anx/dep](plots/ac4_anx_and_dep.png)

![plot4_anx](plots/ac4_anx_only.png)

in both categories most patients chose higher scores(3 or 4)

*summary* statement one showed the most difference where there were significantly less individuals choosing lower scored(1 or 2) in the anxiety symptoms only category wheres other statements showed almost similar distribution for both categories (anxiety symptoms only, anxiety and depression symptoms)

### 2. Coping (planning coping strategy)

similar scoring strategy to active coping

this scale measures weather an individual use planning as a coping strategy to deal with problems
[for more information about the scale](https://positivepsychology.com/coping-scales-brief-cope-inventory/#:~:text=The%20Brief%20COPE%20Inventory%20consists,University%20of%20California%2C%20San%20Francisco.).

#### planning statement 1 (I make a plan of action.)

![plan1_anx/dep](plots/plan1_anx_and_dep.png)

![plan1_anx](plots/plan1_anx_only.png)

generally individuals that chose (2)(low score) are less in the anxiety symptoms  only category compared  to other scores whereas  individuals that chose (2)(low score) are more compared to other scores in the anxiety and depression symptoms category.

#### planning statement 2 (I try to come up with a strategy about what to do.)

![plan2_anx/dep](plots/plan2_anx_and_dep.png)

![plan2_anx](plots/plan2_anx_only.png)

generally in both categories individuals who chose (higher scores)(3 or 4) are higher than individuals who chose (1 or 2)
(low scores), the number of individuals in the anxiety and depression symptoms category who chose 2 is high compared to the other scores whereas the number of individuals choosing 2 is lower in the anxiety symptoms only category compared to the other scores.

#### planning statement 3 (I think about how I might best handle the problem.)

![plan3_anx/dep](plots/plan3_anx_and_dep.png)

![plan3_anx](plots/plan3_anx_only.png)

generally in both categories individuals who chose (higher scores)(3 or 4) are higher than individuals who chose (1 or 2)
(low scores)

#### planning statement 4 (I think hard about what steps to take.)

![plan4_anx/dep](plots/plan4_anx_and_dep.png)

![plan4_anx](plots/plan4_anx_only.png)

generally in both categories individuals who chose (higher scores)(3 or 4) are higher than individuals who chose (1 or 2)
(low scores)

*summary* statement_one and statement_two:generally individuals that chose (2)(low score) are less in the anxiety symptoms  only category compared  to other scores whereas  individuals that chose (2)(low score) are more compared to other scores in the anxiety and depression symptoms category.

### 3. OCI-R (Total)

obsessive compulsive inventory revised, is used to measure the OCD symptoms across 6 different sub-scales
washing, checking, neutralizing, obsessing, ordering and hoarding.

![plot_3](plots/three.png)

people with both anxiety and depression symptoms reached to scores up to 66, whereas people with anxiety symptoms only had a maximum of 59 on the OCIR scale.

* anxiety symptoms present depression symptoms absent:

50% scored below or equal 38 (50th percentile)

* anxiety and depression symptoms present:
50% scored below 40.5 (50th percentile)

there is not a huge difference and most of it was coming from the hoarding sub-scale

### 4. OCI-R (Hoarding subscale)

the OCI-R HOARDING is one of the OCI-R sub-scales

![plot_4](plots/four.png)

OCIR-hoarding

individuals with both anxiety and depression showed difference in this subscale, compared to the other subscale that did not show much difference

* anxiety and depression symptoms present:

this category had individuals scoring up to 12 on the OCIR-hoarding subscale (highest score)

* anxiety symptoms present depression symptoms absent:

individuals in this category did not reached scores that are greater than 10

### 5. CATS (Total)

the Child abuse and trauma scale has multiple sub-scales to measure types of stress, we used the total as a measure of the early life stress generally

![plot_5](plots/five.png)

similarly to OCIR, we can also see that people with both anxiety and depression symptoms reached higher scores on the CATS scale (that some scores were never reached by people with anxiety symptoms only)

* anxiety and depression symptom  present:

  * With patients reaching scores above 120 (128)
  * 50% scored below or equal 61 (50th percentile)

* anxiety present, depression absent:

  * 0 patients reaching scores above  95
  * 50% scored below or equal 40 (50th percentile)

### 6. Brief experiential avoidance (Total)

measure the tendency to to avoid unwanted thoughts and sensations.
Scores range from 15 to 90, higher scores indicating higher levels of EA.
[for more information about the scale](https://novopsych.com/assessments/formulation/brief-experiential-avoidance-questionnaire-beaq/)

![plot_6](plots/six.png)

for individuals with both anxiety and depression symptoms some individuals  reached up to 87 on the EA scale, this score was never reached by individuals with anxiety symptoms only.

for individuals with anxiety symptoms only some individuals scored up to 78 (maximum)

## Machine learning (Part two)

for more details [visit the machine learning notebook](ML/ML2.ipynb)

this part incorporated training a logistic regression model to predict the two main classes that were compared:

* anxiety symptoms only
* anxiety and depression symptoms

using some of the scales mentioned above CATS_Total,  OCIR_Total,
OCIR_Hoarding_Total, OCIR_Checking_Total, OCIR_Ordering_Total, OCIR_Neutralizing_Total, OCIR_Washing_Total, OCIR_Obsessing_Total, Brief_Experiential_Avoidance_Questionnaire_Total.
we are basically using the childhood abuse and trauma scale total, the brief experiential avoidance scale total, and the OCI-R scale total along with its sub-scales total.

### accuracy

the overall accuracy was around 65%, which is better than predicitng the most class (58.5%).

### presion and recall

* treating label 0 (anxiety and depression symptoms present) as the positive class, out of all individuals that the model predict they have both anxiety and depression symptoms, 0.68 (68%) are actually with both anxiety and depression symptoms(Precision).

* out of all the individuals with both anxiety and depression symptoms, the model predicted (0.77) 77% correctly. meaning the rest are false negatives (around 23%)

### ROC CURVE

![plot_roc](plots/roc.png)

### confusion matrix

![plot_roc](plots/cm.png)
