---
lab:
  title: 在 Vision Studio 中分析影像
---

# 在 Vision Studio 中分析影像 

**Azure AI 視覺**包含許多功能，可用來了解影像內容和內容，以及從影像擷取資訊。 Azure AI Vision Studio 可讓您試用影像分析的許多功能。 

在此練習中，您將使用 Vision Studio 以使用內建的試用體驗來分析影像。 假設虛構零售業者 *Northwind Traders* 已決定實作「智慧商店」，由 AI 服務監視商店，以識別需要協助的客戶，並指示員工協助他們。 使用 Azure AI 視覺，可以分析整間商店的攝影機拍攝的影像，以提供其拍攝內容有意義的說明。

## 建立 *Azure AI 服務*資源

您可以透過 **Azure AI 服務**的多服務資源來使用 Azure AI 視覺的影像分析功能。 如果您尚未建立此資源，請在 Azure 訂閱中建立 **Azure AI 服務**資源。

1. 在另一個瀏覽器索引標籤中，開啟位於 [https://portal.azure.com](https://portal.azure.com?azure-portal=true) 的 Azure 入口網站，並使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

1. 按一下 **＋建立資源 **按鈕並搜尋  * Azure AI 服務 *。 選取**建立** **Azure AI 服務**方案。 系統會帶您前往建立 Azure AI 服務資源的頁面。 使用下列設定對其進行設定：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **區域**：*選取最接近的地理區域。如果在美國東部，請使用 "美國東部 2"*。
    - **名稱**：*輸入唯一名稱*。
    - **定價層**：*標準 S0。*
    - **核取此方塊即表示我確認我已閱讀並了解下列所有條款**：*已選取*。

1. 選取 [檢閱 + 建立]****，然後再選取 [建立]**** 並等待部署完成。

## 將您的 Azure AI 服務資源連線至 Vision Studio

接下來，將上面您已佈建的 Azure AI 服務資源連線到 Vision Studio。

1. 在另一個瀏覽器索引標籤中，瀏覽至 [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true)。

1. 使用您的帳戶登入，並確保使用與建立 Azure AI 服務資源的目錄相同的目錄。

1. 在 [Vision Studio] 首頁上，選取 [開始使用視覺]**** 標題底下的 [檢視所有資源]****。

    ![在 Vision Studio 中的 [開始使用視覺] 底下，[檢視所有資源] 連結會反白顯示。](./media/analyze-images-vision/vision-resources.png)

1. 在 [選取要使用的資源]**** 頁面上，將滑鼠游標停留在您在清單中上面所建立的資源上，並核取資源名稱左邊的方塊，然後選取 [選取為預設資源]****。

    > **注意**：如果未列出您的資源，您可能需要**重新整理**頁面。

    ![即會顯示 [選取要使用的資源] 對話方塊，其中反白顯示並核取了 cog-ms-learn-vision-SUFFIX 認知服務資源。 [選取為預設資源] 按鈕會反白顯示。](./media/analyze-images-vision/default-resource.png)

1. 選取畫面右上方的 "x" 以關閉設定頁面。

## 產生影像的輔助字幕

現在您已準備好使用 Vision Studio 來分析 *Northwind Traders* 商店中相機所拍攝的影像。

讓我們看看 Azure AI 視覺的影像輔助字幕功能。 影像輔助字幕可透過 [輔助字幕]**** 和 [密集輔助字幕]**** 功能來取得。

1. 在網頁瀏覽器中，瀏覽至 [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true)。

1. 在 [開始使用視覺]**** 登陸頁面上，選取 [影像分析]**** 索引標籤，然後選取 [將輔助字幕新增至影像]**** 圖格。

    ![在 Vision Studio 首頁上，已選取並醒目提示 [影像分析] 索引標籤。 [將輔助字幕新增至影像] 圖格會醒目顯示。](./media/analyze-images-vision/add-captions.png)

1. 在 [試用]**** 子標題下，閱讀並核取方塊來確認資源使用原則。  

1. 選取 [**https://aka.ms/mslearn-images-for-analysis**](https://aka.ms/mslearn-images-for-analysis) 以下載 **image-analysis.zip**。 開啟電腦上的資料夾，並找出名為 **store-camera-1.jpg** 的檔案；其中包含下列影像：

    ![影像：父母在店裡使用手機相機拍攝小孩的照片](./media/analyze-images-vision/store-camera-1.jpg)

1. 將 **store-camera-1.jpg** 影像拖曳至 [將檔案拖放於此處]**** 方塊，或瀏覽至檔案系統上的檔案，以上傳該影像。

1. 觀察產生的輔助字幕文字，該文字會顯示在影像右側的 [偵測到的屬性]**** 面板中。

    [輔助字幕]**** 功能提供描述影像內容的單一人類可讀英文句子。

1. 接下來，使用相同的影像來執行 [密集輔助字幕]****。 返回 [Vision Studio]**** 首頁，如同您先前所做的一樣，選取 [影像分析]**** 索引標籤，然後選取 [密集輔助字幕]**** 圖格。

    [密集輔助字幕]**** 功能與 [輔助字幕]**** 功能不同，因為它為影像提供多個人類可讀的輔助字幕，其中一種描述影像的內容，另一種涵蓋了圖片中偵測到的重要物件。 每個偵測到的物件都包含週框方塊，此方塊會定義與物件相關聯影像內的像素座標。

1. 將滑鼠停留在 [偵測到的屬性]**** 清單中的其中一個輔助字幕上，並觀察影像內會發生什麼事。

    ![影像及其輔助字幕隨即顯示。](./media/analyze-images-vision/dense-captioning.png)

    將滑鼠游標移至清單中的其他輔助字幕上方，並注意週框方塊在影像中如何移動，以醒目提示用來產生輔助字幕的影像部分。

## 標記影像

您將嘗試的下一個功能是 [擷取標籤]**** 功能。 擷取標籤是以數千個可辨識的物件為基礎，包括生物、風景和動作。

1. 返回 Vision Studio 的首頁，然後選取 [影像分析]**** 索引標籤底下的 [從影像擷取常見標籤]**** 圖格。

2. 在 [選擇您想要試用的模型]**** 中，保留 [預先建置的產品與差距模型]**** 選取。 在 [選擇您的語言]**** 中，選取 [英文]**** 或喜好設定的語言。

3. 開啟包含您所下載影像的資料夾，並找出名為 **store-image-2.jpg** 的檔案，如下所示：

    ![影像：在超市中拿著購物籃的人](./media/analyze-images-vision/store-camera-2.jpg)

4. 上傳 **store-camera-2.jpg** 檔案。

5. 檢閱從影像擷取的標籤清單，以及偵測到的屬性面板中每個標籤的信賴度分數。 在這裡，信賴度分數是偵測到的屬性文字描述影像中實際內容的可能性。 請注意，標籤清單中不僅包含物件，也包括*購物*、*銷售*及*站立*等動作。

    ![Vision Studio 中偵測屬性面板的螢幕擷取畫面，其中顯示於原始影像旁的文字和信賴度分數。](./media/analyze-images-vision/detect-attributes.png)

## 物件偵測

在這項工作中，您會使用影像分析的 [物件偵測]**** 功能。 物件偵測會根據數千個可辨識的物件和生物來偵測和擷取週框方塊。

1. 返回 Vision Studio 的首頁，然後選取 [影像分析]**** 索引標籤底下的 [偵測影像中的常見物件]**** 圖格。

1. 在 [選擇您想要試用的模型]**** 中，保留 [預先建置的產品與差距模型]**** 選取。

1. 開啟包含您所下載影像的資料夾，並找出名為 **store-camera-3.jpg** 的檔案，如下所示：

    ![影像：推著購物車的人](./media/analyze-images-vision/store-camera-3.jpg)

1. 上傳 **store-camera-3.jpg** 檔案。

1. 在 [偵測到的屬性]**** 方塊中，觀察偵測到的物件清單及其信賴度分數。

1. 將滑鼠游標停留在 [偵測到的屬性]**** 清單中的物件上方，以醒目提示影像中物件的週框方塊。

1. 移動 [閾值]**** 滑桿，直到滑桿右側顯示 70 的值為止。 觀察清單中物件會發生什麼事。 閾值滑桿會指定只應顯示識別為信賴度分數或機率大於閾值的物件。

## 清理

如果您不打算進行更多的練習，請刪除不再需要的任何資源。 這可以避免產生任何不必要的成本。

1.  開啟 [Azure 入口網站]( https://portal.azure.com)，然後選取包含您所建立資源的資源群組。 
1.  選取資源並選取 [刪除]****，然後再選取 [是]**** 以確認。 接著即會刪除該資源。

## 深入了解

若要深入了解此服務的功能，請參閱 [Azure AI 視覺頁面](https://learn.microsoft.com/azure/ai-services/computer-vision/overview)。
