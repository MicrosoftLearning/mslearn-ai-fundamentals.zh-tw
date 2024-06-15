---
lab:
  title: 使用 Language Studio 分析文字
---

# 使用 Language Studio 分析文字

在本練習中，您將藉由分析一些範例旅館評論來探索 Azure AI 語言的功能。 您將使用 Language Studio 來了解評論大多是正面的還是負面的。

自然語言處理 (NLP) 是 AI 的一個分支，可處理書面和口說的語言。 您可以使用 NLP 來建置從文字或語音中擷取語意的解決方案，或以自然語言制定有意義的回應的解決方案。

例如，假設虛構的旅行社 Margie's Travel 鼓勵客戶提交旅館住宿的評論。 您可以使用語言服務來識別關鍵片語、判斷哪些評論是正面的，哪些是負面的，或分析評論文字中是否提及已知的實體 (例如位置或人物)。

Azure AI 語言服務包含文字分析和 NLP 功能。 這些包括文字中關鍵片語的識別，以及根據情感的文字分類。

## 建立*語言*資源

您可以使用許多 Azure AI 語言功能搭配**語言**或 **Azure AI 服務**資源。 有一些執行個體只能使用語言資源。 針對下列練習，我們將使用**語言**資源。 如果您尚未建立此資源，請在 Azure 訂用帳戶中建立 [語言]**** 資源。

1. 在另一個瀏覽器索引標籤中，開啟位於 [https://portal.azure.com](https://portal.azure.com?azure-portal=true) 的 Azure 入口網站，並使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

1. 按一下 [&#65291;建立資源]**** 按鈕並搜尋*語言服務*。 選取 [建立]**** **語言服務**方案。 系統會帶您到一個頁面，以**選取其他功能**。 保留預設選取項目，然後按一下 [繼續]**** 以建立您的資源。 

1. 在 [建立語言]**** 頁面上，使用下列設定進行設定：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **區域**：*選取最接近的地理區域。如果在美國東部，請使用 "East US 2"*。
    - **名稱**：*輸入唯一名稱*。
    - **定價層**：*如果無法使用免費 F0，則為免費 F0 或 S*
    - **核取此方塊即表示我確認我已閱讀並了解下列所有條款**：*已選取*。

1. 選取 [檢閱 + 建立]****，然後再選取 [建立]**** 並等待部署完成。

## 在 Azure AI Language Studio 中設定您的資源

1. 在另一個瀏覽器索引標籤中，開啟 [Language Studio]**** (位於 [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true))，然後登入。

1. 當出現 [選取 Azure 資源]**** 的提示時，請進行下列設定：
    - **Azure 目錄**：*預設目錄 (您正在使用的目錄)*
    - **Azure 訂用帳戶**：*選取您正在使用的訂用帳戶*
    - **資源類型**：語言
    - **資源名稱**：*選取您剛才建立的語言服務資源*

然後，選取**完成**。

> **重要**：自 2023 年 7 月起，Azure AI 服務包含過去稱為認知服務和 Azure 應用 AI 服務的所有項目。 有些使用者介面仍在將其參考從 `Cognitive Services` 更新為 `Azure AI services`。 這兩個名稱會參考相同類型的資源。

> **注意**：如果您***未***收到選擇語言資源的提示，可能是因為您的訂用帳戶中有多個語言資源；在此情況下：
> 1. 在頁面頂端的列上，選取 [設定 (&#9881;)]****。 
> 1. 在 [設定]**** 分頁上，檢視 [資源]**** 索引標籤。
> 1. 選取您剛才建立的資源，然後選取 [切換資源]****。 確定受控識別**已啟用**。
> ![啟用語言資源。](media/analyze-text-language-service/language-resource-enabled.png)
> 1. 在頁面頂端，選取 [Language Studio]**** 以回到 Language Studio 首頁。

## 在 Language Studio 中分析評論

1. 在網頁瀏覽器中，瀏覽至 [Language Studio]**** (位於 [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true))。

1. 在 [歡迎使用 Language Studio]**** 登陸頁面上，選取 [分類文字]**** 索引標籤，然後選取 [分析情感和我的意見]**** 磚。

1. 在 [選取文字語言]** 下，選取 [英文]****。

1. 在 [選取您的 Azure 資源]** 下，選取您的資源。

1. 在 [輸入您自己的文字、上傳檔案，或使用我們的其中一個範例文字]** 中，複製並貼上下列評論：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 核取該方塊以確認示範會產生使用量且可能會產生費用，然後選取 [執行]****。

1. 檢閱輸出。 請注意，會對*文件* (以及每個*句子*) 進行情感分析。 選取 [句子 1]**** 以顯示該句子的情感分析。 

請注意，有一個整體情緒，後面接著三個類別旁邊的分數：*正分數*、*中性分數*、*負分數*。 在每個類別中，提供 0 到 1 之間的分數。 這些信賴度分數表示所提供的文字是特定情緒的可能性有多大。 

再次選取 [句子 1]**** 以關閉。

1. 向上捲動以選取 [清除文字輸入框]****，然後複製並貼上下列評論：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```
    
    
1. 選取**執行**。 檢閱輸出並檢閱情緒和信賴等級。

1. 再次選取 [清除文字輸入框]****，然後複製並貼上下列評論：

    >很吵雜而且房間很小。The Lombard Hotel, San Francisco, USA 9/5/2018。旅館位於 Lombard 街道，這是一條非常忙碌的六線街道，就在金門大橋旁。 交通流量從清晨到深夜，特別是週末。 如果房間隔音好一點，噪音就不會那麼糟。 我必須把棉球放在我的耳朵才能睡覺，我累到隔天都無法好好享受城市。 房間很小。 我選了這個房間，因為有兩張加大雙人床，但房間的空間要放這兩張床不太夠。 四人的家庭在房間中就太窄了。 結論是房間很乾淨，而且他們已努力更新了。 旅館位於海港區，有許多好地方可用餐，且距離要塞公園是步行可到的距離。 可能是適合晚睡的年青人或預算有限成人的旅館

1. 選取 [執行]**** 並檢閱情緒與信賴等級。 查看文字，並將文字與服務傳回的情感分析進行比較。

在本練習中，您已使用 Language Studio 建立新的語言資源或使用現有的語言資源。 在嘗試情緒和意見挖掘服務之前，您已在 [設定] 中啟用了該資源。 然後，您使用三段文字測試了該服務。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 **Azure 入口網站** (位於 [https://portal.azure.com](https://portal.azure.com))，然後選取包含您所建立資源的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 以確認。 接著即會刪除該資源。

## 深入了解

若要深入了解您可以使用此服務完成的動作，請參閱[語言服務頁面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
