# Breast-Cancer-Detection
Breast cancer detection with screening mammograms obtained from regular screening.

## Motivation
According to the WHO, breast cancer is the most commonly occurring cancer worldwide. In 2020 alone, there were 2.3 million new breast cancer diagnoses and 685,000 deaths. Yet breast cancer mortality in high-income countries has dropped by 40% since the 1980s when health authorities implemented regular mammography screening in age groups considered at risk. Early detection and treatment are critical to reducing cancer fatalities. In this project, I developed multiple cancer detection models from routine mammography scans and compared their performance.


## Analysis
### Target column distribution
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/target.png)

### Correlation
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/correlation.png)

### Healthy breasts
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/healthy.png)

### Abnormal breasts
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/abnormal.png)

### Natural breast with cancer
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/natural%20with%20cancer.png)

### Implant breast with cancer
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/implant%20with%20cancer.png)

## My Approch:
<p>
<li>The given DCM image files were converted to PNG. I tried converting the file in the data generator, but it took 
  extra time.
</li>
<li>Most of the regions in the image didn't contain useful information. So, I extracted the Region of
  Interest (ROI) and created a new dataset to work with.
</li>
<li>Transfer learning was used to evaluate the performance of various well-known architectures 
  (AlexNet, VGG-16, Resnet50, and EfficientNet). The performance of various vision transformers was then evaluated.</li>
<li>The performance of vision transformer was satisfactory and the results are given in the table below.</li>


## Result

<table>
  <thead>
    <tr>
      <th>Algorithm</th>
      <th>Accuracy</th>
      <th>AUC</th>
      <th>Pf1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>EfficientNetV1B0</td>
      <td>0.9767</td>
      <td>0.5920</td>
      <td>0.0417</td>
    </tr>
     <tr>
      <td>ConvNeXtTiny</td>
      <td>0.9793</td>
      <td>0.7009</td>
      <td>0.0647</td>
    </tr>
     <tr>
      <td>FlexiViTSmall</td>
      <td>0.9778</td>
      <td>0.5297</td>
      <td>0.0305</td>
    </tr>
     <tr>
      <td>DaViT_T</td>
      <td>0.9781</td>
      <td>0.6953</td>
      <td>0.0719</td>
    </tr>
  </tbody>
</table>

### ConvNeXtTiny history
![alt text](https://github.com/Bakar31/Breast-Cancer-Detection/blob/master/convnet%20history.png)
