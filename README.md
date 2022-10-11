# Data-Science-Projects

## 1- Audio Classification for Capuchinbird Project
![image](https://user-images.githubusercontent.com/68142873/195213198-3ef21afa-be90-4221-8731-b04ca46e1ec2.png)

## DataSet
It is a challange on Kaggle the link is: https://www.kaggle.com/datasets/kenjee/z-by-hp-unlocked-challenge-3-signal-processing
It containe 3 folders the first is Forest Recordings where contains files mp3 with long 3 min, second files is Parsed_Capuchinbird_Clips containes the bird sound
the third one is Parsed_Not_Capuchinbird_Clips it containes another voices.

## Aim of the project:
is to do classification on the audio to detect if it is have Capuchin voice or not and how many times.

## Project Steps:
### 1- processing
 process our audio files and convirt it into 16K H after that we can plot the audio waves
 as we see in the picture below: the blue is for capuchin bird and the orange for not capuchin
 
 ![image](https://user-images.githubusercontent.com/68142873/195216266-c8224531-a0e9-4ee5-93e7-904c32d23262.png)
 
 ### 2- Build Preprocessing Function to Convert to Spectrogram
 and now we can draw aour spectogram and we can see the different between the capuchin bird and not capuchin bird
 
 this is not capuchin bird 
 
 ![image](https://user-images.githubusercontent.com/68142873/195214952-1b4ec785-6fcc-42bc-a2a2-1822e95bf937.png)
 
 while this is capuchin bird 
 ![image](https://user-images.githubusercontent.com/68142873/195215110-9e162634-5b25-4425-bc01-1bef5b1fe714.png)
 
 ### 3- Build Deep Learning Model
 using Tensrflow we build the model as follwing 
 ![image](https://user-images.githubusercontent.com/68142873/195215404-ec95e522-2dfa-40f9-9bdf-1e068cae933c.png)
 
 and we get the following results 
 as we see we get a really good recall and prescion
 ![image](https://user-images.githubusercontent.com/68142873/195215345-a8a6ae3a-a1fe-45e2-aaa3-3b4a4a56c08a.png)
 
 
![image](https://user-images.githubusercontent.com/68142873/195215597-c24353f4-6fee-46bb-9921-9e6cfe25e3f9.png)

![image](https://user-images.githubusercontent.com/68142873/195215638-efd0b432-4e9f-4fbc-b9e6-6ad05f199651.png)

![image](https://user-images.githubusercontent.com/68142873/195215658-09e837df-f446-4d2e-9e6b-09ba4aad8cec.png)

 ### 4- Make a Prediction on a Single Clip
 
we tooked a one full mp3 file and convert it to 60 window
We gonna take those windows and convert it to spectograme and loop through them all and make predictions

## Here we can see some part of the results
![image](https://user-images.githubusercontent.com/68142873/195215938-b5f9ffb9-c65a-4755-ac18-fcd6886b48db.png)



