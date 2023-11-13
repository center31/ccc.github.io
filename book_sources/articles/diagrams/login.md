```mermaid
graph TD
subgraph SOP
C -->|成功| D{身份確認}
A{問題} -->B[Webmail登入失敗]
B -->C{使用email帳號登入Portal測試}
C -->|失敗| E[密碼錯誤]
A -->F["第三方軟體登入失敗\n(e.g.Outlook, GMail, thunderbird)"]
F -->G{登入Webmail測試}
G -->|成功| H[第三方軟體設定錯誤]
G -->|失敗| C
D -->X[在校生、在職教職員]
D -->Y[畢業生、退休教職員]
X -->I[濫用鎖定]
Y -->M{6個月未曾收信}
M -->|是| K[請洽客服查詢帳號狀態]
M -->|否| I
I -->J[變更密碼後自動解除鎖定]
end
subgraph Action
E -->Z1([#1])
H -->R([#2])
J -->L([#3])
K -->NL([#4])
end
```

<br>

---

<br>

- #0, 第三方軟體:e.g. PC(Outlook, thunderbird), GMail, Outlook.com

- #1, 忘記密碼:
    - 若有在 Portal 有綁定"計中帳號"的備用電子信箱, 可透過備用電子信箱設定密碼: https://portal.ncu.edu.tw/reset-password
    - 若無, 則透過以下說明變更密碼: https://www.cc.ncu.edu.tw/page/account_password

- #2, [第三方郵件軟體設定](../articles/config.md)

- #3, 變更密碼:
    - https://portal.ncu.edu.tw/my/profile/password
    
- #4, 客服:
    - 計中服務櫃台, 03-4227151, 分機57555, 57566
    - Email: ncucc@cc.ncu.edu.tw
