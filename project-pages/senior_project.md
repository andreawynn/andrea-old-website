## Senior Research Project: Anomaly Detection on Computer Networks using Machine Learning
### Advisor: Dr. Michael Wollowski
### In Collaboration with MIT Lincoln Laboratory
*August 2021 - May 2022*

### Motivation for Research
Given the computational power available to modern hackers, the scale of the cyber attacks that could be performed today are much larger than what is possible to track manually in real time. To speed up network security analysis, cyber security teams can utilize tools based on machine learning algorithms for dynamic network analysis. 
After research over existing work in the area, my team and I developed an understanding of ways to work with data, as well as the types of data to investigate to assist in the creation of such a tool. Our projects uses random forests, convolutional neural networks, and feed-forward neural networks to explore network packet data to discern between malicious (DDoS) and benign network activity. The later segment of the project includes a meta-analysis of current cutting-edge research in cyberattack detection to provide recommendations for researchers and cybersecurity engineers hoping to build effective intrusion detection products. 

### Data for DDOS Detection
Many open-source datasets are available, using both real and simulated network data, for identifying malicious network traffic. One of the datasets we used is a dataset with network traffic metadata, with each packet labeled as either part of benign traffic or DDoS (Distributed Denial of Service) traffic [https://www.kaggle.com/devendra416/ddos-datasets]. This dataset contains information about network traffic during simulated DDoS attacks, produced by multiple researchers from the years 2016-2018. The dataset consists of 12,794,627 records, each representing a single flow (forward or reverse), has 84 total features, and has a balanced distribution of DDoS and benign records. 

We chose to work with this dataset because it is specifically focuses on DDoS attacks, making a good starting point for training models to predict one type of attack. Some of the most significant features include the timestamp, source and destination IPs, source port, and total forwarded packets. The dataset draws from 3 other simulated DDoS datasets, produced from 2016-2018. [https://www.ijcseonline.org/pdf_paper_view.php?paper_id=4011&28-IJCSE-06600.pdf ]. The dataset is large enough (6.97 GB, with 84 features and no missing entries) to be used for training data-hungry models such as deep learning networks and random forests.

### My Contributions
I began by processing the DDoS dataset. First, I identified all non-numerical variables, which in this case were the flow ID, source IP, destination IP, and timestamp. The flow ID was just a combination of the other 3 non-numeric features, so I chose to remove that feature. I then converted the timestamp to a float, and encoded the source and destination IPs as integers, so that they could be fed directly into a model as numerical features. I chose to anonymize the IPs because we would like to predict based on general patterns in network traffic data, not for a specific IP or machine. I chose to keep the timestamp and IP information, even though all the data was simulated, because having multiple packets sent to a single IP in a short time frame could be one of the main indicators of a DDoS attack. Our team wants to build a model that can identify true indicators of DDoS attacks in practice, rather than mistakenly identifying the algorithms used to generate the data instead of learning to predict actual attacks. Additionally, I wrote a section of the paper regarding alternative models for cyberattack detection, such as information theory, probability models, signal processing, and others. 

### Findings
The first model we are training with this dataset is the random forest classifier, which our team was able to tune to achieve over 99% accuracy on this dataset (over 96% accuracy when using the one most important feature).

## Publication, Presentations & Awards
This project has been presented in a Research Laboratory group and will be presented at multiple student work showcases at Rose-Hulman. 

### Tools and Methods Used
Python – All code for this project was written in Python, using libraries such as TensorFlow and Scikit-Learn. <br>
Jupyter Notebooks – All code for this project so far was written using Jupyter Notebooks. There may be an opportunity to build a tool once a proof of concept is demonstrated to have high effectiveness in predicting cyberattacks. <br>
