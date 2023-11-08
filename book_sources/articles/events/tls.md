# NCU Mail 伺服器連線安全性強化作業
---
因應資安法, NCU Mail 即日起執行伺服器連線安全性強化作業。

## **NCU Mail 將僅支援 TLS 1.2(含) 以上的加密連線;**
---
若您使用舊版本軟體、或未設定加密連線, 將無法使用 NCU Mail。
若您的 NCU Mail 會受到影響, 您將會收到通知; 
請依照下列相關說明, 檢查您的設定。

## 立即檢查您的加密連線是否已啟用
---
### 使用 GMail, 請參考以下文件檢查是否已啟用加密連線:
- [GMail Configuration Check ](/articles/events/gmailtls.md)
- 需求: 您需要記得您 NCU Mail 的密碼, 因為 GMail 會要求您再次輸入
- 變更密碼/忘記密碼: [https://www.cc.ncu.edu.tw/page/account_password](https://www.cc.ncu.edu.tw/page/account_password)

### 我的 Windows 版本是?
- 打開 檔案總管, 於左側使用滑鼠右鍵點選"本機" -> "內容", 即可得知 Windows 版本
- 請使用 Microsoft 支援中的 Windows 10/11
- Microsoft 已不支援 Windows 8.1(含) 之前的 Windows 版本
- for Windwos 7 使用者, [Windows 7 啟用 TLS 1.2](/articles/events/win7tlsv12.md)

### 我的 Outlook 版本是?
- 打開 Outlook, 於左上角點選"檔案" -> "Office 帳戶", 即可得知 Outlook 版本

### 使用 Outlook 2021, 請參考以下文件檢查是否已啟用加密連線:
#### [Outlook 2021 Configuration Check](/aiticles/events/outlook2021tls.md)

#### 使用 Outlook 2019/2016, 請參考以下文件檢查是否已啟用加密連線:
  - [Outlook Configuration Check](/aiticles/events/outlook2019tls.md)

#### 使用 iOS, 請參考以下文件檢查是否已啟用加密連線:
  - [IOS Configuration Check](/articles/events/iostls.md)

#### 使用其它的客戶端軟體:
- google: 軟體名稱 + "啟用tls"
- 並參考 [NCU Mail 的設定](/articles/config.md)


### 若您使用以下軟體, 將無法使用 NCU Mail
---
- Windows 8.1 (含)、Outlook 2013 (含)、Live Mail 2012 (含)前的版本, Microsoft 皆已終止支援, 請勿使用。
  - Windows 8 (含) 前的作業系統用瀏覽器開啟 NCU Mail 可能出現「無法顯示此網頁」的錯誤畫面。
  - Outlook 2010 (含) 前的版本可能出現「連線失敗」的警示。

- 未更新的瀏覽器。

> 若要使用 NCU Mail, 請儘速升級作業系統/Outlook/瀏覽器。
