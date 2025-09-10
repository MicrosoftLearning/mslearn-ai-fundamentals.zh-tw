---
lab:
  title: 探索 Azure AI Foundry 入口網站中的生成式 AI
---

# 探索 Azure AI Foundry 入口網站中的生成式 AI

生成式 AI 描述 AI 中建立內容的功能類別。 人員通常會與聊天應用程式內建的生成式 AI 互動。 在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，試用生成式 AI。 

此練習大約需要 **20 分鐘**。

## 在 Azure AI Foundry 入口網站中建立專案

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時，已開啟任何提示或是快速入門窗格。 

1. 在瀏覽器中，先瀏覽至 `https://ai.azure.com/managementCenter/allResources`，再選取 [建立新項目]****。 然後選擇選項，以便建立**新的 Azure AI Foundry 資源**。

1. 請在 *[建立專案]* 精靈中，輸入專案的有效名稱。

1. 請展開 *[進階選項]*，為專案指定下列設定：
    - **訂用帳戶**：您的 Azure 訂用帳戶
    - **資源群組**：建立或選取資源群組
    - **地區**：選取以下位置之一：
        * 美國東部
        * 法國中部
        * 南韓中部
        * 西歐
        * 美國西部

    選取 **建立**。 等候您的專案建立。 這可能需要幾分鐘的時間。

1. 當建立專案時，系統會將您導向專案詳細資料的 [*概觀*] 頁面。

1. 在畫面的左側功能表上，選取 [遊樂場]****。 

    >*注意*：按一下頂部的「展開」圖示展開選單並閱讀其內容。

## 探索 Azure AI Foundry 聊天遊樂場中的生成式 AI

1. 在 Azure AI Foundry 的遊樂場頁面中，選取 [試用聊天遊樂場]****。 聊天遊樂場是一種使用者介面，可讓您嘗試使用不同的生成式 AI 模型建置聊天應用程式。  

    >*注意*：若您沒有在聊天遊樂場畫面上看到 [設定]** 窗格，請調整視窗大小。  

1. 若要使用聊天遊樂場，您必須將它與已部署的模型產生關聯。 在聊天遊樂場的 [設定]** 窗格中，選取 [+ 建立部署]****。 若出現提示，請選取 [從基礎模型建立]**，否則請繼續進行下一個步驟。 

1. 搜尋 **gpt-4o** 模型，然後選取 [確認]****。 保留預設模型名稱、部署類型和部署詳細資料。 然後選取 [部署]****。

1. 在聊天遊樂場中，您可以在 [部署]** 選取功能表中出現已部署的模型時使用它。 關閉任何開啟的提示或快速入門窗格。 

    >*注意*：在對 [設定] ** 進行任何變更之後，您必須選取 [套用變更]****。 

1. 瀏覽至 [聊天記錄]** 窗格。 您將使用查詢方塊來輸入您的提示。 

1. 不妨考慮採用下列方式，改善生成式 AI 助理提供的回覆：
    - 從您希望助理達成的特定目標開始
    - 根據先前的提示和回覆逐一查看，縮小結果範圍
    - 提供來源，以特定資訊範圍為回覆基礎
    - 新增內容，將回覆的適當性和相關性最大化
    - 為回覆設定明確的期望

1. 讓我們試著使用具有特定目標的提示，生成回覆看看。 在聊天方塊中，輸入下列提示：

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. 檢閱回應。 **注意**：請注意，您收到的特定回覆可能會因生成式 AI 的性質而有所不同。
 
1. 讓我們試試另外一個提示。 輸入下列：

    ```prompt
    Where's a good location in Paris to stay? 
    ```

1. 檢閱回覆，其中應該會提供一些巴黎住宿。

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

1. 當您完成時，您可以關閉瀏覽器視窗。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 **Azure 入口網站** (位於 [https://portal.azure.com](https://portal.azure.com))，然後選取包含您所建立資源的資源群組。

1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。
