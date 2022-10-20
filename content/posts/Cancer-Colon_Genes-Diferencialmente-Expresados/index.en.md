---
weight: 1
title: "Analysis of Differentially Expressed Genes in Colon Cancer"
date: 2021-04-30T21:54:48-05:00
lastmod: 2022-10-04T21:54:48-05:00
draft: false

author: "Cristian Gonzaga"
description: "This project identified genes involved in cancer tissue formation, 
focusing on genes differentially expressed in colon cancer in adults 
aged 50 to 60 years, taking advantage of the vast amount of information 
found in different databases (related to the topic) and the R programming 
language."

tags: ["NCBI","Data Science","R"]
categories: ["Co-Curricular Projects"]

lightgallery: true

toc:
 auto: false
---
<!--more-->

## About

This project identified genes involved in cancer tissue formation, 
focusing on genes differentially expressed in colon cancer in adults 
aged 50 to 60 years, taking advantage of the vast amount of information 
found in different databases (related to the topic) and the R programming 
language.

The code of the analyzed dataset GSE44076 was retrieved from the *Geo 
DataSets* database, which refers to different types of mucosa in the colon, 
in which some adenocarcinoma and tumor cells were detected. From these data, 
a classification of subjects with healthy colon mucosa and with cancerous tumors 
was made according to their age: 50 to 60 years old (adults) and 70 to 85 years 
old (elders). 

In the case of the search for differentially expressed genes, distinct considerations 
(age, sex, nationality, among others) were made for the creation of the groups. Also, it was 
determined the number of samples to be used for each group, the number of genes to 
be analyzed, the magnitude of change (log base change) and the statistical 
significance (p-value) to calculate their significant influence on the results. 

After statistical processing in R Studio, using the limma and GEOquery packages and
the algorithm implemented to find the most significant p-values and effect sizes, 
10 differentially expressed genes were obtained from the ratio classification 
between healthy adults and those in a pathological state, which are: CRNDE, MMP7, 
MEPB1B, CA7, among others.

Once the genes were obtained, various bioinformatics resources were used to make 
sense of the genes. This step allowed to validate the information and provide a 
livelihood, identifying the functionalities of these genes, their relationship 
to biological processes, their type of molecules, among others. Thus, a better 
analysis and understanding of the impact of genes was achieved.

Finally, once it has been proven that the selected genes have a close relationship 
with the object of study, it is appropriate to consider these genes as important 
in the pathological processes, so that solutions and strategies can be developed 
based on them. Thus, by identifying a gene that is specifically present 
in adults in a certain age range with colon cancer, it is possible to understand 
its threat (to a certain extent), or to treat it if it lends itself to it. Therefore, 
different alternatives to colonoscopy can be developed, such as the implementation 
of low-cost microchips to analyze the biomarkers that cause colon cancer.


