---
lab:
  title: 在 Vision Studio 中讀取文字
---

# 在 Vision Studio 中讀取文字

在此練習中，您將使用 Azure AI 服務來探索 Azure AI 視覺的光學字元辨識功能。 您將使用 Vision Studio 來實驗從影像中擷取文字，而不需要撰寫任何程式碼。

常見的電腦視覺挑戰是偵測和解譯內嵌在影像中的文字。 這稱為光學字元辨識（OCR）。 在此練習中，您將使用 Azure AI 服務資源，其中包括 Azure AI 視覺服務。 接著，您將使用 Vision Studio 來試用具有不同類型的影像的 OCR。

## 建立 *Azure AI 服務*資源

您可以使用 Azure AI 視覺的 OCR 功能搭配 **Azure AI 服務** 多服務資源。 如果您尚未建立此資源，請在 Azure 訂閱中建立 **Azure AI 服務**資源。

1. 在另一個瀏覽器索引標籤中 **，開啟 at[](https://portal.azure.com?azure-portal=true)https://portal.azure.com 的 Azure 入口網站，使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。**

1. 按一下 **＋建立資源 **按鈕並搜尋  * Azure AI 服務 *。 選取**建立** **Azure AI 服務**方案。 系統會帶您前往建立 Azure AI 服務資源的頁面。 使用下列設定對其進行設定：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **區域**：美國東部。
    - **名稱**：*輸入唯一名稱*。
    - **定價層**： *標準 S0。*
    - **勾選此方塊，我確認我已閱讀並瞭解下列**所有條款： *已選取*。

1. 選取 [**檢閱 + 建立**]，然後**** 等候部署完成。

## 將 Azure AI 服務資源 連線 至 Vision Studio

接下來，將您布建的 Azure AI 服務資源連線至 Vision Studio。

1. 在另一個瀏覽器索引標籤中，流覽至**位於的 Vision Studio[**](https://portal.vision.cognitive.azure.com?azure-portal=true)https://portal.vision.cognitive.azure.com。

1. 使用您的帳戶登入，並確定您使用的目錄與您建立 Azure AI 服務資源所在的目錄相同。

1. 在 Vision Studio 首頁上，選取 **[開始使用視覺 **] 標題下方的 **[檢視所有資源**]。

    ![在 Vision Studio 中開始使用視覺下，[檢視所有資源] 連結會反白顯示。](./media/analyze-images-vision/vision-resources.png)

1. 在 [ **選取要使用的** 資源] 頁面上，將滑鼠游標暫留在您在清單上方建立的資源上，然後核取資源名稱左邊的方塊，然後選取 [ **選取為默認資源**]。

    > **注意**：如果未列出您的資源，您可能需要重新**** 整理頁面。

    ![[選取要使用的資源] 對話框會顯示為醒目提示並核取 cog-ms-learn-vision-SUFFIX 認知服務資源。 [選取為預設資源] 按鈕會反白顯示。](./media/analyze-images-vision/default-resource.png)

1. 選取畫面右上方的 「x」 以關閉設定頁面。

## 從 Vision Studio 中的影像擷取文字
    
1. 在網頁瀏覽器中，流覽至 **位於的Vision Studio[](https://portal.vision.cognitive.azure.com?azure-portal=true)**https://portal.vision.cognitive.azure.com。

1. 在 [**開始使用視覺**登陸] 頁面上，選取 [光學字元辨識 **]，然後**選取 **[從影像**擷取文字] 圖格。

1. 在 [ **試用]** 子標題下，閱讀並核取方塊來確認資源使用原則。  

1. 選取[](https://aka.ms/mslearn-ocr-images)https://aka.ms/mslearn-ocr-images**** 以下載**ocr-images.zip。** 然後開啟資料夾。

1. 在入口網站上，選取 [ **瀏覽檔案]** ，然後流覽至您下載 **ocr-images.zip**計算機上的資料夾。 選取 **advert.jpg** ，然後選取 [ **開啟**]。

1. 現在，請檢閱傳回的內容：
    - 在 **[偵測到的屬性**] 中，影像中找到的任何文字會組織成區域、線條和文字的階層式結構。
    - 在影像上，文字的位置會以周框方塊表示，如下所示：

    ![所概述影像中文字的影像。](media/read-text-computer-vision/advert-bounding-boxes.jpg)

1. 您現在可以嘗試另一個影像。 選取 [ **瀏覽檔案]** ，然後流覽至您從 GitHub 儲存盤案的資料夾。 選取 **[letter.jpg**]。

    ![打字信的影像。](media/read-text-computer-vision/letter.jpg)

1. 檢閱第二個影像的結果。 它應該會傳回文字的文字和周框方塊。 如果您有時間，請嘗試 **note.jpg** 並 **receipt.jpg**。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. **在 開啟 Azure 入口網站[https://portal.azure.com**](https://portal.azure.com?azure-portal=true)，然後選取包含您所建立資源的資源群組。
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

若要深入瞭解如何使用這項服務，請參閱 Azure AI 視覺關於光學字元辨識[的檔](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr)。
