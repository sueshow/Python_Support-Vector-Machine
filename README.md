# Support-Vector-Machine

* 名稱：簡寫為SVM，支撐向量機，
* 監督式的學習方法，用統計風險最小化的原則來估計一個分類的超平面(hyperplane)，其基礎的概念非常簡單，就是找到一個決策邊界(decision boundary)讓兩類之間的邊界(margins)最大化，使其可以完美區隔開來。對小樣本、非線性、高維度與局部最小點等問題具有相對的優勢。
* 分類
  * 說明：所有分類的問題都是在不同的假設或是條件下找那條分類的線，不一定是直線，有可能是曲線，如：高斯分類器就是在利用兩組資料的高斯機率分布/高斯概似函數(Gaussian likelihood function)，去判斷誰的後驗機率(posteriori probability)/概似函數值較大，就判給哪一類別。
  * 優點
    * 使用核函數可以有效處理高維數據
    * 透過不同核函數的選擇，可以處理不同的資料
    * 決策函數由少量的支持向量決定，預測效率高
  * 缺點
    * 維度過高容易造成運算上的負擔
    * 特徵遠大於樣本的情況下容易造成過度擬和的問題
* 數學式子
  * 假設訓練資料為
  * 
* Kaggle
  * 範例資料：[Heart Disease UCI](https://www.kaggle.com/c/heart-disease-uci/data)
  * 分析結果：[Heart Disease UCI](https://github.com/sueshow/Comp_Kaggle/blob/main/%E7%9B%A3%E7%9D%A3_SVM_%E5%AE%8C%E6%95%B4%E7%89%88_Kaggle_Heart_Disease_UCI.ipynb)
* 參考資料
