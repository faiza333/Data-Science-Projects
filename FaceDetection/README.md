
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
   


