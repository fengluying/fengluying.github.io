---
title: "Locomotion Joint Angle and Moment Estimation with Soft Wearable Sensors for Personalized Exoskeleton Control"
collection: publications
permalink: /publication/LJAME-SWS-PEC
excerpt: 'This study developed a flexible sensing system capable of accurately predicting joint angles and moments, and validated it through a flexible exosuit. '
date: 2025-03-09
venue: 'IEEE Transactions on Neural Systems and Rehabilitation Engineering'
paperurl: 'https://doi.org/10.1109/TNSRE.2025.3547361'
citation: 'L. Feng et al., "Locomotion Joint Angle and Moment Estimation with Soft Wearable Sensors for Personalized Exosuit Control," in IEEE Transactions on Neural Systems and Rehabilitation Engineering, doi: 10.1109/TNSRE.2025.3547361.'
year: 2025
---
## Abstract
Recent advancements in flexible sensing and machine learning have positioned soft sensors as promising alternatives to traditional methods for human posture detection. However, most research has centered on calibration, with limited progress in practical applications due to the challenges posed by diverse users and complex scenarios such as human-robot interaction. To address these challenges, this study developed a flexible sensing system capable of accurately predicting joint angles and moments, and validated it through a flexible exosuit. To improve the model's accuracy and generalization, gait data from eight participants with varying walking patterns were collected. Calibrated data were used as static features and trained alongside dynamic features. The model was pre-trained on a large open-source dataset and fine-tuned using transfer learning for our data. Long Short-Term Memory (LSTM) and Convolutional Neural Network (CNN) models were specifically applied to estimate knee joint angles and hip joint moments, achieving a Mean Absolute Error (MAE) of 4.43° and 0.12 Nm/kg, respectively. A flexible exosuit was then developed to provide assistance based on real-time estimations of hip joint moments, enabling personalized control. Testing with five volunteers showed reduced muscle activation, while user satisfaction surveys indicated significant improvements in mobility and comfort. This research not only enhances the practical application of soft sensors but also demonstrates their potential in advancing human-robot interaction.

### Data Collection
<div style="display:flex;justify-content:center;">
<video width="600" controls>
  <source src="/images/Data_collection_LOCO.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div>

### Personalized Assistance Experiments
<div style="display:flex;justify-content:center;">
<video width="600" controls>
  <source src="/images/Personalized.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div>

### Appandx
<div style="display:flex;justify-content:center;">
   <img src="/images/TNSRE_appendix_00.png" width="600" alt="Fig" style="margin:auto;">
</div>
<div style="display:flex;justify-content:center;">
   <img src="/images/TNSRE_appendix_01.png" width="600" alt="Fig" style="margin:auto;">
</div>
<br>

### Questionnaire Survey Results
<div style="display:flex;justify-content:center;">
   <img src="/images/WEN.png" width="600" alt="Fig" style="margin:auto;">
</div>
<br>

