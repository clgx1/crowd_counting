1.标准化行人密度图  取175的平均身高进行缩放
2.密度图计算同时考虑人头和身体， 人头用高斯核函数 ，参数取0.2M  M是1米多少个像素，
   身体用二元正态分布
3.建立一个CNN模型 （待更新）   同时计算密度图和人数
4.候选场景检索和局部片段检索
  挑选出20个候选场景 他们的透视角度相似 we use its vertical gradient ΔMy as the perspective descriptor
  然后检索出不同密度的片段 放回cnn进行fine—tuning  来适应目标场景
4.数据集
  建立了一个新的数据集 上海世博会 WorldExpo’10
  UCSD
  UCF_CC_50
