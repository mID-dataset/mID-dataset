# mID-dataset

mID is an accurate and robust user identification and authentication system by utilizing millimeter wave (mmWave) sensing. mID only asks the user to perform an "in air" capital letter 'S' as the "password" to unlock the smart phone at runtime. 

This dataset here contains the gesture samples used in mID, 22,440 samples in total. It is collected by a mmWave radar, Infneon EVAL BGT0TR24B V8 evaluation board, which radios FMCW signals operating in the 57-64 GHz range. We place the radar chip on a horizontal table with a height of 75cm. We ask volunteers to perform the predefined gesture inside the detection range, which is set as a cone with a generatrix of 60cm.

<img src="https://github.com/mID-dataset/mID-dataset/tree/main/README_md_files/image (2).png" width="300"  alt="reflectors"/><br/>

For the convenience of readers, we provide not only the features used in mID but also the corresponding raw signals directly returned from the mmWave radar. Please note that we have uploaded the feature data, totaling 6.96GB. However, the data volume of the original signal is too large, i.e., 36.2GB, so we are still working hard to upload. But in order not to hinder the readers, we have also provided a link to the external network storage in the folder "AuthenRaw".

## Dataset Description
We collect three data sets of hand gesture samples from our volunteers.We refer the first set as dataset 1 (D1), the second as data set 2 (D2), and the last as data set 3 (D3).

**Data Set 1** is utilized to show that different users have unique behaviors when performing the predefined gesture but any given user exhibits the same behavior every time he performs the gesture. In this data set, we gather 6,950 pieces of gesture samples from 39 volunteers in 4 environments. The 39 volunteers consist of 22 potential host users (200 samples for each) and 17 strangers (100 samples for each). They comprise 21 males and 18 females and their ages range from 19 to 50 years. We collected these samples after obtaining their approval. To collect samples form them, we verbally explain the gesture “S” to each volunteer and ask them to perform the gesture to the best of his/her understanding. We ask the volunteers to randomly choose any environment they like to collect gestures.
![](README_md_files%5Cimage%20%286%29.png?v=1&type=image)

**Data Set 2** is used to show how the behavior of any given user changes over time while performing a predefined gesture. In this data set, we collect 8,400 samples from 24 volunteers (all of them are the same as the “potential hosts” in D1 in the classroom environment. The reason why we collect samples in only 1 environment
is that the purpose of D2 is to only explore how the volunteers change their behavior in performing the same gesture over different time interval; in this case, we do not need to evaluate gestures in all 4 environments. The 24 volunteers comprise 13 males and 11 females with ages from 20-50 years. We divide the 24 volunteers into four groups, each group comprising 6 volunteers. Every volunteer in each group start to collect gestures from this data set (D2) after the their samples in D1 have been collected.
![](README_md_files%5Cimage%20%284%29.png?v=1&type=image)

**Data Set 3** consists of variable movements which is not the predefined gesture, which is utilized to validate the robustness of mGID. The purpose of this data set (D3) is to study how to recognize the un-predefined gestures so that avoid false triggering. The purpose of this data set D3 is to study how to recognize the un-predefined gestures so that avoid false triggering.For this, we collect 840 samples from 1 volunteer. Then, explain several different kinds. We divide these 14 kinds of different data into three classes by movement extent: **Slight Movement Categories** (1-3), **Larger Movement Categories** (4-10), and **Large Movement Categories** (11-14). Each category contains 60 samples of data. For all movements(including gestures), there is no requirement for the distance, height, speed, and direction of the volunteer’s gestures from the volunteer and the antenna. The volunteer can complete the specified gestures according to his wishes.Before gathering all the above movements (including gestures) samples, we just use a few words to tell the volunteers how to perform the above movements. Thus, there is no requirement for the distance, height, speed, and direction of the volunteer’s gestures from the volunteer and the antenna. The volunteer can complete the specified gestures according to his wishes. We ask the volunteer to perform each movement 60 times.
![](README_md_files%5Cimage%20%285%29.png?v=1&type=image)

We have also uploaded an individual file "Gesture Instruction.pdf" which contains more details of the gestures/movements collected in mID.

## Directory Structure
There are two folders, i.e., 'AuthenFeatures' contains the features extracted in mID; 'AuthenRaw' contains the raw signals corresponding to the gesture samples. Both of them possess the same directory structure.
In each main folder, we archive the following three data sets:

In **D1**, each user is asked to perform 200 samples of the predefined gesture 'S'. All of the 200 samples are collected in the folder named "'name'_S_feature" or "`name`_data _file _128-15". The former is the features, the latter is the raw signal.
In **D2**, each user is asked to repeat two sessions 5 times. The first session contains 20 samples, the second one contains 50 samples. We ask 24 volunteers to perform for 4 different interruption periods. 6 volunteers (using different code-names) for each period: one day, two days, half a week, and a whole week. The folder name of the first session is "`name`-`time`_S_feature" or "`name`-`time`_data_file_128-15". The one of the second session is "`name`-`time`T_S_feature" or "`name`-`time`T_data_file_128-15". The specific `name` of each period is listed in the "Gesture Instruction.pdf".
In **D3**, each user is asked to perform 60 samples of each non-predefined movements. Each 60 samples are collected in the folder "`name`-RED-`sort`_S_feature" or "`name`-RED-`sort`_data _file _128-15".


## Data Structure
The data structure of the features extracted from the gesture sample is a each gesture is 100 × 9 × 60, which has been introduced in mID in details.
The data structure of the raw signals corresponding to the gesture samples is 128 (sample) × 3 (Rx) × 15 (chirps) × 60 (frames).


## Parameters of mmWave Radar

We enable the ability of the mmWave radar as follows: The range resolution of the radar is 2.5cm and it has a sensing range of up to 2.5m. The doppler resolution is 1.63cm/s and the maximum doppler detection is 4.16m/s.

|Radar parameters|value  |
|--|--|
|Rx channels|3|
|Tx channels|2|
|ADC sampling rate|2 MHz|
|chirps per frame|15|
|samples per chirp|128|
