# Internet-Video-traffic-analysis-using-Stacking-Ensemble-in-ML

### Introduction
    Since many years, the demand for high speed transmission rates over the 
    internet has become a clear problem and it has been evident amid this pandemic.

   ![image](https://user-images.githubusercontent.com/57587354/108511246-a9655600-72e5-11eb-8c30-82d6ef01fe78.png)

    So prioritizing the live video streaming services(like Cisco Webex, G-meet,Zoom) should be our top prior concern
    Short video on demand services are instagram, tiktok, vigo etc.
    Long video on demand services are netflix, youtube, prime video, etc.
   ![image](https://user-images.githubusercontent.com/57587354/108511284-b71adb80-72e5-11eb-9a17-ef894e300884.png)
    
    In this project, we have first collected various network traffic of video streaming services like Amazon Prime, Netflix, Youtube, Dailymotion, 
    Cisco Webex, and G-meet. We then preprocessed the dataset with the imputation of the missing values, binned by mean, and variance 
    on various attributes, label encoded the categorical attributes analyzed outliers with the help of 
    boxplots, removed skewness present in the dataset, performed feature selection with the help of correlation and class imbalancy problem
    was kept in mind while constructing the dataset itself.
    
   ![image](https://user-images.githubusercontent.com/57587354/109194658-a7a50200-77bf-11eb-9814-afbcb3e052e2.png)
 
   ### Constraints set while capturing the dataset :

    -  Allowing protocols of UDP , TCP and HTTP only. These are the protocols followed by the network for video transmission. 
       When using this protocol other protocols which are   using the machine are left out like ARP requests , SMTP protocols 
       for mails are excluded while capturing.
    -  The videos were captured for 1 hour unrestricted on different machines and for several days.
    -  The source and destination IP address were dropped off.
    -  Length of packet size is fixed to a certain threshold.

    With these constraints applied we were able to capture a total of around 23,000 packets for each streaming platform.
    
   ![image](https://user-images.githubusercontent.com/57587354/109196454-ba203b00-77c1-11eb-8376-177f73763c7a.png)
   

    Model classification was done with stacking ensemble technique where we stacked 4 different algorithms namely, Gradient Boosted Decision Tree, 
    SVM, k-NN as base learners and XGBoost as meta-learner, we achieved 98.6% of accuracy and plotted confusion matrix for false positives 
    (which were very negligible) and checked other performance metrics like precision, accuracy, recall, and f1-score too.
    
   ![image](https://user-images.githubusercontent.com/57587354/109196913-52b6bb00-77c2-11eb-9f47-901757b4d835.png)
   
   ### Practical Application of our Model
    Our proposed algorithm can be beneficial to both ISP's and on client side where an application 
    would be running in desktop which can classify the network packets but would take RAM from local machine and needs access from ISP as well, 
    but if implemented on server side of ISPs then it would help them to classify the incoming packets and efficiently utilize the 
    bandwidth of the network which has been a problem this whole time in many areas.
    
   ![image](https://user-images.githubusercontent.com/57587354/109198060-c73e2980-77c3-11eb-9aae-825a83bd0d6f.png)
   
   ### References
    [1]Klenilmar Lopes Dias∗, Mateus Almeida Pongelupe, Walmir Matos Caminhas, Luciano de Errico, (2019). An innovative approach for 
    real-time network traffic classification, Elsevier Vol. 158, pg : 143 - 153.

    [2] Andersson R. “Classification of Video Traffic: An Evaluation of Video Traffic Classification using Random Forests and 
    Gradient Boosted Trees”. Karlstad University, Sweden, 2017.

    [3]Tamuka, Nyashadzashe & Sibanda, Khulumani. (2019). Modelling the Classification of Video Traffic Streaming Using Machine Learning. 

    [4] Zhang, Jun & Chen, Xiao & Xiang, Yang & Zhou, Wanlei & Wu, Jie. (2014). Robust Network Traffic Classification. IEEE/ACM Transactions 
    on Networking. 23. 1-1. 10.1109/TNET.2014.2320577. 

    [6] https://www.oberlo.com/blog/video-marketing-statistics

    [7] https://manpages.debian.org/testing/argus-client/ra.1.en.html
    
 

