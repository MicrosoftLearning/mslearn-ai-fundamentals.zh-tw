---
lab:
  title: 探索適用於 Microsoft 365 的 Copilot
---
# 探索適用於 Microsoft 365 的 Copilot

在此練習中，您將探索 Microsoft Copilot 在建立新內容時，可以使用產生 AI 來協助您提高生產力的一些方式。 在此練習的案例中，您將從商務構想的一些高階筆記開始，並在 Word、PowerPoint 和 Excel 等多個應用程式中使用 Copilot for Microsoft 365，以協助您開發商務計劃和潛在投資者的簡報。

此練習大約需要 **40** 分鐘才能完成。

> **注意**：此練習需要 **貴組織的 Microsoft 365** 授權 Copilot。

## 使用 Copilot 探索檔並研究想法

若要開始探索產生 AI，讓我們使用 Copilot for Word 來檢查現有的檔，並從中擷取一些見解。

1. 在網頁瀏覽器中，於 開啟商務Idea.docx[`https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx`檔](https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx)。 
1. 選取 [ **下載** ] 將檔案儲存至計算機的 **[下載]** 資料夾。
1. **移動** 或 **複製並貼** 上您剛下載至 **OneDrive** 資料夾的檔案。
1. 從您的 **OneDrive** 資料夾中，在 Microsoft Word 中開啟 **商務Idea.docx** （關閉任何歡迎訊息或新功能通知），並檢閱檔，其中描述了紐約市清潔業務的一些高階想法。 如果出現提示，請選取頂端的 [ **啟用編輯** ]。
1. 尋找並選取 **Word 工具列上的 Copilot 圖示以開啟 Copilot** 窗格，如下所示（您的視覺主題可能會有所不同）：

    ![Microsoft Word 中 Copilot 窗格的螢幕快照。](./media/generative-ai/copilot-word-pane.png)

1. 在 [Copilot] 窗格中，於底部的文字區域中輸入下列提示：

    ```
    What is this document about?
    ```

1. 檢閱 Copilot 的回應，其應該摘要說明檔中的要點，如下所示：

    ![Word 中 Copilot 窗格的螢幕快照，其中包含回應。](./media/generative-ai/copilot-response-word.png)

    > 您收到的特定回應可能會因產生 AI 的性質而有所不同。

1. 返回 [Copilot] 窗格，詢問 Copilot 下列問題：

    ```
    How do I setup a new business in New York?
    ```

1. 檢視回應，並視需要追蹤其他問題。 當您滿意回應時，請使用 **回應底下的 [複製** ]（&#128461;） 圖示，將它複製到剪貼簿。 將它貼到 Word 檔中，選取所有文字，然後選取 Copilot 圖示，將文字可視化為表格。

    ![要求 Copilot 以表格格式可視化的螢幕快照。](./media/generative-ai/copilot-rewrite-as-table.png)

1. 檢閱數據表並要求 Copilot 新增詳細資訊，例如參考以取得詳細數據。  您的回應看起來應該像這樣（您可能需要使用 [ **重新產生** ] 按鈕）：

    ![表格格式之 Copilot 回應的螢幕快照。](./media/generative-ai/copilot-rewrite-as-table-response.png)

    > **重要**事項：AI 產生的回應是以網路上公開的資訊為基礎。 雖然協助您了解設定業務所需的步驟可能很有用，但並不保證正確 100%，而且不會取代專業建議的需求！

1. 當您滿意 Copilot 產生的數據表時，請選取 [ **保留]** 選項。

## 使用 Copilot 建立商務方案的內容

既然您已進行過一些初步研究，讓我們讓 Copilot 協助您為清潔公司制定業務計劃。

1. 當 **商務Idea.docx** 檔仍然開啟時，在 [Copilot] 窗格中，輸入下列提示：

    ```
    Can you suggest a name for my cleaning business?
    ```

1. 檢閱建議並選取清潔公司的名稱（或繼續提示尋找您想要的名稱）。
1. 在 Word 檔中，選取邊界中的 Copilot 圖示以草稿新內容。 輸入下列提示，以 **您選擇的公司名稱取代 Contoso Cleaning** ：

    ```
    Write a business plan for "Contoso Cleaning" based on the information in this document. Include an executive summary, market overview, and financial projections.
    ```

    ![Copilot 起草商務方案的螢幕快照。](./media/generative-ai/copilot-draft-business-plan-prompt.png)

1. 檢閱 Copilot 起草的回應，並保留它、調整語氣、長度，或要求 Copilot 以新的提示重寫它。 將適當的標題和樣式套用至您的檔，使其看起來很專業。 您的回應看起來會如下：

    ![Word 檔的螢幕快照，其中包含 Copilot 產生的商務方案。](./media/generative-ai/copilot-draft-business-plan-response.png)

1. 如果商務計劃中的財務預測未格式化為數據表，請選取它並使用 Copilot 將投影可視化為數據表。
1. 選取財務預測數據表，並將其複製到剪貼簿。
1. 儲存 Word 檔。

## 在 Copilot for Excel 中將財務預測可視化

有了商務計劃，讓我們在財務預測上取得其中一些數據，並要求 Excel 中的 Copilot 將這些數據可視化，以便我們可以將其包含在電子郵件或簡報中給投資者。

1. 在已安裝 Microsoft 365 應用程式的電腦上，開啟 **Excel** 並建立新的空白活頁簿。 立即將活頁簿儲存為 **財務Projetions.xlsx** 至 OneDrive，或 Copilot 將無法運作。
1. 將商務Idea.docx的銷售投影**數據表貼到 Excel 電子表格中，並將其**格式化為數據表**。** 若要這樣做：
    1. **選取數據中的數據格**。
    1. 選取 [ **首頁** ]，然後選擇 [樣式] 底下的 [ **格式化為表格** ]。 
    1. 選擇表格的樣式。
    1. 在 [ **建立數據表]** 對話框中，確認或設定儲存格範圍。
    1. 如果您的數據表有標頭，請標示，然後選取 [ **確定**]。
1. 將銷售投影格式化為數據表后，從 Excel 功能區開啟 [Copilot] 窗格，然後輸入下列提示：

    ```
    Suggest ways to visualize these financial projections.
    ```
    
1. Copilot 應該建議 1 或 2 種方式來可視化您的數據，並提供將樞紐圖表新增至新工作表。

    ![Excel 中 Copilot 將財務預測可視化的螢幕快照。](./media/generative-ai/copilot-excel-visualize-projections.png)

1. 不過，您可能會想要在圖表中看到更多數據以顯示逐年變更，因此請輸入下列提示以新增更多數據：

    ```
    Visualize these financial projections in a line chart to show year-over-year revenue and profits.
    ```

    ![Excel 中 Copilot 將財務預測可視化的螢幕快照。](./media/generative-ai/copilot-excel-visualize-more.png)

1. 將樞紐分析圖新增至新的工作表，並加以開啟。 選取圖表，然後選取 **[設計** ] 以套用樣式、變更圖表類型和其他動作。 最後，您應該會有類似如下的內容：

    ![Excel 中 Copilot 新增樞紐分析圖的螢幕快照。](./media/generative-ai/copilot-excel-chart-design.png)

1. 將檔案儲存至 OneDrive 並關閉 Excel。

您剛使用從 Word 中的 Copilot 建立的數據，以在 Excel 中將其可視化。 在下一個練習中，您將繼續在 Outlook 中使用 Copilot 來撰寫及傳送您已完成工作的電子郵件。

## 使用 Copilot 撰寫電子郵件

您已建立一些抵押品，以協助您開始業務。 現在是時候與尋求一些創業資金的投資者接觸了。

1. 在已安裝 Microsoft 365 應用程式的電腦上，開啟 **Outlook**。 如果您尚未使用 Microsoft 365 帳戶設定 Outlook，請參閱[設定和使用 Outlook - Microsoft 支援服務](https://support.microsoft.com/office/set-up-and-use-outlook-4636f361-d5e3-4a87-9cd4-382858de55fa)。
1. 開啟 **新的 Outlook** 體驗。 若要取得 Outlook 中最新的 Copilot 功能，您應該使用「新增 Outlook」體驗。 若要查看您使用哪個版本，請參閱[我有哪些 Outlook 版本？ - Microsoft 支援服務](https://support.microsoft.com/office/what-version-of-outlook-do-i-have-b3a9568c-edb5-42b9-9825-d48d82b2257c)。
1. 建立新的電子郵件，並使用您自己的電子郵件地址填入 **[收** 件者] 方塊。
1. 您可以從 [Copilot] 窗格開始起草您的電子郵件，或從電子郵件本文的右側開始草稿：

    ![Outlook 的螢幕快照，以及使用 Copilot 起草電子郵件的選項。](./media/generative-ai/copilot-draft-email-outlook.png)
    
1. 輸入下列提示，並將音調調整為「正式」，並將長度調整為「中」：

    ```
    Request a meeting with an investment bank to discuss funding for a commercial cleaning business.
    ```

    ![在 Outlook 中使用 Copilot 起草電子郵件的螢幕快照。](./media/generative-ai/copilot-draft-email-adjust-tone-outlook.png)

1. 選取 [ **產生草稿**]，然後檢閱產生的輸出。 調整語氣，或告訴 Copilot 您想要變更電子郵件的內容。

    ![Outlook 中 Copilot 產生之電子郵件的螢幕快照。](./media/generative-ai/copilot-draft-email-results-outlook.png)

1. 如果您想要的話，您可以將電子郵件傳送給自己！

## 使用 Copilot 建立簡報的內容

在科皮洛特的協助下，您已為清潔業務構想建立了業務計劃草案，並準備了一些財務預測，並傳送電子郵件來要求與潛在投資者會面。 現在您將需要有效的簡報，以傳達您企業的優點。

1. 開啟 **PowerPoint** 並建立新的 **空白簡報**。 如果 [設計工具] **** 窗格自動開啟，請關閉它。

    ![在PowerPoint中建立新空白簡報的螢幕快照。](./media/generative-ai/powerpoint-create-blank-presentation.png)

1. 將簡報儲存為 **OneDrive 資料夾中的清除Company.pptx** 。
1. **在功能區的 [首頁 **] 索引卷標中**選取 [Copilot] 按鈕**，選取 **[關於建立簡報...**]，然後在 [Copilot] 窗格中完成提示，如下所示：

    ```
    Create a presentation about a corporate cleaning service in New York City.
    ```

1. Copilot 會在簡報中產生投影片。  此程式可能需要幾分鐘的時間，您的輸出看起來應該會像這樣，其主題不同：

    ![Copilot 從 Word 檔建立的 PowerPoint 簡報螢幕快照。](./media/generative-ai/copilot-powerpoint-create-image.png)

1. 選取簡報中的第二張最後一張投影片。 然後，在 [Copilot] 窗格中，要求使用此提示新增投影片：

    ```
    Add a slide that describes the benefits of an eco-friendly approach to cleaning. 
    ```

    ![PowerPoint 簡報建立新投影片的螢幕快照。](./media/generative-ai/copilot-powerpoint-add-new-slide.png)

1. 儲存簡報。

## 挑戰

現在您已瞭解如何在幾個不同的應用程式中使用 Copilot for Microsoft 365 來研究想法並產生內容，為什麼不嘗試進一步探索？ 請嘗試使用科皮洛特計劃活動，以促進當地圖書館的兒童識字。 您可以嘗試的一些事項包括：

- 研究鼓勵兒童在早期閱讀的一些秘訣。
- 建立事件的傳單或海報。
- 撰寫一封電子郵件，邀請當地兒童作者在活動上發表演講。
- 建立簡報以啟動事件。

盡可能有創造力，並探索 Copilot 如何透過尋找資訊、產生和精簡文字、建立影像和回答問題來協助您。

## 結論

在此練習中，您已使用 [Copilot for Microsoft 365](https://www.microsoft.com/microsoft-365/enterprise/copilot-for-microsoft-365) 來尋找資訊併產生內容。 希望您已瞭解如何在 Copilot 中使用產生 AI 來協助提高生產力和創造力。 Microsoft 365 可讓您將產生 AI 的強大功能帶入商務數據和程式，同時整合至現有的 IT 基礎結構，以確保可管理且安全的解決方案。
