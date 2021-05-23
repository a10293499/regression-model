#  Regression model in R
## machine learning in R
 * 資料
    * 資料名:保險費用預測 (A dataset for heart attack classification) 
    * 資料來源:<https://www.kaggle.com/mirichoi0218/insurance> 
 * 目標
    * 以變數(年齡 性別 BMI 撫養兒童數 是否吸菸 居住地區)建立模型(線性模型及迴歸樹)，預測保險費用

 * 方法與結果
    * [R code](https://github.com/a10293499/regression-model/blob/main/code)
   
    * 資料讀取
    
    * 資料處裡
    > - 將性別 是否吸菸 居住地區 由文字類別轉換成factor
    > - 觀察資料集，發現保險費用分布不均(圖1)，因此將保險費用取log(圖2)
    > - 確認變數是否有outlier，發現BMI值有outlier(圖3)
    > - 移除outlier
    > - ![charge](https://github.com/a10293499/regression-model/blob/main/charge.png)
      >- 圖1:保險費用分布
    > - ![charge_log](https://github.com/a10293499/regression-model/blob/main/charge%20log.png)
      >- 圖2:保險費用取log後分布
    > - ![outlier](https://github.com/a10293499/regression-model/blob/main/outlier.png)
      >- 圖3:年齡及BMI盒狀圖
    
    
    * 將資料以8:2分成訓練集與測試集
    
    * 線性性建立
    
    * 模型檢驗
    > - residual無任意分布，也不接受常態檢測，故不符合線性模型規則
    * 迴歸樹建立(圖4)
    > - ![regression_tree](https://github.com/a10293499/regression-model/blob/main/regression%20tree.png)
      > - 圖4:迴歸樹
    > - RMSE:0.438
    * Bootstrap: Bagging with ipred 平均模型預測結果，降低單一模型變異度
    > -  Out-of-bag(OOB) sample 估計模型錯誤率
    > - RMSE:0.383
    * Bootstrap: Bagging with caret 
    > -  Cross validation 估計模型錯誤率
    > - 建立10-fold crodd validation
    > - RMSE:0.375(與上述相比最低)
    > - Rsquared: 0.833
    > - 確認變數是最重要的，圖5由上而下，最重要為年齡，其次為BMI值
    > - ![variable importance](https://github.com/a10293499/regression-model/blob/main/variable%20important.png)
      > - 圖5:變數重要性
    
