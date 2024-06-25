---
lab:
  title: 在 Microsoft Edge 中探索 Copilot
---
# 在 Microsoft Edge 中探索 Microsoft Copilot

在此練習中，您將探索 Microsoft Copilot 有哪些方式可使用生成式 AI 協助您在建立新內容時提高生產力。 在此練習的案例中，您將從商業構想的一些概要筆記開始著手，並在 Microsoft Edge 中使用 Copilot，以協助您研擬商務計劃和對潛在投資者的簡報。

完成此練習約需要 **40** 分鐘。

> **注意**：此練習假設您有[個人 Microsoft 帳戶](https://signup.live.com) (例如 outlook.com 帳戶)，且已用此帳戶在電腦上登入 [Microsoft Edge](https://www.microsoft.com/edge/download)。

## 使用 Copilot 探索文件及研究構想

為了開始探索生成式 AI，我們將在 Edge 中使用 Microsoft Copilot 來檢查現有的文件，並從中擷取一些深入解析。

1. 在 Microsoft Edge 中瀏覽至 [OneDrive](https://onedrive.live.com) (`https://onedrive.live.com`)，並使用您的個人 Microsoft 帳戶登入 - 關閉任何顯示的歡迎訊息或供應項目。
1. 在另一個瀏覽器索引標籤中，從 `https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx` 開啟 [Business Idea.docx](https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx) 文件。 然後，當文件在 Edge 中開啟時，選取 [將複本儲存至 OneDrive]**** 的選項，並將文件儲存在 OneDrive 的**文件**資料夾中。 文件應會隨即在 Microsoft Word Online 中自動開啟。

    > **秘訣**：若未看到將檔案複本儲存至 OneDrive 的選項，請將其下載到本機電腦。 然後，在 OneDrive 中開啟**文件**資料夾，並使用 [+ 新增]**** 按鈕，將 **Business Idea.docx** 檔案從本機電腦上傳至 OneDrive。

1. 檢視 **Business Idea.docx** 中的文字，其中描述了關於紐約市清潔業務的一些概要構想。
1. 使用 Edge 工具列上的 **Copilot** 圖示開啟 Copilot 窗格，如下所示：

    ![此螢幕擷取畫面顯示 Microsoft Edge 中的 Copilot 窗格。](./media/generative-ai/edge-copilot.png)

1. 在 Copilot 窗格中向下捲動，以查看所有必要的內容，並確定已選取 [聊天]**** 索引標籤，且交談樣式設定為 [更加平衡]**** - 這可確保 Copilot 在回應時會兼顧創造性與事實精確度。
1. 在 Copilot 窗格底部的聊天方塊中，輸入下列提示：

    ```
    What is this document about?
    ```

    如果出現提示，請確認您想要允許 Copilot 存取頁面。

1. 檢閱 Copilot 的回應，其中應該會摘錄文件中的要點，如下所示：

    ![此螢幕擷取畫面顯示含有回應的 Copilot 窗格。](./media/generative-ai/copilot-response.png)

    > **注意**：具體回應可能有所不同。

1. 輸入下列提示：

    ```
    How do I go about setting up a business in New York?
    ```

1. 檢閱回應，其中應該會包含協助您開始在紐約開展業務的建議和資源連結，並可能包含一些建議的後續提示以取得詳細資訊。

    > **重要**：AI 產生的回應以網路上的公開資訊為基礎。 雖然協助您了解開展業務所需的步驟可能有其效用，但並不保證 100% 正確，同時也無法取代專業建議的需求！

## 使用 Copilot 建立商務計劃的內容

在您進行了一些初步研究後，接著即可讓 Copilot 協助您為清潔公司擬定商務計劃。

1. 在 **Business Idea.docx** 文件仍在 Microsoft Edge 中開啟的情況下，在 Copilot 窗格中輸入下列提示：

    ```
    Suggest a name for my cleaning business
    ```

1. 檢閱建議，並選取清潔公司的名稱 (或繼續進行提示以尋找您想要的名稱)。
1. 輸入下列提示，將 *Contoso Cleaning* 取代為您選擇的公司名稱：

    ```
    Write a business plan for "Contoso Cleaning" based on the information in this document. Include an executive summary, market overview, and financial projections.
    ```

1. 檢閱回應，並在輸出底下使用**複製** (🗍) 圖示將其複製到剪貼簿。 然後，選取 **Business Ideas.docx** 文件中的所有文字，並將複製的文字貼到文件中加以取代。 最後，將回應中的初始文字 (Copilot 藉此確認了指令) 取代為清潔公司名稱的標題，以整理貼上的文字。 最後您應該會有一份商務計劃文件，如下所示：

    ![Word 文件的螢幕擷取畫面，其中包含 Copilot 產生的商務計劃。](./media/generative-ai/generated-content.png)

1. 在 Copilot 窗格中，輸入下列提示：

    ```
    Create a corporate logo for the cleaning company. The logo should be round and include an iconic New York landmark.
    ```

1. 檢閱回應，其中應該會針對 Microsoft Designer 所建立的標誌顯示四個選項。
1. 使用更多提示來反覆操作設計 (例如 `Make it green and blue`)，直到您獲得滿意的標誌。
1. 以滑鼠右鍵按一下您偏好的標誌設計，並將其複製到剪貼簿。 然後，將其貼到商務計劃文件的頂端，如下所示：

    ![Word 文件的螢幕擷取畫面，其中包含 Copilot 產生的影像。](./media/generative-ai/generated-image.png)

1. 關閉 [Microsoft Word] 索引標籤，並返回 OneDrive 中的**文件**資料夾。

## 使用 Copilot 建立簡報的內容

藉助於 Copilot，您為清潔業務構想建立了商務計劃的草案。 此時您需要一份有效的簡報，用以說服投資者提供資金來開展業務。

1. 在 OneDrive 的**文件**資料夾中，新增 **PowerPoint 簡報**。

    如果 [設計工具]**** 窗格自動開啟，請加以關閉。

1. 在簡報的標題投影片上，輸入清潔公司的名稱作為標題，並以 `Investor Opportunity` 作為子標題。
1. 使用「兩個內容」**** 投影片版面配置 (其中包含標題和兩個內容預留位置)，新增投影片。
1. 將投影片標題變更為 `Benefits of Hiring a Commercial Cleaner`。
1. 在 Copilot 窗格中，輸入下列提示：

    ```
    Write a summary of the benefits of using a corporate cleaning company for your business. The summary should consist of five short bullet points.
    ```

1. 將 Copilot 的回應複製到剪貼簿，並將其貼到左側的內容預留位置中。 然後，刪除確認要求的初始句子，並將預留位置中的文字重新格式化，直到您滿意為止。
1. 在 Copilot 窗格中，輸入下列提示：

    ```
    Create a photorealistic image of a clean office.
    ```

1. 在 Copilot 產生您想要的影像後，將其複製到剪貼簿，並貼到投影片右側的內容預留位置中。

    如果 [設計工具]**** 窗格自動開啟，請選取您想要的投影片設計。 然後，關閉 [設計工具]**** 窗格。

1. 套用任何您認為必要的其他重新格式化，直到您製作出如下的投影片：

    ![PowerPoint 簡報的螢幕擷取畫面，其中包含 Copilot 產生的內容。](./media/generative-ai/powerpoint-slide.png)

1. 在 PowerPoint 標題列上選取預設的簡報名稱 (**簡報**)，並將其重新命名為 `Business Presentation.pptx`。
1. 關閉 [PowerPoint] 索引標籤，並返回 OneDrive 中的**文件**資料夾。

## 使用 Copilot 撰寫電子郵件

您建立了一些隨附品以利展開業務。 接下來即應吸引投資者為您的新創基金注資。

1. 使用 OneDrive 標題列左側的**應用程式啟動器**，開啟 **Outlook**。
1. 建立新的電子郵件，並在 [收件者]**** 方塊中填入您自己的電子郵件地址。
1. 在 Copilot 窗格中，選取 [撰寫]**** 索引標籤。然後，設定下列選項以撰寫新內容：
    - **撰寫主題**：`Request a meeting with an investment bank to discuss funding for a commercial cleaning business.`
    - **語氣**：專業
    - **格式**：電子郵件
    - **長度**：適中
1. 選取 [產生草稿]****，然後檢閱產生的輸出。
1. 使用產生的內容完成您的電子郵件，如下所示：

    ![此螢幕擷取畫面顯示 Copilot 所產生的電子郵件訊息。](./media/generative-ai/generated-email.png)

    如果您想要的話，可以將電子郵件傳送給自己！

## 挑戰

既然您已了解如何使用 Copilot 來研究構想並產生內容，何不嘗試進一步探索？ 若要啟動新的 Copilot 工作階段，請在 [聊天]**** 索引標籤上選取提示方塊旁的 [新增主題]**** 圖示，然後嘗試使用 Copilot 規劃地方圖書館的活動，以提高兒童的讀寫能力。 可行的嘗試包括：

- 研究一些鼓勵兒童及早閱讀的技巧。
- 製作活動的傳單或海報。
- 撰寫活動的電子郵件，邀請當地的兒童讀物作家出席活動並發言。
- 建立簡報以展開活動。

請盡情發揮您的創造力，並探索 Copilot 如何藉由尋找資訊、產生並精煉文字、建立影像和回答問題，為您提供協助。


## 結論

在此練習中，您在 Microsoft Edge 中使用了 Copilot 來尋找資訊並產生內容。 希望您已了解如何在 Copilot 中利用生成式 AI 來提高生產力和創造力。

此練習中使用的免費服務當然非常強大，但您仍可使用[適用於 Microsoft 365 的 Copilot](https://www.microsoft.com/microsoft-365/enterprise/copilot-for-microsoft-365) 等服務達成更多目標；其中的 Microsoft Copilot 已整合到 Windows 和 Microsoft Office 生產力應用程式中，可為常見工作提供高度情境化的協助。 Microsoft 365 可讓您將生成式 AI 的強大功能導入商務資料和程序中，同時整合至您現有的 IT 基礎結構，以確保解決方案易於管理且安全無虞。