# Executive Summary

**Paper Title:** 
What You See is Not What the Network Infers: Detecting Adversarial Examples Based on Semantic Contradiction 

**Conference:** NDSS

**Year:** 2022 

## Project Time

**Total Time:** 13 hrs

**Researching Time:** 6 hrs 

**Coding Time:** 7 hrs

## Paper Summary

The paper focuses on the area of Computer Network Security aiming to identify contradictions between AE’s(Adversarial examples) semantic meaning and thier DNN extracted features.Adversarial examples (AEs) pose severe threats to the applications of deep neural networks (DNNs) to safety-critical domains, e.g., autonomous driving. 

The latest modern solutions defend against only a subset of AEs or cause a relatively high accuracy loss for legitimate inputs. Moreover, most solutions cannot defend against adaptive attacks. ContraNet is an ML-based solution to this issue.

To perform semantic comparison at the input space, 
ContraNet employs an Encoder to capture the low-level features of the input image and
feed it together with inference results of a DNN model to the GAN.
The output is an image that can be easily differentiated from the AE's image and used for detection.
Furthermore, it is shown semantic information is highly dependent on the inferred results.

ContraNet employs an encoder, a conditional Generation (cGAN), and a similarily measurement model.
The encoder embeds features of an image as a latent vector, which is fed to the generator.
The generator makes an image that is relevant to the label provided. 
Finally, the similarity measurement model aims to improve the performance of ContraNet by learning the similarity metric.
The similarity models used are DMM, Dis, and SSIM and are employed simultaneously.
DMM is responsible for AEs with small perbutations. 
SSIM aims to detect extra-large perturbed AEs. 
Dis detects AEs relying only on synthetic images.

Experimental results show that ContraNet outperforms state-of-the-art AE detectors by a large margin. 
For whitebox attacks, ContraNet performs consistently well against a large number of attacks on a variety of datasets.
For Adaptive attacks like PGD, C&W, and Orthogonal-PGD, overall ContraNet is robust but the right loss function can be determining its performance.
ContraNet outperforms four SOTA detection-based defenses under the "otrh" and "select" attack settings.

List any contributions of the paper. 

- ContraNet is the first work to explore the AE’s intrinsic property for detection at input space, which has the potential to resist adaptive attacks.
- Designing a new conditional Generative Adversarial Network (cGAN) network.
- Development of an effective and efficient similarity measurement model to tell the semantic difference between the input and the synthetic samples.

When it comes to cons, ContraNet has difficulty in differentiating classes that are inherently similar in semantics.


## Available Materials 

The paper does not produce it's own dataset.
There are 3 publically available datasets that are used: 
- MNIST -> (http://yann.lecun.com/exdb/mnist/)
- GTSRB -> (https://sid.erda.dk/public/archives/daaeac0d7ce1152aea9b61d9f1e19370/published-archive.html)
- CIFAR-10 datasets -> (https://www.cs.toronto.edu/~kriz/cifar.html).

Fortunately, I was able to find and download all of them.

The data is mainly images of the .png format.

Furthermore, all the datasets vary greatly in their sizes where:
- MNIST is of size 11.5 MB.
- GTSRB is of size 5.7 GB.
- CIFAR-10 is of size 163 MB.

To reproduce the results of the paper fully, all 3 datasets are needed.

Also, all of the code is available. -> https://github.com/cure-lab/ContraNet/tree/main/cifar10_ContraNet

They have also provided untrained models. 
-> https://github.com/cure-lab/ContraNet/tree/main/cifar10_ContraNet/models

The requirements for setting up the necessary environment are also mentioned. 
-> https://github.com/cure-lab/ContraNet/blob/main/whitebox_attacks/environment.yaml

## Reproduction Experience

In my experience, the data was easy to find. 
In the case of the GTSRB dataset, there are multiple datasets with the same name so that can be misleading in the paper its not mentioned where to find the relevant ones.
Based on the availability of code and datasets, the paper seems to be reproducible.

I have cloned the github repository and downloaded the datasets. The datasets are easy to find but its not clear in which directory they are supposed to be in. Initially, when i attempted to install the python dependencies, they were in yaml which is a anaconda format. 
The paper nor the github mentions that anaconda is required so i downloaded and setup the conda environment but the requirements.yaml file was not executing. Meanwhile, I converted the yaml requirements file to txt file and pip installed the requirements which took 30 min to install.
After installing dependances, i ran followed the instruction to execute code.
The first error i encountered was that the python file name was incorrect and i had to correct it.
Then i attempted first to execute the pre-trained models  which threw an error that the file mentioned in local directory was not present there.
Therefore, i went to the training and testing steps for the for adaptive attacks and then for whitebox attacks.
Both of which crashed due to modules not found.
Overall, the Git Directory structure does not match the one mentioned in paper or in description, and its  hard to understand where to move files when follwing the instructions, meanwhile some directories dont have the files that are being referred to.

Conclusively, i beleive the paper is not reproducable as its alot of code with alot of errors and bad documentation that isnt coherent to be understood.
The paper does a poor job to explain what is practically happening. There are many gaps in conveying the understanding and also bugs in the code.


## Recommendations

I would recommend that containerization using docker or Kubernetes would have been a great ease for the reproduction of paper.

The paper doesnt include enough relevant details to code the paper myself and the github repo is over complicated and tedious to make sence of. 
The author should include the requirement file in .txt as they have not used anaconda environment nor is there any mention of it.
They should also try to run the code and write better descriptions on what the steps are doing.

Small sample sets should be included in papers to help get the code running and replicate results without much wait or struggle.

If there is a GitHub link, there is usually an issue tab. 
I would recommend the reader to check that out before attempting to reproduce the paper.
In the issues tab, people have raised issues with the code and dataset, which might save a lot of time.
https://github.com/cure-lab/ContraNet/issues

Secondly, I would also recommend checking out the youtube video related to the paper which in some cases is available by the authors.
https://www.youtube.com/watch?v=IZc4mgc3fUg

Yes, after reading the introduction of the paper, I would go straight to the youtube video of the paper.
