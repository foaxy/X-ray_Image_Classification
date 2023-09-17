## Pneumonia Detection from X-ray Images using Deep Learning



## Business Understanding

Safer Health Centre aims to improve patient care and diagnosis accuracy by integrating advanced technology into their medical processes. To achieve this, they want to implement a deep learning model that can classify whether a pediatric patient has pneumonia or not based on chest x-ray images. This initiative aligns with their mission of providing the best care using advanced technology in an atmosphere of trust, safety, and comfort. The current diagnostic process, while effective, relies heavily on the expertise of medical professionals and can be time-consuming. To enhance diagnostic efficiency and accuracy, there is a need to develop an automated system that can classify whether a pediatric patient has pneumonia or not based on chest x-ray images.

## Problem Statement

The key problems to address in this project are as follows:

- **Manual Diagnosis Limitations**: The current manual diagnosis of pneumonia from chest x-ray images is subjective, time-intensive, and can be prone to errors due to human variability.

- **Scaling Diagnostic Capability**: Safer Health Centre desires to scale its diagnostic capabilities by incorporating advanced technology, allowing for faster and more consistent diagnosis, especially in cases of a high patient load.

- **Accuracy and Reliability**: The hospital aims to develop a model that can provide accurate and reliable pneumonia diagnosis, ensuring that patients receive appropriate and timely treatment.

- **Integration with Existing Workflow**: The solution should seamlessly integrate into Safer Health Centre's existing diagnostic workflow, allowing medical professionals to use the automated system as a supplementary tool for diagnosis.

- **Safety and Patient Trust**: Maintaining patient trust and safety is paramount. The developed model must be rigorously tested and validated to ensure it aligns with international healthcare standards and provides results that medical professionals can trust.

- **Efficiency and Speed**: The automated system should significantly reduce the time required for diagnosis, enabling prompt treatment decisions and potentially saving lives in critical cases.

In light of these challenges, the project aims to build a deep neural network model for image classification that can accurately determine whether a pediatric patient has pneumonia based on chest x-ray images. This model will contribute to Safer Health Centre's mission of providing advanced, trustworthy, and efficient healthcare services while upholding the highest standards of patient care and safety



## Data Understanding

The dataset provided for this project comprises chest X-ray images of pediatric patients, encompassing individuals with both pneumonia-affected lungs and those with normal lung conditions. The dataset has been meticulously organized to support the development and evaluation of machine learning or deep learning models for pneumonia classification. It is structured into three primary directories: "test," "train," and "val," each serving distinct purposes in the modeling process.

Within these directories, the data is categorized into two primary groups:

- 1. **Normal**: This category consists of chest X-ray images depicting pediatric patients with healthy lungs.

- 2. **Pneumonia**:These images reflect conditions characterized by lung infections or inflammations.

The dataset's meticulous organization into training, testing, and validation subsets ensures that it can be effectively employed for the following purposes:

- **Training**: It contains a substantial number of labeled chest X-ray images, both normal and pneumonia-affected, enabling the model to learn the distinguishing features between the two classes.

- **Testing**: It contains a separate set of labeled images to assess the model's ability to generalize and correctly classify new, unseen data.

- **Validation**: It aids in fine-tuning the model's hyperparameters and ensuring its robustness by assessing performance on a distinct set of data.

The availability of both normal and pneumonia-affected cases within this dataset offers a comprehensive foundation for building a reliable pneumonia detection model, contributing to Safer Health Centre's mission of leveraging advanced technology to improve patient care and diagnosis accuracy.

## Data Visualization

Below is a plot of X-ray images of normal and infected lungs. The images unveil conspicuous regions of opacity or consolidation within the lung tissue of the infected lungs.

![Imabalance](https://github.com/foaxy/X-ray_Image_Classification/blob/master/Images/imbalance.png)

## Data Exploration

The train data seems imbalanced . To increase the number of training examples, we will use data augmentation.

![Images](https://github.com/foaxy/X-ray_Image_Classification/blob/master/Images/sample_images.png)

## Data Modelling

### Baseline model

![Baseline_Model](https://github.com/foaxy/X-ray_Image_Classification/blob/master/Images/dense_curves.png)

The dense model achieved a test accuracy of 78.04%, indicating that it can classify the test data with a reasonable level of accuracy. However, the test loss of 0.4762 suggests that there is still room for improvement, and further optimization or tuning of the model may be beneficial to reduce this loss and potentially increase accuracy.

### CNN Model

![CNN_Model](https://github.com/foaxy/X-ray_Image_Classification/blob/master/Images/cnn_curves.png)

- **Test Loss**: The test loss for the CNN model is 0.3408. This is significantly lower than the test loss of the dense model (0.4762). A lower test loss indicates that the CNN model's predictions are, on average, closer to the true labels in the test dataset. This suggests that the CNN model is better at capturing the underlying patterns and features in the data.

- **Test Accuracy**: The test accuracy for the CNN model is 88.62%. This accuracy is notably higher than that of the dense model (78.04%). The CNN model correctly classifies approximately 88.62% of the test samples, indicating a substantial improvement in performance over the dense model.

In comparison to the dense model, the CNN model demonstrates superior performance with both a lower test loss and higher test accuracy. Therefore, the CNN model is more effective at recognizing and classifying pneumonia status of an individual using X-ray images

## Conclusion

The dense model achieved a test accuracy of 78.04% with a test loss of 0.4762, while the CNN model outperformed it significantly, attaining a higher test accuracy of 88.62% and a notably lower test loss of 0.3408. These results underscore the effectiveness of Convolutional Neural Networks (CNNs) in image classification tasks, as they are specifically designed to capture intricate spatial patterns and hierarchical features within images. Therefore, when dealing with image data as in our case, the CNN model is the preferred choice due to its superior performance in both accuracy and loss compared to the dense model. 

![Confusion_matrix](https://github.com/foaxy/X-ray_Image_Classification/blob/master/Images/c_matrix.png)

The displayed confusion matrix above provides insights into the classification results. It shows that 264 predictions successfully identified X-rays as pneumonia cases, constituting true positives. 

## Recommendation

In light of the business understanding and problem statement provided, we strongly recommend proceeding with the development and implementation of a deep learning model for pneumonia classification from chest X-ray images. This initiative aligns seamlessly with Safer Health Centre's mission to enhance patient care, diagnosis accuracy, and overall healthcare services. Here are key reasons to support this recommendation:

- **Improved Accuracy and Reliability**: By leveraging advanced technology, Safer Health Centre can develop a model that provides accurate and reliable pneumonia diagnoses. This ensures that patients receive timely and appropriate treatment, which is crucial for their well-being.

- **Scale Diagnostic Capabilities**: Implementing a deep learning model allows Safer Health Centre to scale its diagnostic capabilities. This is especially valuable during periods of high patient loads, where automation can alleviate the burden on medical professionals.

- **Integration with Existing Workflow**: The project's focus on seamless integration into the existing diagnostic workflow is commendable. This ensures that medical professionals can easily adopt the automated system as a supplementary tool, enhancing their diagnostic capabilities.

In conclusion, the development and implementation of a deep learning model for pneumonia classification from chest X-ray images represent a valuable opportunity for Safer Health Centre to enhance patient care, diagnosis accuracy, and overall healthcare services. This project embodies the organization's commitment to leveraging advanced technology to benefit both medical professionals and patients.

## Non-Technical Presentation

Click here [Link](https://docs.google.com/presentation/d/1Sgbs_X1BPQPpGx0ROMIyjm3qvhVgisnv88GU7RviOTM/edit?usp=sharing) to view the non-technical presentation.
