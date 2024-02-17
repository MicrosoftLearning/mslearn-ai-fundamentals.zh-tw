---
lab:
  title: 偵測 Vision Studio 中的臉部
---

# 偵測 Vision Studio 中的臉部

視覺解決方案通常需要 AI 才能偵測人臉。 假設虛構的零售公司 Northwind Traders 想要找出客戶站在商店中的位置，以協助他們。 若要達成此目的，其中一種方法是判斷影像中是否有任何臉部，如果是，則傳回顯示其位置的周框方塊座標。

若要測試 Azure AI 臉部服務的臉部偵測功能，您將使用 [Azure Vision Studio](https://portal.vision.cognitive.azure.com/)。 這是UI型平臺，可讓您探索 Azure AI 視覺功能，而不需要撰寫任何程序代碼。

## 建立 *Azure AI 服務*資源

您可以使用 Azure AI 臉部服務搭配 **Azure AI 服務** 多服務資源。 如果您尚未建立此資源，請在 Azure 訂閱中建立 **Azure AI 服務**資源。

1. 在另一個瀏覽器索引標籤中，開啟 at [https://portal.azure.com](https://portal.azure.com?azure-portal=true)的 Azure 入口網站，使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

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

## 偵測 Vision Studio 中的臉部 

1. 在網頁瀏覽器中，流覽至 **位於的Vision Studio[](https://portal.vision.cognitive.azure.com?azure-portal=true)**https://portal.vision.cognitive.azure.com。

1. 在 [**開始使用視覺**登陸] 頁面上，選取 [**臉部**] 索引卷標，然後選取影像**圖格中的 [** 偵測臉部]。

1. 在 [ **試用]** 子標題下，閱讀並核取方塊來確認資源使用原則。  

1. 選取每個範例影像，並觀察傳回的臉部偵測數據。

1. 現在讓我們嘗試一些自己的影像。 選取[](https://aka.ms/mslearn-detect-faces)https://aka.ms/mslearn-detect-faces**** 以下載**detect-faces.zip。** 然後開啟電腦上的資料夾。

1. 找出名為 **store-camera-1.jpg** 的檔案;其中包含下列影像：

    ![商店中人員影像。](./media/create-face-solutions/store-camera-1.jpg)

1. 上傳 **store-camera-1.jpg** 並檢閱傳回的臉部偵測詳細數據。

1. 找出名為 **store-camera-2.jpg** 的檔案，其中包含下列影像：

    ![商店中更多人的影像。](./media/create-face-solutions/store-camera-2.jpg)

1. 上傳 **store-camera-2.jpg** 並檢閱傳回的臉部偵測詳細數據。

1. 找出名為 **store-camera-3.jpg** 的檔案，其中包含下列影像：

    ![商店裡的人形象，工廠遮蔽了臉。](./media/create-face-solutions/store-camera-3.jpg)

1. 上傳 **store-camera-3.jpg** 並檢閱傳回的臉部偵測詳細數據。 請注意 Azure AI 臉部如何偵測到遮蔽的臉部。

在此練習中，您已探索 Azure AI 服務如何偵測影像中的臉部。 如果您有時間，您可以隨意試用範例影像或一些您自己的影像。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1. **開啟 位於 [https://portal.azure.com](https://portal.azure.com?azure-portal=true) 的** Azure 入口網站，然後選取包含您所建立資源的資源群組。
1. 選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

若要深入瞭解如何使用這項服務，請參閱 [Azure AI 臉部服務頁面](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity)。
