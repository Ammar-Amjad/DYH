# Do Your Homework: Ensuring Reproducibility in Deep Learning Research

## Abstract
This repository hosts the project "Do Your Homework," which addresses the critical issue of reproducibility in scientific research, particularly within the field of computer network security. The project presents a framework of metrics to measure the reproducibility of Deep learning research papers, aiming to save researchers time by providing a streamlined method for assessing a paper's credibility based on code and data availability, as well as the ease of recreating results.

## Introduction
Reproducibility is the cornerstone of scientific credibility. Yet, the scientific community grapples with the challenge of irreproducible research. "Do Your Homework" introduces methodological improvements to the traditional paper review process, enhancing the efficiency of validating research findings by up to 80%.

## Methodology
Our methodology encompasses several stages, from reading and understanding research papers to collecting data, writing and running code, and finally, verifying the results. We leverage metrics such as the time taken to: find datasets, read papers, recreate unavailable code, and verify results as credible criteria for reproducibility.

## Analysis
The data collected reveals that over 80% of the time spent on reproducing research is dedicated to verifying its reproducibility. Our findings suggest that proper code versioning and Docker-izing can significantly improve this process. However, challenges remain with hardware dependencies and incomplete datasets.

## Future Directions
To enhance reproducibility, we advocate for the use of tools like GitHub and Docker, as well as community engagement through reproducibility contests and rewards. Moreover, we emphasize the potential of containerization to replicate research environments faithfully.

## Project Details

### Project Statement
We examine papers from leading security conferences, aiming to highlight the importance of reproducibility and identify whether the models presented are reproducible.

### Project Task
The task involves evaluating the reproducibility of models outlined in the research papers.

### Project Deliverables
This repository contains:
- Reproducible code and models.
- Datasets used in the papers.
- Execution instructions for the models.
- Results of running the models.
- Write-ups explaining cases of irreproducibility.

## Recommendations for Reproducibility

### Containerization and Detailed Methods
- **Containerization**: We strongly advocate for the use of containerization tools such as Docker or Kubernetes. These tools can streamline the reproduction process by providing a consistent environment for running code.
- **Method Detailing**: Authors should offer a clear method for labeling data clusters or provide a labeled dataset. This would significantly lower the barrier to entry for reproducing results.

### Sample Data and Issues Tab
- **Sample Data Sets**: Including smaller sample data sets in papers can enable quick validation of code and methods without extensive computation or data wrangling.
- **GitHub Issues Tab**: Before attempting to reproduce results, we recommend visiting the paper's GitHub Issues tab for insights into common problems and solutions others have encountered, potentially saving significant time.
  - DeepCASE example: [DeepCASE Issues](https://github.com/Thijsvanede/DeepCASE/issues?q=is%3Aissue+is%3Aclosed)
  - Whisper example: [Whisper Issues](https://github.com/fuchuanpu/Whisper/issues)
  - ContraNet example: [ContraNet Issues](https://github.com/cure-lab/ContraNet/issues)

## Related Work
The project is inspired by and builds upon previous works that have tackled the reproducibility crisis, such as "Reproducing 150 Research Papers and Testing Them in the Real World: Challenges and Solutions" with Grigori Fursin.
