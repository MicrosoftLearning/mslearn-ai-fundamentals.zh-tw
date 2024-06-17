---
lab:
  title: 探索適用於 Microsoft 365 的 Copilot
---
# 探索適用於 Microsoft 365 的 Copilot

在本練習中，您將探索 Microsoft Copilot 有哪些方式可使用生成式 AI 協助您在建立新內容時提高生產力。 在本練習的案例中，您將從商業構想的一些概要筆記開始著手，並在多個應用程式 (例如 Word, PowerPoint, and Excel) 中使用適用於 Microsoft 365 的 Copilot，以協助您針對潛在投資者研擬商務計劃和簡報。

完成本練習大概需要 **40** 分鐘。

> **注意**：本練習需要貴組織提供**適用於 Microsoft 365 的 Copilot** 授權。

## 使用 Copilot 探索文件及研究構想

為了開始探索生成式 AI，我們會使用適用於 Word 的 Copilot 來檢查現有的文件，並從中擷取一些深入解析。

1. 在網頁瀏覽器中，開啟位於 `https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx` 的 [Business Idea.docx](https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx) 文件。 
1. 選取 **[下載]**，將檔案儲存至電腦的 **[下載]** 資料夾。
1. 將您剛下載的文件**移動**或**複製並貼上**到 **OneDrive** 資料夾。
1. 從 **OneDrive** 資料夾中，在 Microsoft Word 中開啟 **Business Idea.docx** (關閉所有歡迎訊息或新功能通知) 並檢閱該文件，其中會描述紐約市清潔業務的一些高階構想。 如果出現提示，請選取頂端的 **[啟用編輯]**。
1. 尋找並選取 Word 工具列上的 **Copilot** 圖示以開啟 Copilot 窗格，如下所示 (您的視覺效果主題可能會有所不同)：

    ![Microsoft Word 中 Copilot 窗格的螢幕擷取畫面。](./media/generative-ai/copilot-word-pane.png)

1. 在 Copilot 窗格中，在底部的文字輸入區域中，輸入下列提示：

    ```
    What is this document about?
    ```

1. 檢閱 Copilot 的回應，其中應該會摘錄文件中的要點，如下所示：

    ![Word 中 Copilot 窗格以及回應的螢幕擷取畫面。](./media/generative-ai/copilot-response-word.png)

    > 您收到的特定回應可能會因生成式 AI 的性質而有所不同。

1. 返回 Copilot 窗格，詢問 Copilot 下列問題：

    ```
    How do I setup a new business in New York?
    ```

1. 檢閱回應，並視需要對其他問題進行後續追蹤。 當您滿意回應時，請使用回應底下的 **[複製]** (&#128461;) 圖示，將回應複製到剪貼簿。 在 Word 文件中將它貼上，選取所有文字，然後選取 Copilot 圖示，將文字視覺化為資料表。

    ![要求 Copilot 採用資料表格式進行視覺化的螢幕擷取畫面。](./media/generative-ai/copilot-rewrite-as-table.png)

1. 檢閱資料表並要求 Copilot 新增詳細資訊，例如更多詳細資料的參考。  您的回應應如下所示 (您可能需要使用 **[重新產生]** 按鈕)：

    ![以資料表格式顯示 Copilot 回應的螢幕擷取畫面。](./media/generative-ai/copilot-rewrite-as-table-response.png)

    > **重要**：AI 產生的回應以網路上的公開資訊為基礎。 雖然對於協助您了解開展業務所需的步驟可能有幫助，但並不保證 100% 正確，同時也無法取代專業建議的需求！

1. 當您滿意 Copilot 產生的資料表時，請選取 **[保留]** 選項。

## 使用 Copilot 建立商務計劃的內容

在您進行了一些初步研究後，接著即可讓 Copilot 協助您為清潔公司擬定商務計劃。

1. 在 **Business Idea.docx** 文件仍開啟的情況下，在 Copilot 窗格中輸入下列提示：

    ```
    Can you suggest a name for my cleaning business?
    ```

1. 檢閱建議，並選取清潔公司的名稱 (或繼續進行提示以尋找您想要的名稱)。
1. 在 Word 文件中，選取邊界中的 Copilot 圖示以撰寫新內容的草稿。 輸入下列提示，將 **Contoso Cleaning** 以您選擇的公司名稱取代：

    ```
    Write a business plan for "Contoso Cleaning" based on the information in this document. Include an executive summary, market overview, and financial projections.
    ```

    ![Copilot 撰寫商務計畫草稿的螢幕擷取畫面。](./media/generative-ai/copilot-draft-business-plan-prompt.png)

1. 檢閱 Copilot 撰寫的回應草稿，並予以保留、調整語氣、長度，或要求 Copilot 根據新提示重寫。 將適當的標題和樣式套用至您的文件，使其看起來很專業。 您的回應看起來會如下：

    ![Word 文件的螢幕擷取畫面，其中包含 Copilot 產生的商務計劃。](./media/generative-ai/copilot-draft-business-plan-response.png)

1. 如果商務計劃中的財務預測未格式化為資料表，請選取預測內容並使用 Copilot 將其視覺化為資料表。
1. 選取財務預測資料表，並將其複製到剪貼簿。
1. 儲存 Word 文件。

## 以適用於 Excel 的 Copilot 將財務預測視覺化

有了商務計劃，我們即可採用一些有關財務預測的資料，並要求 Excel 中的 Copilot 將這些資料視覺化，以便我們可以給投資者的電子郵件或簡報中包括這些資料。

1. 在已安裝 Microsoft 365 應用程式的電腦上，開啟 **Excel** 並建立新的空白活頁簿。 立即將活頁簿以 **Financial Projetions.xlsx** 儲存至 OneDrive，否則 Copilot 會無法運作。
1. 將 **Business Idea.docx** 中的銷售預測貼到 Excel 試算表中，並**將其格式化為資料表**。 若要這樣做：
    1. 選擇資料中的**儲存格**。
    1. 選取 **[首頁]**，然後選擇 [樣式] 底下的 **[格式化為資料表]**。 
    1. 選擇資料表的樣式。
    1. 在 **[建立資料表]** 對話方塊中，確認或設定儲存格範圍。
    1. 如果您的資料表具有標頭，請標示，然後選取 **[確定]**。
1. 將銷售預測格式化為資料表後，從 Excel 功能區開啟 Copilot 窗格，然後輸入下列提示：

    ```
    Suggest ways to visualize these financial projections.
    ```
    
1. Copilot 應該會建議 1 或 2 種視覺化資料的方法，並提供將樞紐分析圖新增至新工作表的建議。

    ![Excel 中的 Copilot 視覺化財務預測的螢幕擷取畫面。](./media/generative-ai/copilot-excel-visualize-projections.png)

1. 不過，您可能會想要在圖表中查看更多資料以顯示逐年變更，因此請輸入下列提示以新增更多資料：

    ```
    Visualize these financial projections in a line chart to show year-over-year revenue and profits.
    ```

    ![Excel 中的 Copilot 視覺化財務預測的螢幕擷取畫面。](./media/generative-ai/copilot-excel-visualize-more.png)

1. 將樞紐分析圖新增至新的工作表，並將其開啟。 選取圖表，然後選取 **[設計]** 以套用樣式、變更圖表類型和其他動作。 最後，您應該會有類似如下的內容：

    ![Excel 中的 Copilot 新增樞紐分析圖的螢幕擷取畫面。](./media/generative-ai/copilot-excel-chart-design.png)

1. 將檔案儲存至 OneDrive 並關閉 Excel。

您剛剛使用了 Word 中的 Copilot 所建立的資料，並在 Excel 中將其視覺化。 在下一個練習中，您將繼續在 Outlook 中使用 Copilot 來撰寫及傳送關於已完成工作的電子郵件。

## 使用 Copilot 撰寫電子郵件

您建立了一些隨附品以利展開業務。 接下來應聯繫希望能為新創公司提供資金的投資者。

1. 在已安裝 Microsoft 365 應用程式的電腦上，開啟 **Outlook**。 如果您尚未使用 Microsoft 365 帳戶設定 Outlook，請參閱[設定和使用 Outlook - Microsoft 支援服務](https://support.microsoft.com/office/set-up-and-use-outlook-4636f361-d5e3-4a87-9cd4-382858de55fa)。
1. 開啟**新的 Outlook** 體驗。 若要取得 Outlook 中最新的 Copilot 功能，您應該使用「新的 Outlook」體驗。 若要查看您正在使用哪個版本，請參閱[我擁有哪個版本的 Outlook？- Microsoft 支援服務](https://support.microsoft.com/office/what-version-of-outlook-do-i-have-b3a9568c-edb5-42b9-9825-d48d82b2257c)。
1. 建立新的電子郵件，並在 **[收件者]** 方塊中填入您自己的電子郵件地址。
1. 您可以從 Copilot 窗格或從電子郵件本文的右側開始撰寫電子郵件草稿：

    ![螢幕擷取畫面為 Outlook 以及使用 Copilot 撰寫電子郵件草稿的選項。](./media/generative-ai/copilot-draft-email-outlook.png)
    
1. 輸入下列提示並將語氣調整為「正式」，長度調整為「中」：

    ```
    Request a meeting with an investment bank to discuss funding for a commercial cleaning business.
    ```

    ![在 Outlook 中使用 Copilot 撰寫電子郵件草稿的螢幕擷取畫面。](./media/generative-ai/copilot-draft-email-adjust-tone-outlook.png)

1. 選取 **[產生草稿]**，然後檢閱產生的輸出。 調整語氣，或告訴 Copilot 您想要對電子郵件進行哪些變更。

    ![在 Outlook 中使用 Copilot 產生之電子郵件的螢幕擷取畫面。](./media/generative-ai/copilot-draft-email-results-outlook.png)

1. 如果您想要的話，可以將電子郵件傳送給自己！

## 使用 Copilot 建立簡報的內容

在 Copilot 的協助下，您針對清潔業務構想建立了一份商務計劃草案，準備了一些財務預測，並傳送了一封要求和潛在投資者會面的電子郵件。 現在您需要一份有效的簡報來傳達您的企業優勢。

1. 請開啟 **PowerPoint** 並建立新的**空白簡報**。 如果 **[設計工具]** 窗格自動開啟，請將其關閉。

    ![在 PowerPoint 中建立新空白簡報的螢幕擷取畫面。](./media/generative-ai/powerpoint-create-blank-presentation.png)

1. 將簡報以 **Cleaning Company.pptx** 儲存在 OneDrive 資料夾中。
1. 在功能區的 **[首頁] 索引標籤**中選取 **Copilot 按鈕**，選取 **[建立關於...的簡報]**，然後在 Copilot 窗格中完成提示，如下所示：

    ```
    Create a presentation about a corporate cleaning service in New York City.
    ```

1. Copilot 會在簡報中產生投影片。  此流程可能需要幾分鐘的時間，您的輸出應如下所示 (使用不同的主題)：

    ![Copilot 根據 Word 文件建立之 PowerPoint 簡報的螢幕擷取畫面。](./media/generative-ai/copilot-powerpoint-create-image.png)

1. 選取簡報中倒數第二張投影片。 然後，在 Copilot 窗格中，要求使用此提示新增投影片：

    ```
    Add a slide that describes the benefits of an eco-friendly approach to cleaning. 
    ```

    ![PowerPoint 簡報建立新投影片的螢幕擷取畫面。](./media/generative-ai/copilot-powerpoint-add-new-slide.png)

1. 儲存簡報。

## 挑戰

現在您已了解如何在幾個不同的應用程式中使用適用於 Microsoft 365 的 Copilot，以研究想法並產生內容，為什麼不嘗試進一步探索呢？ 請嘗試使用 Copilot 在當地圖書館策劃一場提升兒童讀寫能力的活動。 可行的嘗試包括：

- 研究一些鼓勵兒童盡早閱讀的技巧。
- 製作活動的傳單或海報。
- 撰寫活動的電子郵件，邀請當地的兒童讀物作家出席活動並發言。
- 建立簡報以展開活動。

請盡情發揮您的創造力，並探索 Copilot 如何藉由尋找資訊、產生並精煉文字、建立影像和回答問題，為您提供協助。

## 結論

在本練習中，您已使用[適用於 Microsoft 365 的 Copilot](https://www.microsoft.com/microsoft-365/enterprise/copilot-for-microsoft-365) 來尋找資訊並產生內容。 希望您已了解如何在 Copilot 中利用生成式 AI 來提高生產力和創造力。 Microsoft 365 可讓您將生成式 AI 的強大功能導入商務資料和流程中，同時整合至您現有的 IT 基礎結構，以確保解決方案易於管理且安全無虞。
