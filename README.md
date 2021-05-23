#  Regression model in R
## machine learning in R
 * 資料
    * 資料名:保險費用預測 (A dataset for heart attack classification) 
    * 資料來源:<https://www.kaggle.com/mirichoi0218/insurance> 
 * 目標
    * 以變數(年齡 性別 BMI 撫養兒童數 是否吸菸 居住地區)建立模型(線性模型及迴歸樹)，預測保險費用

 * 方法與結果
    * 資料讀取
    * 資料處裡
    > - 將性別 是否吸菸 居住地區 由文字類別轉換成factor
    > - 觀察資料集，發現保險費用分布不均(圖1)，因此將保險費用取log(圖二)
    * ![classification]()
      * 圖2:群聚分析結果
 
    > -  [R code])
