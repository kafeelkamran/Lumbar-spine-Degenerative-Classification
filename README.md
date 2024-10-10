# Lumbar-spine-Degenerative-Classification

Table of Contents
Introduction
The Spine: Basic Overview
Lumbar Spine Anatomy
Vertebrae
Intervertebral Discs
Facet Joints
Vertebral Levels and Their Significance
Intervertebral Disc Anatomy
Lumbar Disc Degeneration and Zones of Degeneration
Degenerative Spine Conditions
Canal Stenosis
Foraminal Narrowing
Subarticular Stenosis
MRI Imaging of the Lumbar Spine
T1-Weighted Imaging
T2-Weighted Imaging
STIR Imaging
Severity Classification Criteria
MRI in the Diagnosis of Spinal Stenosis
Dataset Overview and Key Files
Conclusion

# Introduction

In this notebook, we explore the anatomical aspects essential for developing a deep learning model aimed at detecting and classifying the severity of lumbar spine degeneration using MRI scans. Understanding the anatomy is crucial for accurate data annotation, model training, and interpretation of results. The dataset used in this study includes DICOM (.dcm) files and accompanying metadata in CSV format, encompassing data from 1975 patients. This comprehensive dataset provides a solid foundation for training and evaluating machine learning models, offering a valuable resource in the development of automated diagnostic tools for lumbar spine degeneration.

Let's briefly discuss the anatomy relevant to this dataset to understand what we're asking you to detect

## The Spine: Basic Overview 
The human spine is a column of bones (vertebrae) and intervertebral discs that provide structural support and protect the spinal cord. It is divided into five sections:

 - Cervical Spine (Neck): C1-C7 vertebrae
 - Thoracic Spine (Upper Back): T1-T12 vertebrae
 - Lumbar Spine (Lower Back): L1-L5 vertebrae
 - Sacral Spine (Pelvis): S1-S5 fused vertebrae
 - Coccyx (Tailbone): 3-4 fused vertebrae


![image](https://github.com/user-attachments/assets/870a3ddf-6ee2-4619-b2d6-e0b79c621658)


### Basic Functions of the Spine:

#### Protection: Encloses and protects the spinal cord and nerve roots.
#### Mobility: Allows for bending, twisting, and other movements.
#### Support: Bears the weight of the head and trunk, transferring forces to the pelvis and lower limbs.

### Lumbar Spine Anatomy
The lumbar spine refers to the lower back region, consisting of five vertebrae (L1 to L5) and several related anatomical structures that are prone to degeneration and can lead to pain or nerve impingement. Understanding these structures will enhance the ability to interpret MRI images and classify conditions more effectively.

1. Vertebrae
 The lumbar vertebrae are larger and stronger than the vertebrae in the upper spine because they bear more weight.
  Each vertebra consists of:
   - Body: The thick, anterior part that bears the weight.
   - Vertebral Arch: A bony ring forming the spinal canal, where the spinal cord passes through.
   - Spinous and Transverse Processes: Projections that provide points of attachment for muscles and ligaments.

2. Intervertebral Discs
 Between each pair of lumbar vertebrae is an intervertebral disc. These discs act as shock absorbers, cushioning the bones during movement and preventing the vertebrae from rubbing against each other.
  Structure of an Intervertebral Disc:
   - Nucleus Pulposus: The soft, gel-like center that absorbs shock.
   - Annulus Fibrosus: The tough, outer layer made of collagen fibers, which keeps the disc in place.
  
3. Facet Joints
  Each vertebra connects to the one above and below it through facet joints, which allow controlled motion and provide stability to the spine.
   - Facet joints are located at the back of the spine, between the vertebrae.
   - Degeneration in these joints can result in pain and limited motion.


![image](https://github.com/user-attachments/assets/73931edf-5ead-4c80-8d64-558919814bce)


### Vertebral Levels and Their Significance
 Understanding the vertebral levels is crucial for precise diagnosis and treatment planning. Each level from L1/L2 to L5/S1 has distinct anatomical and functional characteristics.

 - L1-L2: Upper lumbar region, less mobility compared to lower levels.
 - L2-L3: Mid-lumbar region, common site for disc herniations.
 - L3-L4: Lower lumbar region, significant for weight-bearing.
 - L4-L5: Highly mobile, frequent site for degenerative changes.
 - L5-S1: Junction between lumbar spine and sacrum, critical for stability.


![image](https://github.com/user-attachments/assets/d09f3c0d-1435-4a42-a118-0b005dd3fd28)


### Intervertebral Disc Anatomy
 Intervertebral disc is a cushion-like structure between the vertebrae of the spine.

  - Nucleus pulposus: The soft, jelly-like center of the intervertebral disc.
  - Annulus fibrosus: The tough, outer ring of the intervertebral disc.
  - Spinal cord: A long, bundled structure of nerves that runs through the spinal canal.
  - Neural foramen: A passageway for nerves to exit the spinal column.
  - Nerve root: The beginning of a spinal nerve, which branches off from the spinal cord

 
 ![image](https://github.com/user-attachments/assets/02e25dad-6e36-4b67-9260-2ac80eeeb8d1)
 

 ### Lumbar Disc Degeneration
  A condition where the soft, gel-like nucleus of a lumbar disc bulges or ruptures through the outer, tougher annulus.
    
  Zones of Degeneration
  
   - Central zone: The innermost part of the disc.
   - Subarticular zone: Between the central zone and the facet joint.
   - Foraminal zone: Toward the nerve root foramen.
   - Extraforaminal zone: Beyond the nerve root foramen.

 
 ![image](https://github.com/user-attachments/assets/c6a26cab-ebd7-47d3-af16-b47b61188ee9)
 

### Degenerative Spine Conditions
 As the spine ages or due to mechanical stress, certain degenerative conditions may develop in the lumbar region, affecting the spinal nerves. Your model will classify these conditions into normal/mild, moderate, or severe grades based 
 on the compression and narrowing.

### 1) Canal Stenosis
  Spinal canal stenosis is a condition where the spinal canal becomes narrowed, compressing the spinal cord or the cauda equina (a bundle of nerve roots). This can result in significant neurological symptoms, including pain, numbness, 
  and muscle weakness.
   - Unlike foraminal or subarticular stenosis, canal stenosis does not affect one side of the spine but can occur at specific lumbar levels (L1/L2 to L5/S1).

### 2) Foraminal Narrowing
 Foraminal narrowing, or foraminal stenosis, occurs when the foramen becomes smaller due to disc degeneration, bone spurs, or ligament thickening. This can compress the spinal nerves exiting the spinal canal, leading to symptoms such as 
 pain, numbness, or weakness.
   - Left/Right Neural Foraminal Narrowing: The narrowing can happen on either the left or right side of the spine at any lumbar level (L1/L2 to L5/S1).

### 3) Subarticular Stenosis
 Subarticular stenosis involves the narrowing of the space where the nerve roots exit the spine, which may lead to impingement of the nerves before they reach the foramina. This condition is also known as lateral recess stenosis.
   - Left/Right Subarticular Stenosis: Can occur on either side of the spine, usually due to disc herniation or bone spurs.

 
 ![image](https://github.com/user-attachments/assets/0fe2cd73-ab5c-484e-9f43-4229502db044)
 

## MRI Imaging of the Lumbar Spine
 Magnetic Resonance Imaging (MRI) is a valuable tool for evaluating the lumbar spine. By using strong magnetic fields and radio waves, it provides detailed images of the bones, discs, spinal cord, and surrounding tissues.

 Key MRI sequences used in lumbar spine imaging include:

 ### 1) T1-Weighted Imaging:
   - Appearance: Bone appears bright, while soft tissues and cerebrospinal fluid (CSF) appear dark.
   - Purpose: Excellent for evaluating bone anatomy, cortical bone, and certain types of tumors.

### 2) T2-Weighted Imaging:
  - Appearance: Bone appears dark, while soft tissues and CSF appear bright.
  - Purpose: Ideal for detecting inflammation, edema, fluid collections, and certain types of tumors.

### 3) STIR (Short T1 Inversion Recovery) Imaging:
  - Appearance: Similar to T2-weighted, but with increased suppression of fat
  - Purpose: Used to better visualize inflammatory changes, edema, and lesions within the bone marrow.
  
  Note: In the dataset, Sagital T2 and STIR images are likely the same. This is because STIR is a specific type of T2-weighted sequence that is optimized for detecting fluid-containing tissues.

 
 ![image](https://github.com/user-attachments/assets/3ca9147a-3a21-4302-aa90-1ce3d6be3e1b)
 

 ### MRI Views:

  1. Sagittal Plane: Divides the body into left and right halves.

  2. Coronal Plane: Divides the body into anterior (front) and posterior (back) halves.

  3. Axial Plane: Divides the body into superior (top) and inferior (bottom) halves.

 Note: The dataset contains sagittal and axial MRI scans, but no coronal images.


![image](https://github.com/user-attachments/assets/16149ed3-ae7c-400f-b371-fc0519d0d4a4)


### Severity Classification Criteria
  Each condition is classified into three severity levels based on the degree of compression:

  - Normal/Mild (0 - 0.33): Minimal or no compression, unlikely to cause significant symptoms.
  - Moderate (0.34 - 0.66): Noticeable compression with potential symptoms.
  - Severe (0.67 - 1.00): Significant compression, likely causing severe symptoms.


![image](https://github.com/user-attachments/assets/2b8b7117-b044-44ac-a894-ec96dc5781ac)


### MRI in the Diagnosis of Spinal Stenosis
 The Role of Radiologists

  - Radiologists specialize in interpreting medical images, including MRI scans.
  - They identify and diagnose spinal stenosis and other conditions based on MRI findings.
  - Radiologists prepare detailed reports outlining their findings and recommendations.
  - Neurologists or orthopedic surgeons may also review MRI images and the radiologist's report.
  - They confirm the diagnosis and determine the appropriate course of treatment.


![image](https://github.com/user-attachments/assets/990fb61e-969a-4334-99ae-720deaee30ce)


### MRI Techniques for Spinal Stenosis

 -  Visualizing the Spinal Canal: MRI provides detailed images of the spinal canal, allowing for measurement of its size and identification of narrowing.
 -  Examining Nerve Roots: MRI can visualize nerve roots exiting the spinal cord and assess their relationship to surrounding bony structures. Foraminal narrowing occurs when nerve roots are compressed by encroaching bone or soft 
   tissues.
 -  Assessing Facet Joints: MRI can evaluate the size and condition of facet joints, located between vertebrae. Subarticular stenosis occurs when these joints become enlarged or develop bony overgrowths that narrow the spinal canal.
 - Detecting Soft Tissue Changes: MRI can identify soft tissue abnormalities, such as herniated discs or spinal tumors, which can contribute to spinal stenosis.

![image](https://github.com/user-attachments/assets/7dfe20e9-7c5a-4bc2-ad16-44ffdbfca2e3)

## Dataset Overview:

  Total Files: 147,320 files.
  
  Total Size: 35.34 GB.
  
  File Types: Primarily DICOM (.dcm) files and CSV files.
  
  The test dataset contains MRI data from only one patient, while the training dataset includes MRI data from 1975 patients. Both datasets contain sagittal and axial MRI scans in T1 and T2 weighting.

##### Directory Structure:

   kaggle/input/rsna-2024-lumbar-spine-degenerative-classification: This is the root directory of the dataset.
   - test_images:
       44036939 (study_id): A subdirectory containing test images.
       
       2828203845 (series_id): A subdirectory within the previous one, likely representing a specific test case.

       1.dcm, 2.dcm, 3.dcm, ... : DICOM image files.
     
... : Indicates additional subdirectories with similar structure.

   - test_series_descriptions.csv: A CSV file containing descriptions for the test series.
 
   - train_images:
        4003253 (study_id): A subdirectory containing training images.
     
        702807833 (series_id): A subdirectory within the previous one, likely representing a specific training case.

     1.dcm, 2.dcm, 3.dcm, ... : DICOM image files.
     
... : Indicates additional subdirectories with similar structure.

... : Indicates additional subdirectories with similar structure.

   - train_label_coordinates.csv: A CSV file containing label coordinates for the training MRI images.

   - train_series_descriptions.csv: A CSV file containing descriptions for the training series.

   - train.csv: A CSV file likely containing information about the training data.


![image](https://github.com/user-attachments/assets/a1ffb0c9-7532-457b-8823-cc77337a3937)


### Key Files and Their Contents:
  
  - train.csv:

    - Purpose: Contains labels for the training set.

    - 26 Columns:

      - study_id: Unique identifier for each study, which may include multiple image series.
       [condition]_[level]: Labels for specific conditions, with severity levels: Normal/Mild, Moderate, or Severe. 
       [spinal_canal_stenosis/left_neural_foraminal_narrowing/right_neural_foraminal_narrowing/left_subarticular_stenosis/right_subarticularstenosis][l1_l2/l2_l3/l3_l4/l4_l5/l5_s1]
       Note that some entries may have incomplete labels.


 - train_label_coordinates.csv:

     - Purpose: Provides coordinates for labeled regions in training images.

     - 7 Columns:

        - study_id: Identifies the study.
        - series_id: Identifies the specific series within the study.
        - instance_number: Indicates the slice number within the 3D stack of MRI.
        - condition: Specifies conditions like spinal canal stenosis, left/right neural foraminal narrowing, and left/right subarticular stenosis, with some conditions evaluated on spine.
        - level: Specifies the vertebral level involved (e.g., l3_l4).
        - [x/y]: Coordinates marking the center of the labeled region of MRI.
      

  - [train/test]_series_descriptions.csv:

     - Purpose: Provides metadata on each series.
     
     - 3 Columns:

        - study_id: Study identifier.
        - series_id: Series identifier.
        - series_description: Describes the scan orientation, which is essential for understanding the anatomical view (e.g., Axial T2, Sagittal T1, Sagittal T2/STIR).
      
   - sample_submission.csv:

      - Purpose: Provides a template for how predictions should be formatted.

      - 4 Columns:

        - row_id: A unique identifier combining study ID, condition, and level (e.g., 4003253_spinal_canal_stenosis_l3_l4).
 
        - [normal_mild/moderate/severe] - The three prediction columns.


## Conclusion

In this notebook, we covered the key anatomical structures of the lumbar spine, along with their significance in lumbar spine degeneration. We also explored various degenerative conditions such as canal stenosis, foraminal narrowing, and subarticular stenosis, which are critical for detecting and classifying lumbar spine conditions using MRI scans. Additionally, we provided an overview of the dataset, which includes CSV files and DICOM (.dcm) files containing metadata. This dataset comprises 1975 patients, offering a valuable resource for training and evaluating models for lumbar spine condition classification. Have fun with the challenge!











