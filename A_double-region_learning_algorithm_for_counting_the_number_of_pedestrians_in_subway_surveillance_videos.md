1.对图像做一个水平分割， 分割高度等于  期望高度  求和pi*hi  

每个高度hi 有一个概率pi  pi=ki（当前高度的人数）/总人数

2.用ACFES计算第一个区域的人数  
提取特征用高斯过程回归计算第二个区域的人数  
根据某种规则相加  

3.数据集  
贡献了上海地铁站监控拍摄到的人群数据集
