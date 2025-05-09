---
lab:
  title: 探索 Azure AI Foundry 中的內容安全
---

# 探索 Azure AI Foundry 中的內容安全

Azure AI 服務可協助使用者使用現成、預先建置且可自訂的 API 與模型來建立 AI 應用程式。 在此練習中，您將查看其中一項服務 Azure AI 內容安全，讓您能夠調節文字和影像內容。 在 Microsoft 用來建立智慧型應用程式的 Azure AI Foundry 入口網站中，您將使用 Azure AI 內容安全來分類文字並指派嚴重性分數。 

> **注意** 本練習的目標是要大致瞭解 Azure AI 服務的佈建和使用方式。 內容安全僅作為範例，但並不要求您透過此練習獲得有關內容安全的全面知識！

## 在 Azure AI Foundry 入口網站中建立專案

1. 在瀏覽器索引標籤中，瀏覽至 [Azure AI Foundry 入口網站][](https://ai.azure.com?azure-portal=true)。

2. 使用您的帳戶登入。 

3. 在 Azure AI Foundry 入口網站的首頁中，選取 [建立專案]****。 在 Azure AI Foundry 中，專案是可協助您組織工作的容器。  

    ![Azure AI Foundry 首頁的螢幕擷取畫面，其中已選取 [建立專案]。](./media/azure-ai-foundry-home-page.png)

4. 在 [建立專案]** 窗格中，您會看到產生的專案名稱，您可以保留現有名稱。 視您過去是否已建立中樞而定，您將會看到要建立的*新* Azure 資源清單或現有中樞的下拉式清單。 如果您看到現有中樞的下拉式清單，請選取 [建立新中樞]**，為您的中樞建立唯一的名稱，然後選取 [下一步]**。  
 
    ![[建立專案] 窗格的螢幕擷取畫面，其中包含中樞和專案的自動產生名稱。](./media/azure-ai-foundry-create-project.png)

> **重要**：您需要在特定位置佈建 Azure AI 服務資源，才能完成實驗的其餘部分。

5. 在相同的 [建立專案]** 窗格中，選取 [自訂]****，然後選取下列其中一個**位置**：美國東部、法國中部、韓國中部、西歐或美國西部，以完成實驗的其餘部分。 然後選取 [建立]****。 

1. 記下所建立的資源： 
- Azure AI 服務
- Azure AI 中樞
- Azure AI 專案
- 儲存體帳戶
- 金鑰保存庫
- 資源群組  

6. 建立資源之後，系統會將您帶到專案的 [概觀]** 頁面。 

7. 若要使用內容安全，您必須對 *Azure AI 中樞*資源進行權限更新。 若要這樣做，請開啟 [Azure 入口網站](https://portal.azure.com?portal-azure=true)，並使用您用來建立 AI Foundry 資源的相同訂用帳戶登入。  

8. 在 Azure 入口網站中，使用頁面頂端的搜尋列來尋找並選取 [Azure AI Foundry]****。 在資源頁面中，選取您剛才建立且*類型***為 Azure AI 中樞**的資源。  

9. 在 Azure 入口網站的左側窗格中，選取 [存取控制 (IAM)]****。 然後在開啟的窗格中，選取加號旁的 [新增]****，然後選取 [新增角色指派]****。 

![在 [存取控制] 窗格中選取 [新增角色指派] 位置的螢幕擷取畫面。](./media/content-safety/access-control-step-one.png)

10. 在角色清單中搜尋 [Azure AI 安全評估工具]****，然後加以選取。 然後選取**下一步**。 

11. 使用下列設定自行指派給角色： 
    - **存取權指派對象為**：選取 [使用者、群組或服務主體]**
    - **成員**：按一下 [選取成員]**
        - 在開啟的 [選取成員]** 窗格中，尋找您的名稱。 按下您名稱旁的加號圖示。 然後按一下 [選取]****。
    - **描述**：*保留空白*

12. 選取 [檢閱並指派]****，然後再次選取 [檢閱並指派]**** 以新增角色指派。    

13. 在瀏覽器中，返回 [Azure AI Foundry 入口網站](https://ai.azure.com?azure-portal=true)。 選取您的專案 

14. 在畫面的左側功能表上，選取 [AI 服務]****。
 
    ![專案畫面上左側功能表的螢幕擷取畫面，其中已選取 [AI 服務]。](./media/azure-ai-foundry-ai-services.png)  

15. 在 [AI 服務]** 頁面上，選取 [視覺 + 文件]** 圖格，以試用 Azure AI 視覺和文件功能。
    
    ![內容安全圖格的螢幕擷取畫面。](./media/content-safety-tile.png)

## 在 Azure AI Foundry 入口網站中使用內容安全試用文字調節 

1. 在 [內容安全性]** 頁面的 [篩選文字內容]** 下，選取 [調節文字內容]****。

2. 在 [調節文字內容]** 頁面的 [試用]** 標題底下，選取您剛從下拉式功能表中建立的 Azure AI 服務資源。   

3. 在 [執行簡單測試]** 底下，選取 [安全內容]**** 圖格。 請注意，文字會顯示於下方方塊。 

4. 按一下 [執行測試]****。 執行測試會呼叫 Content Safety Service 的深度學習模型。 深度學習模型已經過定型，可辨識不安全內容。

5. 在 [結果]** 面板檢查結果。 有四種嚴重性層級，從安全到高，以及四種有害內容類型。 內容安全 AI 服務是否認為此範例可接受？ 請務必注意的是，結果在信賴區間內。 訓練良好的模型 (例如 Azure AI 的現成模型之一) 所傳回的結果具高度機率符合人類標記結果。 每次執行測試時，您都會再次呼叫模型。 

6. 現在請嘗試另一範例。 選取 [拼字錯誤的暴力內容] 底下的文字。 檢查內容是否顯示於下方方塊。

7. 按一下 [執行測試]****，然後在 [結果] 面板再次檢查結果。 

您可針對提供的所有範例執行測試，然後檢查結果。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取您建立的資源所屬的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

此練習僅示範內容安全服務的部分功能。 若要深入了解這項服務的功用，請參閱[內容安全頁面](https://learn.microsoft.com/azure/ai-services/content-safety/overview)。