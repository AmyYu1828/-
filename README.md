#  Azure 基礎概念
![](https://i.imgur.com/77xKwPb.png)

## Microsoft Azure :
* >> 1.是微軟的公用雲端服務 (Public Cloud Service) 平台
* >> 2.是微軟線上服務 (Microsoft Online Services) 的一部份。
* >> 3.自 2008 年開始發展，2010年2月份正式推出。
* >> 4.目前全球有54座資料中心以及44個CDN跳躍點 (POP)，並且於2015年時被 Gartner 列為雲端運算的領先者。
* >> 5. 2015年度 Microsoft Azure 已包含 30 餘種服務，數百項功能，並且為微軟帶來了12億美元的獲利，目前 Azure 上的服務與功能仍然在增加中。。

>補充：
* >> 1.內容分發網路（英語：Content Delivery Network或Content Distribution Network，縮寫：CDN）是指一種透過網際網路互相連接的電腦網路系統，利用最靠近每位使用者的伺服器，更快、更可靠地將音樂、圖片、影片、應用程式及其他檔案傳送給使用者，來提供高效能、可擴展性及低成本的網路內容傳遞給使用者。
* >> 2.入網點（POP，point-of-presence）是一個將網際網路從一個地方接到其他地方的接入點。POP必需有一個唯一的網際網路協議（IP）地址。網際網路服務提供商（ISP）或在線服務提供商（如美國在線）在網際網路上有一個入網點，有時可能不止一個。網際網路服務提供商（ISP）或在線服務提供商所有的入網點數量，有時被用來作為衡量其規模和增長速度的標準。實際上，入網點（POP）可能安裝在電信運營商（如Sprint）所有的租用空間中，網際網路服務提供商可以租借這些空間來提供服務。入網點通常包括路由器、數字模擬電話集合器、伺服器和幀中繼或ATM交換機。




## 接下來即將介紹 :
### 1.雲端運算的基礎概念
### 2.Azure 實作概念
### 3.資源移轉至雲端運算環境
----

### 1.雲端運算的基礎概念
#### 什麼是雲端服務模型
 >**型號IaaS**
 >定義：基礎結構即服務
* >>IaaS 是最具彈性的雲端服務類別。 
* >>它旨在讓您完整控制執行您應用程式的硬體。(有 IaaS，您不用購買硬體了)
* >>用多少付多少為基礎，提供企業運算資源，包括伺服器、網路、儲存及資料中心空間。

 >**型號PaaS**
 >定義：平台即服務
* >>專注在應用程式開發。
* >>平台管理是由雲端提供者處理的。 
* >>提供支援建置與交付 Web 型（雲端）應用程式的完整生命週期所需的一切。
>**型號SaaS** 
>定義：軟體即服務
* >> SaaS是為您和使用者或客戶集中裝載和管理的軟體。
* >> 通常應用程式的一個版本會用於所有客戶，並透過每月或每年訂閱進行授權。
* >> 雲端應用程式（或軟體即服務）透過網際網路和（通常是）Web 瀏覽器，在「雲端」中其他人所擁有與運作且連接到使用者電腦的遠端電腦上執行。



| 型號 | IaaS 基礎設施即服務 ( Infrastructure as a Service)     | PaaS 平臺即服務 ( Platform as a Service )  |SaaS 軟體即服務 ( Software as a Service )|
| -------- | -------- | -------- |-------- |
| 說明     | 此雲端服務模型最接近管理實體伺服器；雲端提供者會將硬體保持在最新狀態，但是作業系統維護與網路設定會留給雲端租用戶。 例如，Azure 虛擬機器是在 Microsoft 資料中心內執行的完全運作虛擬計算裝置。 此雲端服務模型其優勢為可快速部署新的計算裝置。 設定新的虛擬機器會比採購、安裝及設定實體伺服器快很多。    | 此雲端服務模型是受控的主控環境。 雲端提供者負責管理虛擬機器與網路資源，而雲端租用戶則負責將應用程式部署到受控的主控環境。 例如：Azure App Service 提供受控的主控環境，讓開發人員可於該處上傳其 Web 應用程式，而無須擔心實體硬體與軟體需求。 |在此雲端服務模型中，雲端提供者會管理與應用程式環境有關的所有層面，例如虛擬機器、網路資源、資料儲存體和應用程式。 雲端租用戶只需要向雲端提供者所管理的應用程式提供資料。 例如：Microsoft Office 365 提供可在雲端執行的完整 Microsoft Office 版本。 您只需要建立內容，Office 365 就會處理其他所有事項。     |


| 型號 | IaaS 基礎設施即服務 ( Infrastructure as a Service)  |PaaS 平臺即服務 ( Platform as a Service ) |SaaS 軟體即服務 ( Software as a Service ) |
| -------- | -------- | -------- |-------- |
| 優點     | 沒有 CapEx。 使用者沒有預付成本。   |沒有 CapEx。 使用者沒有預付成本。   |沒有 CapEx。 使用者沒有預付成本。    |
| 優點     | 靈活度。 可快速存取應用程式，並在需要時取消佈建。     | 有靈活度。 PaaS 比 IaaS 更為敏捷，且使用者無需設定執行應用程式所需的伺服器。   |靈活度。 使用者可快速且輕鬆地為員工提供最新軟體的存取權。     |
| 優點     | 管理性。 已套用共同責任模型；使用者管理及維護已佈建的服務，而雲端提供者會管理及維護雲端基礎結構。    | 以使用量為基礎的模型。 在 OpEx 模型下，使用者只需支付所使用及操作的內容。    |隨用隨付定價模型。 不論使用者使用軟體的多寡，都需支付訂用帳戶模型所使用的軟體 (通常是月付或年付)。    |
| 優點     | 以使用量為基礎的模型。 在營運費用 (OpEx) 模型下，組織只需支付所使用及操作的內容。    | 技能。 無須深入的技術技能就能部署、使用及獲得 PaaS 的權益。    |技能。 無需深入的技術技能就能部署、使用及獲得 SaaS 的權益。   |
| 優點     |有技能。 無須深入的技術技能就能部署、使用及獲得公用雲端的權益。 組織可使用雲端提供者的技能與專長，以確保工作負載的安全性與高可用性。    | 雲端權益。 使用者可利用雲端提供者的技能與專長，以確保其工作負載的安全性與高可用性。 此外，使用者也可以存取最新的開發工具。 其接著可在應用程式的生命週期間套用這些工具。     |彈性。 使用者可從任何地方存取相同的應用程式資料。    |
| 優點     | 雲端權益。 組織可使用雲端提供者的技能與專長，以確保工作負載安全且高度可用。    | 生產力。 因為雲端提供者會處理所有平台管理，所以使用者可只專注在應用程式開發。 因為平台是透過網際網路存取的，所以與作為服務的分散式小組共同工作會更為容易。 您可更輕鬆地讓平台供全域使用。     |-    |
| 優點     | 有彈性。 IaaS 是最具彈性的雲端服務，因為您可控制設定及管理執行應用程式的硬體。     | -    |-   |
| 缺點     | -     | 平台限制。 有一些可能會影響應用程式執行方式的雲端平台限制。 在評估哪一個 PaaS 平台最適合工作負載時，請務必考慮此區域中的任何限制。     |軟體限制。 有一些可能會影響使用者工作方式的軟體應用程式限制。 因為您正在依現狀使用軟體，所以無法直接控制功能。 在評估哪一個 SaaS 平台最適合工作負載時，請務必考慮任何商務和軟體限制。    |
- - -
>下圖是雲端服務模型裡執行的服務：
![](https://i.imgur.com/2XuK2Aq.png)
- - - 
>下圖說明雲端提供者與雲端租用戶之間的各種責任層級：
![](https://i.imgur.com/ifyJ56h.png)
- - -
#### 雲端運算模型建構
> 雲端運算有三種部署模型：「公用雲端」、「私人雲端」與「混合雲端」。 當移轉至雲端時，須考慮每個部署模型都有不同的層面。


| 部署模型 |公用雲端 | 私人雲端 | 混合式雲端 |
| -------- | -------- | -------- | -------- |
| 說明     | 服務透過公用網際網路提供，想要購買該服務的任何人都可以使用。 雲端資源 (例如伺服器與儲存體) 由協力廠商雲端服務提供者所擁有及操作，並透過網際網路傳遞。     | 私人雲端是由某個企業或組織的使用者以獨佔方式使用的運算資源所組成。 私人雲端可實際位於組織的本地 (內部部署) 資料中心，或透過協力廠商服務提供者裝載。   |混合式雲端是一種運算環境，可讓資料和應用程式在公用雲端與私人雲端之間共用，藉以結合這兩種雲端。      |
| 比較1     | 沒有會擴大的資本支出。|一開始必須購買硬體，而且之後需要維護。 |提供最大的彈性。 |
| 比較2     | 可以快速佈建及取消佈建應用程式。| 組織可以完全掌控資源與安全性。 |組織決定要執行其應用程式的位置。|
| 比較3     | 組織只需為其使用的項目支付費用。| 組織負責硬體維護及更新。  |組織控制安全性、合規性或法律需求。 |

#### 雲端運算的優勢
>相較於實體環境，雲端環境有幾個優勢?


| 高可用性 | 延展性      | 彈性      | 靈活度      | 地理位置散發     | 災害復原          |
| -------- | ------------- | ------------- |------------- | ------------- | ------------- |
| 視所選的服務等級協定 (SLA) 而定，雲端式應用程式可提供持續的使用者體驗，即使發生問題，也不會有任何有感的停機。 | 雲端中的應用程式可透過「垂直方式」及「水平方式」進行縮放。| 您可設定雲端式應用程式利用自動縮放，以讓應用程式一律擁有所需要的資源。| 在應用程式需求變更時，快速部署及設定雲端式資源。    | 您可將應用程式與資料部署到世界各地的區域資料中心，藉此確保客戶在其區域中一律擁有最佳效能。 |利用雲端式備份服務、資料複寫與地理位置散發，您知道如果發生災害，資料會很安全，所以可放心地部署應用程式。 |
>>補充:
>>延展性：雲端中的應用程式可透過「垂直方式」及「水平方式」進行縮放：
* >>透過新增虛擬機器的 RAM 或 CPU 進行垂直縮放，以增加計算容量。
* >>透過新增資源的執行個體 (例如在設定中新增 VM) 進行水平縮放，以增加計算容量。

#### 資本支出與營運費用
* >**資本支出 (CapEx)** ：是預先在實體基礎結構上花費，然後經過一段時間後再扣除這筆預先費用。 CapEx 的預付成本價值會隨著時間而降低。
* >**營運費用 (OpEx)** ：是服務或產品的花費，且目前正在支付這筆費用。 您可在花費的同一年扣除此費用。 因為您會在使用服務或產品時支付，所以無預付費用。
 
* >>當公司行號擁有雲端基礎結構時，會購買進入其資產負債表的設備作為資產。 因為已進行資本投資，所以會計會將此交易分類為 CapEx。 經過一段時間，為考慮資產的有限壽命，會對資產進行折舊或攤提。

* >>另一方面，雲端服務會因**使用量模型**分類為 OpEx。 沒有資產可供公司行號攤銷時，雲端服務提供者 (Azure) 會管理與實體設備購買及生命週期建立關聯的成本。 因此，OpEx 會直接影響淨收益、納稅收入與資產負債表上相關聯的費用。

* >>總而言之，CapEx 需要大量的預付財務成本，還須持續維護與支援費用。 
* >>相較之下，OpEx 是以使用量為基礎的模型，只會負責其所使用的運算資源成本。
* >>雲端運算是以使用量為基礎的模型，表示終端使用者只需支付其使用的資源。 他們使用的內容即為其所需支付費用。

#### 以使用量為基礎的模型的權益
>包括：
* >>無需預付費用。
* >>無需購買和管理使用者不一定會完全用到的昂貴基礎結構。
* >>能夠在必要時為額外的資源付費。
* >>能夠停止為不再需要的資源付費。

#### 什麼是無伺服器運算？
* >>「無伺服器運算」透過排除開發人員管理基礎結構的需求，使其能夠更快速地建置應用程式。 
* >>有了無伺服器應用程式，雲端服務提供者可自動佈建、調整及管理執行程式碼所需的基礎結構。 
* >>無伺服器架構可隨需調整，且為事件驅動，僅會在發生特定函式或觸發程式時使用資源。




### 參考資料
- - - 
https://zh.wikipedia.org/wiki/Microsoft_Azure#cite_note-3
https://zh.wikipedia.org/wiki/%E5%85%A7%E5%AE%B9%E5%82%B3%E9%81%9E%E7%B6%B2%E8%B7%AF
https://zh.wikipedia.org/wiki/POP%E7%BD%91%E7%BB%9C%E6%9C%8D%E5%8A%A1%E6%8F%90%E4%BE%9B%E7%82%B9
https://accord-tec.com.tw/iaas%e3%80%81paas%e3%80%81saas-%e5%93%aa%e7%a8%ae%e9%81%a9%e5%90%88%e6%82%a8%e7%9a%84%e9%9c%80%e6%b1%82/
https://medium.com/@stfk1105/iaas-paas-saas-%E4%B8%89%E5%85%84%E5%BC%9F-c745dfa0cfd4
https://channel9.msdn.com/Series/Microsoft-Azure-Quickstart
- - - 
