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