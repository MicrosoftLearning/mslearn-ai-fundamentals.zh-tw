---
lab:
  title: 搭配 Language Studio 使用問題解答
---

# 搭配 Language Studio 使用問答模型

在此練習中，您將使用 Language Studio 來建立和訓練客戶服務 Bot 將使用的問答 知識庫。 知識庫 的內容將來自瑪吉旅遊網站的現有常見問題頁面，這是一家虛構的旅行社。 接著，您將使用 Language Studio 來查看客戶使用時的運作方式。

實作 Bot 時，第一個步驟是建立問答組 知識庫。 這與內建的自然語言處理功能搭配使用，讓 Bot 可以解譯問題，並尋找最適合使用者的答案。

Azure AI 語言包含*問題解答*功能，您將用來建立 知識庫。 您可以手動輸入問答組，或從現有的檔或網頁建立知識庫。 Margie 的旅遊想要使用其現有的常見問題檔。

語言服務的問答功能可讓您藉由輸入問答組，或從現有的檔或網頁，快速建立 知識庫。 然後，它可以使用一些內建的自然語言處理功能來解譯問題並尋找適當的答案。

## 建立 *語言* 資源

若要使用問題解答，您需要 **語言** 資源。

1. 在另一個瀏覽器索引標籤中，開啟 at [https://portal.azure.com](https://portal.azure.com?azure-portal=true)的 Azure 入口網站，使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

1. **按兩下 &#65291;建立資源**按鈕並搜尋*語言服務*。 選取 **[建立**** 語言服務**方案]。 系統會帶您前往頁面以 **選取其他功能**。 使用下列設定：
    - **選取 [其他功能**]：
        - **預設功能**：保留預設功能**。
        - **自訂功能**：選取自訂問題解答**。
     - 選取 [ **繼續] 以建立已啟用自定義問題解答的資源**
    ![建立語言服務資源。](media/create-a-bot/create-language-service-resource.png)

1. 在 [建立語言]**** 頁面上，指定下列設定：
    - **專案詳細資料**
        - **訂用帳戶**：*您的 Azure 訂用帳戶*。
        - **資源群組**：*選取現有資源群組或建立新的資源群組*。
    - **執行個體詳細資料**
        - **區域**： *選取區域*      
        - **名稱**：語言資源的唯一名稱**。
        - **定價層**：S (每分鐘 1K 次呼叫)
    - **自訂問題解答**
        - **Azure 搜尋服務位置**：任何可用的位置**。
        - **Azure 搜尋服務定價層**：免費 F （3 個索引） - （*如果無法使用此層，請選取 [基本*]
    - **負責任的 AI 通知**
        - **核取此方塊表示我確認已檢閱並認同「負責任 AI 注意事項」中的條款。**：選取**。

1. 選取 [ **檢閱並建立]** ，然後選取 [ **建立**]。 等候語言服務的部署，其將支援您的自訂問題解答知識庫。

    > **注意** 如果您已布建免費層 **Azure 認知搜尋** 資源，您的配額可能無法建立另一個資源。 在此情況下，請選取 [免費 F]**** 以外的層。

## 建立新專案

1. 在新的瀏覽器索引標籤中，開啟位於 [https://language.azure.com](https://language.azure.com?azure-portal=true) 的 Language Studio 入口網站，然後使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。
1. 若系統提示您選擇語言資源，請選取下列設定：
    - **Azure 目錄**： *包含訂用帳戶*的 Azure 目錄。
    - **Azure 訂用帳戶**： *您的 Azure 訂用帳戶*。
    - **語言資源**： *您先前*建立的語言資源。

    如果您***未***收到選擇語言資源的提示，可能是因為您的訂用帳戶中有多個語言資源；在此情況下：
    1. 在頁面頂端的列上，選取 **[設定 （&#9881;）** 。      
    1. 在 [設定]**** 分頁上，檢視 [資源]**** 索引標籤。
    1. 選取您剛才建立的語言資源，然後選取 [ **切換資源**]。
    1. 在頁面頂端，選取 **[Language Studio] 以返回 Language Studio** 首頁。

1. 在 Language Studio 入口網站頂端的 [新建]**** 功能表中，選取 [自訂問題解答]****。

    ![自訂問題解答](media/create-a-bot/create-custom-question-answering.png)

1. 在 [選擇資源 *your resource* 的語言設定]**** 頁面上，選取 [當我在此資源中建立專案時，我想選取語言]****，然後按 [下一步]****。
  ![我想選取語言](media/create-a-bot/create-project.png)

1. 在 [輸入基本資訊]**** 頁面上，輸入下列詳細資料，然後按 [下一步]****：
    - **語言資源**：*選擇您的語言資源*。  
    - **Azure 搜尋服務資源**：*選擇您的 Azure 搜尋資源*。
    - **名稱**：`MargiesTravel`
    - **描述**：`A simple knowledge base`
    - **來源語言**：英文
    - **未傳**回答案時的預設答案： `No answer found`
1. 在 [ **檢閱和完成** ] 頁面上，選取 [ **建立專案**]。
1. 系統將帶您前往 [管理來源]**** 頁面。 選取 **&#65291;新增來源** ，然後選取 **[URL**]。
1. 在 [ **新增 URL] 方塊** 中，選取 **[+ 新增 URL**]。 輸入下列資料，然後選取 [全部新增]****：
    - **網址名稱**： `MargiesKB`
    - **URL**：`https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/natural-language/margies_faq.docx`
    - **分類檔案結構**：自動偵測**
1. 選取 [ **全部新增]。**  

 ![新增 URL](media/create-a-bot/add-url.png)

## 編輯知識庫

您的知識庫是以常見問題集文件和一些預先定義的回應為基礎。 您可以新增自訂的問答配對來補充這些配對內容。

1. 展開左側面板，然後選取 [**編輯 知識庫**]。 然後選取 **+** 以新增問題組。
1. 在 [**新增問題答案組**] 對話方塊的 **[問題**類型`Hello`] 和 [答案**類型`Hi`] 中**，選取 [**完成**]。
1. 展開 **[替代問題]，** 然後選取 **[+ 新增替代問題**]。 然後輸入 `Hiya`作為 「Hello」 的替代片語。
1. 在 [問題答案組 **] 窗格頂端**，選取 [**儲存**] 以儲存您的 知識庫。

## 定型和測試知識庫

現在您已擁有知識庫，您可以進行測試。

1. 在 [問題答案組 **] 窗格頂端**，選取 [**測試**] 以測試您的 知識庫。
1. 在測試窗格底部輸入訊息 `Hi`。 應該傳回回應 *Hi* 。
1. 在測試窗格底部輸入訊息 `I want to book a flight`。 應該會從常見問題集中傳回適當的回應。

    > **注意** 回應包含「簡短答案」** 以及更詳細的「答案段落」**- 答案段落顯示常見問題集文件中最相符問題的全文，而簡短答案是從段落中巧妙擷取。 您可以使用測試窗格頂端的 [顯示簡短答案]**** 核取方塊，來控制簡短答案是否來自該回應。

1. 嘗試其他問題，例如 `How can I cancel a reservation?`
1. 當您完成測試 知識庫 時，請選取 [**測試**] 以關閉測試窗格。

## 為知識庫建立 Bot

知識庫提供用戶端應用程式可用來透過某種使用者介面回答問題的後端服務。 通常，這些用戶端應用程式是 Bot。 若要讓知識庫可供 Bot 使用，您必須將其發佈為可透過 HTTP 存取的服務。 然後，您可以使用 Azure Bot Service 來建立和裝載使用知識庫來回答使用者問題的 Bot。

1. 在左側面板中，選取 [**部署 知識庫**]。
1. 在頁面頂端，選取 [ **部署**]。 對話框會詢問您是否要部署專案。 選取**部署**。

 ![部署 知識庫。](media/create-a-bot/deploy-knowledge-base.png)

1. 部署服務之後，請選取 **[建立 Bot**]。 這將在新的瀏覽器索引標籤中開啟 Azure 入口網站，以便您可以在 Azure 訂用帳戶中建立 Web 應用程式 Bot。
1. 在 Azure 入口網站 中，建立 **Web 應用程式 Bot**。 （您可能會看到警告訊息來檢查範本的來源是否值得信任。 您不需要針對該訊息採取任何動作。更新下列設定以繼續：

    - **專案詳細資料**
        - **訂用帳戶**：您的 Azure 訂用帳戶**
        - **資源群組**：*包含您語言資源的資源群組*
    - [執行個體詳細資料]****
        - **資源群組位置**： *與您的語言服務*相同的位置。
    - **Azure Bot**
        - **Bot 句柄**： *Bot* 的唯一名稱（*預先填入*）
    - **選擇您的定價層**
        - **定價層**：免費 （F0） （您可能需要選取 *[變更方案*]
    - **Microsoft 應用程式識別碼**
        - **建立類型**： *選取 **[建立新的使用者指派的受控識別]*** 

5. 選取 **[下一步** ] 以繼續更新設定。 
    - **應用程式服務**
        - **應用程式名稱**：*與自動附加 **.azurewebsites.net** 的 **Bot 控制碼**相同*
        - **SDK 語言**：*選擇 C# 或 Node.js*
    - **App Service 方案**
        - **建立類型**： *選取 **[建立新的 App Service 方案]***
    - **應用程式設定**
        - **語言資源金鑰**： *您必須複製語言資源金鑰，並將其貼到這裡*：
            - 開啟另一個瀏覽器索引標籤，然後流覽至 位於 [https://portal.azure.com](https://portal.azure.com?azure-portal=true)的 Azure 入口網站。
            - 流覽至您的語言服務資源。
            - 在 [ **金鑰和端點]** 頁面上，複製其中一個金鑰
            - 將它貼到這裡。
        - **語言專案名稱**：MargiesTravel
        - **語言服務端點主機名**： *預先填入您的語言服務端點*
    - **語言服務詳細數據**
        - **訂用帳戶標識碼**： *預先填入您的訂用帳戶標識碼*
        - **資源組名**： *預先填入您的資源組名*
        - **帳戶名稱**： *預先填入您的資源名稱*

1. 選取 **建立**。 然後等待建立 Bot（右上方的通知圖示看起來像鈴鐺，會在您等候時產生動畫效果）。 然後在部署已完成的通知中，選取 **[移至資源** ] （或者，在首頁上按兩下 **[資源群組]，開啟您建立 Bot 的資源群組**，然後選取 **Azure Bot** 資源。
1. 在 Bot 的左側窗格中尋找 **設定，選取 **[在 網路聊天**** 中測試]，並等候 Bot 顯示 Hello 和 Welcome** 訊息**（可能需要幾秒鐘才能初始化）。
1. 使用測試聊天介面，確保您的 Bot 如預期從您的知識庫回答問題。 例如，嘗試提交 `I need to cancel my hotel`。

使用 Bot 來試驗。 您可能會發現它可以非常準確地回答常見問題集的問題，但無法解譯尚未定型的問題。 您一律可以使用 Language Studio 來編輯知識庫以改善它，並重新發佈它。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. [開啟 Azure 入口網站]( https://portal.azure.com)，然後選取包含您所建立資源的資源群組。 
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

- 若要深入了解問題解答服務，請檢視[文件](https://docs.microsoft.com/azure/cognitive-services/language-service/question-answering/overview)。
- 若要深入了解 Microsoft Bot Service，請檢視 [Azure Bot Service 頁面](https://azure.microsoft.com/services/bot-service/)。
