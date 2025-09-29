---
lab:
  title: 分析 Azure AI Foundry 入口網站中的文字
---

# 分析 Azure AI Foundry 入口網站中的文字

Azure AI 語言包含文字分析，具備實體辨識、關鍵片語擷取、摘要和情感分析等功能。 例如，假設虛構的旅行社 Margie's Travel 鼓勵客戶提交旅館住宿的評論。 您可以使用語言服務來擷取具名實體、識別關鍵片語、摘要文字等等。

在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中，使用 Azure AI 語言分析飯店評價。 

此練習大約需要 **20 分鐘**。

## 在 Azure AI Foundry 入口網站中建立專案

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時開啟的所有提示或快速啟動窗格，如有必要，使用左上角的 **Azure AI Foundry** 標誌瀏覽到首頁，首頁類似於下圖（若 [說明]**** 窗格已開啟，請將其關閉）：

    ![Azure AI Foundry 入口網站首頁的螢幕擷取畫面。](./media/ai-foundry-portal.png)

1. 捲動至頁面底部，然後選取 [探索 Azure AI 服務]**** 圖格。

    ![[探索 Azure AI 服務] 圖格的螢幕擷取畫面。](./media/ai-services.png)

1. 在 [Azure AI 服務] 頁面上，選取 [語言 + 翻譯工具]**** 圖格。

    ![[語言 + 翻譯工具] 圖格的螢幕擷取畫面。](./media/language-tile.png)

1. 在 [語言 + 翻譯工具]**** 頁面上，選取 [試用語言遊樂場]****。 然後在收到提示時，使用下列設定建立新專案：
    - **專案名稱**：*輸入專案的有效名稱。*
    - **進階設定**：
        - **訂用帳戶**：您的 Azure 訂用帳戶**
        - **資源群組**：建立或選取資源群組**
        - **區域**：*選取任何**建議的 AI Foundry** 區域*
        - **AI Foundry 或 Azure OpenAI** *建立具有有效名稱的新 Azure AI Foundry 資源*

1. 選取 **建立**。 等候您的專案建立。 這可能需要幾分鐘的時間。

1. 建立專案後，系統會將您帶到 [語言]**** 遊樂場 (若沒有，請在左側的工作窗格中選取 [遊樂場]****，然後從該處開啟語言遊樂場。)

    語言遊樂場是一種使用者介面，可讓您嘗試一些 Azure AI 語言功能。  

## 使用 Azure AI 語言分析文字

Azure AI 語言提供各種文字分析功能。

### 使用 Azure AI Foundry 入口網站中的 Azure AI 語言擷取具名實體

*具名實體*是描述具有專有名稱的人員、地點和物件的單字。 讓我們使用 Azure AI 語言的具名實體擷取功能來識別評價中的資訊類型。

1. 在 [語言遊樂場] 中，選取 [擷取資訊]****。 然後選取 [擷取具名實體]**** 圖格。 

1. 在 [範例]** 下方，輸入下列評論：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 選取**執行**。 檢閱輸出。

    ![語言遊樂場中擷取已命名實體介面的螢幕擷取畫面。](./media/entity-extraction.png)

    請注意，在 [詳細資料]** 區段中，擷取的實體如何隨附其他資訊，例如類型和信賴度分數。 信賴度分數代表識別的類型實際屬於該類別的可能性。

### 使用 Azure AI Foundry 入口網站中的 Azure AI 語言擷取關鍵片語

*關鍵片語*是文字中最重要的資訊片段。 讓我們使用 Azure AI 語言的關鍵片語擷取功能，從評價中提取重要資訊。

1. 在 [語言遊樂場] 中，選取 [擷取資訊]****。 然後選取 [擷取關鍵片語]**** 圖格。 

1. 在 [範例]** 下方，輸入下列評論：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. 選取**執行**。 檢閱輸出。

    ![語言遊樂場中擷取關鍵片語介面的螢幕擷取畫面。](./media/key-phrases.png)

    請注意*詳細資料*一節中擷取的不同片語。 這些片語應該對文字的意義造成最大貢獻。

### 使用 Azure AI Foundry 入口網站中的 Azure AI 語言摘要文字
 
讓我們看看 Azure AI 語言的摘要功能。

1. 在語言遊樂場中，選取 [摘要資訊]****，然後選取 [摘要文字]**** 圖格。

1. 在 [範例]** 下方，輸入下列評論：
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. 選取**執行**。 檢閱輸出。

    ![語言遊樂場中摘要文字介面的螢幕擷取畫面。](./media/summarize-text.png)

    請注意*詳細資料*中的*擷取摘要*會提供最突出句子的順位分數。

### 分析文字中的情感

情感分析常見於分析飯店評論等文字。

1. 在 [語言遊樂場] 中，選取 [分類文字]****。 然後選取 [分析情感]**** 圖格。

1. 在 [範例]** 下方，輸入下列評論：
    
    ```
    Disappointing Stay at The City Hotel
    The City Hotel, London
    9/5/2018
    My experience at The City Hotel in London was far from pleasant. The constant noise from nearby train tracks made it nearly impossible to sleep, with vibrations felt throughout the building. The rooms were outdated, dusty, and poorly maintained—dripping faucets, squeaky beds, and broken fixtures were just the beginning. Sound insulation was nonexistent, so every conversation from neighboring rooms was clearly audible. While the location near public transport was convenient and the staff were friendly, these positives couldn't make up for the overall discomfort and lack of value. I wouldn’t recommend this hotel to anyone seeking a restful or enjoyable stay.
    ```

1. 選取**執行**。 檢閱輸出。

    ![語言遊樂場中感情分析介面的螢幕擷取畫面。](./media/sentiment-analysis.png)

    請注意，分析會產生每個句子的整體情感分數和個別分數。

## 偵測語言並翻譯文字

Azure AI 語言可讓您偵測文字所用的語言。 此外，Azure AI 翻譯器可讓您輕鬆將文字從一種語言翻譯成另一種語言。

### 偵測語言種類

讓我們從偵測評論所使用的語言開始。

1. 在 [分類文字]**** 窗格中，選取 [偵測語言]**** 圖格。

1. 在 [範例]** 下方，輸入下列評論：
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. 選取**執行**。 檢閱輸出。

    ![語言遊樂場中偵測語言介面的螢幕擷取畫面。](./media/detect-language.png)

    請注意，已偵測該語言為法文。 

### 翻譯文字

現在讓我們將法文評論翻譯成英文。

1. 在頁面頂端，使用 [語言遊樂場]**** 網頁標題旁的 **&larr;** (返回) 連結來檢視所有可用的遊樂場。
1. 在遊樂場清單中，開啟 [翻譯工具遊樂場]****。
1. 在翻譯工具遊樂場中，選取 [文字翻譯]****。
1. 在 [設定]**** 窗格中，選取下列語言選項：
    - **翻譯自**：法文
    - **翻譯成**：英文
1. 在 [範例]** 下方，輸入法文評論：
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. 選取 [翻譯]****。 檢閱輸出。

    ![翻譯工具遊樂場中文字翻譯介面的螢幕擷取畫面。](./media/text-translation.png)

    請注意，法文評論已翻譯成英文。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 **Azure 入口網站** (位於 [https://portal.azure.com](https://portal.azure.com))，然後選取包含您所建立資源的資源群組。
1. 選取 [刪除資源群組]****，然後**輸入資源群組的名稱**以確認。 接著即會刪除該資源群組。

## 深入了解

若要深入了解您可以使用此服務完成的動作，請參閱[語言服務頁面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
