# COVID-19：使用深度學習的醫學診斷
11124108 林柏辰
## 介紹
正在進行的名為COVID-19 的全球大流行是由SARS-COV-2引起的，該病毒傳播迅速並發生變異，引發了幾波疫情，主要影響第三世界和發展中國家。隨著世界各國政府試圖控制傳播，受影響的人數正穩定上升。
## COVID-19:使用深度學習的醫學診斷

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%871.jpg)

本文將使用CoronaHack-Chest X 光資料集。它包含胸部X 光影像，我們必須找到受冠狀病毒影響的影像。
我們之前談到的SARS-COV-2 是主要影響呼吸系統的病毒類型，因此胸部X 光是我們可以用來識別受影響肺部的重要影像方法之一。這是一個並排比較:

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%872.jpg)

如你所見，COVID-19 肺炎如何吞噬整個肺部，並且比細菌和病毒類型的肺炎更危險。
本文，將使用深度學習和遷移學習對受Covid-19影響的肺部的X 光影像進行分類和識別。

## 導入庫和載入數據

![image](https://github.com/a0986990059/456/blob/main/1.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%873.jpg)

![image](https://github.com/a0986990059/456/blob/main/2.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%874.jpg)

## 處理缺失值

![image](https://github.com/a0986990059/456/blob/main/3.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%875.jpg)

![image](https://github.com/a0986990059/456/blob/main/4.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%876.jpg)

![image](https://github.com/a0986990059/456/blob/main/5.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%877.jpg)

![image](https://github.com/a0986990059/456/blob/main/6.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%878.jpg)

我們將用“unknown”填充缺失值。

![image](https://github.com/a0986990059/456/blob/main/7.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%879.jpg)

因此標籤2 類別包含COVID-19案例

## 顯示影像

![image](https://github.com/a0986990059/456/blob/main/8.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8710.jpg)

## 視覺化

![image](https://github.com/a0986990059/456/blob/main/9.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8711.jpg)

## 對於COVID-19 病例

![image](https://github.com/a0986990059/456/blob/main/10.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8712.jpg)

## 對於正常情況

![image](https://github.com/a0986990059/456/blob/main/11.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8713.jpg)

![image](https://github.com/a0986990059/456/blob/main/12.png)

## 數據增強

![image](https://github.com/a0986990059/456/blob/main/13.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8714.jpg)

![image](https://github.com/a0986990059/456/blob/main/14.png)

注意：輸出太長，無法包含在文章中。這是其中的一小部分。

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8715.jpg)

![image](https://github.com/a0986990059/456/blob/main/15.png)

## 將所有資料轉換為張量

![image](https://github.com/a0986990059/456/blob/main/16.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8716.jpg)

## 產生批次

![image](https://github.com/a0986990059/456/blob/main/17.png)

## 使用ResNet50 進行遷移學習

![image](https://github.com/a0986990059/456/blob/main/18.png)

現在我們的遷移學習成功了！ ！

![image](https://github.com/a0986990059/456/blob/main/19.png)

## 為影像分類添加密集層

![image](https://github.com/a0986990059/456/blob/main/20.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8717.jpg)

![image](https://github.com/a0986990059/456/blob/main/21.png)

## 預測

![image](https://github.com/a0986990059/456/blob/main/22.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8719.jpg)

![image](https://github.com/a0986990059/456/blob/main/23.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8720.jpg)

所以正如你所看到的，預測還不錯。我們將繪製一個混淆矩陣來視覺化我們模型的表現：

![image](https://github.com/a0986990059/456/blob/main/24.png)

![image](https://github.com/a0986990059/456/blob/main/%E5%9C%96%E7%89%8721.jpg)

## 尾註
這個資料集很有趣，學習資料科學和機器學習越多，就越覺得這個主題很有趣。如今，我們可以透過多種方式使用數據，使用數據可以挽救無數生命。

