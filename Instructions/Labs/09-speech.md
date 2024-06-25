---
lab:
  title: 探索 Speech Studio
---

# 探索 Speech Studio

**Azure AI 語音**服務會將語音轉譯為文字，並將文字轉譯為可聽語音。 您可以使用 AI 語音，建立可轉譯會議筆記或從面試的錄製內容產生文字的應用程式。

在此練習中，您將使用 Azure AI Speech Studio 來試用 Azure AI 語音的功能。 

## 建立 *Azure AI 語音*資源

您可以建立**語音**資源或 **Azure AI 服務**資源，以使用語音服務。

在此練習中，您將建立 AI 語音資源，除非您已有可用的資源。

1. 在另一個瀏覽器索引標籤中，開啟 [Azure AI Speech Studio](https://speech.microsoft.com/)，並使用您的 Microsoft 帳戶登入。

1. 選取 [設定]****，然後選取 [建立資源]****。 使用下列設定對其進行設定：
    - **新資源的名稱**：輸入唯一名稱**。
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **區域**：*選取[支援的區域](https://learn.microsoft.com/azure/ai-services/speech-service/regions)*。
    - **定價層**：*免費 FO (如果不適用，請選取 [標準 S0])。*
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
1. 選取 [建立資源]****。 等到資源建立完成後，選取 [使用資源]****。 [開始使用語音] 頁面隨即顯示。

## 在 Speech Studio 中探索語音轉換文字功能

1. 選取 [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) 以下載 **speech.zip**。 開啟  資料夾。 

1. 在 [開始使用語音] 頁面的 [語音轉換文字]** 底下，尋找 [即時語音轉換文字]**。 選取 [試用即時語音轉換文字]****。

    ![開始使用語音](media/recognize-synthesize-speech/try-out-speech-to-text.png)

1. 在 [選擇音訊檔案]** 底下選取 [瀏覽檔案]****，然後瀏覽至您儲存檔案的資料夾。 選取 [WhatAICanDo.m4a]****，然後選取 [開啟]****。

    ![瀏覽檔案](media/recognize-synthesize-speech/browse-files-speech.png)

1. 語音服務會即時轉譯並顯示文字。 如果電腦上有音訊，您可以在文字轉譯期間聽取錄製內容。
1. 檢閱輸出，應該已成功辨識音訊並轉譯為文字。

    > **注意**：如果出現錯誤訊息，請稍候幾分鐘再重試。 語音資源第一次使用時需要一些時間。

在此練習中，您在 Speech Studio 中建立了 AI 語音資源。 然後，您使用即時語音轉換文字服務來轉譯音訊錄製內容。 您可以在音訊檔案播放期間查看產生的文字轉譯。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取您建立的資源所屬的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

此練習僅示範語音服務的部分功能。 若要深入了解這項服務的功用，請參閱[語音頁面](https://azure.microsoft.com/services/cognitive-services/speech-services)。
