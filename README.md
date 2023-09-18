# Leveraging GANs to Portray the Modern World in Historic Styles
## Domain Translation Using CycleGAN and CUT
Course Project for CS444 @ UIUC. In collaboration with Muhammad Abdullah Hashmi (UIUC) and Nic Prate (UIUC).

![Alt Text](/video_samples/gan_monet_1.gif) ![Alt Text](/video_samples/gan_monet_2.gif) ![Alt Text](/video_samples/gan_monet_4.gif)

## Introduction
The goal of this project is to expand the reach of historic artists and their paintings to include the architectural advancements of today. We wish to study how artists such as Monet would view today’s world and capture it in their unique art style, and what would a person in today’s world look like in Monet’s craft. The proposed approach uses a combination of a segmentation model, an interactive texture transfer technique, and generative models. For the latter, we put up two state-of-the-art image-to-image models against each other to determine which models outperforms the other in different video settings. We conduct a thorough analysis of the output video frames, and some of the interesting observations can be summarized as follows: the models tend to perform better in bright, outdoor environments as compared to their darker, indoor counterparts, and the Contrastive Unpaired Learning (CUT) model outperformed a pretrained CycleGAN even when trained for a lower number of iterations. The video outputs are posted online and can be viewed [here](https://www.youtube.com/playlist?list=PLlLS2I-uuaABND4jzxIl6pvTRNuLkokHj).

## Quantitative Evaluation

The evaluation metric used for a quantitative assessment of the models is the Frechet Inception Distance (FID). A popular metric used to evaluate GANs, the FID compares the distribution of the generated images with the distribution of the real images (i.e., the ground truth). In the case of translation models, the target domain images are considered to be the ground truth. Since we are working with unpaired images with no specific target images (i.e., we are translating certain features and not attempting to generate a new instance of an image from the target domain), we assume a set of Monet paintings to be the ground truth.

|   Model    |    FID    |
|:--------:|:----------:|
| CycleGAN |  599.949   |
|   <ins>**CUT**</ins>    |   <ins>**506.564**</ins> |

## Qualitative Evaluation
![Alt Text](/comparison.png)
