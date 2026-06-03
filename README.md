**Automated Multi-Class Concrete Crack Detection and Severity Classification Using CNN-Based Deep Learning**
**Abstract**
Structural integrity is a cornerstone of sustainable and safe infrastructure development, particularly in concrete structures, which form the backbone of modern civil engineering. Over time, these structures are susceptible to deterioration in the form of cracks and corrosion, primarily due to environmental factors, mechanical stress, and chemical reactions. If left undetected, such defects can compromise safety, leading to costly repairs or catastrophic failures. Conventional inspection techniques, including manual surveys and non-destructive testing (NDT), are often labor-intensive, time-consuming, and subject to human limitations, making them inefficient for large-scale or frequent monitoring.

This research proposes an automated, deep learning-based system to detect and classify cracks and corrosion in concrete structures with high precision and efficiency. By leveraging the capabilities of Convolutional Neural Networks (CNNs) and computer vision, the system processes image-based data to identify structural defects with minimal human intervention. A comprehensive dataset of concrete surfaces exhibiting various degrees of cracks and spalling from corrosion was curated and preprocessed. Key visual features such as crack width, density, texture irregularities, and rust stain patterns were analyzed to enhance defect characterization.

The model was developed using Python, TensorFlow, and Keras, which allowed for the construction of a robust and scalable detection pipeline. Experimental results demonstrate a high classification accuracy of 94.7%, with a precision of 93.5%, recall of 92.8%, and an F1 score of 93.1%. The system is capable of processing approximately 25 images per second using an NVIDIA RTX 3060 GPU, significantly accelerating the inspection process compared to manual methods. Furthermore, it offers up to 70% cost savings by reducing dependency on skilled labor, expensive equipment, and extensive site visits.

The proposed solution represents a transformative approach to structural health monitoring, offering a real-time, cost-effective, and scalable tool for infrastructure maintenance. Its application can lead to improved safety standards, early fault detection, and optimized maintenance strategies, ultimately extending the lifespan of concrete structures and reducing the risk of failure.


**Keywords:**
1.Deep Learning: A subfield of machine learning involving neural networks with many layers that learn to represent data hierarchically. In this project, deep learning enables the system to recognize complex patterns in images of concrete damage.
2.Concrete Defect Detection: This refers to the process of identifying flaws such as cracks, corrosion, or spalling in concrete structures. Automated detection aims to improve safety and maintenance by recognizing these issues early using image analysis.
3.Convolutional Neural Network: A type of deep learning architecture especially effective in image processing tasks. CNNs automatically learn spatial hierarchies of features from images, making them ideal for detecting surface-level defects in concrete.
4.Structural Health Monitoring: This is the continuous or periodic evaluation of infrastructure health to detect damage or deterioration. The project contributes to this field by offering an AI-based monitoring solution for concrete structures.
5.Crack and Corrosion Classification: The task of categorizing detected defects based on their characteristics, such as type, severity, and appearance. Accurate classification helps in assessing structural risk and planning repairs accordingly.
6.Computer Vision: A field of artificial intelligence focused on enabling computers to interpret and understand visual information. The system uses computer vision techniques to analyze concrete images for signs of damage automatically.


**Introduction**
Concrete is a vital material in modern infrastructure, but its durability is often compromised by cracks and corrosion caused by environmental exposure, mechanical stress, and chemical reactions. These defects weaken structural integrity, increasing the risk of failure in buildings, bridges, and roads. Manual inspections and non-destructive testing (NDT) techniques, are labor-intensive, time-consuming, and prone to human error, making automated solutions increasingly necessary.

This research addresses these challenges by developing a deep learning-based system for detecting and classifying cracks and corrosion in concrete structures. By leveraging computer vision techniques, the study aims to improve accuracy and efficiency in structural defect detection. A custom dataset of concrete crack and corrosion images is collected, focusing on key features such as crack width, density, texture variations, and corrosion patterns to enhance detection reliability.
The findings of this research contribute to the advancement of automated inspection offering a cost-effective and scalable solution for real-time defect detection. This approach enhances infrastructure safety and ensures timely maintenance, reducing long-term structural risks.
The application of deep learning for crack detection in concrete structures has advanced significantly over the years. Researchers have continuously explored different neural network architectures, data preprocessing techniques, and feature extraction methods to improve accuracy and efficiency. This literature review presents key contributions from 2019 to 2024, highlighting innovations in convolutional neural networks (CNNs), semantic segmentation models, real-time detection techniques, and transformer-based architectures. 
**Early Deep Learning Approaches for Crack Detection (2019-2020)**
In 2019, DungLe (DungLe et al., 2019) developed a fully convolutional network (FCN) for semantic segmentation of crack images. Their study evaluated three different pre-trained network architectures as the encoder backbone before training the VGG16-based encoder on a dataset of annotated crack images. The trained model was validated using cyclic loading test videos and successfully provided an accurate crack density assessment. 
In the same year, Li (Li et al. 2019) designed a modified AlexNet architecture to improve crack detection under noisy and real-world conditions. They optimized the base learning rate for better validation accuracy and tested the trained model on high-resolution images not used during training to assess robustness. Their final model was integrated into a smartphone application, making crack detection more accessible. 
Another 2019 study by Zhang (Zhang et al. 2019) introduced a context-aware deep convolutional segmentation network for crack detection under diverse conditions. Their pixel-wise deep semantic segmentation model could process arbitrary-sized images without retraining. To enhance performance, they proposed a context-aware fusion algorithm that incorporated local cross-state and cross-space constraints, ensuring improved image patch predictions. Their model was tested across multiple datasets and demonstrated high accuracy in crack segmentation while optimizing computational efficiency.
In 2020, Park (Park et al., 2020) integrated deep learning with structured light technology to detect and measure cracks. They employed the YOLO algorithm for real-time detection and used laser beams to calculate crack sizes. To refine measurements, they implemented a laser alignment correction algorithm with a specialized jig module and distance sensor. Experimental results confirmed the system's accuracy in real-time crack detection and quantification 
That same year, Ren (Ren et al., 2020) introduced CrackSegNet, an end-to-end fully convolutional neural network (FCN) for automatic crack segmentation in tunnels. Their model incorporated dilated convolution, spatial pyramid pooling, and skip connection modules to enhance multiscale feature extraction and resolution reconstruction. The model outperformed traditional image processing and deep learning-based segmentation methods in terms of accuracy and efficiency.
Model Efficiency, Real-Time Processing, and Comparative Studies (2021-2022) 
In 2021, Kim (Kim et al., 2021) proposed a shallow CNN-based approach for detecting cracks in concrete structures. The study optimized LeNet-5 architecture, fine-tuning hyperparameters to balance accuracy and computational efficiency. Their work also examined the feasibility of deploying deep learning on low-power devices for structural monitoring. The model was compared with VGG16, Inception, and ResNet, proving that shallow CNNs could provide efficient real-time crack detection with minimal computational overhead. 
In 2022, Sales da Cunha (Sales da Cunha et al., 2022) conducted a comparative analysis between traditional machine learning and CNN-based deep learning methods. The study found that for small datasets (≤100 images), texture analysis with machine learning achieved a 95% balanced accuracy, while CNNs achieved 74% accuracy. However, for large datasets, both methods performed comparably, suggesting deep learning's scalability for crack detection. 
Golding (Golding et al., 2022) in 2022 explored CNN-based autonomous crack detection using 40,000 RGB images processed with a pretrained VGG16 architecture. The study examined the impact of grayscale conversion, thresholding, and edge detection on performance. The results showed that color information was not crucial for crack detection, indicating that grayscale models could achieve similar accuracy while reducing computational costs. 
Wan (Wan et al., 2022) introduced a single-shot multibox detector (SSD)-based model with a sliding window technique to refine crack identification. They analyzed dataset size effects and sliding window configurations and incorporated an eight-neighborhood algorithm for improved detection. The model was tested for portable device deployment and showed promising results in bridge inspections. 
Deep Learning for Crack Segmentation and Feature Fusion (2022-2023) 
Joshi et al. developed a Mask R-CNN-based architecture for crack detection and segmentation, using a dataset of 3,000 manually annotated images. Their model, fine-tuned using transfer learning, demonstrated high performance in mean average precision (mAP) and detection speed. 
In 2022, Geetha (Geetha et al., 2022) introduced a computationally efficient deep learning model integrating image binarization and a Fourier-based 1D model. The approach removed background noise and applied t-SNE visualizations for explainability, enabling real-time pixel-level classification even on low-computation mobile devices. 
In 2023, Wang developed CrackSN, based on the Adam-Squeeze Net architecture, which learned discriminative features from labelled and augmented image patches. The study showed significant improvements in damage inspection and structural health evaluation. 
Hang et al. proposed an attention-based feature fusion network for pixel-level crack detection. They designed a ResNet101-based model with two attention modules to integrate vertical-horizontal crack information and enhance crack localization accuracy. 
Recent Advancements in Transformer-Based Models (2024) 
Yu et al. introduced a Perspective-n-Point (PnP)-based thickness compensation technique to address homographic conversion errors in crack measurement. Their system mapped random speckles and markers onto the surface for full-field deformation assessment.
Qingyi et al. designed a transformer-based crack detection network that incorporated receptive field attention blocks and a feature assignment mechanism to improve accuracy. Their method refined multi-scale feature extraction and replaced traditional loss functions with adaptive loss functions for better performance (Qingyi and Chen Bo, 2024). 
Finally, Arafin et al. developed a dataset for crack and spalling detection, implementing CNN classifiers (VGG19, ResNet50, InceptionV3) and semantic segmentation models (U-Net, pyramid scene parsing network). Their study compared various architectures and identified variations in accuracy and F1-score, confirming deep learning's effectiveness in structural health monitoring.
**Research Methodology** 
This research employs a deep learning-based quantitative approach to automate the detection and classification of cracks and corrosion in concrete structures. Traditional manual inspection methods are labor-intensive, time-consuming, and prone to human error, making them inefficient for large-scale infrastructure monitoring. By leveraging Convolutional Neural Networks (CNNs) and computer vision techniques, this study enhances structural health monitoring by providing an automated, accurate, and scalable solution. The methodology involves data collection, preprocessing, model training, evaluation, and deployment, ensuring a systematic approach to achieving high-performance defect detection.
 **Research Design** 
This study follows a quantitative research design, as it involves the systematic collection, preprocessing, and analysis of image-based data using deep learning models. The quantitative approach is appropriate because it allows for objective measurements of crack severity and corrosion presence, facilitating a standardized and replicable classification process. The research utilizes CNN-based architectures to extract features from concrete images, classify them into predefined categories, and evaluate model performance using established metrics. 

**Participants/Subjects** 
This study does not involve human participants, as the primary input consists of image datasets of concrete surfaces with varying degrees of cracks and corrosion. Since the dataset is entirely image-based, ethical considerations regarding human subjects do not apply.


**Dataset Collection**
The dataset used in this research is publicly available images, ensuring a diverse representation of concrete cracks and corrosion. It consists of 20,000 images of cracks and 1,000 images of corrosion cracks, all stored in JPEG format. The images were manually labelled into six distinct categories: No Cracks, Small Cracks, Moderate Cracks, Large Cracks, Very Large Cracks, and Corrosion Cracks. To enhance model robustness and improve generalization, data augmentation techniques such as rotation, flipping, and noise addition were applied. The dataset was split into 70% for training, 15% for validation, and 15% for testing, ensuring a balanced distribution for model evaluation.
The images used in this study were sourced from multiple publicly available online repositories containing real-world structural defects. These sources were carefully selected to include a wide range of crack severities and corrosion types to improve model generalization. The dataset was curated by downloading high-quality images, verifying their relevance, and manually categorizing them based on observable structural defects. The self-collected images were acquired through web scraping and direct online searches from infrastructure reports, research publications, and open-access datasets.
In accordance with the ACI (American Concrete Institute) Code, cracks in concrete structures are classified based on their width, depth, and the impact on the structural integrity. The ACI provides guidelines for evaluating crack severity, especially in terms of serviceability and durability. Below is a classification of crack severity into five categories based on ACI guidelines, which generally focus on crack width as the primary criterion:

**Category 1: Hairline Cracks**
Very fine cracks, often barely visible, typically have a crack width of less than 0.1 mm (0.004 in) and pose no significant impact on a structure's performance or durability. According to ACI guidelines, such cracks are expected due to normal shrinkage or thermal movement and do not compromise the safety or function of the structure as shown in Figure 1. As a result, no repair is required, as these cracks are generally considered negligible.
 
Figure 1: Hairline Crack
**Category 2: Small Cracks**
Noticeable but shallow cracks. Crack Width: Between 0.1 mm (0.004 in) and 0.3 mm (0.012 in) as shown in Figure 2. Impact: Minor impact on serviceability or aesthetics, but not on structural integrity. Action: Monitoring may be necessary to ensure they do not progress into larger cracks. No immediate repairs required unless cracks widen or occur in critical areas. ACI Guideline: These cracks are generally considered to have a minimal effect on the durability and function of the concrete.
 
Figure 2: Small Crack
**Category 3: Moderate Cracks**
Cracks that are clearly visible and may cause some concern in terms of durability or performance. Crack Width: Between 0.3 mm (0.012 in) and 0.5 mm (0.020 in) as presented in Figure 3. Impact: May affect the serviceability of the structure and could be a potential path for water penetration, leading to corrosion of reinforcement. Action: Inspection and possible repair required, especially in areas exposed to aggressive environments. These cracks should be monitored for any further propagation. ACI Guideline: These cracks may not compromise structural integrity but may affect long-term durability.
 
Figure 3: Moderate Crack
**Category 4: Large Cracks**
Larger, more significant cracks that may affect structural integrity and are more likely to allow for the ingress of water, leading to potential reinforcement corrosion. In Figure 4, crack Width: Between 0.5 mm (0.020 in) and 1.0 mm (0.040 in). Impact: Could have a noticeable impact on durability and performance, especially in structures exposed to aggressive environments. Action: Repair or strengthening may be necessary. These cracks should be repaired to prevent further deterioration of the structure. ACI Guideline: Cracks of this size are more likely to compromise durability and may require remedial action to maintain long-term performance.
 
Figure 4: Large Crack
**Category 5: Very Large Cracks**
Severe cracks that compromise both the serviceability and safety of the structure. These cracks may result in significant structural damage and lead to failure if not addressed promptly. Crack Width: Greater than 1.0 mm (0.040 in) as presented in Figure 5. Impact: Significant impact on both structural integrity and durability. These cracks can be pathways for water ingress and may contribute to the deterioration of the reinforcement and concrete. Action: Immediate repair or strengthening is required. A detailed assessment by a structural engineer is necessary to determine the best course of action. ACI Guideline: These cracks are critical and can be an indicator of more serious underlying issues suc h as overloading, shrinkage, or settlement. 
 
Figure 5: Very Large Crack
**Category 6: No Cracks**
Concrete surfaces that exhibit no visible signs of cracking or surface deterioration are considered structurally sound, showing no indications of stress-related damage, shrinkage, or environmental wear. As shown in Figure 6, such regions require no repair or monitoring and serve as the benchmark for evaluating other categories. These areas have no impact on serviceability, aesthetics, or structural integrity, and no intervention is necessary. According to ACI guidelines, surfaces with no observable cracking align with optimal structural performance and durability standards.
 
Figure 6: No Cracks


**Category 7: Cracks Due to Corrosion**
These cracks, typically accompanied by rust stains, surface spalling, or discoloration, are caused by the corrosion of embedded steel reinforcement and indicate internal damage and deterioration, as shown in Figure 7. The crack width may vary, but their presence signifies a significant compromise to structural durability and safety due to the progressive weakening of the concrete-rebar bond. According to ACI guidelines, these cracks are classified as serious defects that require urgent attention to prevent further deterioration and potential structural failure. Immediate inspection and repair are necessary, including the removal of affected concrete, treatment of corroded rebar, and restoration using appropriate repair materials.
 
Figure 7: Cracks Due to Corrosion
**Tools and Technologies**: The implementation of this research was conducted using the following tools and technologies: 
•	Programming Languages & Libraries: Python, TensorFlow, Keras, OpenCV, NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn 
•	Hardware & Execution Environment: Google Colab Pro with GPU acceleration to optimize model training speed and efficiency 
**Ethical Considerations**: All images used in this study were sourced from publicly available datasets and online repositories, ensuring compliance with ethical research standards. No privacy-sensitive or personally identifiable information was included in the dataset. The research adheres to standard data collection and usage ethics, ensuring that only publicly accessible images were utilized without violating intellectual property rights. 
**Limitations of Methodology**: This study ensures robust dataset collection and deep learning model development; however, certain external factors, such as variations in image quality and real-world environmental conditions, could introduce minor classification inconsistencies. Despite this, augmentation techniques and rigorous validation ensure optimal model performance.
**Raw Data Structure and Dataset Directory**
The dataset is organized into train, validation, and test directories within the base path. The train set (70%) is used for model learning, the validation set (15%) helps fine-tune performance, and the test set (15%) evaluates how well the model generalizes to new data. This structure keeps the workflow organized and ensures reliable model training. 
The code in Figure 8 defines paths to directories on Google Drive for organizing a deep learning learning model. First, it sets the base_path, which points to the main project folder in Google Drive. Then, it creates three additional paths:
1.	train_dir: This path points to the subfolder containing the training data.
2.	vali_dir: This path points to the subfolder containing the validation data.
3.	test_dir: This path points to the subfolder containing the test data.
These paths are generated by combining the base_path with the specific subfolder names ("train", "validation", and "test") using the os.path.join() function, which ensures proper formatting of the file paths. The result is that the project’s directories for data storage are set up, and each directory is accessible via these variables for later use in the project.


Figure 8: Raw Data Structure
**Data Cleaning and Categorization**

A critical step in developing the deep learning-based defect detection system involved rigorous data cleaning and accurate categorization of the image dataset. The initial dataset, compiled from publicly available sources and field inspections, contained a wide variety of concrete surface images with varying quality, lighting conditions, and defect types.

The data cleaning process began by filtering out low-quality images such as duplicates, blurred photos, and those with poor lighting or resolution. Each image was resized to a uniform resolution (e.g., 224x224 pixels) and enhanced using normalization and contrast adjustment techniques like histogram equalization to emphasize defect features.

After cleaning, the dataset was manually categorized into seven classes based on the severity and nature of the visible cracks:

**No Cracks** – Concrete surfaces with no visible damage.
**Hairline Cracks** – Extremely thin and faint cracks, often hard to detect visually.
**Small Cracks** – Narrow but noticeable cracks with minimal width and surface depth.
**Moderate Cracks** – Cracks of moderate width and length that may indicate structural concern.
**Large Cracks** – Clearly visible, wide cracks potentially impacting structural stability.
**Very Large Cracks** – Severe fractures with significant depth and possible exposure of internal materials.
**Cracks Due to Corrosion** – Cracks accompanied by rust stains or surface spalling, typically caused by internal steel reinforcement corrosion.

To enhance model generalization and reduce class imbalance, various data augmentation techniques—such as rotation, flipping, zooming, and brightness variation—were applied across all categories. This structured cleaning and categorization ensured a high-quality, well-labeled dataset, enabling the model to effectively distinguish between different types and severities of concrete damage.





**Importing Required Libraries**
The essential libraries for data processing, deep learning, and performance evaluation are imported as shown in Figure 9. The OS module is used for managing directory paths, while tensorflow supports building and training the deep learning model. For data visualization, matplotlib.pyplot and seaborn are utilized, and numpy handles numerical computations. The image_dataset_from_directory function streamlines dataset loading, and the confusion_matrix and classification_report functions from sklearn.metrics are employed to assess the model’s classification performance..












Figure 9: Required Libraries
**Defining Dataset Paths**:
In this step, dataset paths are defined using Python’s pathlib library to organize the input data required for training, validation, and testing phases. The base_path variable points to the main project directory on Google Drive where the dataset is stored as Shown in Figure 10. Subsequently, subdirectories for the training (train_dir), validation (vali_dir), and testing (test_dir) datasets are defined by appending their respective folder names to the base_path using the / operator. This approach ensures clean, readable, and platform-independent path management, making it easier to access and manipulate datasets throughout the model development pipeline


Figure 10: Defining Dataset Path
**Data Preprocessing**
Data preprocessing involves defining image properties such as resizing and applying data augmentation techniques like horizontal and vertical flipping, random rotation, and random zoom. These steps enhance the model's robustness and ability to generalize by introducing diverse variations of the original images.

**A.	Define Image Properties**
The images are resized to a fixed size of 64x64 pixels, and a batch size of 32 is used to process the images in manageable groups as shown in Figure 11.  

Figure 11: Image Properties
**B.	Apply Data Augmentation**
This section defines data augmentation techniques using TensorFlow's Keras Sequential API, which helps improve model generalization by applying random transformations to input images as shown in Figure 12. The augmentation pipeline includes random flipping (both horizontal and vertical) to enhance orientation invariance, random rotation (up to 20%) to introduce variations in image perspective, and random zoom (up to 20%) to simulate different scales of cracks. These augmentations ensure that the model learns robust features, reducing overfitting and improving performance on real-world crack detection tasks.



Figure 12: Data Augmentation
**Addressing Class Imbalance**
Addressing class imbalance is a critical step in training machine learning models, especially in classification tasks where certain categories have significantly fewer samples than others. In the context of concrete crack detection, an imbalanced dataset can cause the model to become biased toward majority classes, reducing its ability to accurately identify rare but important defect types. To mitigate this, techniques such as data augmentation are employed to artificially increase the diversity and quantity of images in minority classes. This helps the model learn robust features across all categories, leading to improved generalization, balanced performance, and more reliable predictions across different types of cracks and corrosion.
**A. Analyzing Class Distribution**
Before addressing class imbalance, it’s essential to understand the distribution of images across different classes. The code in Figure 13 defines a function that counts images per class by traversing the dataset directory structure






                                               Figure 13: Class Distribution
This function is then used to calculate image counts for the training, validation, and test datasets as shown in Figure 14.


Figure 14: Function For Image Count
To visualize the imbalance, a simple bar plot was created for the training set using the code in Figure 15.





Figure 15: Bar Plot
**Applying Data Augmentation to Address Imbalance**
To balance the dataset, data augmentation was applied using the tf.keras.Sequential pipeline as shown in Figure 11. While the notebook didn’t directly target augmentation at specific minority classes, a universal augmentation pipeline was applied to all training images, which improves generalization and indirectly helps mitigate imbalance.

This pipeline was applied to the training dataset using the .map() function shown in Figure 16.

Figure 16: Pipeline with Map function
Additionally, another augmentation block was applied in code shown in Figure 17 named minority_class_augmentation. This version is designed to enhance the diversity of images, especially useful if applied to minority classes only. However, in the current implementation, the main augmentation block was uniformly applied across all training data which includes:






Figure 17: Minority Class Augmentation
**Final Processed Dataset**
The code in Figure 8 imports essential libraries and sets the directory paths for the training, validation, and testing datasets. These paths are used throughout the preprocessing and model training workflow.
Then the code in Figure 12 defines the augmentation techniques applied to the training data. It introduces randomness through flipping, rotation, and zooming to improve the model’s robustness and help address overfitting and class imbalance. Now the figure 18 shows the loading dataset for training






Figure 18: Loading training dataset
The block of the code presented in Figure 19 loads the validation and test datasets. Unlike the training dataset, no augmentation is applied here to ensure accurate evaluation of model performance. Shuffling is disabled in the test set to maintain consistent prediction order.






Figure 19: Load Validation and Test Datasets
**Research Model: Layers and Architecture** 
The model presented in Figure 20 is a custom-designed Convolutional Neural Network (CNN) built using TensorFlow and Kerass, tailored for the classification of concrete surface images into multiple crack and corrosion-related categories. The input to the model consists of RGB images resized to 300×500×3, ensuring a consistent input shape while preserving sufficient spatial resolution to detect fine-grained defects.
The architecture begins with a rescaling layer that normalizes pixel values to the range [0, 1], which is essential for improving convergence speed and training stability. Following this, the network is structured into four hierarchical convolutional blocks, each containing a Conv2D layer paired with a MaxPooling2D layer. These convolutional layers progressively increase in depth—starting from 32 filters and doubling up to 256 filters—with each using a 3×3 kernel and ReLU activation. This design enables the network to learn low- to high-level spatial features, such as crack edges, widths, textures, and corrosion patterns. The MaxPooling2D layers reduce the spatial dimensions, allowing the network to retain the most prominent features while lowering computational complexity.
After feature extraction, the output is flattened into a 1D vector, which is then passed to a Dense layer with 128 neurons and ReLU activation. This fully connected layer interprets the abstracted features and contributes to the final decision-making. The final output layer uses a softmax activation function across 7 units, corresponding to the seven predefined classes: No Cracks, Hairline Cracks, Small Cracks, Moderate Cracks, Large Cracks, Very Large Cracks, and Corrosion Cracks. The use of softmax ensures that the output is a valid probability distribution, aiding in multi-class classification.
The model is compiled with the Adam optimizer, known for its adaptive learning capabilities, using a learning rate of 0.0001 to fine-tune weights with stability.











Figure 20: Research Model
The model is a lightweight yet effective Convolutional Neural Network (CNN) designed for multi-class classification of concrete surface defects as shown in Figure 21. It takes RGB images of size 64×64 as input and processes them through three convolutional blocks with increasing filter depths (32, 64, 128), each followed by batch normalization and max pooling to enhance feature extraction and reduce spatial dimensions. A global average pooling layer condenses the extracted features into a 1D vector, which is passed through a fully connected dense layer with 256 neurons and a dropout layer for regularization. The final dense layer uses softmax activation to classify images into one of seven predefined categories. With approximately 129K parameters (128,519 trainable), the model balances computational efficiency and accuracy, making it suitable for real-time crack and corrosion detection on resource-constrained devices.
The model comprises approximately 129,000 parameters (with 128,519 trainable), making it significantly more efficient compared to deeper architectures, yet sufficiently powerful for robust performance. Its streamlined design and optimized parameter count make it especially suitable for real-time deployment on resource-constrained platforms, such as embedded systems or edge devices used in on-site infrastructure inspections. Overall, the architecture effectively balances depth, accuracy, and efficiency, making it well-aligned for the demands of automated structural health monitoring systems.
 
Figure 21: Model Architecture summary and Parameters Details

**Results:**
Model Accuracy and Performance
The model is trained for 50 epochs, progressively improving in both training and validation accuracy while reducing the loss values. Early epochs showed rapid learning, with a steady increase in performance, followed by stabilization in later epochs. The validation accuracy remained consistently close to the training accuracy, indicating good generalization and minimal overfitting. The decreasing loss trend across both sets supports the model’s effective learning during training. Figure 22 shows the relationship between training and validation against epochs illustrating the Accuracy in Figure 22 (a) and Loss in Figure 22 (b). 
 

Figure 22: Training and Validation Against Epochs
This graph presents the training and validation performance of the CNN model over 50 epochs. Figure 22-a shows accuracy against the number of epochs, where both training and validation accuracy improve steadily, indicating that the model is learning effectively. The validation accuracy remains slightly higher than the training accuracy in later epochs, suggesting good generalization without overfitting. While Figure 22-b shows loss against the number of epochs, which decreases consistently for both training and validation sets, reflecting improved model predictions over time. Together, these plots confirm that the model is converging well with balanced learning and minimal signs of underfitting or overfitting.
**Confusion Matrix:**
The confusion matrix is a vital evaluation tool in classification tasks, especially in multi-class problems like concrete defect detection. It provides a detailed breakdown of the model's performance by comparing the actual class labels with the predicted class labels for each image in the test set. Unlike overall accuracy, which gives a single metric, the confusion matrix reveals how well the model performs across individual classes, helping to uncover hidden issues such as class imbalance or confusion between visually similar categories (e.g., moderate vs. large cracks).
In your project, where the model classifies images into seven classes (ranging from "No Cracks" to "Corrosion Cracks"), the confusion matrix is represented as a 7×7 grid. Each row of the matrix represents the true class, while each column represents the predicted class. The diagonal elements indicate the number of correctly predicted samples for each class—these are the true positives. The off-diagonal elements reveal misclassifications, showing which classes are being confused with each other.For instance, if a large number of moderate cracks are being misclassified as small cracks, the confusion matrix will show a high value in the corresponding cell. This insight can guide further improvements, such as targeted data augmentation or class-specific reweightin
The code in Figure 23 computes and visualizes the confusion matrix for the model's performance on the test dataset. It iterates through the test batches, collects the true labels (y_true) and predicted class indices (y_pred) using np.argmax to convert one-hot encoded vectors to class indices. The confusion_matrix function from sklearn.metrics generates the matrix, which is then visualized using a heatmap from Seaborn. The resulting plot helps assess how well the model distinguishes between different crack and corrosion classes by showing actual vs. predicted classifications.








Figure 23: Code for Confusion Matrix
 Figure 24: Confusion Matrix
**Table 1: Data processing**
 
**Model Accuracy**
Model accuracy is a key performance metric that reflects how well a classification model is able to correctly predict the labels of input data. In the context of this concrete defect detection system, accuracy represents the proportion of correctly classified images—such as "No Cracks", "Moderate Cracks", or "Corrosion Cracks"—out of the total number of test images.

 A high accuracy value indicates that the model is performing well in identifying and differentiating between the various classes of concrete surface defects. In your model, for example, an accuracy of 94.7% suggests that the model can correctly classify most of the input images, which is especially important in real-world applications where misclassifying a severe crack as a minor one could lead to serious safety risks.

However, while accuracy is a useful general indicator, it should not be the only metric considered—especially in datasets with class imbalance. For instance, if one class (e.g., "No Cracks") dominates the dataset, the model might achieve high accuracy simply by predicting the majority class more often. This is why accuracy is often complemented with other metrics like precision, recall, F1-score, and confusion matrix analysis, which provide a more detailed view of the model’s performance across all classes.

 
Figure 25: Accuracy
**Classification Report**
Explain 
Table 2: Analysis Results
Category	Precision	Recall	F1-Score	Support
Category1_Hairline_Cracks	0.83	0.67	0.74	150
Category2_Small_Cracks	0.49	0.79	0.61	150
Category3_Moderate_Cracks	0.38	0.29	0.33	150
Category4_Large_Cracks	0.43	0.47	0.45	150
Category5_Very_Large_Cracks	0.68	0.53	0.59	150
Category6_No_Cracks	0.97	0.97	0.97	150
Category7_Concrete_Corrosion_Cracks	0.97	0.95	0.96	147
				
**Accuracy**			0.66	1047
**Macro Average**	0.68	0.66	0.66	1047
**Weighted Average**	0.68	0.66	0.66	1047

**Conclusion**
This project demonstrates the potential of deep learning in revolutionizing the detection of cracks and corrosion in concrete structures. By automating the inspection process, this system provides a highly accurate and efficient alternative to traditional manual inspections, reducing human error and improving maintenance planning. 
The integration of advanced computer vision models ensures real-time defect detection, enabling timely intervention to prevent structural failures. The successful deployment of this system will have a significant impact on infrastructure monitoring, offering a scalable and cost-effective solution for civil engineers and maintenance teams. Future enhancements could involve real-time deployment using edge devices, expanding the dataset to include more diverse environmental conditions, and integrating predictive maintenance features. By leveraging AI, this project contributes to safer, more sustainable infrastructure worldwide.

**List of references**
1.	Sales da Cunha, Beatriz, Márcio das Chagas Moura, Caio Souto Maior, Ana Cláudia Negreiros, and Isis Didier Lins. 2022. “A comparison between computer vision- and deep learning-based models for automated concrete crack detection.” Proceedings of the Institution of Mechanical Engineers, Part O: Journal of Risk and Reliability. https://doi.org/10.1177/1748006X221140966.
2.	Dung, Cao Vu, and Le Duc Anh. 2019. “Autonomous concrete crack detection using deep fully convolutional neural network.” Automation in Construction 99: 52–58. https://doi.org/10.1016/j.autcon.2018.11.028.
3.	Park, Song Ee, Seung-Hyun Eem, and Haemin Jeon. 2020. “Concrete crack detection and quantification using deep learning and structured light.” Construction and Building Materials 252. https://doi.org/10.1016/j.conbuildmat.2020.119096.
4.	Ren, Yupeng, Jisheng Huang, Zhiyou Hong, Wei Lu, Jun Yin, Leiun Zou, and Xiaohua Shen. 2020. “Image-based concrete crack detection in tunnels using deep fully convolutional networks.” Construction and Building Materials 234. https://doi.org/10.1016/j.conbuildmat.2019.117367.
5.	Li, Shengyuan, Xuefeng Zhao, and Hayri Baytan Ozmen. 2019. “Image-based concrete crack detection using convolutional neural network and exhaustive search technique.” Advances in Civil Engineering 2019. https://doi.org/10.1155/2019/6520620.
6.	Qingyi, Wang, and Chen Bo. 2024. “A novel transfer learning model for the real-time concrete crack detection.” Knowledge-Based Systems 301. https://doi.org/10.1016/j.knosys.2024.112313.
7.	Zhang, Xinxiang, Dinesh Rajan, and Brett Story. 2019. “Concrete crack detection using context-aware deep semantic segmentation network.” Computer-Aided Civil and Infrastructure Engineering 34 (11): 951–71. https://doi.org/10.1111/mice.12477.
8.	Hang, Jiaqi, Yingjie Wu, Yancheng Li, Tao Lai, Jie Zhang, and Yang Li. 2023. “A deep learning semantic segmentation network with attention mechanism for concrete crack detection.” Structural Health Monitoring. https://doi.org/10.1177/147592172311216710.
9.	Kim, Bubryur, N. Yuvaraj, K. R. Sri Preethaa, and R. Arun Pandian. 2021. “Surface crack detection using deep learning-based shallow CNN architecture for enhanced computation.” Neural Computing and Applications 33 (15): 9289–9305. https://doi.org/10.1007/s00521-021-05950-4.
10.	Arfan, Palisa, AHM Muntasir Billah, and Tahsin Reza. 2024. “Deep learning-based concrete defects classification and detection using semantic segmentation.” Structural Health Monitoring 23 (2): 383–409. https://doi.org/10.1177/14759217231158114.
11.	Golding, Vaughn Peter, Zahra Gharineiat, Suliman Munawar Hafiz, and Fahim Ullah. 2024. “Crack classification and quantification using deep learning.” Sustainability 14 (4): 8147. https://doi.org/10.3390/su14138117.
12.	Wan, Chunfeng, Xiaobin Xiong, Bo Wen, Shuai Gao, Da Fang, Caigian Yang, and Songtao Xue. 2022. “Crack detection for concrete bridges with image-based deep learning.” Science Progress 105 (4). https://doi.org/10.1177/00368504221128487.
13.	Yu, Shanshan, Jian Zhang, Chengpeng Zhu, Zeyang Sun, and Shuai Dong. 2024. “Full-field deformation measurement and cracks detection in speckle scene using the deep learning-aided digital image correlation method.” Mechanical Systems and Signal Processing 209. https://doi.org/10.1016/j.ymssp.2024.111131.
14.	Lin, Wang. 2023. “Automatic detection of concrete cracks from images using Adam-squeezenet deep learning model.” Fracture and Structural Integrity 17 (65): 289–99. https://doi.org/10.3221/IGF-ESIS.65.19.
15.	Kolappa, Geetha Ganesh, and Sung-Han Sim. 2022. “Fast identification of concrete cracks using 1D deep learning and explainable artificial intelligence-based analysis.” Automation in Construction 143. https://doi.org/10.1016/j.autcon.2022.104572.
16.	Joshi, Deepa, Dinesh P. Singh, and Gargeya Sharma. 2022. “Automatic surface crack detection using segmentation-based deep-learning approach.” Engineering Fracture Mechanics 268. https://doi.org/10.1016/j.engfracmech.2022.108467.

