1.密度图生成还是用 自适应的高斯核  高斯核大小等于0.15*M  M 是透视值 1米多少个像素  
2.提出了一个deconvolution network  
  perspective fusion 透视融合  但是不能把透视图拼在一开始 会随着网络传播 信息分散  
  将透视图 concate upsampling process  
3.数据集  
   数据集是WorldExpo’10  mae is 11.2 比 MCNN 11.6好  
   比crowd CNN+RR 10.7 差点
