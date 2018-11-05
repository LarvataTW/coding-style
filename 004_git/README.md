## Git

0. 依照專案類型建立適當的 .gitignore。
0. Branch 名稱保持全小寫英文 (a-z)、減號 (-)、數字 (0-9)。
0. Branch 名稱的英文單詞使用減號 (-) 連接。
0. __嚴格遵守 git-flow 流程。__

* git-flow 分：git-flow, git-flow-avh 目前公司內部還沒有定論 ...

### Git Branch 命名原則

#### 使用 scoped-branch-name 樣式

使用 scoped branch name 是理想且合理的命名方式，亦即在分支名中使用 `/`。

* 重構的 branch 一律以 refactor/ 為前綴開頭
* 程式整理的 branch 一律以 syntax_enhancement/ 為前綴開頭
* 套件升級及相關設定的 branch 一律以 upgrade/ 為前綴開頭

範例：
- `feature/my-awesome-feature`
- `fix/issue-666`
- `release/0.1.0`

**note:** git-flow 也採用此法來命名分支。

#### 分支 section 使用 url-friendly 字元

建議使用 `/[a-zA-Z0-9-]+/` 作為 `feature/{placeholder}` 分支使用之字元，並應具有合理語意、且**動詞**一律採用**現在簡單式**。

命名邏輯範例：

- **IF** 有相關 issue/pull-request/redmine-issue
  - **issue**
    後綴採用 `issue-%d` 格式；例如 `fix/issue-26`
  - **pull-request**
    後綴採用 `pr-%d` 格式；使用例為 patch some problems derivative from another pull-request
  - **redmine-issue**
    後綴採用 `redmine-%d` 格式；例如 `feature/redmine-20324`
- **ELSE**
  - 採用直接關係功能導向語意作為命名方向，範例：
    - `feature/update-footer-copyright`
    - `feature/drop-contact-page`
    - etc.

#### 確保主要分支前綴命名列舉

使用如：

- `master`
- `develop`
- `feature`
- `hotfix`
- `release`
- ...

等，建立一套分支前綴作為第一原則。

#### 其它

如團隊引用 github-flow，討論是否採用 username-scoped-branch-name 配合 pull-request 作為主要分支命名方式

### Commit 命名原則

- 方便往後了解演變，單一 commit 完成單一主旨
- 如果有相關的 issue 需以 refs #issue 編號為前綴開頭

