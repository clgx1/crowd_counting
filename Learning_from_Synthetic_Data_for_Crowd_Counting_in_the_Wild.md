1. 从electronic game GTA5 创建了数据集 GCC  
上来先强调自动标注  ，但是论文中只提到了 gta的引擎标注 ，所以适用性还是个问题。
Rockstar Advanced Game En-gine (RAGE) to improve its draw distance rendering ca-pabilities.  

人头的自动标注 based on the rendering pipeline.  

先前的工作在GTA5里面没有congested scene ，所以我们需要design a strategy to construct crowd scenes

Scenes Synthesis for Congested Crowd: 由于在GTA5里面放置人最多放256个，So we adopt a step-by-step method to generate scenes. 即合成图片  

the number of people is set asrandom value in the range of its level. Therefore, GCC has more large-range than other real datasets.  



2.提出一个有监督的策略，  网络 SFCN     ，利用数据预训练crowd counter ，  可以提供更好的完整的初始参数    

Many current methods suffer from the over-fitting because of scarce real labeled data  


SFCN用VGG-16 as backbone
SFCN†用ResNet101 backbone


Therefore, we attempt to propose a crowd counting method via domain adaptation to save man- power, which learns specific patterns or features from the synthetic data and transfers them to the real world.  
Unfortunately, the generated synthetic data are very differ- ent from real-world data (such as in color style, texture and so on), which is treated as “domain gap”. 

用SSIM Embedding (SE) Cycle GAN把训练数据转化为真实图片  然后在真实图片上测试



Annotating the groundtruth is  time-consuming and labor-intensive work, especially for pixel-wise tasks (such as semantic segmentation, density map estimation).

where SSIM(·, ·) is standard computation: the parameter settings are directly followed by  
[39] Z. Wang, A. C. Bovik, H. R. Sheikh, and E. P. Simoncelli. Image quality assessment: from error visibility tostructural similarity. IEEE transactions on image processing, 13(4):600–612, 2004.

During the training phase, the µ is set as 1, other parameters and set-tings are the same as Cycle GAN [44].  

J.-Y. Zhu, T. Park, P. Isola, and A. A. Efros. Unpaired imageto-image translation using cycle-consistent adversarial networks. arXiv preprint, 2017.




 
