## 项目说明
智能营销工具可以帮助商家预测用户购买的行为，这里比赛方提供了**品牌商家的历史订单数据**，请构建一个预测模型，**预估用户人群在规定时间内产生购买行为的概率。**
该模型可应用于各种电商数据分析，不仅可以帮助商家基于平台流量，进行商品售卖、支付，还可以通过MarTech技术更精准地锁定核心用户，对用户的购买行为进行预测。
该预测模型包括xgboost和DNN，**其中DNN采用百度Paddle框架搭建。所有代码均可在baidu aistudio平台运行。**
## 数据及比赛资料
[比赛链接](https://aistudio.baidu.com/aistudio/competition/detail/21)  
[数据集链接](https://aistudio.baidu.com/aistudio/datasetDetail/19383)
## 1.环境配置和所需依赖库:
* paddle
* scikit-learn
* numpy
* pandas
* xgboost
## 2.步骤说明
(1)原始数据集包含了不同用户在一月到八月间的购买行为以及订单资料，为了构建训练集，需要将八月的购买行为单独划分出来作为标签。  
(2)进行数据预处理(包括缺失值填充，归一化，独热编码等)，以及特征工程(针对时间特征做rfm模型处理等)  
(3)分别采用xgboost和DNN进行训练和预测，其中DNN采用百度Paddle框架搭建。  
(4)模型融合输出结果  
## 3.文件说明
原始数据train.csv  
基于原始数据打标签以及特征工程文件data_feature_project.ipynb  
模型1:xgboost以及模型训练和预测结果xgboost_predict.ipynb  
模型2:基于百度paddle框架的DNN搭建，以及DNN模型训练和预测paddle_DNN_predict.ipynb  
基于两种模型的模型融合结果输出xgboost_DNN_predict.ipynb  

