# Visual Captioning - For Images and Artwork
**Members:** Anah Veronica, Nagapriya, Niegil, Sakthisree, Shivani, Surojit <br>
**Link to Google Drive:** https://drive.google.com/drive/u/0/folders/1gNShRvPH5sYv-ScG9e7eymUUpE_jc8Xl

![](https://64.media.tumblr.com/9b9da05e29b370faab64da19badca472/tumblr_mud1hsUDcu1rb40pco4_500.gifv)

## Problem Statement

Artworks are highly subjective and are open to many interpretations. According to Panofsky’s three levels of analysis, captions of natural images are of ”pre-iconographic” description - an objective view where it is simply listing the elements present within an image. But for artwork images, this type of description does not adequately represent the tonality or accurate description of the painting. In the context of artwork images, it would be more interesting to generate ”iconographic” captions that capture the subject and symbolic relations between objects.

## Our Solution
![image](https://user-images.githubusercontent.com/22959465/140273132-668ae628-4a91-4408-8dcf-a1474ee8f21d.png)

## Technical Architecture
![image](https://user-images.githubusercontent.com/22959465/140273186-8e8f10c1-20ce-4d3e-b1dc-84471a4b4afb.png)

## Models
We trained three different models to cater to three different use cases. The models were based on [Show, Attend and Tell](https://arxiv.org/abs/1502.03044) and provides three model outputs. The first model was trained on the COCO,Flickr 8K and Iconclass datasets, with a focus on everyday real life images, whereas the second and third model was trained on the ArtEmis dataset, with a focus on artwork. The third model was based on [Artemis](https://arxiv.org/abs/2101.07396) which differs from the second in that it undergoes two stages :
- A ground emotion is predicted by the image to emotion classifier  
- The predicted emotion is fed into the image to caption generator

This gives the model a more subjective caption as compared to the other two models. 

## Sample Output
A sample output for a painting
<img src="arty_painting.gif" alt="App" width="1000"/>
A sample output for a real life image
<img src="arty.gif" alt="App" width="1000"/>

Here we can see the difference in outputs. The first model performs quite accurately on a real life image while the second and the third model work quite well on the artwork.

Link to more information - [Arty PDF](https://drive.google.com/file/d/12iQr0c6j_cdHER66uLtFuh2ztAHyjzn1/view?usp=sharing)


--------------------------------------------------------------------------------------------------------

## References
[1] https://cocodataset.org/#home <br>
[2] https://www.kaggle.com/adityajn105/flickr8k <br>
[3] http://tems.umn.edu/pdf/Panofsky_iconology2.pdf <br>
[4] [Cetinic, E., 2021. Iconographic image captioning for artworks. arXiv preprint arXiv:2102.03942.](https://arxiv.org/abs/2102.03942) <br>
[5] https://github.com/optas/artemis

@article{achlioptas2021artemis,
    title={ArtEmis: Affective Language for Visual Art},
    author={Achlioptas, Panos and Ovsjanikov, Maks and Haydarov, Kilichbek and
            Elhoseiny, Mohamed and Guibas, Leonidas},
    journal = {CoRR},
    volume = {abs/2101.07396},
    year={2021}
}

