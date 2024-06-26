---
lab:
  title: 在文件智慧服務工作室中擷取表單資料
---

# 在文件智慧服務工作室中擷取表單資料

Azure AI 文件智慧服務能夠分析及擷取表單和文件的資訊，然後識別欄位名稱和資料。 

文件智慧服務如何建立光學字元辨識 (OCR) 上？ 雖然 OCR 可以讀取列印或手寫的文件，但 OCR 會擷取非結構化格式的文字，難以儲存至資料庫中或進行分析。 文件智慧服務藉由擷取文字的結構 (例如，表格中的索引鍵/值組和資訊) 來理解非結構化資料。 

在此練習中，您將查看文件智慧服務中預先建置的模型，該模型經訓練可識別收據的資料。 

> **注意** Azure AI 文件智慧服務是 Azure 表格辨識器的新名稱。 您仍然可以在 Azure 入口網站或文件智慧服務工作室中看到 Azure 表格辨識器。

## 建立*文件智慧服務*資源

您可以藉由建立*文件智慧服務*資源或 *Azure AI 服務* 資源，來使用 Azure AI 文件智慧服務。 在此練習中，如果您還沒有文件智慧服務，則您將建立一個*文件智慧服務*資源。

1. 在另一個瀏覽器索引標籤中，開啟[文件智慧服務工作室](https://formrecognizer.appliedai.azure.com/studio)，並使用您的 Microsoft 帳戶登入。
1. 選取 [設定]**** ，然後選取 [資源]**** 索引標籤。選取 [建立新的資源]****。
1. 在 [建立資源] 對話方塊中，輸入下列內容：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **新的資源名稱**：輸入唯一名稱**。
    - **位置**：*選取區域。如果在美國東部，請使用 "美國東部 2"*。
    - **定價層**：*免費 FO (如果不適用，請選取 [標準 SO])*。
1. 選取 [繼續]****，然後 [完成]****。 等候資源部署。

    >**注意**如果未列出您的資源，您可能需要 [重新整理]**** 頁面。

讓文件智慧服務工作室保持開啟。

## 在文件智慧服務工作室中分析收據

您現在已準備好分析虛構 Northwind Traders 零售公司的收據。

1. 選取 [**https://aka.ms/mslearn-receipt**](https://aka.ms/mslearn-receipt) 以將範例文件下載到您的電腦。 開啟  資料夾。 
1. 選取 [文件智慧服務工作室]****，返回 [開始使用文件智慧服務工作室]**** 頁面，然後在 [收據] 底下選取 [試用]****。
1. 在 [預先建置] 下拉式清單中，確定已選取 [收據]****。
1. 選取 [瀏覽以找到檔案]****，然後瀏覽至您儲存圖片的資料夾。 選取收據的圖片，然後 [開啟]****。 圖片隨即出現在視窗左側。

    ![Northwind 收據的螢幕擷取畫面。](media/document-intelligence/receipt.jpg)

1. 在右側，選取 [執行分析]****。
1. 當分析執行時，會傳回結果。 請注意，服務已辨識特定資料欄位，例如商家的名稱、地址、電話號碼和交易日期和時間，以及商品明細、小計、稅金和總金額。 每個欄位旁邊是該欄位正確的百分比可能性。

在此練習中，您已使用文件智慧服務工作室來建立文件智慧服務資源。 接著，您使用服務來分析收據。 從傳回的結果中，您已了解文件智慧服務如何識別特定欄位，讓日常文件的資料更加容易處理。 在您關閉文件智慧服務工作室之前，為什麼不嘗試一些範例收據，包括不同語言的收據？

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取您建立的資源所屬的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

此練習僅示範 AI 文件智慧服務的部分功能。 若要深入了解這項服務的功用，請參閱[文件智慧服務](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0) (部分機器翻譯) 頁面。
