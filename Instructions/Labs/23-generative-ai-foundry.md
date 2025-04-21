---
lab:
  title: 探索 Azure AI Foundry 入口網站中的生成式 AI
---

# 探索 Azure AI Foundry 入口網站中的生成式 AI

生成式 AI 描述 AI 中建立內容的功能類別。 人員通常會與聊天應用程式內建的生成式 AI 互動。 在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，試用生成式 AI。 

## 在 Azure AI Foundry 入口網站中建立專案

1. 在瀏覽器索引標籤中，瀏覽至 [Azure AI Foundry][](https://ai.azure.com?azure-portal=true)。

1. 使用您的帳戶登入。 

1. 在 Azure AI Foundry 入口網站的首頁中，選取 [建立專案]****。 在 Azure AI Foundry 中，專案是可協助您組織工作的容器。  

    ![Azure AI Foundry 首頁的螢幕擷取畫面，其中已選取 [建立專案]。](./media/azure-ai-foundry-home-page.png)

1. 在 [建立專案]** 窗格中，您會看到產生的專案名稱，您可以保留現有名稱。 視您過去是否已建立中樞而定，您將會看到要建立的*新* Azure 資源清單或現有中樞的下拉式清單。 如果您看到現有中樞的下拉式清單，請選取 [建立新中樞]**，為您的中樞建立唯一的名稱，然後選取 [下一步]**。  
 
    ![[建立專案] 窗格的螢幕擷取畫面，其中包含中樞和專案的自動產生名稱。](./media/azure-ai-foundry-create-project.png)

> **重要**：您需要在特定位置佈建 Azure AI 服務資源，才能完成實驗的其餘部分。

1. 在相同的 [建立專案]** 窗格中，選取 [自訂]****，然後選取下列其中一個**位置**：美國東部、法國中部、韓國中部、西歐或美國西部，以完成實驗的其餘部分。 然後選取 [建立]****。 

1. 記下所建立的資源： 
- Azure AI 服務
- Azure AI 中樞
- Azure AI 專案
- 儲存體帳戶
- 金鑰保存庫
- 資源群組  
 
1. 建立資源之後，系統會將您帶到專案的 [概觀]** 頁面。 在畫面的左側功能表上，選取 [遊樂場]****。
 
    ![專案畫面上左側功能表的螢幕擷取畫面，其中已選取 [AI 服務]。](./media/azure-ai-foundry-playgrounds.png)  

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