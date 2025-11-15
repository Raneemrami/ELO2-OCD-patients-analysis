# Project overview

This project aims to analyze OCD patients' data to answer different questions about Obsessive-compulsive disorder using different tools.

## Current Project idea summary and main challenges

Studying the  Comorbid Anxiety and Depression in OCD patients, and I aim to use simple EDA as well as ML to predict comorbidity. 

## Main research question

How do early-life stress and coping style, as well as OCD symptoms severity and type  influence the presence of co-occurring anxiety and depression adults with OCD?

The co-occurring mental problems in this research are only anxiety and depression

## Project objectives and main points

**one**: classify people to:

* probable clinical anxiety/ depression (High HADS-D/HADS-A scores)(severe/moderate severity)
* possible(breadline case) anxiety/depression (medium HADS-D/HADS-A scores) (mild severity)
* No anxiety/ Depression (low HADS-D/HADS-A scores)

**Two**: study the differences and correlations between the above categories and other problems like childhood trauma and coping style, as well as OCD severity and other symptom dimensions.

**Three**: build an ML model to predict the above classes based on things like CATS score (Child abuse and trauma scale), Coping style (active coping and planing) from the COPE scale as well as OCD symptoms severity and type.

Correlations between features and co-occurring mental problems (anxiety, depression, None) are also going to be studied to inspect if they affect the presence of anxiety and/or depression.

## Data used

please refer to [this link](https://datashare.ed.ac.uk/handle/10283/8698#:~:text=Participants%20were%20also%20asked%20to,was%20also%20recorded) that has the original data used in this project from the university of Edinburgh data share under this License [Creative Commons License: Attribution 4.0 International](https://datashare.ed.ac.uk/bitstream/handle/10283/8698/license_text?sequence=5&isAllowed=y)

### Data Citation

Kirkham, Elizabeth; Król, Martyna; Cao, Yintao. (2024). Associations between obsessive-compulsive disorder, early life stress, psychological variables and treatment resistance, [dataset]. University of Edinburgh. https://doi.org/10.7488/ds/7661.

### Data Description

This dataset was collected using an online survey between May and July 2022. People with and without obsessive-compulsive disorder (OCD; n = 390) were asked to complete a survey which included the following questionnaires: Obsessive-Compulsive Inventory Revised (OCI-R); Child Abuse and Trauma Scale (CATS; Sanders & Becker-Lausen, 1995); Brief Experiential Avoidance Questionnaire (BEAQ; Gamez et al., 2014); Hospital Anxiety and Depression Scale (HADS; Zigmond & Snaith, 1983); and the "Planning" and "Active Coping" subscales of the Coping Orientation to Problems Experienced (COPE) questionnaire (Carver, 1989). Participants were also asked to provide information on whether they had OCD (and if it was self- or professionally- diagnosed) and what treatment they had received for OCD. Brief demographic information (age, gender, ethnicity, university attendance) was also recorded.

### Important notes

1. the description of the original data under the `Data Description` heading above was copied from the website.
2. in my project I edited and cleaned the data and I will provide a description and data dictionary for the edited and cleaned data, lines of code used will also be provided as much as possible.

## Other research questions

Do certain types of compulsion tend to occur more with anxiety compared to other types in OCD patients?

Do certain types of compulsion tend to occur more with depression compared to other types in OCD patients?

Do certain types of obsessions tend to occur more with anxiety compared to other types in OCD patients?

Do certain types of obsessions tend to occur more with depression compared to other types in OCD patients?

**NOTE**: adjustments could be made as the project is evolving

### Personal learning goals

* Reinforce data science knowledge.

* Apply machine learning
