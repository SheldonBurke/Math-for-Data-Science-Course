 <h1 align="center"> Flower Project Using Alexnet Project</h1>
 

<img src="https://platthillnursery.com/wp-content/uploads/2021/05/platt-hill-top-perennials-for-full-sun-blanket-flower.jpg" alt="Blanket Flowers, my favorite" > 

 <h3 align="center"> Introduction </h3>

<p align="center"> This is a project to use Alexnet for object recognition to accurately predict type of flower. Twenty five types of flowers are used in the dataset. Originally each flower had four images for validation and one image for testing. However, the accuracy was inadequate at those levels (only 78.8%) so for some flowers, more validation images and test images were needed. This was because of what I will dub the pansy problem. More on the pansy problem to come. </p>


 <h3 align="center"> Dataset </h3>

<p align="center"> This is a project to use Alexnet for object recognition to accurately predict type of flower. Twenty five types of flowers are used in the dataset. Originally each flower had four images for validation and one image for testing. However, the accuracy was inadequate at those levels (only 78.8%) so for some flowers, more validation images and test images were needed. This was because of what I will dub the pansy problem. More on the pansy problem to come. </p>


![Flower Project (2)](https://user-images.githubusercontent.com/122634321/233112054-aef43716-5c50-4d3f-ac4e-b1915dc43adb.jpg)

<h6 align="center">

The flowers in the dataset are:
1. Yellow Pimpernel
2. Tecoma capenis
3. Tagetes erecta
4. Starburst Clerodendrum
5. Star Jasmine
6. Siberian larkspur
7. Shoeblack plant
8. Ruelia Simplex
9. Rose
10. Pyrostegia venusta
11. Plumbago auriculata
12. Pelargonium Inquinans
13. Pansy
14. Oleander
15. Madagascar Periwinkle
16. Jatropha bush
17. Galphimia gracilis
18. Florida Pusley
19. Firespike Cardinals
20. Euryops pectinatus
21. Crinum asiaticum
22. Common Sunflower
23. Bougainvillea
24. Blanket Flowers
25. Black-eyed Susan

</h6>

 <h3 align="center"> Test </h3>

<p align="center"> To test Alexnet after training, we decided to use five species of plant which will test if Alexnet can accurately predict flowers from images outside our dataset. So what flowers will we use for testing. From observation, I have decided the following species would be great for testing with the following reasons:

1. Pansy 
2. Common Sunflower
3. Tagetes erecta For 1,2,3 I wanted to test them because they share similarities in the dataset so it would be useful to see if Alexnet can tell the difference between these yellow flowers. Especially since to the human eyes (at least to me, there are clear difference especially with the tagest erecta which has a more wavey pattern and tends to be more orange yellow than yellow). 
4. Bougainvillea, I wanted to test the Bougainvillea since it is so different than the other flowers in the dataset and comes in an array of flowers (technically the colorful parts are leaves and are not the flowers).
5. Jatropa Bush (similarily Jatropa is a bush and not a flower so it would be good to see if Alexnet can still accurately predict a Jatropa from other "flowers")
 
  </p>
  
  <h3 align="center"> Results </h3>
  
  <p align="center"> 
 
 So our intial valid results was 78.8% accuracy and it showed. Alexnet had issue telling the difference between the common sunflower and Tagestes erecta and Pansy, but accurately predicted Bougainvillea, Black Flowers and Black eyed Susan. So a decision was made to update the dataset and add more samples to the folders of these yellow flowers. Intially this raised the accuracy to 81% then 83%, and then maddeningly 78%. Finally, after taking out some common sunflower images that had too much other data in it we were able to get valid to 84% which seems to be the best we can get with twenty five flowers and limited number of flower photos. </p>
 
 <p align "center"> 
<img width="227" alt="Screenshot 2023-04-19 at 12 58 31 PM" src="https://user-images.githubusercontent.com/122634321/233148094-fd4f64ce-5cd2-43ce-8d6f-305decad4a3a.png"> </p>

  <p align "center">
  So here is how our final test did in predictions. 
  
 <img width="904" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233150469-610e97a0-3832-42e2-9b17-c9d41ac0f29a.png">

1. Pansy (correct)
  
  <img width="500" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233149270-7510dd3f-99a0-4923-9d54-4154b278d390.png">


2. Common Sunflower (correct)

 <img width="500" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233150296-1ef3cb09-fe78-4175-ad0f-372b7f67f728.png">
 

3. Tagetes erecta (correct)
 <img width="500" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233151241-e737191e-2940-4899-a412-9ae0a43fedf6.png">



4. Bougainvillea (incorect)

Incorrectly guessed firespike

 <img width="500" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233152245-da53dc2e-e5f3-4b08-8eae-0ca4ec1219ca.png">


5. Jatropha bush (correct)

<img width="500" alt="Screenshot 2023-04-19 at 1 14 28 PM" src="https://user-images.githubusercontent.com/122634321/233152567-3c8f5829-fff6-4e69-a6e9-6e2dc2c3e738.png">


Overall 4 out of 5 correct. Which matches the valid data. However, it does show that perhaps the issues in accuracy stems from other flowers besides the yellows ones with a dark center which has been my focus. In fairness to Alexnet, our dataset only incldues purple Bougainvillea and our prediction photo has many different colors. 
 
  </p>
  
  
