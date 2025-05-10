---
lab:
  title: 使用 Azure AI Foundry 入口網站中的內容瞭解擷取資料
---

# 使用 Azure AI Foundry 入口網站中的內容瞭解擷取資料

**Azure AI 內容瞭解（預覽版）** 使用生成式 AI 將許多類型的內容（文件、影像、影片和音訊）處理成使用者定義的輸出格式。

在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，使用 Azure AI 內容瞭解來辨識發票中的資料。 

此練習大約需要 **25** 分鐘。

## 建立 Azure AI Foundry 專案

讓我們從建立 Azure AI Foundry 專案開始。

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時開啟的所有提示或快速啟動窗格，如有必要，使用左上角的 **Azure AI Foundry** 標誌瀏覽到首頁，首頁類似於下圖（若 [說明]**** 窗格已開啟，請將其關閉）：

    ![Azure AI Foundry 首頁的螢幕擷取畫面，其中已選取 [建立專案]。](./media/azure-ai-foundry-home-page.png)

1. 在首頁中，選取 **+ 建立專案**。

1. 請在** [建立專案**精靈] 中，輸入專案有效名稱。如果建議使用現有的中樞，請先選擇建立新的中樞選項。 然後審查 Azure 資源，將會自動建立，以便支援中樞和專案。

1. 選取**自訂**，然後為您的中樞指定下列設定：
    - **中樞名稱**：*請提供有效的中樞名稱*
    - **訂用帳戶**：您的 Azure 訂用帳戶**
    - **資源群組**：建立或選取資源群組**
    - **位置：** 美國西部 
    - **連接 Azure AI 服務或 Azure OpenAI**：*[建立新的 AI 服務資源]*
    - **連接 Azure AI 搜尋服務**：跳過連接

1. 選取**下一步**並檢閱您的設定。 然後選取**建立**並等待該流程完成。

1. 建立專案後，關閉顯示的所有提示並檢閱 Azure AI Foundry 入口網站中的專案頁面，該頁面應類似於下圖：

    ![Azure AI Foundry 入口網站中 Azure AI 專案詳細資料的螢幕螢幕擷取畫面。](./media/ai-foundry-project.png)
 
1. 瀏覽螢幕左側的功能表。 然後，選取 [AI 服務]****。

1. 在 [AI 服務]** 頁面上，選取 [內容瞭解]** 圖格，以試用 Azure AI 內容瞭解功能。

## 使用 Azure AI Foundry 中的 Azure AI 內容瞭解來分析發票 

假設您想要從許多發票擷取資料，並將資料放入資料庫中。 您可以使用 Azure AI 內容瞭解來分析一張發票，並建置自己的分析器來分析其他類似的發票。 讓我們從建立內容瞭解工作開始。

![內容瞭解主頁面的螢幕擷取畫面。](./media/content-understanding/content-understanding-1.png)

1. 選取 [自訂分析器]****。 

1. 選取 [+ 建立]****，並使用下列設定來建立內容瞭解工作：
    - **工作名稱**：contoso-invoice
    - **描述**：發票分析工作
    - **Azure AI 服務連線**：*使用預設*
    - **Azure Blob 儲存體帳戶**：*使用預設*

1. 選取 [建立]****，然後等候系統建立工作。 
1. 選取您的 **contoso-invoice** 工作。 

#### 定義結構描述 

1. 在 [定義結構描述]** 頁面上，您可以新增測試檔案。 從 `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf` 下載 [contoso-invoice-1.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/contoso-invoice-1.pdf)。 

1. 將檔案上傳至 [定義結構描述]** 頁面。 選取*發票分析*範本。 發票範本已預先選取分析器會嘗試偵測的資料欄位。 

    ![內容瞭解工具中定義結構描述頁面的螢幕擷取畫面。](./media/content-understanding/define-schema.png)

1. 選取 **建立**。 現在您可以藉由新增或刪除欄位來修改結構描述。 當您完成檢閱欄位時，請選取 [儲存]****。

    ![選取 [建立] 之後顯示的定義結構描述頁面的螢幕擷取畫面。](./media/content-understanding/define-schema-2.png)

1. 等待分析執行。 這可能需要一些時間。

#### 測試分析器 

1. 分析完成時，您將能夠在 [測試分析器]** 頁面中查看分析器如何完成。 檢閱 [欄位]** 索引標籤。此資料是否符合您在發票上看到的內容？ 
    ![測試分析器頁面的螢幕擷取畫面，其中已醒目提示 [功能變數結果] 索引標籤。](./media/content-understanding/test-analyzer-fields.png)

1. 請注意每個欄位旁的*信賴度分數*。 信賴度分數代表模型對其結果正確無誤的信賴度。 信賴度分數接近 100% 的結果表示預測的信賴度更高。
1. 檢閱 [結果]** 索引標籤。您在 [欄位] 索引標籤中看到的相同資訊位於 JSON 中的 [結果] 索引標籤中。 JSON 會顯示資訊在用戶端應用程式中傳送時的外觀。 

    ![測試分析器頁面的螢幕擷取畫面，其中已醒目提示 [結果] 索引標籤。](./media/content-understanding/test-analyzer-result.png)

1. 內容瞭解服務應該正確識別與架構中的欄位相對應的文字。 如果未能如此，您可以使用*標籤資料*頁面上傳另一個範例表單，並明確標識每個欄位的正確文字。 若您滿意分析器在偵測發票中的資料時所取得的結果，請選取 [組建分析器]**** 索引標籤。 

#### 組建分析器 

現在您已經訓練了一個模型來從發票樣本中擷取欄位，您可以組建一個分析器來與類似的表單一起使用。 藉由組建分析器，您可以部署模型，並用它來自動化其他發票工作。

1. 在 [組建分析器]** 索引標籤中，選取 [+ 組建分析器]****。 輸入下列內容： 
    - **名稱**：invoice-analyzer
    - **描述**：發票分析器

    ![組建分析器頁面的螢幕擷取畫面。](./media/content-understanding/build-analyzer.png)

1. 選取 [組建]****。 等待新的分析器準備就緒（使用重新整理按鈕進行檢查）。 您的分析器會使用以您在先前步驟中定義及測試之結構描述為基礎的預測模型。 
1. 現在讓我們嘗試測試您所組建的分析器。 從 `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-2.pdf` 的 Contoso [contoso-invoice-2.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-2.pdf) 中下載不同的發票。
1. 返回 [組建分析器]** 頁面並選擇 invoice-analyzer 連結。 分析器結構描述中定義的欄位隨即顯示。
1. 在 invoice-analyzer 頁面中，選取 [測試]**。
1. 使用 [+ 上傳測試檔案]**** 按鈕來上傳 *contoso-receipt-2.pdf*。 選取 [執行分析]**** 以從測試表單擷取欄位資料。 檢閱測試的結果。

    ![您所組建的分析器測試結果的螢幕擷取畫面。](./media/content-understanding/build-analyzer-2.png)

1. 選取 [程式碼範例]** 索引標籤。尋找程式碼中的*端點*。 在程序的*組建分析器*階段中，您已將內容瞭解模型部署至端點。 端點可在與您在範例中看到的內容類似的程式碼中使用，以將模型併入應用程式中的可重複程序。  

    ![您組建之分析器程式碼範例的螢幕擷取畫面。](./media/content-understanding/code-example.png)

## 清理

如果您已完成使用內容瞭解服務，則應刪除在此練習中建立的資源，以避免產生不必要的 Azure 成本。

- 在 Azure AI Foundry 入口網站中，瀏覽至 contoso-receipt 專案並加以刪除。
- 前往您在 Azure 入口網站中針對這些練習所建立的資源群組。