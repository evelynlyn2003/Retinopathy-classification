# 辨識糖尿病視網膜病變影像，進行嚴重度分類
### A 數據 (Dataset & DataLoader)
#### 1.資料來源 : Kaggle 糖尿病視網膜病變分級競賽 (diabetic-retinopathy-classification-3) 的資料集。
https://www.kaggle.com/competitions/diabetic-retinopathy-classification-3/overview
#### 2.資料規模 : 測試集：1,465 張。訓練/驗證集：共 2,197 張，依據病變嚴重程度分為 0 到 4 個等級
#### 3.torchvision.transforms，水平/垂直翻轉、隨機仿射變換 (旋轉、縮放、剪切)。




### B.模型 (Model)
#### 1.採用 深度遷移學習 (Deep Transfer Learning)。
#### 2.使用 ResNet50 預訓練模型，透過殘差塊 (Residual Blocks) 解決了深度網絡訓練中的梯度消失問題。
#### 3.將基礎 ResNet50 模型的所有參數凍結，有效防止在小數據集上過度擬合。

### C.訓練與優化 (Training)
#### 1.優化器採用 Adam 優化器，初始學習率$1e-3$。

### D.結果與評估
#### 1.kaggle的評分
#### --- Advanced Baseline --- 0.72218
#### ---- Medium Baseline ---- 0.56730
#### 本次成績:0.79863


