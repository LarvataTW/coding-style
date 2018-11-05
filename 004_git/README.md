## Git

0. 依照專案類型建立適當的 .gitignore。
0. Branch 名稱保持全小寫英文 (a-z)、減號 (-)、數字 (0-9)。
0. Branch 名稱的英文單詞使用減號 (-) 連接。
0. __嚴格遵守 git-flow 流程。__

* git-flow 分：git-flow, git-flow-avh 目前公司內部還沒有定論 ...

### Git 全域設定

0. git config --global core.autocrlf true
0. git config --global core.filemode true

### Branch 命名原則

- 重構的 branch 一律以 refactor_ 為前綴開頭
- 程式整理的 branch 一律以 syntax_enhancement_ 為前綴開頭
- 套件升級及相關設定的 branch 一律以 upgrade_ 為前綴開頭

### Commit 命名原則

- 方便往後了解演變，單一 commit 完成單一主旨
- 如果有相關的 issue 需以 refs #issue 編號為前綴開頭
