# SignLanguage
----
Description: Sign language is a tool for the deaf. They can communicate among themselves or receive information from non-disabled people through sign language. This means very unreasonable one-way communication. Because non-disabled people do not know sign language, they cannot receive information from deaf people. Although it is acknowledged that it lacks practical necessity in daily life, it is difficult to find people around you who can communicate in sign language, even though Korean has been legally adopted as the second official language in Korea. Also, unlike other translators, it is difficult to find a sign language translator. This is why I chose this topic. Even though the results may be lacking, I hope to use this opportunity to develop a real-time sign language translator and provide a good experience. Finger joint detection technologies have already been developed as open-source. We plan to proceed with development using these parts.
***
The main idea is as follows.
1. Calculate the coordinates of each joint in our body using mediapipe provided by Google.
2. Calculate the connection of coordinates of each joint.
3. Calculate the angle between each connection.
4. Classify gestures using DTW, taking advantage of the fact that the connection angle is different for each posture.
***
In fact, while I was writing code, I found a [github code](https://github.com/gabguerin/Sign-Language-Recognition--MediaPipe-DTW) with the same idea and proceeded to develop it. 
***
The idea I added was to add an embedding vector based on the shoulder line as well as the existing hand, and through this, I wanted to use the geometric positional relationship between the hand, arm, shoulder, and back for classification. In addition, we attempted to use deep learning using soft-DTW and extract objective performance indicators, but this part remained unfinished.
The added embedding vector can be expected to slightly improve performance, but no dynamic performance improvement was seen.
***
If you install all the libraries in requirements.txt and run yt_downloads.py, you can receive the sign language video provided in the original GitHub link. If an error occurs, it will be resolved by setting the python version to 3.10 and upgrading all installed libraries to the latest.
***
After executing train.py, press the r key to start motion recognition. Please refer to the downloaded sign language video for motion. Since the algorithm operates based on the CPU, it may not work smoothly if your computer does not provide sufficient performance.
