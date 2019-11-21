# FinancialStatement
這個練習的目的在爬取台灣公開資訊觀測站內指定股票的指定季報，以方便日後計算各項財報比率以利基本面分析。

心得:

一.網頁爬蟲的post和get不同，網址在轉換的過程中網址不會變動，而是form_data裡的數值會隨著查詢的輸入不同而改變，觀察這些並了解如何輸入我要的資訊是一個很棒的經驗。request內含貼心的post函式，將爬蟲程式變得相當簡單易懂。－資料擷取

二.pd.read_html得到的結果是一個list，需要在裡面篩選有用的資料且使用header參數指定我要的行數成為欄位名稱以方便後面使用。－資料清洗

三．公開資訊觀測站滿貼心的。在回傳指定的季報外還額外提供去年同一季的季報，方便計算年增率等財務比率。

#沒有刪除一些無用欄位的原因是因為日後計算比率時是直接提取相關欄位計算，除了美觀外沒有特別需要刪除無用欄位的必要
