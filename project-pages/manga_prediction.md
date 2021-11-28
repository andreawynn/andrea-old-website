## Manga Image Processing & Metadata Prediction Project
## Course: MA416/CSSE416 - Deep Learning
*Completed in Fall 2021-22*

**Please note that I cannot share the source code for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The Manga109 dataset is a collection of scans from 109 different manga series from roughly 1970 - 2010. Labels in the original dataset were bounding boxes for faces, panels (the squares surrounding images in manga), text, and entire people. While detecting these would be a reasonably interesting object detection task, my team decided to gather our own tabular data - author, publishing year, publishing decade - and use them as prediction targets for the image dataset. Is it possible to predict publishing information based solely on artstyle? Are artists’ artstyle well-recognized by existing models (like LeNet) and convolutional networks? 

In this project, we seek to determine whether we can train deep learning networks to be able to recognize authors’ unique styles, identify manga from a particular time period, and learn to identify objects within a single manga page. We take data from the extensive Manga109 dataset, with image data from 109 different manga and information about bounding boxes for faces, frames, and other significant features. Some of the techniques used include: logistic regression, feed forward neural networks, the LeNet network, and YOLOv5 object detection. Authors were able to be predicted using features extracted from VGG16 as inputs; however, both publishing decade and year tasks were unable to outperform baseline classification and regression methods respectively. YOLO v5 was able to accurately detect faces in manga pages.

### My Contribution
I wrote a Python script to take individual cropped images from manga, then separated images by type (for instance, faces vs frames) across all mangas and scaled them all down to 32x32 pixels. Along with a list of these standardized images, I also paired them with their corresponding manga titles, publishing years & decades, and authors, and compressed all of that information in a single NPZ file. This resulted in two final datasets: one for faces across all mangas, and one for frames across all mangas. I further determined that the images other than faces and frames were not needed for the scope of this project through initial data analysis. 

Additionally, I was responsible for implementing the author prediction model. Mangaka (manga authors/illustrators) are said to have distinct drawing styles that can be identified by simply examining their art. Critics and fans of manga can identify art styles by a number of features: detail, roughness, shading, etc. My work centered around using the dataset described above to predict which of 86 different authors is most likely to have written and illustrated a particular manga panel. 

I began by selecting out the frames (panels) only and start with a baseline accuracy of 0.0437 using the simple bias classifier (always predicting ‘Aida Mayumi’). I trained two models on the manga frames date: a logistic regression model, optimizing for the hyperparameter C & a fully connected feed forward network with early stopping (patience = 3), 3 hidden layers, a learning rate of 0.01 and 40 epochs. A few variations on these parameters were tested, but due to the ineffectiveness as compared to the baseline, transfer learning was adopted as an alternative instead, using VGG16. 

With the extracted features from VGG16, I trained a logistic regressor, which gave a maximum accuracy of 0.314 (C = 0.0001), a significant improvement over the baseline accuracy of 0.0437. Additionally, a fully connected feed forward network was trained with a maximum accuracy of 0.3575, also a significant improvement over the baseline. This was achieved using 2 hidden layers, a learning rate of 0.00001, and 10 training epochs, after optimizing for the number of hidden layers (between 0-5) and learning rate (from 0.00001 to 1). 

### Technical Architecture and Tools Used
*Programming Languages and Tools* <br>
Python - All code was written using Python in Jupyter Notebooks. Many Python libraries were used for data exploration & preprocessing and machine learning model implementations, including Tensorflow and NumPy. <br>
Jupyter Notebooks - All code was written in Python using Jupyter Notebooks. The notebooks were mostly run on remote servers, due to the high demands on computation power required to handle a dataset as large as ours (tens of gigabytes).
