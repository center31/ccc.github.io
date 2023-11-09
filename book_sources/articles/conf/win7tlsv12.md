# Windows 7 啟用 TLS 1.2
---

## 參考 https://support.microsoft.com/zh-tw/topic/c4bd73d2-31d7-761e-0178-11268bb10392
## 摘錄必要部分
- 1. 前題確認您的 Windows 7 版本, 系統類型為何
    - 確認 "Windows 版本" 部分是否包含 "Service Pack 1"
        - 若無, 請手動下載安裝 Service Pack 1, 請依據系統類型, 64位元請下載x64字樣版本; 32位元下載無x64字樣版本
    - 確認 "系統區塊" 部分, 系統類型為 64 or 32 位元, 等等會用到
        - How: [我正在執行哪個版本的-windows-作業系統](https://support.microsoft.com/zh-hk/windows/我正在執行哪個版本的-windows-作業系統-628bec99-476a-2c13-5296-9dd081cdd808#WindowsVersion=Windows_7)
- 2. 安裝 KB3140245
    - https://catalog.update.microsoft.com/search.aspx?q=kb3140245
        - 請依據系統類型, 64位元請下載x64字樣版本; 32位元下載無x64字樣版本
- 3. 執行簡易修正程式, https://download.microsoft.com/download/0/6/5/0658B1A7-6D2E-474F-BC2C-D69E5B9E9A68/MicrosoftEasyFix51044.msi
- 4. 啟用SCHANNEL TLS 1.2
    - 開始 > 於搜尋輸入"powershell" > 於 "Windows PowerShell" 點滑鼠右鍵 -> 以管理管理員身份執行 -> 是
    - 執行以下指令, 請1行1行複製貼上, 請小心注意是否完整, 是否產生錯誤
        - $regTLS12 = "HKLM:SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2\Client"
        - $regTLSDefault = "DisabledByDefault"
        - $regTLSValue = "0x00000000"
        - New-Item -Path $regTLS12 -Force | Out-Null
        - New-ItemProperty -Path $regTLS12 -Name $regTLSDefault -Value $regTLSValue -PropertyType DWORD -Force | Out-Null
- 5. 重開機後, Outlook 若設定正確應可啟用
    - 若仍無法, 請參考 Outlook 設定文件