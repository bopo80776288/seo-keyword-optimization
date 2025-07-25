# SEO 關鍵字優化專案說明

## 1. 專案目標與背景
本專案旨在透過關鍵字資料分析與語意分群，優化「老協珍」雞精品牌於「滴雞精推薦」相關搜尋詞的SEO表現，目標是提升品牌於Google搜尋結果的排名與點擊率。專案聚焦於SEO四大指標（CTR、Impressions、Position、Clicks），並結合語意嵌入與分群演算法，提出具體的內容優化策略。

## 2. 資料來源與預處理
- **資料來源**：以Google Search Console匯出的關鍵字成效資料為主，並以CSV格式儲存。
- **預處理步驟**：
  - 下載Excel檔後轉存為CSV，方便pandas讀取。
  - 移除空白行列與不相關欄位。
  - 將百分比字串（如CTR）轉為數值型態。

## 3. 分析步驟
### (1) SEO指標分析
- 以CTR、Impressions、Position、Clicks等指標進行資料視覺化，找出高潛力與需優化的關鍵字。

### (2) 關鍵字語意分群
- 使用`sentence-transformers`多語言模型將關鍵字轉為向量，並以Agglomerative Clustering分為5群。
- 以PCA降維視覺化分群結果。

### (3) 分群策略設計
- 針對每一群設計不同的內容優化策略（如：品牌推薦、疑慮解除、購買導向、成分營養、競品比較）。

## 4. 如何在Colab執行與下載正確的.ipynb檔案
1. 點選本專案的 `.ipynb` 檔案上方的「Open in Colab」徽章，於Colab開啟。
2. 如需儲存或下載，請於Colab選單選擇「檔案」→「下載」→「下載 .ipynb」。
3. 請勿直接複製Colab的cell內容另存為文字檔，務必以官方「下載 .ipynb」功能取得正確格式。

## 5. 注意事項
- 若將Colab下載的`.ipynb`檔案上傳至GitHub後，出現「Invalid Notebook」或無法顯示：
  請於GitHub下載檔案後在Colab環境下開啟

## 6. 主要依賴套件
- pandas
- numpy
- matplotlib
- seaborn
- tabulate
- sentence-transformers
- scikit-learn

---