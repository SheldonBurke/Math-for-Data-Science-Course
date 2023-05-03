 <h1 align="center"> Using Alexnet Object Recognition to Identify Obstacles on Sidewalks for Disabled Safety</h1>
 
 <p align="center">
 <img src="https://whyy.org/wp-content/uploads/2017/07/japanese-artist-tomoteru-saito-of-japan-created-this-dinosaur-1-768x432.jpg" style="vertical-align:bottom" > 
</p>


 <h3 align="center"> Introduction </h3>

<p align="center">
 
 Video presentation to go along with markdown: https://youtu.be/iD6ckydxhuY 
 
 For the blind and/or disabled obstructive objects make navigating potentially dangerous for simple, everyday travel. 

Uneven pavements, cars on sidewalks, piled trash, downed trees, and other pedestrians create: unfair impediments to a fair and equal life, risk of bodily injury, and potentially dangerous situations where the disabled must travel into ongoing traffic. 

Currently there are aids which help with these such as guide dogs, walking sticks, canes and gps. 

However, they are not enough, guide dogs require daily training, and maintenance. Walking sticks are good for objects on the ground but won't tell you of a hanging tree limb. Gps cannot account for the constant changing conditions of a sidewalk from day to day. Ultimately, none of these will help if governments cannot identify impediments on sidewalks to address them swiftly. 

Therefore there needs to be a solution where visually impaired, the disabled, governments and their stakeholders can get real time feedback on obstacles on pedestrian walk ways. So these matters can be addressed. </p>

 <h3 align="center"> Proposed Solution </h3>
 
 <p align="center"> To create a more equitable society, reduce risk to disabled pedestrians, and protect taxpayers from liability, we will analyze images to train a deep learning model--Alexnet to identify potential obstacles or hazards on sidewalks.

Since we are just beginning with the basics of project, our first test project will only test whether a sidewalk has obstacles or not.
</p>


 <h3 align="center"> Dataset </h3>
 
 For our dataset, we used some existing data from a user named Wu, Tang (has anyone hit a better name lottery than this?) and creative common images from Unsplash.com. 
 
 Tang's dataset can be seen on their Google Drive here: https://drive.google.com/drive/u/0/folders/1ksOuWxXQS_mbWmhwq37hFj8lUqkpcrTn 
 
 <h6 align="center"> Sample of no obstruction dataset </h6>
  <p align="center">
 <img src="https://user-images.githubusercontent.com/122634321/235795048-40cdc7bd-558e-48f1-9f18-4b8ded008407.jpg" width="500" height="250" > 
</p>

 <h6 align="center"> Sample of obstruction dataset </h6>
  <p align="center">
  
 <img src="https://user-images.githubusercontent.com/122634321/235797276-b413b11f-8773-463c-ab45-bd91f970d685.jpg" width="500" height="250" > 
</p>

  <h3 align="center">Alexnet </h3>
  <p align="center"> 
 <img src="https://user-images.githubusercontent.com/122634321/235797852-c19cc916-3455-4cad-b11b-6639590a123a.png" width="500" height="250" > 

AlexNet is a deep convolutional neural network (CNN) architecture that was designed to recognize images by learning from millions of labeled examples.

AlexNet works by processing an input image through a series of convolutional and pooling layers to extract low-level and high-level features, followed by fully connected layers to perform classification.

 AlexNet consists of 8 layers, including 5 convolutional layers and 3 fully connected layers.

 The first convolutional layer takes as input a color image of size 224x224x3 and applies 96 filters of size 11x11x3 to generate 96 feature maps. The second convolutional layer applies 256 filters of size 5x5x48 to the output of the first layer, generating 256 feature maps. The third, fourth, and fifth convolutional layers follow a similar pattern of applying filters to the previous layer's output.

After the convolutional layers, the output is fed into three fully connected layers that perform classification. The first fully connected layer has 4,096 neurons, the second has 4,096 neurons, and the final output layer has 1,000 neurons.
  </p>


 <h3 align="center"> Test and Training  </h3>

<p align="center"> 
  
  Code for Alexnet testing is avaliable on Google Colab:
  https://colab.research.google.com/drive/1qZrxkOmqGEP0WHDFaTQQh_mIMAS506yw#scrollTo=EwBsL__ySiKa
  
  For Alexnet training, we gathered a dataset of 120 images. 100 for valid and 20 for training. Our dataset seemed straight forward in thought, but was actually difficult to curate. 

The images had to include common obstacles that may be on a sidewalk, which was easy to gather (fire hydrants, bicycles, cars, trash, and people). The dataset had to be vast, and all encompassing which was a bit difficult with only 120 images since you needed to be very broad--anything could be on a sidewalk.

It also had to include cracked and uneven pavement. Which proved a bit tougher as we had to gather images of mostly open sidewalks with small images of cracks and unevenness to train our model to tell to subtle difference between an open sidewalk with no obstacle and an open sidewalk with obstacles. 

Despite these challenges, we were able to get a very accurate model with 95% validity.
  
  ![image](https://user-images.githubusercontent.com/122634321/235798403-6baedaac-e0c6-4ea9-a4a7-d1c349e4124e.png)

 But let's see it in action.
  

  </p>
  
  <h3 align="center"> Results </h3>
  
  <p align="center"> 
  
   To test Alexnet after training, we decided to use five images to test the accuracy of the model we created. 
  

  1. No Obstacle (correct)
  
   <img src="https://user-images.githubusercontent.com/122634321/235798661-b438eca3-e3da-42ae-bd70-6f92469bdc1a.jpg" width="350" height="250" > 


  2. No Obstacle (correct)

   <img src="https://user-images.githubusercontent.com/122634321/235798663-2cadcb64-c6a8-4a51-a93c-8c459b90d3c2.jpg" width="400" height="250" > 


  3. Obstacle (correct)
  
   <img src="https://user-images.githubusercontent.com/122634321/235798665-773a0ebd-46c6-407f-aa4c-8002965a6d85.jpg" width="400" height="250" > 

  4. Obstacle (correct)

   <img src="https://user-images.githubusercontent.com/122634321/235798669-69e3e881-7cad-4cd5-9ce7-d14cf9ae7cb1.jpg" width="400" height="250" > 

  
  5. No Obstacle (correct)

   <img src="https://user-images.githubusercontent.com/122634321/235798672-036a2cc0-0bc0-4a47-8453-fc40a1c20732.jpg" width="500" height="350" > 


Overall 5 out of 5 correct. The model struggled at first to identify cracks on the pavement as obstacles but we were able to train the model with more weight on images of cracked sidewalks and it was able to accurately label those as obstacles. 
  
</p>

