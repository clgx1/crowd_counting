1.生成自适应密度图 ，为了解决透视图的问题， 每个行人的头占得像素个数不一样  
高斯核大小取0.3*(k个最近的人头的平均距离）  

2.提出MCNN模型（multi-column cnn) 经过三行的卷积 最后 把结果合起来  然后得出密度图  
可以适应不同的size  
（待更新）  

3.数据集  
贡献了一个new dataset：Shanghaitech dataset    

UCSD  
UCF CC 50  
WorldExpo’10
