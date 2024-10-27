# Lumbar Spine Degenerative Classification 📊

## Overview

 This project utilizes MRI scans to detect and classify lumbar spine degeneration, focusing on degenerative conditions like canal stenosis, foraminal narrowing, and subarticular stenosis. Using deep learning models and a comprehensive    MRI dataset, this project aims to automate the diagnosis of lumbar spine conditions, enhancing the accuracy and speed of clinical assessments.

## Table of Contents

- Project Overview
- The Spine & Lumbar Anatomy
- Degenerative Conditions
- MRI Imaging & Classification
- Dataset
- Key Files
- Conclusion

## The Spine & Lumbar Anatomy 🧠

The human spine supports movement, protects the spinal cord, and consists of five main sections: Cervical, Thoracic, Lumbar, Sacral, and Coccyx. The lumbar spine (L1-L5), the focus of this project, is crucial for weight-bearing and is susceptible to degeneration.

### Key Structures:

- Vertebrae: Larger and stronger in the lumbar region, supporting significant weight.
- Intervertebral Discs: Cushions between vertebrae for shock absorption.
- Facet Joints: Provide stability and controlled movement between vertebrae.

## Degenerative Conditions 🚑

The model focuses on detecting three major lumbar degenerative conditions:

- Canal Stenosis: Narrowing of the spinal canal, compressing the nerves.
- Foraminal Narrowing: Compression of spinal nerves exiting through the foramen.
- Subarticular Stenosis: Narrowing affecting nerve roots near the exit foramina.

  Each condition is classified as Normal/Mild, Moderate, or Severe based on compression severity.

## MRI Imaging & Classification 📷

MRI imaging provides detailed views of lumbar spine structures:

- T1-Weighted: Highlights bone anatomy.
- T2-Weighted: Shows soft tissues, inflammation, and fluid.
- STIR: Specialized T2-weighted for better visualization of inflammatory changes.

  MRI sequences (Sagittal and Axial) are used to diagnose and classify degeneration.


## Dataset 📁
  
  Size: 35.34 GB, 147,320 files.
  Format: DICOM (.dcm) files and CSV files for metadata.
  Patients: MRI data from 1975 patients in the training set, providing Sagittal and Axial T1, T2, and STIR images.

 ### Key Files
 - train.csv: Labels and conditions for the training set (e.g., spinal canal stenosis).
 - train_label_coordinates.csv: Coordinates marking labeled regions in MRI images.
 - [train/test]_series_descriptions.csv: Metadata for each MRI series, including orientation and description.


## Conclusion

  This project provides an in-depth look at the anatomy, degenerative conditions, and MRI imaging necessary for developing a model to classify lumbar spine degeneration severity. The dataset and techniques offer a powerful resource for 
  advancing automated diagnostic tools in spinal health. Explore the code and dataset to tackle the complexities of lumbar spine degeneration classification! 🚀












