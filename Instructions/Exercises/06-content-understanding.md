---
lab:
  title: 使用 Azure AI Foundry 入口網站中的內容瞭解擷取資料
---

# 使用 Azure AI Foundry 入口網站中的內容瞭解擷取資料

Azure AI 內容瞭解提供文件、音訊檔案、影片和影像的多模態分析，以擷取資訊。

在本練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，使用 Azure AI 內容瞭解以從發票擷取資訊。 

此練習大約需要 **25** 分鐘。

## 建立用於內容瞭解的 Azure AI Foundry 專案

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時開啟的所有提示或快速啟動窗格，如有必要，使用左上角的 **Azure AI Foundry** 標誌瀏覽到首頁，首頁類似於下圖（若 [說明]**** 窗格已開啟，請將其關閉）：

    ![Azure AI Foundry 入口網站首頁的螢幕擷取畫面。](./media/ai-foundry-portal.png)

1. 捲動至頁面底部，然後選取 [探索 Azure AI 服務]**** 圖格。

    ![[探索 Azure AI 服務] 圖格的螢幕擷取畫面。](./media/ai-services.png)

1. 在 Azure AI 服務頁面上，選取 [試用內容瞭解]****。

    ![試用內容瞭解按鈕的螢幕擷取畫面。](./media/try-content-understanding.png)

1. 在 [內容瞭解] 頁面中，選取 [建立要開始的專案]****。 然後在 [建立專案]**** 對話中，選取建議的資源類型 (**Azure AI Foundry 資源**)：

    ![分析結果的螢幕擷取畫面。](./media/resource-type.png)

1. 在 [下一步]**** 頁面上，輸入專案的有效名稱。 然後選取 [進階選項]**** 並指定以下設定：
    - **Azure AI Foundry 資源**：*Azure AI Foundry 資源的有效名稱*
    - **訂用帳戶**：您的 Azure 訂用帳戶**
    - **資源群組**：建立或選取資源群組**
    - **區域**：選取下列其中一個位置\*：
        * 美國西部
        * 瑞典中部
        * 澳大利亞東部

    \**在撰寫本文時，內容瞭解適用於這些區域支援。*

    ![專案設定的螢幕擷取畫面。](./media/content-project-settings.png)

1. 選取 **建立**。 等候設定程序完成。 這可能需要幾分鐘的時間。

## 從發票擷取資訊

1. 從 `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf` 下載 [contoso-invoice-1.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf)。 

1. 在 [內容理解] 頁面上，選取 [試用]**** 索引標籤，然後選取 [發票資料擷取]**** 圖格。

    ![內容瞭解「試用」頁面的螢幕擷取畫面。](./media/content-understanding-invoice.png)

    提供範例發票。

1. 選取範例發票，並使用 [執行分析]**** 按鈕從中擷取資訊。 分析完成時，請檢視結果。

    ![分析範例發票結果的螢幕擷取畫面。](./media/sample-invoice-analysis.png)

1. 使用 [瀏覽檔案]**** 連結上傳您先前下載的 **contoso-invoice-1.pdf** 文件，並對該檔案執行分析。

    ![分析 Contoso 發票結果的螢幕擷取畫面。](./media/contoso-invoice-analysis.png)

    請注意，內容瞭解分析器可以從此發票擷取資訊，即使其格式與範例不同。

1. 在顯示擷取欄位的右側窗格中，檢視 [結果]**** 索引標籤，以查看將傳送至用戶端應用程式的 JSON 回應。 開發人員會撰寫程式碼來處理此回應，並使用擷取的欄位執行特定動作。

    ![分析 Contoso 發票結果的螢幕擷取畫面。](./media/invoice-analysis-json.png)

## 清理

如果您已完成使用內容瞭解服務，則應刪除在此練習中建立的資源，以避免產生不必要的 Azure 成本。

- 前往您在 Azure 入口網站中針對這些練習所建立的資源群組。
