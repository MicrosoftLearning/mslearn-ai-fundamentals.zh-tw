---
lab:
  title: 探索 Azure AI Foundry 入口網站中的生成式 AI
---

# 探索 Azure AI Foundry 入口網站中的生成式 AI

生成式 AI 描述 AI 中建立內容的功能類別。 人員通常會與聊天應用程式內建的生成式 AI 互動。 在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，試用生成式 AI。 

此練習大約需要 **20 分鐘**。

## 在 Azure AI Foundry 入口網站中建立專案

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時開啟的所有提示或快速啟動窗格，如有必要，使用左上角的 **Azure AI Foundry** 標誌瀏覽到首頁，首頁類似於下圖（若 [說明]**** 窗格已開啟，請將其關閉）：

    ![Azure AI Foundry 入口網站首頁的螢幕擷取畫面。](./media/ai-foundry-portal.png)

1. 在 [探索模型和功能]**** 區段中，搜尋 `gpt-4o`。 然後，在搜尋結果中，選取 **gpt-4o** 模型以檢視其詳細資料。

    ![gpt-4o 詳細資料頁面的螢幕擷取畫面。](./media/gpt-4o-details.png)

1. 選取 [使用此模型]****。

1. 請在 **[建立專案]** 精靈中，輸入專案的有效名稱。 展開 [進階選項]****，為專案指定下列設定：
    - **Azure AI Foundry 資源**：*輸入 AI Foundry 資源的有效名稱。*
    - **訂用帳戶**：您的 Azure 訂用帳戶**
    - **資源群組**：建立或選取資源群組**
    - **區域**：選取任何 [AI Foundry 建議]**** 區域\*
    
    \**模型部署受限於區域配額。如果您選取可用配額不足的區域，您可能需要稍後選取新資源的替代區域。*

1. 選取 **建立**。 等候您的專案建立。 這可能需要幾分鐘的時間。

    如果系統提示您將模型部署到不同區域，請使用預設設定來執行此動作。

## 探索 Azure AI Foundry 聊天遊樂場中的生成式 AI

1. 建立專案之後，在左側的工作窗格中，選取 [遊樂場]****。 

    >*秘訣*：如有必要，按一下頂部的「展開」圖示展開功能表並閱讀其內容。

1. 在 Azure AI Foundry 的遊樂場頁面中，選取 [試用聊天遊樂場]****。 關閉任何開啟的提示或快速入門窗格。

    聊天遊樂場是一種使用者介面，可讓您嘗試使用不同的生成式 AI 模型建置聊天應用程式。

    ![gpt-4o 詳細資料頁面的螢幕擷取畫面。](./media/chat-playground.png)

    >*秘訣*：如果您沒有在聊天遊樂場畫面上看到 [設定]**** 窗格，請調整視窗大小。  

1. 若要使用聊天遊樂場，您必須將它與已部署的模型產生關聯。 在聊天遊樂場的 [設定 ]**** 窗格中，確定已選取您先前部署的 **gpt-4o** 模型。 

    >*注意*：在對 [設定] **** 進行任何變更之後，必須選取 [套用變更]****。

1. 在 [設定] **** 窗格中，記下模型的預設指示和內容，其內容應該類似於：

    `You are an AI assistant that helps people find information.`

    這些類型的指令通常稱為*系統提示*，用於為模型回應提供指導和限制。

1. 檢閱 [聊天記錄]** 窗格，其中包含一些協助您開始使用的範例提示，以及輸入您自己的提示的查詢方塊。 

1. 讓我們試著使用具有特定目標的提示，生成回覆看看。 在聊天方塊中，輸入下列提示：

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. 檢閱回應。 請注意，您收到的特定回覆可能會因生成式 AI 的性質而有所不同。

1. 讓我們試試另外一個提示。 輸入下列：

    ```prompt
    Where's a good location in the city to stay?
    ```

1. 檢閱回覆，其中應該會提供一些巴黎住宿。 或者聊天工作階段會保留先前提示的內容，因此能夠理解此處所指的「城市」為巴黎。

1. 讓我們根據先前的提示和回覆逐一查看，縮小結果範圍。 輸入下列提示：

    ```prompt
    Can you give me more information about dining options near the first location?
    ```

1. 檢閱回覆，其中應該會提供先前回覆中的位置附近的餐飲選項。 

1. 現在，讓我們提供來源，以特定資訊範圍為回覆基礎。 輸入下列： 

    ```prompt
    Based on the information at https://en.wikipedia.org/wiki/History_of_Paris, what were the key events in the city's history?
    ```

1. 檢閱回覆，其中應該會根據所提供的網站提供資訊。 

1. 讓我們嘗試新增內容，以最大化回覆的相關性。 輸入下列提示： 

    ```prompt
    What three places do you recommend I stay in Paris to be within walking distance to historical attractions? Explain your reasoning.
    ```

1. 檢閱回覆和回覆的原因。  

1. 現在嘗試為回覆設定明確的期望。 輸入下列提示：

    ```prompt
    What are the top 10 sights to see in Paris? Answer with a numbered list in order of popularity.
    ```

1. 檢閱回回覆，其中應該會提供巴黎景點的編號清單。

## 檢視客戶端程式碼

1. 在 [聊天遊樂場] 頁面頂端，選取 [檢視程式碼]****。
1. 檢閱程式碼範例適用於多種程式設計語言、SDK 和驗證選項。

    這些程式碼範例可協助開發人員在建置與已部署模型聊天的用戶端應用程式時，快速開始使用。

1. 關閉範例程式碼視窗。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 **Azure 入口網站** (位於 [https://portal.azure.com](https://portal.azure.com))，然後選取包含您所建立資源的資源群組。
1. 選取 [刪除資源群組]****，然後**輸入資源群組的名稱**以確認。 接著即會刪除該資源群組。
