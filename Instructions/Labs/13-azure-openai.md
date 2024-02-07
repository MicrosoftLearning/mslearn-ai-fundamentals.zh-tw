---
lab:
  title: 探索 Azure OpenAI 服務
---

# 探索 Azure OpenAI

Azure OpenAI 服務將 OpenAI 開發的產生式 AI 模型帶入 Azure 平臺，讓您開發功能強大的 AI 解決方案，以受益於 Azure 雲端平臺所提供的服務的安全性、延展性和整合。

在此練習中，您將探索 Azure OpenAI 服務，並使用它來部署和實驗產生的 AI 模型。

此練習大約需要 **25** 分鐘。

## 在您開始使用 Intune 之前

您將需要已核准的 Azure 訂用帳戶，以存取文字和程式代碼模型的 Azure OpenAI 服務，以及 DALL-E 映射產生模型。

- 若要註冊免費的 Azure 訂用帳戶，請造訪 [https://azure.microsoft.com/free](https://azure.microsoft.com/free)。
- 若要要求存取 Azure OpenAI 服務，請造訪 [https://aka.ms/oaiapply](https://aka.ms/oaiapply)。

## 布建 Azure OpenAI 資源

您必須先在 Azure 訂用帳戶中布建 Azure OpenAI 資源，才能使用 Azure OpenAI 模型。

1. 登入 [Azure 入口網站](https://portal.azure.com)。
2. 使用下列設定建立 **Azure OpenAI** 資源：
    - **訂**用帳戶： *已核准存取 Azure OpenAI 服務的 Azure 訂用帳戶。*
    - **資源群組：*選擇現有的資源群組**，或以您選擇的名稱建立新的資源群組。*
    - **區域**：選擇任何可用的區域**。
    - **名稱**： *您選擇的唯一名稱。*
    - **定價層**:標準 S0
3. 等候部署完成。 然後移至 Azure 入口網站 中已部署的 Azure OpenAI 資源。

## 探索 Azure OpenAI Studio

您可以使用 Azure OpenAI Studio 在 Azure OpenAI 服務中部署、管理及探索模型。

1. 在 Azure OpenAI 資源的 [**概觀] 頁面上，使用 **[探索**] 按鈕在新瀏覽器索引標籤中開啟 Azure OpenAI Studio。或者，直接流覽至 [Azure OpenAI Studio](https://oai.azure.com/)**。

    當您第一次開啟 Azure OpenAI Studio 時，看起來應該如下所示：

    ![Azure OpenAI Studio 的螢幕快照。](./media/generative-ai/ai-studio.png)

1. 檢視左側窗格中可用的頁面。 您一律可以返回頂端的首頁。 此外，OpenAI Studio 提供多個頁面，您可以在其中：
    - 在遊樂場*中*實驗模型。
    - 管理模型部署和數據。

## 部署用於產生語言的模型

若要實驗自然語言產生，您必須先部署模型。

1. 在 [ **模型]** 頁面上，檢視 Azure OpenAI 服務實例中的可用模型。
1. 選取 [可**部署狀態] **為 [是**] 的任何 **gpt-35-turbo** 模型**，然後選取 [**部署**]：

    ![Azure AI Studio 中 [模型] 頁面的螢幕快照。](./media/generative-ai/deploy-model.png)

1. 使用下列設定建立新的部署：
    - **模型**：gpt-35-turbo
    - **模型版本**：自動更新為預設值
    - **部署名稱**：*模型部署的唯一名稱*

## *使用 Chat* 遊樂場來處理模型

既然您已部署模型，您可以在聊天*遊樂場中*使用它，從您在聊天介面中提交的提示產生自然語言輸出。

1. 在 [Azure OpenAI Studio](https://oai.azure.com/) 中，流覽至左窗格中的 **[聊天** 遊樂場]。

    *Chat* 遊樂場提供聊天機器人介面，您可以與其部署的模型互動，如下所示：

    ![Azure OpenAI Studio 中聊天遊樂場的螢幕快照。](./media/generative-ai/chat-playground.png)

1. 在 [ **組態** ] 窗格中，確定已選取您的模型部署。
1. 在 [ **助理設定** ] 窗格中，選取 **[默認** 系統訊息] 範本，然後檢視此範本所建立的系統訊息。 系統訊息會定義模型在聊天會話中的運作方式。
1. 在 [ **聊天會話] 區** 段中，輸入下列使用者訊息。

    ```
   What is generative AI?
    ```

1. 觀察模型所傳回的輸出，其應該提供產生 AI 的定義。
1. 輸入下列使用者訊息作為後續問題：

    ```
   What are three benefits it provides?
    ```

1. 檢閱輸出，指出聊天會話已持續追蹤先前的輸入和回應以提供內容（因此它會正確地將「它」解譯為參考「產生式 AI」），並根據所要求的內容提供適當的回應（它應該傳回產生式 AI 的三個優點）。

## *使用 DALL-E* 遊樂場來產生影像

除了語言產生模型之外，Azure OpenAI 服務還支援用於產生影像的 DALL-E 2 模型。

> **注意**：您必須已套用並接收 Azure OpenAI 服務存取應用程式中 DALL-E 功能的存取權，才能完成本練習的這一節。

1. 在 [Azure OpenAI Studio](https://oai.azure.com/) 中，流覽至左窗格中的 **DALL-E** 遊樂場。
1. 輸入下列提示：

    ```
    A robot eating spaghetti
    ```

1. 選取 **[產生** ] 並檢視結果，其應該會根據您在提示中提供的描述來組成影像，如下所示：

    ![Azure OpenAI Studio 中 DALL-E playgrund 的螢幕快照。](./media/generative-ai/dall-e-playground.png)

1. 修改提示以產生第二個影像：

    ```
    A robot eating spaghetti in the style of Rembrandt
    ```
1. 確認新的映像符合提示的需求，如下所示：

    ![Azure OpenAI Studio 中 DALL-E 產生的映射螢幕快照。](./media/generative-ai/dall-e-results.png)

## 清理

當您完成 Azure OpenAI 資源時，請記得刪除 Azure 入口網站[ 中的](https://portal.azure.com/?azure-portal=true)部署或整個資源。
