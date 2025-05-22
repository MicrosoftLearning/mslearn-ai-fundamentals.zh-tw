---
lab:
  title: 分析 Azure AI Foundry 入口網站中的文字
---

# 分析 Azure AI Foundry 入口網站中的文字

自然語言處理 (NLP) 是 AI 的一個分支，可處理書面和口說的語言。 您可以使用 NLP 來建置從文字或語音中擷取語意的解決方案，或以自然語言制定有意義的回應的解決方案。

Azure AI 語言服務包含文字分析，其中包含實體辨識、關鍵片語擷取、摘要和情感分析等功能。 例如，假設虛構的旅行社 Margie's Travel 鼓勵客戶提交旅館住宿的評論。 您可以使用語言服務來擷取具名實體、識別關鍵片語、摘要文字等等。

在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，使用 Azure AI 語言分析飯店評價。 

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

1. 在 [遊樂場]** 頁面上，選取 [語言遊樂場]**** 圖格，試用一些 Azure AI 語言功能。

## 使用 Azure AI Foundry 入口網站中的 Azure AI 語言擷取具名實體

*具名實體*是描述具有專有名稱的人員、地點和物件的單字。 讓我們使用 Azure AI 語言的具名實體擷取功能來識別評價中的資訊類型。

1. 在 [語言遊樂場] 中，選取 [擷取資訊]****。 然後選取 [擷取具名實體]**** 圖格。 

1. 在 [範例]** 底下，複製並貼上下列檢閱：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 選取**執行**。 檢閱輸出。 請注意，在 [詳細資料]** 區段中，擷取的實體如何隨附其他資訊，例如類型和信賴度分數。 信賴度分數代表識別的類型實際屬於該類別的可能性。

## 使用 Azure AI Foundry 入口網站中的 Azure AI 語言擷取關鍵片語

*關鍵片語*是文字中最重要的資訊片段。 讓我們使用 Azure AI 語言的關鍵片語擷取功能，從評價中提取重要資訊。

1. 在 [語言遊樂場] 中，選取 [擷取資訊]****。 然後選取 [擷取關鍵片語]**** 圖格。 

1. 在 [範例]** 底下，複製並貼上下列檢閱：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. 選取**執行**。 檢閱輸出。 請注意*詳細資料*一節中擷取的不同片語。 這些片語應該對文字的意義造成最大貢獻。

## 使用 Azure AI Foundry 入口網站中的 Azure AI 語言摘要文字
 
1. 讓我們看看 Azure AI 語言的摘要功能。 在語言遊樂場中，選取 [摘要資訊]**，然後選取 [摘要文字]**** 圖格。

1. 在 [範例]** 底下，複製並貼上下列檢閱：
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. 選取**執行**。 檢閱輸出。 請注意*詳細資料*中的*擷取摘要*會提供最突出句子的順位分數。   

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 **Azure 入口網站** (位於 [https://portal.azure.com](https://portal.azure.com))，然後選取包含您所建立資源的資源群組。

1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

若要深入了解您可以使用此服務完成的動作，請參閱[語言服務頁面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
