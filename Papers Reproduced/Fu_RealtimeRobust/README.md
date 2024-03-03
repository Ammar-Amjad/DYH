# Executive Summary

**Paper Title:** Realtime Robust Malicious Traffic Detection via Frequency Domain Analysis

**Conference:** CCS

**Year:** 2021

## Project Time

**Total Time:** 11 hrs

**Researching Time:** 9 hrs

**Coding Time:** 2

## Paper Summary

The paper is about Computer Network Security.

ML-based malicious traffic detection is not suitable to use against zero-day attack detection. Using frequency domain features coupled with ML modeling gives high performance and delivers results faster.

The author aims to solve the problem of detecting malicious attacks, especially zero-day attacks.

Packets are initially parsed by the High-speed parser which sends feature sequences for frequency domain feature extraction. Meanwhile, the data is simultaneously sent to the automatic parameter selection module where an encoding vector is generated and fed into the frequency domain feature extraction module.
The feature extraction module performs feature encoding, Fourier transform, and then log transformation to generate frequency domain features. Clustering is performed on the features to detect normal and abnormal packets.  

Using Whisper against 42 types of attacks and comparing them against state-of-the-art systems yields an improvement of AUC by 18.26%. This is true for various evasion attacks where Whisper delivers around 90% detection accuracy.

List contributions of the paper:

•   Whisper, a novel malicious traffic detection system by utilizing frequency domain analysis.
•   Developed automatic encoding vector selection for Whisper to reduce manual efforts for parameter selection.
•   Develop theoretical analysis framework to prove Whisper’s properties.
•   Prototype Whisper with Intel DPDK and validate performance.

Whisper has a higher throughput but the input system has a physical limit of 10 GBPS NIC. Therefore multiple input flow generators with high-speed optical fibers are required. Limitations are not mentioned in depth in paper but rather on the github repo.


## Available Materials 

Three publically available dataset were used i.e. MAWI 2020.06.10, MAWI 2019.1.2, and MAWI 2020.1.1 datasets.
I was able to find the datasets on the website and downloaded them.
The format used was .csv and the size of data is collectively 2.45 GB + 2.72 GB + 1.43 GB respectively.
To reproduce the 3 different datasets are needed to get the results.
Meanwhile, the code is also made available on github. -> https://github.com/fuchuanpu/Whisper
They have also provided the models they used. -> https://github.com/fuchuanpu/Whisper/blob/master/commune/kMeansLearner.hpp
The libraries required are not mentioned on the github repo nor in the paper but they are mentioned in the README which redirects to other websites. This is a bit inconvenient to setup.

## Reproduction Experience

The data was easy to find as it's given linked in the GitHub repo which is linked in the paper. 
The code is also linked in the repo and the link can be found in the paper.
I have gone thru the paper and the github repo twice. 
The requirements are better defined in the repo rather than the paper itself.
I have seen that the requirements include alot of hardware and alot of configurations.
There is a need for NICs supporting DPDK with fiber laser modules which have alteast throughput of 10 Gbps and atleast 17 cores attached.
Since i dont have access to multiple NICs, fiber laser modules and my internet throughput is around 50 mbps, and i dont have such a powerful CPU either; Therefore i cannot reproduce this paper.

## Recommendations

They should write the requirements portion in one area instead of linking to alot of websites.
The hardware devices should be more clearly defined.

For the code, containerization using docker or Kubernetes would have been a great ease for the reproduction of paper.

If there is a GitHub link, there is usually an issue tab. 
I would recommend the reader check that out before attempting to reproduce the paper.
In the issues tab, people have raised issues with the code and dataset, which might save a lot of time.
https://github.com/fuchuanpu/Whisper/issues

I would recommend the user to look at the github repo first as the writter has consolidated the requirements there.
It would be quick for the reader to find the requirements and see if its feasible to arrange them and save time.