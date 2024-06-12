---
lab:
  title: 在 Vision Studio 中分析影像
---

# 在 Vision Studio 中分析影像 

**Azure AI 視覺** 包含許多功能，可用來瞭解影像內容和內容，以及從影像擷取資訊。 Azure AI Vision Studio 可讓您試用影像分析的許多功能。 

在此練習中，您將使用 Vision Studio 使用內建的試用體驗來分析影像。 假設虛構的零售商 *Northwind Traders* 已決定實作「智慧型商店」，其中 AI 服務會監視商店，以識別需要協助的客戶，並引導員工協助他們。 藉由使用 Azure AI 視覺，可以分析整個商店中相機拍攝的影像，以提供其描述的有意義描述。

## 建立 *Azure AI 服務*資源

您可以使用 Azure AI 視覺的影像分析功能搭配 **Azure AI 服務** 多服務資源。 如果您尚未建立此資源，請在 Azure 訂閱中建立 **Azure AI 服務**資源。

1. 在另一個瀏覽器索引標籤中，開啟位於 [https://portal.azure.com](https://portal.azure.com?azure-portal=true)的 Azure 入口網站，使用與您的 Azure 訂用帳戶相關聯的 Microsoft 帳戶登入。

1. 按一下 **＋建立資源 **按鈕並搜尋  * Azure AI 服務 *。 選取**建立** **Azure AI 服務**方案。 系統會帶您前往建立 Azure AI 服務資源的頁面。 使用下列設定對其進行設定：
    - **訂用帳戶**：*您的 Azure 訂用帳戶*。
    - **資源群組**：*選取或建立具有唯一名稱的資源群組*。
    - **區域**： *選取最接近的地理區域。如果在美國東部，請使用「美國東部 2」*。
    - **名稱**：*輸入唯一名稱*。
    - **定價層**： *標準 S0。*
    - **勾選此方塊，我確認我已閱讀並瞭解下列**所有條款： *已選取*。

1. 選取 [**檢閱 + 建立**]，然後**** 等候部署完成。

## 將 Azure AI 服務資源連線至 Vision Studio

接下來，將您布建的 Azure AI 服務資源連線到 Vision Studio。

1. 在另一個瀏覽器索引標籤中，流覽至 [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true)。

1. 使用您的帳戶登入，並確定您使用的目錄與您建立 Azure AI 服務資源所在的目錄相同。

1. 在 Vision Studio 首頁上，選取 **[開始使用視覺 **] 標題下方的 **[檢視所有資源**]。

    ![在 Vision Studio 中開始使用視覺下，[檢視所有資源] 連結會反白顯示。](./media/analyze-images-vision/vision-resources.png)

1. 在 [ **選取要使用的** 資源] 頁面上，將滑鼠游標暫留在您在清單上方建立的資源上，然後核取資源名稱左邊的方塊，然後選取 [ **選取為默認資源**]。

    > **注意**：如果未列出您的資源，您可能需要重新**** 整理頁面。

    ![[選取要使用的資源] 對話框會顯示為醒目提示並核取 cog-ms-learn-vision-SUFFIX 認知服務資源。 [選取為預設資源] 按鈕會反白顯示。](./media/analyze-images-vision/default-resource.png)

1. 選取畫面右上方的 「x」 以關閉設定頁面。

## 產生影像的標題

現在您已準備好使用 Vision Studio 來分析 Northwind Traders* 商店中相機拍攝的*影像。

讓我們看看 Azure AI 視覺的影像輔助功能。 影像標題可透過 **Caption 和 **Dense Captions**** 功能取得。

1. 在網頁瀏覽器中，流覽至 [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true)。

1. 在 [ **開始使用視覺** 登陸] 頁面上，選取 [ **影像分析** ] 索引標籤，然後選取 [ **將標題新增至影像** ] 圖格。

    ![在 Vision Studio 首頁上，已選取並醒目提示 [影像分析] 索引標籤。 [將標題新增至影像] 圖格會反白顯示。](./media/analyze-images-vision/add-captions.png)

1. 在 [ **試用]** 子標題下，閱讀並核取方塊來確認資源使用原則。  

1. 選取[](https://aka.ms/mslearn-images-for-analysis)https://aka.ms/mslearn-images-for-analysis**** 以下載**image-analysis.zip。** 開啟電腦上的資料夾，並找出名為 **store-camera-1.jpg** 的檔案;其中包含下列影像：

    ![影像：父母在店裡使用手機相機拍攝小孩的照片](./media/analyze-images-vision/store-camera-1.jpg)

1. **將store-camera-1.jpg**影像拖曳至 **[在這裡拖放檔案**] 方塊，或流覽至文件系統上的檔案，以上傳store-camera-1.jpg影像。

1. 觀察產生的標題文字，該文字會顯示在 **影像右側的 [偵測到的屬性** ] 面板中。

    **Caption** 功能提供描述影像內容的單一人類可讀英文句子。

1. 接下來，使用相同的影像來執行 **密集字幕**。 **返回 Vision Studio** 首頁，如同您先前所做的一樣，選取 **[影像分析**] 索引標籤，然後選取 **[密集標題]** 圖格。

    **「密集字幕」** 功能與 **Caption** 功能不同，因為它為影像提供多個人類可讀的標題，其中一個描述影像的內容，另一個說明圖片中偵測到的基本物件。 每個偵測到的物件都包含周框方塊，此方塊會定義與對象相關聯之影像內的圖元座標。

1. 將滑鼠停留在 **[偵測** 到的屬性] 清單中的其中一個標題上，並觀察影像內會發生什麼事。

    ![影像及其標題隨即顯示。](./media/analyze-images-vision/dense-captioning.png)

    將滑鼠游標移至清單中的其他標題上方，並注意周框方塊在影像中如何移動，以醒目提示用來產生標題的影像部分。

## 標記影像

您將嘗試的下一個功能是擷 **取標籤** 功能。 擷取標記是以數千個可辨識的對象為基礎，包括活生生生物、風景和動作。

1. 返回 Vision Studio 的首頁，然後選取 **[影像分析 **] 索引卷標底下的 **[從影像**擷取通用捲標] 圖格。

2. 在 [ **選擇您想要試用**的模型] 中，保留 **[預先建置的產品與差距模型** ] 選取。 在 [ **選擇您的語言]** 中，選取 **[英文** ] 或喜好設定的語言。

3. 開啟包含您所下載影像的資料夾，並找出名為 **store-image-2.jpg** 的檔案，如下所示：

    ![影像：在超市中拿著購物籃的人](./media/analyze-images-vision/store-camera-2.jpg)

4. **上傳store-camera-2.jpg**檔案。

5. 檢閱從影像擷取的標記清單，以及偵測到的屬性面板中每個標記的信賴分數。 在這裡，信賴分數是偵測到屬性文字描述影像中實際內容的可能性。 請注意，標籤清單中不僅包含物件，而且包括購物 *、*銷售*及*站立*等*動作。

    ![Vision Studio 中偵測屬性面板的螢幕快照，其中顯示原始影像旁的文字和信賴分數。](./media/analyze-images-vision/detect-attributes.png)

## 物件偵測

在這項工作中，您會使用 **影像分析的物件偵測** 功能。 對象偵測會根據數千個可辨識的物件和活體來偵測和擷取周框方塊。

1. 返回 Vision Studio 的首頁，然後選取 [影像分析 **] 索引卷標底下的 **[**偵測影像**圖格中的常見物件]。

1. 在 [ **選擇您想要試用**的模型] 中，保留 **[預先建置的產品與差距模型** ] 選取。

1. 開啟包含您下載映像的資料夾，並找出名為 **store-camera-3.jpg** 的檔案，如下所示：

    ![影像：推著購物車的人](./media/analyze-images-vision/store-camera-3.jpg)

1. **上傳store-camera-3.jpg**檔案。

1. 在 [ **偵測到的屬性]** 方塊中，觀察偵測到的物件清單及其信賴分數。

1. 將滑鼠游標停留在 **[偵測到的屬性** ] 清單中的物件上方，以反白顯示影像中物件的周框方塊。

1. **移動 [閾值]** 滑桿，直到滑杆右邊顯示 70 的值為止。 觀察清單中物件會發生什麼事。 臨界值滑桿會指定只顯示信賴分數或機率大於閾值的物件。

## 清理

如果您不打算執行更多練習，請刪除不再需要的任何資源。 這可避免產生任何不必要的成本。

1.  [開啟 Azure 入口網站]( https://portal.azure.com)，然後選取包含您所建立資源的資源群組。 
1.  選取資源，然後選取 [刪除]**，然後**選取 **[是**] 以確認。 接著會刪除資源。

## 深入了解

若要深入瞭解如何使用這項服務，請參閱 [Azure AI 視覺頁面](https://learn.microsoft.com/azure/ai-services/computer-vision/overview)。
