----

# Project 1: Energy Disaggregation
[Github repo](https://github.com/King-Zach/disaggproj)
 
Load Disaggregation is a broad term covering a range of techniques able to split a household’s energy consumption by the individual appliances used.

![Energy Disagg image](files/diaggimg.jpeg)
*   Several work related to this uses high frequency data but in this i have modeled for low frequency data which are quite practical at several households
*   Dataset can be downloaded from [kaggle](https://www.kaggle.com/loveall/appliances-energy-prediction)
*   this project involves good amount of data visualisation, feature engineering, model evaluation
*   for modelling i tried various sklearn’s regressors and found out Extra Tree regressor was performing good
*   More details for this project is on Github
*   Further working on deep learning approach to this problem




# Project 2: Face Recognition using CNN
[Github repo](https://github.com/King-Zach/face_recog)

A facial recognition system is a technology capable of matching a human face from a digital image or a video frame against a database of faces. In this particular project i have used CNN based facial recognition system.

![CNN intuition](/files/facerecog1.png)


I used dataset from [kaggle](https://www.kaggle.com/datasets/vasukipatel/face-recognition-dataset) with some
modification


Dataset structure

dataset has 31 classes of images of celebrity and there are some test data from internet
```
+-- face-recognition-dataset
|   +-- Faces
|   +-- Original Images
|   +-- Dataset.csv(labes for images)
+-- test(images taken from internet)
```
Also I used ImageDataGenerator from tensorflow to ease the process of feeding data to CNN.

I was able to achieve 98% accuracy using this CNN architecture
```
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 222, 222, 32)      896       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 111, 111, 32)      0         
_________________________________________________________________
batch_normalization (BatchNo (None, 111, 111, 32)      128       
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 109, 109, 64)      18496     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 54, 54, 64)        0         
_________________________________________________________________
batch_normalization_1 (Batch (None, 54, 54, 64)        256       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 52, 52, 64)        36928     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 26, 26, 64)        0         
_________________________________________________________________
batch_normalization_2 (Batch (None, 26, 26, 64)        256       
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 24, 24, 96)        55392     
_________________________________________________________________
max_pooling2d_3 (MaxPooling2 (None, 12, 12, 96)        0         
_________________________________________________________________
batch_normalization_3 (Batch (None, 12, 12, 96)        384       
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 10, 10, 32)        27680     
_________________________________________________________________
max_pooling2d_4 (MaxPooling2 (None, 5, 5, 32)          0         
_________________________________________________________________
batch_normalization_4 (Batch (None, 5, 5, 32)          128       
_________________________________________________________________
dropout (Dropout)            (None, 5, 5, 32)          0         
_________________________________________________________________
flatten (Flatten)            (None, 800)               0         
_________________________________________________________________
dense (Dense)                (None, 128)               102528    
_________________________________________________________________
dense_1 (Dense)              (None, 31)                3999      
=================================================================

```
# Project 3: Time series clustering and forecasting
[Github repo](https://github.com/King-Zach/clustering-and-forecasting)

Time series forecasting have attracted a great deal of attention from various research communities. One of the method which improves accuracy of forecasting is time series clustering.
![forecast](files/probabilistic-forecasting-graph.png)

- Problem : We are given daily electricity usage data of customers from various residential houses as well as commercial usage and we need to forecast daily usage of each customer
- Here we are leveraging clustering since there are many customers and training a model for each is not scalable and efficient. For forecasting we are using fbprophet

- The given dataset contains 6445 IDs from ID 1000 to ID 7444. The dataset provide daily electricity usage from July 14, 2009 to December 31, 2010.The costumers are not only from housing but also companies.
- Achieved 80-90% accuracy over all the clusters.

# Project 4: Whatsapp chat EDA
[Github repo](https://github.com/King-Zach/whatsapp-chat-analysis)
![whatappchatanalyzer](files/whatsapp-chat.png)
* Analyze summaries of WhatsApp chats with individuals or groups.
* No data is stored or sent outside your system of execution. All chat data is deleted from memory once the insights are generated. Jupyter notebooks are used so that the code generating the summaries can be viewed by the skeptical user.
* various insights can be drawn from these individual chats and look up metrics such as response time, text density, number of emojis, etc.
* have provided good visualizations using `plotly`