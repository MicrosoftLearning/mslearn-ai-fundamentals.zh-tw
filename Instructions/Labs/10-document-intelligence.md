---
lab:
  title: 在 Document Intelligence Studio 中擷取窗體數據
---

# 在 Document Intelligence Studio 中擷取窗體數據

Azure AI 檔智慧能夠分析及擷取表單和文件的資訊，然後識別功能變數名稱和數據。 

文件智慧如何建立在光學字元辨識（OCR）上？ 雖然 OCR 可以讀取列印或手寫的檔，但 OCR 會擷取非結構化格式的文字，而難以儲存在資料庫中或分析。 文件智慧藉由擷取文字的結構來理解非結構化數據，例如數據表中的索引鍵/值組和資訊。 

在此練習中，您將查看檔智慧中預先建置的模型，該模型已定型以辨識收據的數據。 

> **注意** Azure AI 檔智慧是 Azure 表格辨識器 的新名稱。 您仍然可以在 Azure 入口網站 或 Document Intelligence Studio 中看到 Azure 表格辨識器。

## 建立 *文件智能* 資源

您可以藉由建立 *Document Intelligence 資源或 *Azure AI 服務*資源，來使用 Azure AI 檔智慧*。 在此練習中，如果您還沒有檔智慧資源，您將建立 *檔智能* 資源。

1. 在另一個瀏覽器索引標籤中，開啟 [Document Intelligence Studio](https://formrecognizer.appliedai.azure.com/studio)，使用您的 Microsoft 帳戶登入。
1. 選取 **[設定]，** 然後選取 [**資源**] 索引卷標。選取 **[建立新的資源**]。
1. 在 [建立資源] 對話框中，輸入下列專案：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **新的資源名稱**： *輸入唯一的名稱*。
    - **位置**： *選取區域*。
    - **定價層**：*免費 FO（如果有的話，請選取 [標準 SO]。*
1. 選取 [繼續 **]，然後**選取 **[完成**]。 等候資源部署。

    >**注意** 如果您的資源尚未顯示，您可能需要重新**** 整理頁面。

讓 Document Intelligence Studio 保持開啟。

## 在 Document Intelligence Studio 中分析收據

您現在已準備好分析虛構 Northwind Traders 零售公司的收據。

1. 選取[https://aka.ms/mslearn-receipt****](https://aka.ms/mslearn-receipt)以將範例檔下載到您的電腦。 開啟  資料夾。 
1. 選取 **[Document Intelligence Studio] 以返回 **[開始使用檔智慧 Studio****] 頁面，然後在 [收據] 底下選取 [**試用]。**
1. 在 [預先建置] 下拉式清單中，確定 **已選取 [收據** ]。
1. 選取 [ **瀏覽檔案** ]，然後瀏覽至您儲存圖片的資料夾。 選取收據的圖片，然後 **選取 [開啟**]。 影像會出現在畫面左側。

    ![Northwind 收據。](media/document-intelligence/northwind-receipt.jpg)

1. 在右側，選取 [ **執行分析**]。
1. 當分析執行時，會傳回結果。 請注意，服務已辨識特定數據欄位，例如商家的名稱、地址、電話號碼和交易日期和時間，以及明細專案、小計、稅金和總金額。 每個欄位旁邊都是欄位正確百分比的機率。

在本練習中，您已使用 Document Intelligence Studio 來建立文件智慧資源。 接著，您使用服務來分析收據。 從傳回的結果中，您已瞭解「檔智慧」如何識別特定欄位，讓日常文件的數據更容易處理。 在您關閉 Document Intelligence Studio 之前，為什麼不嘗試一些範例收據，包括不同語言的收據？

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. [開啟 Azure 入口網站]( https://portal.azure.com)，然後選取包含您所建立資源的資源群組。
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

此練習僅示範 AI 檔智慧服務的一些功能。 若要深入瞭解如何使用這項服務，請參閱 [檔智能](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0) 頁面。
