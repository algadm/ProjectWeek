---
layout: pw43-project

permalink: /:path/

project_title: Evaluating concordance of AI-based anatomy segmentation models
category: Segmentation / Classification / Landmarking

key_investigators:

- name: Lena Giebeler
  affiliation: BWH/RWTH Aachen
  country: USA/Germany

- name: Deepa Krishnaswamy
  affiliation: BWH
  country: USA

- name: Ron Kikinis
  affiliation: BWH
  country: USA

- name: David Clunie
  affiliation: PixelMed Publishing
  country: USA

- name: Andrey Fedorov
  affiliation: BWH
  country: USA

---

# Project Description

<!-- Add a short paragraph describing the project. -->


Quantitative analysis of large-scale medical imaging datasets can be streamlined using automated segmentation. The growing number of AI-based methods for anatomical segmentation raises a central challenge of choosing among functionally similar models due to: the absence of ground truth data for representative samples, and practical challenges in comparing segmentation results (inconsistent structure naming, non-uniform formats, and complexity of visualization). Our work alleviates these issues by evaluating six open-source segmentation models—TotalSegmentator 1.5 and 2.6, Auto3DSeg, Moose, MultiTalent, and OMAS—on a sample of CT scans from the publicly available National Lung Screening Trial (NLST) dataset. We analyzed 31 anatomical structures—lungs, vertebrae, ribs, and heart—after harmonizing segmentation results to follow consistent representation. To support visual comparison, we developed open-source tools in 3D Slicer automating loading, structure-wise inspection and comparison across models. For quantitative comparison we evaluated consensus segmentations per structure and assessed model agreement using Dice similarity and volume differences. Preliminary results show excellent agreement segmenting some (e.g., lung) but not all structures (e.g., some models produce invalid vertebrae or rib segmentations). Only one model, Moose, segmented the costovertebral joints—rib-to-spine connections. Overall, this work assists in model evaluation in absence of ground truth, ultimately enabling informed model selection.



## Objective

<!-- Describe here WHAT you would like to achieve (what you will have as end result). -->


This project builds upon the previous work "Review of segmentation results quality across various multi-organ segmentation models", conducted during the last Project Week in Gran Canaria. The goal is to systematically evaluate and compare the segmentations of six publicly available multi-organ segmentation models. This evaluation is done by identifying areas of agreement and disagreement across anatomical structures in our dataset, for which ground truth segmentations are unavailable.

During this Project Week, we will improve upon and extend the previous analysis by extending the scope of comparison, and engaging with the users of the evaluated models and model developers.



## Approach and Plan

<!-- Describe here HOW you would like to achieve the objectives stated above. -->


1. Discuss the current analysis results with developers and interested community members
   * discuss problematic results
   * learn about other observed or potential errors we should investigate
   * discuss approaches for selecting representative test data sample from NLST
   * collect feedback, observations, and suggestions for improvement
3. Improve and extend the analysis based on this discussion
4. Secondary: Slicer Segmentation Verification module extension used for visual comparison 
   * revisit loading of DICOM SEG as Segmentation and see if any optimizations can be implemented to the code to speed up Segmentation node creation (need to profile the load process further first)
   * discuss developed new features designed to simplify the process of comparison of the results from different models
   * discuss possible improvements to the performance of populating Segmentation node loaded from DICOM SEG



## Progress and Next Steps

<!-- Update this section as you make progress, describing of what you have ACTUALLY DONE.
     If there are specific steps that you could not complete then you can describe them here, too. -->

Current Status of our Analysis:
- Preliminary results show excellent agreement for the lungs.
- Inconsistencies were found in the segmentation of vertebrae and ribs:  4 out of 6 models produce invalid or anatomically implausible segmentations for these structures.
-  Only one model, Moose, includes segmentation of the costovertebral joints (rib-to-spine connections).
- OMAS uses a different anatomical definition for the heart compared to the other models, leading to differences in the heart segmentation.

The Slicer Segmentation Verification Module Extension currently:
- Displays available segmentations based on the selected volume.
- Visualizes chosen segmentations in both 3D and 2D slice views.
- Allows switching between horizontal (default) and vertical layout.
- Adds functionality to automatically link 3D views via checkbox.
- Provides option to link 2D views using a checkbox.
- Enables displaying only segmentation outlines in 2D slice views.




# Illustrations

<!-- Add pictures and links to videos that demonstrate what has been accomplished. -->

An interactive poster with a summary of the results and the current state of the project can be found at the following link:
[https://www.dropbox.com/scl/fi/c84sm9djytyi80jk2ixfa/giebeler.lena.pptx?rlkey=g3sf82zuv5fgmuog0an3dsy96&dl=0](https://www.dropbox.com/scl/fi/c84sm9djytyi80jk2ixfa/giebeler.lena.pptx?rlkey=g3sf82zuv5fgmuog0an3dsy96&dl=0)

**Current Status of the Slicer Segmentation Verification Module Extension:**


<video
  controls muted
  src="https://github.com/user-attachments/assets/44b9d5e9-f88c-4c82-9bcf-879a62702d38"
  style="max-height:640px; min-height: 200px">
</video>




# Background and References

<!-- If you developed any software, include link to the source code repository.
     If possible, also add links to sample data, and to any relevant publications. -->


* This project is continuing earlier PW42 project ["Review of segmentation results quality across various multi-organ segmentation models"]( https://projectweek.na-mic.org/PW42_2025_GranCanaria/Projects/ReviewOfSegmentationResultsQualityAcrossVariousMultiOrganSegmentationModels/)
* [My fork of the Segmentation Verification Module](https://github.com/LenaGiebeler/SlicerSegmentationVerification)
  * PR adding new features upstream: [https://github.com/cpinter/SlicerSegmentationVerification/pull/3](https://github.com/cpinter/SlicerSegmentationVerification/pull/3)
* AI segmentation models (Git repositories): 
  * [TotalSegmentator](https://github.com/wasserth/TotalSegmentator)
  * [Auto3DSeg](https://github.com/Project-MONAI/tutorials/tree/main/auto3dseg)
  * [Moose](https://github.com/ENHANCE-PET/MOOSE), and [MultiTalent](https://github.com/MIC-DKFZ/MultiTalent)

