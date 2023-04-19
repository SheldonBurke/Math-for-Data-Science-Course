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
 
 So our intial valid results was 78.8% accuracy and it showed. Alexnet had issue telling the difference between the common sunflower and Tagestes erecta and Pansy, but accurately predicted Bougainvillea, Black Flowers and Black eyed Susan.
 
 So, I decided that it needed more training on these flowers so more flowers were added to the valid and training folders of each flowers. Subsequent training showed promise bumping up to 82% and then 83% with more additions. A fourth test surprisingly went down to 78 again when alot more datasets were added to the common sunflower folders, so we decided to remove some of the dataset that had too much negative space and not enough common sunflower data in the photo.
 
  </p>
  
  
