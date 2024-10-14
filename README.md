# Fruit Image Classification 

## Overview
This my submission for Bina University's Deep Learning course mid exam. The task is classifying a dataset containing four different category of fruits (cashew, cempedak, coconut cranberry). 
The question requires the fine tuning of a base VGG-16 model, modifying various hyperparameters and comparing its performance to a standard VGG-16 model.

## Data
The data consists of four categories of fruits which are cashew, cempedak, coconut and cranberry. Each category consists 400 images.

![dlimages](https://github.com/user-attachments/assets/5aed523e-04cf-4463-8ec1-f521520fe5b3)

## Approaches and Techniques
### Feature Engineering
* Histogram Equalization
 Histogram equalization is a technique used in image processing to enhance the contrast of an image. This is used to increase the visibility of the features of the image, making the model able to learn more effectively

  **Before histogram equalization**
    ![image](https://github.com/user-attachments/assets/31b27e3b-4cec-408f-b944-4d5f467f3acf)
    
  **After histogram equalization**  
    ![image](https://github.com/user-attachments/assets/9d642f14-41e6-419c-8a30-dcaeaaa8ba59)
  

* Data augmentation
  Data augmentation is used  to increase the diversity of training datasets without collecting new data. Adding rotation, gaussian blur, linear contrast, image multiplication are some of the techniques that are used for this.
  
  ![image](https://github.com/user-attachments/assets/7566efa4-05c1-4595-bae3-d9e29f613794)


* Image resizing
  The images are resized to be 224 x 224 pixel for model training.

### Modifications
* Added L1 regularization  
* Added L2 regularization  
* Added Batch normalization
* Reducing model size
## Model Performance

<table >
  <thead>
    <th>Model</th>
    <th>Class</th>
    <th>Precision</th>
    <th> Recall </th>
    <th>F1-score</th>
    <th>Accuracy</th>

  </thead>
  <tr></tr>
  


  <tr>
    <tr>
      <td>Base VGG-16</td>
      <td>Cashew</td>
      <td>0.64</td>
      <td>0.36</td>
      <td>0.46</td>
      <td>0.65</td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Cempedak</td>
      <td>0.55</td>
      <td>0.76</td>
      <td>0.64</td>
      <td></td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Coconut</td>
      <td>0.58</td>
      <td>0.64</td>
      <td>0.61</td>
      <td></td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Cranberry</td>
      <td>0.86</td>
      <td>0.85</td>
      <td>0.85</td>
      <td></td>
    </tr>
</tr>

<tr>
    <tr>
      <td>Fine Tuned VGG-16</td>
      <td>Cashew</td>
      <td>0.66</td>
      <td>0.81</td>
      <td>0.73</td>
      <td>0.77</td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Cempedak</td>
      <td>0.76</td>
      <td>0.82</td>
      <td>0.79</td>
      <td></td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Coconut</td>
      <td>0.74</td>
      <td>0.67</td>
      <td>0.71</td>
      <td></td>
    </tr>
    <tr></tr>
    <tr>
      <td></td>
      <td>Cranberry</td>
      <td>0.96</td>
      <td>0.77</td>
      <td>0.86</td>
      <td></td>
    </tr>
</tr>




</table>
