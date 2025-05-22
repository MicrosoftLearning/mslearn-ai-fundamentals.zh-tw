---
lab:
  title: 探索 Azure AI Foundry 入口網站中的生成式 AI
---

# 探索 Azure AI Foundry 入口網站中的生成式 AI

生成式 AI 描述 AI 中建立內容的功能類別。 人員通常會與聊天應用程式內建的生成式 AI 互動。 在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，試用生成式 AI。 

## 在 Azure AI Foundry 入口網站中建立專案

讓我們從建立 Azure AI Foundry 專案開始。

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時開啟的所有提示或快速啟動窗格，如有必要，使用左上角的 **Azure AI Foundry** 標誌瀏覽到首頁，首頁類似於下圖（若 [說明]**** 窗格已開啟，請將其關閉）：

    ![Azure AI Foundry 首頁的螢幕擷取畫面，其中已選取 [代理程式]。](./media/azure-ai-foundry-home-page.png)

1. 在首頁中，選取 [+ 建立代理程式]****。

1. 在 [建立代理程式]**** 精靈中，輸入專案的有效名稱。 

1. 選取 [進階選項]**** 並指定以下設定：
    - **Azure AI Foundry 資源**： *保留預設名稱*
    - **訂用帳戶**：您的 Azure 訂用帳戶**
    - **資源群組**：建立或選取資源群組**
    - **地區**：選取以下位置之一：
        * 美國東部
        * 法國中部
        * 南韓中部
        * 西歐
        * 美國西部

1. 選取 [建立]**** 並檢閱您的設定。 等候設定程序完成。

    >**注意**：如果您收到權限錯誤，請選取 [修復]**** 按鈕新增適當的權限以繼續。

1. 建立專案後，您將預設進入 Azure AI Foundry 入口網站中的代理程式遊樂場，它看起來類似於下圖：

    ![Azure AI Foundry 入口網站中 Azure AI 專案詳細資料的螢幕螢幕擷取畫面。](./media/ai-foundry-project-2.png)

1. 在畫面的左側功能表上，選取 [遊樂場]****。

## 探索 Azure AI Foundry 聊天遊樂場中的生成式 AI

1. 在 Azure AI Foundry 的遊樂場頁面中，選取 [試用聊天遊樂場]****。 聊天遊樂場是一種使用者介面，可讓您嘗試使用不同的生成式 AI 模型建置聊天應用程式。  

1. 若要使用聊天遊樂場，您必須將它與已部署的模型產生關聯。 在聊天遊樂場中，選取 [建立部署]****。 搜尋並選取 [GPT-4]****。 

1. 在 [部署模型]** 視窗中，保留預設命名和選取項目，然後選取 [部署]****。 部署模型可能需要一些時間。 您可以選取 [我的資產]** 下方左側功能表中的 [模型和端點]** 來檢查部署的狀態。
1. 在聊天遊樂場中，您可以在 [部署]** 選取功能表中出現已部署的模型時使用它。 請確定已選取您部署的模型。 重要的是，在對*設定*進行任何變更之後，您必須選取 [套用變更]****。 

1. 不妨考慮採用下列方式，改善生成式 AI 助理提供的回覆：
    - 從您希望助理完成的特定目標開始
    - 根據先前的提示和回覆逐一查看，縮小結果範圍
    - 提供來源，以特定資訊範圍為回覆基礎
    - 新增內容，將回覆的適當性和相關性最大化
    - 為回覆設定明確的期望

1. 讓我們嘗試使用具有特定目標的提示生成回覆。 在聊天方塊中，輸入下列提示：

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. 檢閱回應。 **注意**：請注意，您收到的特定回覆可能會因生成式 AI 的性質而有所不同。
 
1. 讓我們試試另外一個提示。 輸入下列內容：

    ```prompt
    Where's a good location in Paris to stay? 
    ```

1. 檢閱回覆，其中應該會提供一些巴黎住宿。

1. 讓我們根據先前的提示和回覆逐一查看，縮小結果範圍。 輸入下列提示：
    
    ```prompt
    Can you give me more information about dining options near the first location?
    ``` 

1. 檢閱回覆，其中應該會提供先前回覆中的位置附近的餐飲選項。 

1. 現在，讓我們提供來源，以特定資訊範圍為回覆基礎。 輸入下列內容： 
    
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
