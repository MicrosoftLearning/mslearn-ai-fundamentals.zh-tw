---
lab:
  title: 探索 Azure AI Foundry 入口網站中的語音
---

# 探索 Azure AI Foundry 入口網站中的語音

**Azure AI 語音**服務會將語音轉譯為文字，並將文字轉譯為可聽語音。 您可以使用 AI 語音，建立可轉譯會議筆記或從面試的錄製內容產生文字的應用程式。

在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中使用 Azure AI 語音，借助內建試用體驗轉錄音訊。 

## 在 Azure AI Foundry 入口網站中建立專案

1. 在網頁瀏覽器中，開啟 [Azure AI Foundry 入口網站](https://ai.azure.com) 於`https://ai.azure.com` 並使用您的 Azure 認證登入。 關閉首次登入時，已開啟任何提示或是快速入門窗格。 

1. 請在瀏覽器中，先至`https://ai.azure.com/managementCenter/allResources`瀏覽，再選取[**建立**]。 然後選擇選項，以便建立*新的 Azure AI Foundry 資源*。

1. 請在 *[建立專案]* 精靈中，輸入專案的有效名稱。

1. 請展開 *[進階選項]*，為專案指定下列設定：
    - **訂用帳戶**：您的 Azure 訂用帳戶
    - **資源群組**：建立或選取資源群組
    - **地區**：選取以下位置之一：
        * 美國東部
        * 法國中部
        * 南韓中部
        * 西歐
        * 美國西部

    等候建立好專案和中心。

1. 當建立專案時，系統會將您導向專案詳細資料的 [*概觀*] 頁面。
 
1. 在畫面的左側功能表上，選取 [遊樂場]****。

1. 在 [遊樂場]** 頁面上，選取 [語音遊樂場]**** 圖格，試用一些 Azure AI 語音功能。

## 探索 Azure AI Foundry 語音遊樂場中的語音轉換文字

讓我們在 Azure AI Foundry 的語音遊樂場中試用*語音轉換文字*。 

1. 在 [語音]** 頁面上，向下捲動並選取 [試用語音功能]** 底下的 [即時謄寫]****。 您將前往*語音遊樂場*。 

1. 選取 [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) 以下載 **speech.zip**。 開啟  資料夾。 

1. 在 [上傳檔案]** 底下選取 [瀏覽檔案]****，然後瀏覽至您儲存檔案的資料夾。 選取 [WhatAICanDo.m4a]****，然後選取 [開啟]****。

    ![瀏覽檔案](media/recognize-synthesize-speech/browse-files-speech.png)

1. 語音服務會即時轉譯並顯示文字。 如果電腦上有音訊，您可以在文字轉譯期間聽取錄製內容。

1. 檢閱輸出，應該已成功辨識音訊並轉譯為文字。

在本練習中，您已在 Azure AI Foundry 的語音遊樂場中試用 Azure AI 語音服務。 接著，您已使用即時謄寫來轉譯音訊錄製內容。 您可以在音訊檔案播放期間查看產生的文字轉譯。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取您建立的資源所屬的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

此練習僅示範語音服務眾多功能中的一個。 若要深入了解這項服務的功用，請參閱[語音頁面](https://azure.microsoft.com/services/cognitive-services/speech-services)。
