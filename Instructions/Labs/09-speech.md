---
lab:
  title: 探索 Speech Studio
---

# 探索 Speech Studio

**Azure AI 語音**服務會將語音轉譯成文字，並將文字轉譯為可聽見的語音。 您可以使用 AI 語音來建立可轉譯會議筆記或從面試錄製產生文字的應用程式。

在此練習中，您將嘗試使用 Azure AI Speech Studio 的 Azure AI 語音功能。 

## 建立 *Azure AI 語音* 資源

您可以藉由建立**語音資源或 **Azure AI 服務資源，來使用語音**服務**。

在此練習中，您將建立 AI 語音資源，除非您已經有可以使用的資源。

1. 在另一個瀏覽器索引標籤中，開啟 [Azure AI Speech Studio](https://speech.microsoft.com/)，使用您的 Microsoft 帳戶登入。

1. 選取 [設定]，**然後**選取 **[建立資源]。** 使用下列設定對其進行設定：
    - **新資源**的名稱： *輸入唯一的名稱*。
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **區域**： *選取 [支持的區域](https://learn.microsoft.com/azure/ai-services/speech-service/regions)*。
    - **定價層**： *免費 FO（如果有的話，否則請選取 [標準 S0]。*
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
1. 選取 [建立資源]****。 等候資源建立完畢，然後選取 [ **使用資源**]。 [開始使用語音] 頁面隨即顯示。

## 在Speech Studio中探索語音轉換文字

1. 選取[](https://aka.ms/mslearn-speech-files)https://aka.ms/mslearn-speech-files**** 以下載**speech.zip。** 開啟  資料夾。 

1. 在 [開始使用語音] 頁面上，於 [語音轉換文字] 底下*尋找*即時語音轉換文字*。* 選取 [ **試用實時語音到文字**]。

    ![開始使用語音](media/recognize-synthesize-speech/try-out-speech-to-text.png)

1. 在 [選擇音訊檔案] 下 *，選取 [**瀏覽檔案**]，然後流覽至您儲存盤案*的資料夾。 選取 [WhatAICanDo.m4a **]，然後選取 ****[開啟**]。

    ![瀏覽檔案](media/recognize-synthesize-speech/browse-files-speech.png)

1. 語音服務會即時轉譯並顯示文字。 如果您的電腦上有音訊，您可以在正在轉譯文字時接聽錄製內容。
1. 檢閱輸出，其應該已成功辨識並轉譯音訊為文字。

    > **注意** 如果您收到錯誤訊息，請稍候幾分鐘再試一次。 第一次使用語音資源需要一點時間。

在此練習中，您已在Speech Studio中建立 AI 語音資源。 然後，您會使用即時語音轉換文字服務來轉譯音訊錄製。 您可以看到播放音訊檔案時產生的文字轉譯。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. [開啟 Azure 入口網站]( https://portal.azure.com)，然後選取包含您所建立資源的資源群組。
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

此練習僅示範語音服務的一些功能。 若要深入了解這項服務的功用，請參閱[語音頁面](https://azure.microsoft.com/services/cognitive-services/speech-services)。
