---
lab:
  title: 使用 Language Studio 分析文字
---

# 使用 Language Studio 分析文字

在此練習中，您將藉由分析一些範例旅館評論來探索 Azure AI 語言的功能。 您將使用 Language Studio 來了解評論大多是正面還是負面的。

自然語言處理 （NLP） 是 AI 的分支，可處理書面和口語語言。 您可以使用 NLP 來建置解決方案，以從文字或語音擷取語意意義，或以自然語言撰寫有意義的回應。

例如，假設虛構的旅行社 Margie 的 Travel 鼓勵客戶提交旅館住宿評論。 您可以使用語言服務來識別關鍵片語、判斷哪些評論是正面的，以及哪些是負面的，或分析評論文字中提及的已知實體，例如位置或人員。

Azure AI 語言服務包含文字分析和 NLP 功能。 其中包括文字中關鍵片語的識別，以及根據情感的文字分類。

## 建立 *語言* 資源

您可以使用許多 Azure AI 語言功能搭配 **Language** 或 **Azure AI 服務** 資源。 有一些實例只能使用語言資源。 針對下列練習，我們將使用 **語言** 資源。 如果您尚未這麼做，請在 Azure 訂用帳戶中建立 **語言** 資源。

1. 在另一個瀏覽器索引標籤中，開啟 位於[https://portal.azure.com](https://portal.azure.com?azure-portal=true)的 Azure 入口網站，使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

1. **按兩下 &#65291;建立資源**按鈕並搜尋*語言服務*。 選取 **[建立**** 語言服務**方案]。 系統會帶您前往頁面以 **選取其他功能**。 保留預設選取專案，然後按兩下 [ **繼續] 以建立您的資源**。 

1. 在 [建立語言]** 頁面上**，使用下列設定進行設定：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **區域**：美國東部。
    - **名稱**：*輸入唯一名稱*。
    - **定價層**： *免費 F0 或 S，如果無法使用免費 F0*
    - **勾選此方塊，我確認我已閱讀並瞭解下列**所有條款： *已選取*。

1. 選取 [**檢閱 + 建立**]，然後**** 等候部署完成。

## 在 Azure AI Language Studio 中設定您的資源

1. 在另一個瀏覽器索引標籤中，開啟 **[Language Studio** ] ， [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true) 然後登入。

1. 出現 [選取 Azure 資源 **] 提示**時，請進行下列設定：
    - **Azure 目錄**： *預設目錄，您正在使用的目錄*
    - **Azure 訂用帳戶**： *選取您所使用的訂用帳戶*
    - **資源類型**：語言
    - **資源名稱**： *選取您剛才建立的語言服務資源*

然後，選取**完成**。

> **重要**事項：自 2023 年 7 月起，Azure AI 服務包含先前稱為認知服務和 Azure 套用 AI 服務的所有專案。 某些使用者介面仍在將其參考從 `Cognitive Services` 更新為 `Azure AI services`。 這兩個名稱會參考相同類型的資源。

> **注意**：如果未****** 提示您選擇語言資源，可能是因為您的訂用帳戶中有多個語言資源;在此情況下：
> 1. 如果頁面位於頂端的列，請選擇 **[設定 （&#9881;）** 。 
> 1. 在 [設定]**** 分頁上，檢視 [資源]**** 索引標籤。
> 1. 選取您剛才建立的資源，然後選取 [ **切換資源**]。 確定受控識別已啟用****。
> ![啟用語言資源。](media/analyze-text-language-service/language-resource-enabled.png)
> 1. 在頁面頂端，選取 **[Language Studio] 以返回 Language Studio** 首頁。

## 在 Language Studio 中分析評論

1. 在網頁瀏覽器中，流覽至 **位於[](https://language.cognitive.azure.com?azure-portal=true)https://language.cognitive.azure.com的 Language Studio。**

1. 在 [ **歡迎使用 Language Studio** 登陸] 頁面上，選取 [ **分類文字** ] 索引標籤，然後選取 **[分析情感和我的意見** ] 圖格。

1. 在 [選取文字語言]* 底下*，選取 [**英文**]。

1. 在 [ *選取您的 Azure 資源*] 下，選取您的資源。

1. 在 *[輸入您自己的文字]底下，上傳檔案或使用我們的其中一個範例文字*，複製並貼上下列評論：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 核取方塊以確認示範會產生使用量，並可能會產生成本，然後選取 [ **執行**]。

1. 檢閱輸出。 請注意， *文件* 會針對情感以及每個 *句子*進行分析。 選取 **[句子 1** ] 以顯示該句子的情感分析。 

請注意，整體人氣後面接著三個類別的分數，正面分數 *、中性分數、**負分數**。 * 在每個類別中，提供 0 到 1 之間的分數。 這些信賴分數表示所提供文字在特定情感的可能性。 

再次選取 **[句子 1** ] 以關閉。

1. 向上捲動以選取 **[清除] 文字框**，然後複製並貼上下列檢閱：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```
    
    
1. 選取**執行**。 檢閱輸出，並檢閱情感和信賴等級。

1. 再次選取 **[清除] 文本框** ，然後複製並貼上下列評論：

    >很吵雜而且房間很小。The Lombard Hotel, San Francisco, USA 9/5/2018。旅館位於 Lombard 街道，這是一條非常忙碌的六線街道，就在金門大橋旁。 交通流量從清晨到深夜，特別是週末。 如果房間隔音好一點，噪音就不會那麼糟。 我必須把棉球放在我的耳朵才能睡覺，我累到隔天都無法好好享受城市。 房間很小。 我選了這個房間，因為有兩張加大雙人床，但房間的空間要放這兩張床不太夠。 四人的家庭在房間中就太窄了。 結論是房間很乾淨，而且他們已努力更新了。 旅館位於海港區，有許多好地方可用餐，且距離要塞公園是步行可到的距離。 可能是適合晚睡的年青人或預算有限成人的旅館

1. 選取 [ **執行** ]，並檢閱情感與信賴等級。 查看文字，並將文字與服務傳回的情感分析進行比較。

在此練習中，您已使用 Language Studio 來建立新的 Language 資源，或使用現有的 Language 資源。 您已在 設定 中啟用資源，再嘗試情感和意見採礦服務。 然後，您已使用三段文字測試服務。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. **** 開啟 Azure 入口網站，[https://portal.azure.com](https://portal.azure.com)然後選取包含您所建立資源的資源群組。
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

若要深入了解您可以使用此服務完成的動作，請參閱[語言服務頁面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
