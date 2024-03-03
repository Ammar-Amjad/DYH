# Executive Summary

**Paper Title:** DEEPCASE: Semi-Supervised Contextual Analysis of Security Events 

**Conference:** S&P

**Year:** 2022

## Project Time

**Total Time:**
Total Time: 13 hrs

**Researching Time:** 
Researching Time: 6 hrs.

**Coding Time:**
Coding Time: 7 hrs.

## Paper Summary

The area of the work of the paper is Computer Network Security.
The paper attempts to introduce a novel system to reduce the work of Security operators who investigate these security events to determine whether they pose a threat to their organization using a novel machine learning-based solution. 
The paper uses attention-based machine learning to find patterns in security sequences and based on past data, clusters them and classifies them. In some cases where the categorization is unclear, the prediction is then either rejected or approved by the operator manually which in turn helps the model learn.
This semi-autonomous system leads to an overall reduction of 92.26% from the manual work of security operators.
DeepCase is available on GitHub and the DeepCase website where detailed documentation about its utilization is written.
DOS attack where a large number of sequences are sent to the model can lead it to dramatically reduce the performance and therefore the workload reduction is significantly affected. Other limitations include the fixed nature of input sequences and that the sequences only work within the context of the same machine.


## Available Materials

The paper does not provide it's own dataset rather they used a public dataset. 
The datasets used are Lastline and HDFS datasets. 
The Lastline dataset required an NDA to be signed so that isnt available meanwhile HDFS is available.
Link -> https://github.com/wuyifan18/DeepLog/tree/master/data. The data is downloadable.
The data types used in their dataset are either .csv or .txt.
Lastline has 10.5Mil and HDFS has 11.2Mil security events.
To reproduce the results fully both datasets are needed but half of the results can be reproduced from the other dataset.
The code is readibly available on github with documentataion on code execution also availble on their website.
All of the code is available to run the system from start to finish.
Unfortunatly, they have not provided pre trained models but they have provided models in the form of code.
They have further included a requirements file for setting up the necessary environment. 


## Reproduction Experience

The data was easy to find as it's given linked in the GitHub repo which is linked in the paper. 

From looking at the code on GitHub, the dataset provided, the online documentation on their website, and the author's presentation on the paper,
I feel confident that the paper is reproducible even tho we have access to only the HDFS dataset.

I downloaded the code by cloning the git repo of DeepCASE, meanwhile also following the documentation on their website.
The steps are not very clear in particular relating to the data. 
How to read data and how to label it are not mentioned in the paper nor are there any examples as references.
The first issue I faced while trying to run the code was that the dataset was not in the repo.
One of the Datasets was not publically available due to NDA signature requirements.
The other one was linked to a different git repo.
After downloading and running the code as described in the documentation, the code crashed due to an error that took a lot of time to debug as the output logs were horrendous.
I went thru them all and figured out that my python version was a higher version and not supported to run the libraries, scipy in this case so I down versioned python to 3.7 from 3.10.
Then I faced another error in the preprocessor class's module which was incorrectly named and caused the code to crash which I fixed myself in the code.
I went ahead and reported the issue on their GitHub repo with screenshots of error reproducibility here -> https://github.com/Thijsvanede/DeepCASE/issues/6
Finally, after some struggle, the code was working and I got executed the rest of cmd commands.
Ultimately, I ran into a problem that I as a reader do not and cant solve which is that the data is clustered after passing thru the ML models.
That data needs to be labeled by a security operator manually for the first run so that the model knows how to classify the clusters automatically next time.
I did not find any clue on how to correctly label the clusters formed in the research paper, the youtube video, the documentation, and the GitHub repo.
I performed a bit of data analysis in excel on the clustered data produced to try to figure out the pattern myself but it was to no avail. 
Finally, I concluded that without a reference on how to label data or at least a sample dataset with prelabeled clusters so I can skip the first manual run, I simply cannot reproduce the paper.
Therefore, my original claim which i made after seeing the data and code was available, is no longer correct. 
The paper is not reproducible due to the lack of labeling methodology described anywhere.

## Recommendations

To make the results easier to reproduce i would firstly recommend,
Containerization using docker or Kubernetes would have been a great ease for the reproduction of paper.

The reader would just have to get the image and deploy it, simplfying the process.
Secondly, they should have detailed the method on how to label clusters or at least given a labeled dataset of clusters.

Smaller sample sets should be included in papers to help get the code running and replicate results without much wait or struggle.
In the DeepCase paper, sample sets were not provided.

To save time reproducing the paper i recommend to visit the paper's GitHub link, where there is an "issue" tab. 
I would recommend the reader to check that out before attempting to reproduce the paper.
In the issues tab, people have raised issues with the code and dataset, which might save a lot of time.
https://github.com/Thijsvanede/DeepCASE/issues?q=is%3Aissue+is%3Aclosed
Secondly, I would also recommend checking out the DeepCase youtube video related to the paper which is made available by the authors.
https://www.youtube.com/watch?v=vdycTPH_uF0


After reading the introduction of the paper, I would go straight to the youtube video of the paper.
This saved me a lot of time, as papers have an inconvenient way of describing, and the chain of thought is lost easily.
