# Support-Vector-Machine

* 名稱：簡寫為SVM，支撐向量機
* 1960-1990 年代就由數學家 Vapnic 及 Chervonenkis 等人所提出，並建立了這套統計學習理論
* 監督式的學習方法，用統計風險最小化的原則來估計一個分類的超平面(hyperplane)，其基礎的概念非常簡單，就是找到一個決策邊界(decision boundary)讓兩類之間的邊界(margins)最大化，使其可以完美區隔開來。對小樣本、非線性、高維度與局部最小點等問題具有相對的優勢。
* 分類
  * 所有分類的問題都是在不同的假設或是條件下找那條分類的線，不一定是直線，有可能是曲線，如：高斯分類器就是在利用兩組資料的高斯機率分布/高斯概似函數(Gaussian likelihood function)，去判斷誰的後驗機率(posteriori probability)/概似函數值較大，就判給哪一類別。
  * 範例說明：
    * 以直線來說，首先紅色的線會創造兩條黑色平行於紅色線的虛線，並讓黑線平移碰到最近的一個點，紅線到黑線的距離稱為 Margin，而 SVM 就是透過去找 Margin 最大的那個紅線來找最好的線
    * 假設紅線是 w*x =0 在紅線上方的區域就是 w*x >0 紅線下方的區域就是 w*x <0，同理類推來看在左邊虛線上方的區域是 w*x <-k 在右邊虛線下方的區域是 w*x >k，虛線中間不會有資料點
    * 虛線上的點 X1、X2 就是所謂的支援向量(Support vector)，我們主要是利用支援向量來算出 Margin，並最大化 Margin。利用高中數學的知識將 X1 向量- X2 向量得到的向量投影到 W ，在 Y*(W*X) ≥k 的條件下(虛線中間沒有點)，來最大化 margin
    * 公式：$$\bf{\frac{w}{ ||w|| }\cdot (x_+ – x_-)} =\bf{\frac{w^T(x_+-x_-)}{||w||}}=\frac{k}{\bf{||w||}}$$

* 優點
  * 使用核函數(Kernel)可以有效處理高維數據
  * 透過不同核函數的選擇，可以處理不同的資料
  * 決策函數由少量的支持向量決定，預測效率高
* 缺點
  * 維度過高容易造成運算上的負擔
  * 特徵遠大於樣本的情況下容易造成過度擬和的問題
* 圖示說明

  ![得到那條很好的線](https://github.com/sueshow/Support-Vector-Machine/blob/main/picture/SVM_01.png)
  <br>
  ![讓Margin最大01](https://github.com/sueshow/Support-Vector-Machine/blob/main/picture/SVM_02.png)
  <br>
  ![讓Margin最大02](https://github.com/sueshow/Support-Vector-Machine/blob/main/picture/SVM_03.png)
  <br>
  ![怎麼計算margin](https://github.com/sueshow/Support-Vector-Machine/blob/main/picture/SVM_04.png)
  <br>
  ![公式](https://github.com/sueshow/Support-Vector-Machine/blob/main/picture/SVM_05.png)
  <br>
      
* Kaggle
  * 範例資料：[Heart Disease UCI](https://www.kaggle.com/c/heart-disease-uci/data)
  * 分析結果：
    * [Heart Disease UCI](https://github.com/sueshow/Comp_Kaggle/blob/main/%E7%9B%A3%E7%9D%A3_SVM_%E5%AE%8C%E6%95%B4%E7%89%88_Kaggle_Heart_Disease_UCI.ipynb)
    * [Iris]
* 參考資料
  * [支援向量機(Support Vector Machine)介紹](https://medium.com/jameslearningnote/%E8%B3%87%E6%96%99%E5%88%86%E6%9E%90-%E6%A9%9F%E5%99%A8%E5%AD%B8%E7%BF%92-%E7%AC%AC3-4%E8%AC%9B-%E6%94%AF%E6%8F%B4%E5%90%91%E9%87%8F%E6%A9%9F-support-vector-machine-%E4%BB%8B%E7%B4%B9-9c6c6925856b) 
