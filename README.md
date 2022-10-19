# Data-Science-Projects

## 1- Audio Classification for Capuchinbird Project
![image](https://user-images.githubusercontent.com/68142873/195213198-3ef21afa-be90-4221-8731-b04ca46e1ec2.png)

## DataSet
It is a challange on Kaggle the link is: https://www.kaggle.com/datasets/kenjee/z-by-hp-unlocked-challenge-3-signal-processing
It containe 3 folders the first is Forest Recordings where contains files mp3 with long 3 min, second files is Parsed_Capuchinbird_Clips containes the bird sound
the third one is Parsed_Not_Capuchinbird_Clips it containes another voices.

## Aim of the project:
It's Audio analysis problem, where we classify Capuchin Bird in the rainforest using audio clips, Using TensorFlow we numerically represent the audio the data contains 3s clips so we convert it into a waveform, then convert it into spectrogram so we can use CV techniques to be able to perform that classification then push this into CNN so we can get a binary outcome, we will notice that we will get consecutive calls so we will group them out.

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


## 2- Face Detection Project

![image](https://user-images.githubusercontent.com/68142873/196627746-4e59513d-288f-42ec-b569-cffdd90091e7.png)

### Dataset 
We collecting the dataset using the webcam for the face using CV2, the data is not that big it was about 80 photo, but we gonna make some augmintation on it.

### Project Pipeline

1- Collecting the data using webcam
2- ANNOTATE the images so we can draw a box around the face using labelme library
3- Do data Augmentation on the images since the data is not that big using Arbumintation  library, it is gonna make 4 changed:    CROP, BRIGHTNISS, FLIP, GAMMA, THIS librar do ANNOTATE on the images too.
4- DL model, it is 2 different types of models, classification model which it is classify what the object is in our case it is      only on class: face, and we gonna use binary cross entropy loss function 
   - the second model is the regression model trying to estimate coordinate of that particular bounding box, to do that we just      need the top left point or right,  and the bottom left point or right, any two opposing sets of coordinates we can use it      to draw a bounding box, and we gonna use localization 
   - we look to the top coordinate and find out how far our prediction is from that
     then evaluate the width and hight of that particular bounding box.
   - we are using VGG16 which is classification model, we gonna fine tune the model, we gonna play with the last two layers to      be our classification model which gonna give us on of [0, 1] is it face or not, and regression which gonna return to us        [x1,y1,x2,y2].
   


