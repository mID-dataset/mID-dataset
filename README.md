# mGID-dataset
This dataset contains the gesture samples used in mGID. It is collected by millimeter-wave (mmWave) FMCW radar. The range resolution of the radar is 2.5cm and it has a sensing range of up to 2.5m. The doppler resolution is 1.63cm/s and the maximum doppler detection is 4.16m/s.![](README_md_files%5Cimage%20%282%29.png?v=1&type=image)
## Gesture Space
We collect three data sets of hand gesture samples from our volunteers.We refer the first set as dataset 1 (D1), the second as data set 2 (D2), and the last as data set 3 (D3).
**D1** is utilized to show that different users have unique behaviors when performing the predefined gesture but any given user exhibits the same behavior every time he performs the gesture. 
**D2** is used to show how the behavior of any given user changes over time while performing a predefined gesture. 
**D3** consists of variable movements which is not the predefined gesture, which is utilized to validate the robustness of mGID. 
Then, we describe how we gather the samples contained in D1, D2, and D3. Last, we describe which components are controlled and which are not when collecting these three sets of data.
## Collection Settings
**Data Set 1** 
In this data set, we gather 6,950 pieces of gesture samples from 39 volunteers in 4 environments. The 39 volunteers consist of 22 potential host users (200 samples for each) and 17 strangers (100 samples for each). They comprise 21 males and 18 females and their ages range from 19 to 50 years. We collected these samples after obtaining their approval. To collect samples form them, we verbally explain the gesture “S” to each volunteer and ask them to perform the gesture to the best of his/her understanding. We ask the volunteers to randomly choose any environment they like to collect gestures.
![](README_md_files%5Cimage%20%286%29.png?v=1&type=image)
**Data Set 2** 
In this data set, we collect 8,400 samples from 12+12 volunteers (all of them are the same as the “potential hosts” in D1 in the classroom environment. The reason why we collect samples in only 1 environment
is that the purpose of D2 is to only explore how the volunteers change their behavior in performing the same gesture over different time interval; in this case, we do not need to evaluate gestures in all 4 environments. The
12 volunteers comprise 8 males and 3 females with ages from 20-50 years.
We divide the 1 volunteers into four groups, each group comprising 6 volunteers. Every volunteer in each group start to collect gestures from this data set (D2) after the their samples in D1 have been collected.![](README_md_files%5Cimage%20%284%29.png?v=1&type=image)
**Data Set 3**
The purpose of this data set (D3) is to study how to recognize the un-predefined gestures so that avoid false triggering. The purpose of this data set D3 is to study how to recognize the un-predefined gestures so that avoid false triggering.For this, we collect 840 samples from 1 volunteer. Then, explain several different kinds. We divide these 14 kinds of different data into three classes by movement extent: **Slight Movement Categories** (1-3), **Larger Movement Categories** (4-10), and **Large Movement Categories** (11-14). Each category contains 60 samples of data. For all movements(including gestures), there is no requirement for the distance, height, speed, and direction of the volunteer’s gestures from the volunteer and the antenna. The volunteer can complete the specified gestures according to his wishes.Before gathering all the above movements (including gestures) samples, we just use a few words to tell the volunteers how to perform the above movements. Thus, there is no requirement for the distance, height, speed, and direction of the volunteer’s gestures from the volunteer and the antenna. The volunteer can complete the specified gestures according to his wishes. We ask the volunteer to perform each movement 60 times.
![](README_md_files%5Cimage%20%285%29.png?v=1&type=image)
## Directory Structure
**Predefined gestures**: We ask volunteers to explain the gesture “S” in the air. ( D1 and D2 )

**Random actions**: We leave this part of data into a single folder.

**Other documents**: We provide a gesture instruction in the home directory which describes how to perform each arm gesture in details. Note that however, the volunteers learn the gestures only by watching how we perform them.
## Data Structure
The data structure of each gesture is 7* n, where n is various with frames and 7 are 'frame id’, 'detected points in each frame’, 'x coordinate of each point’, 'y coordinate of each point’, 'z coordinate of each point’, 'velocity of each point’ and 'reflection intensity of each point’. 
## Parameters of mmWave Radar
|Radar parameters|value  |
|--|--|
|Rx channels|3|
|Tx channels|
|chirp cycle time|
|ADC sampling rate|
|Rx gain|
|frame periodicity|
|dynamic point detection|
|point energy threshold|
