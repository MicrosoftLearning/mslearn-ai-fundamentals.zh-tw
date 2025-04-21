---
lab:
  title: 探索 Azure AI Foundry 入口網站中的語音
---

# 探索 Azure AI Foundry 入口網站中的語音

**Azure AI 語音**服務會將語音轉譯為文字，並將文字轉譯為可聽語音。 您可以使用 AI 語音，建立可轉譯會議筆記或從面試的錄製內容產生文字的應用程式。

在此練習中，您將在 Microsoft 用來建立智慧型應用程式的平台 Azure AI Foundry 入口網站中使用 Azure AI 語音，借助內建試用體驗轉錄音訊。 

## 在 Azure AI Foundry 入口網站中建立專案

1. 在瀏覽器索引標籤中，瀏覽至 [Azure AI Foundry][](https://ai.azure.com?azure-portal=true)。

1. 使用您的帳戶登入。 

1. 在 Azure AI Foundry 入口網站的首頁中，選取 [建立專案]****。 在 Azure AI Foundry 中，專案是可協助您組織工作的容器。  

    ![Azure AI Foundry 首頁的螢幕擷取畫面，其中已選取 [建立專案]。](./media/azure-ai-foundry-home-page.png)

1. 在 [建立專案]** 窗格中，您會看到產生的專案名稱，您可以保留現有名稱。 視您過去是否已建立中樞而定，您將會看到要建立的*新* Azure 資源清單或現有中樞的下拉式清單。 如果您看到現有中樞的下拉式清單，請選取 [建立新中樞]**，為您的中樞建立唯一的名稱，然後選取 [下一步]**。  
 
    ![[建立專案] 窗格的螢幕擷取畫面，其中包含中樞和專案的自動產生名稱。](./media/azure-ai-foundry-create-project.png)

> **重要**：您需要在特定位置佈建 Azure AI 服務資源，才能完成實驗的其餘部分。

1. 在相同的 [建立專案]** 窗格中，選取 [自訂]****，然後選取下列其中一個**位置**：美國東部、法國中部、韓國中部、西歐或美國西部，以完成實驗的其餘部分。 然後選取 [建立]****。 

1. 記下所建立的資源： 
- Azure AI 服務
- Azure AI 中樞
- Azure AI 專案
- 儲存體帳戶
- 金鑰保存庫
- 資源群組  
 
1. 建立資源之後，系統會將您帶到專案的 [概觀]** 頁面。 在畫面的左側功能表上，選取 [AI 服務]****。
 
    ![專案畫面上左側功能表的螢幕擷取畫面，其中已選取 [AI 服務]。](./media/azure-ai-foundry-ai-services.png)  

1. 在 [AI 服務]** 頁面上，選取 [語音]** 圖格以試用 Azure AI 語音功能。

    ![在 [AI 服務] 頁面上選取 [語音] 圖格的螢幕擷取畫面。](./media/speech-tile.png)

## 探索 Azure AI Foundry 語音遊樂場中的語音轉換文字

讓我們在 Azure AI Foundry 的語音遊樂場中試用*即時語音轉換文字*。 

1. 在 [語音]** 頁面上，向下捲動並選取 [試用語音功能]**** 底下的 [即時語音轉換文字]**。 您將前往*語音遊樂場*。 

1. 選取 [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) 以下載 **speech.zip**。 開啟  資料夾。 

1. 在 [上傳檔案]** 底下選取 [瀏覽檔案]****，然後瀏覽至您儲存檔案的資料夾。 選取 [WhatAICanDo.m4a]****，然後選取 [開啟]****。

    ![瀏覽檔案](media/recognize-synthesize-speech/browse-files-speech.png)

1. 語音服務會即時轉譯並顯示文字。 如果電腦上有音訊，您可以在文字轉譯期間聽取錄製內容。

1. 檢閱輸出，應該已成功辨識音訊並轉譯為文字。

在本練習中，您已在 Azure AI Foundry 的語音遊樂場中試用 Azure AI 語音服務。 然後，您使用即時語音轉換文字服務來轉譯音訊錄製內容。 您可以在音訊檔案播放期間查看產生的文字轉譯。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1. 開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取您建立的資源所屬的資源群組。
1. 選取資源並選取 [刪除]****，然後再選取 [是]**** 加以確認。 接著即會刪除該資源。

## 深入了解

此練習僅示範語音服務的部分功能。 若要深入了解這項服務的功用，請參閱[語音頁面](https://azure.microsoft.com/services/cognitive-services/speech-services)。
