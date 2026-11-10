# GitHub 新手入门路径：从「登录进来不知道点哪」到「会找、会下、会存档」

> 定位：零基础、英文界面、只打算用浏览器（先不装任何软件）。
> 近期目标：**会用 GitHub 找资源、下工具、看教程**。远期才会自己写项目。
> 所以顺序是：先学「读」和「取」，再学「写」。

---

## 0. 先认清一件事（决定你别在哪浪费时间）

**GitHub 不是网盘，也不是论坛。** 它是**带存档点的文件夹**（版本控制）＋**公开的协作广场**（Issue / PR）。

三个词讲透，剩下的都是它俩的组合：

| 概念 | 英文 | 类比 | 一句话 |
|---|---|---|---|
| 仓库 | Repository (repo) | 一个项目文件夹 | 一个项目 = 一个仓库，里面有代码、文档、历史 |
| 提交 | Commit | 游戏存档点 / 文件夹快照 | 每改一次并"提交"，就留一个可回退的存档，带一句说明 |
| 分支 + 合并请求 | Branch + Pull Request (PR) | 草稿副本 → 申请合进正文 | 不敢直接改主线？复制一条分支改，改完发 PR 请求合回去 |

> 记住一句话就够了：**仓库装东西，提交记历史，分支+PR 管"谁改了什么、要不要收"**。
> 你在仓库页上看到的 `12,345 commits`、`230 branches`、`56 Pull requests`，就是这三样东西的计数器。

**为什么要懂一点"写"？** 因为你"找资源"时天天会撞见它们：README 里的"欢迎 PR"、Issue 里别人报的 bug、Releases 里的版本号。只会下载、看不懂上下文，就没法判断一个项目是不是还能用。

---

## 1. 你的起点：现在这个页面在说什么

你现在登录的是 `kid0731422`，0 仓库、0 Issue、0 PR —— 这不是"账号有问题"，是最干净的起点。

2026 年的新版 Dashboard（跟你截图一致，随版本会变）：

| 位置 | 是什么 | 小白要不要管 |
|---|---|---|
| 左上 `Home` / `Feed` | Home = 你的工作台；Feed = 你 Star / 关注的人的最新动态 | Feed 以后很有用（类似订阅） |
| 顶部搜索框（写着 `Type / to search`） | 全局搜索，按 `/` 直接聚焦 | **最该练的地方**，见第 6 章 |
| 右上 `+` | 新建仓库 / Issue / gist / 导入仓库 / codespace | 建仓库就在这 |
| 右上铃铛 | 通知（被 @、被回复、Watch 的仓库有动静） | 先不用 |
| 右上头像 | Your repositories / Your stars / Settings | Stars 在这里找 |
| 中间那排 `Ask / Debug / Agent / Create issue / Write code` | 2026 新加的 AI 助手入口 | **先全部忽略**，别被它吓到 |
| 右侧 Universe'26 / Changelog | 官方活动与更新日志 | 不用管 |

> 界面语言是英文：Edge 里右键 → "翻译成中文"最省事；也可以在 `Settings → Appearance` 里找界面语言选项（有就切，没有就用浏览器翻译）。

---

## 2. 第一课：先认 5 个地方（5 分钟）

1. **github.com/explore** —— 逛。没目标时的入口。
2. **顶部搜索框** —— 有目标时的入口。按 `/` 聚焦。
3. **一个仓库页** —— 你以后 80% 的时间待在这。
4. **右上 `+` → New repository** —— 你自己的东西放哪。
5. **头像 → Your stars** —— 你收藏的东西在哪。

就这 5 个。其余的（Actions、Projects、Codespaces、Copilot）一年后再看也不迟。

---

## 3. 第二课：读懂一个仓库页（最重要的 15 分钟）

打开任意仓库，从上往下是固定的骨架：

```
┌ owner/repo  Public                    Watch  Fork  Star ─┐  ← 身份与三个动作
│ <Code>  <Issues 12>  <Pull requests 3>  <Discussions>     │  ← 四个标签页
├──────────────────────────────────────────┬───────────────┤
│ 文件列表（README.md 排最前，自动渲染在下面）│ About 栏      │
│ src/  docs/  LICENSE  ...                 │  简介/官网     │
│                                           │  Topics 标签   │
│ ── README 正文（项目说明书）──────────────│  License      │
│                                           │  Releases  v2 │
│                                           │  语言构成条    │
│                                           │  Contributors │
└──────────────────────────────────────────┴───────────────┘
```

逐块记：

| 区块 | 你要看什么 | 判断价值 |
|---|---|---|
| **README** | 这是什么、怎么装、怎么用、截图 | **先读它**，90% 的答案在这 |
| **About 右侧栏** | 一句话简介 + 官网链接 + Topics 标签 | 判断分类对不对 |
| **语言构成条** | Python 78% / C++ 12% … | 一眼看出是什么技术栈 |
| **Star 数** | 收藏数，近似"有多少人觉得有用" | 上千通常意味着文档/生态不差 |
| **Fork 数** | 被别人复制走改的数量 | 高 = 被当基础项目用（不是"下载量"） |
| **Watch** | 订阅通知（All / Participating / Ignore / Custom） | 想跟进再开，别乱开 |
| **Issues** | 用户报的 bug 和需求 | **看最近有没有人回**，比 Star 更能说明活不活 |
| **Pull requests** | 待合入的改动 | 有活跃 PR = 项目在推进 |
| **Releases** | 作者打包好的成品（exe/安装包/压缩包） | **想"用"就下这个** |
| **Commits / 最后提交时间** | 最近一次改动时间 | 两年没动的项目，慎重 |
| **License** | MIT / Apache-2.0 / GPL-3.0 / 无 | **商用前必看**，无 License = 默认保留所有权利 |

> 一句话判断法：**README 写得清楚 + 半年内有提交 + Issues 有人回 + License 明确 = 能用**。

---

## 4. 第三课：三种「拿到本地」的方式（别搞混）

| 方式 | 入口 | 你拿到什么 | 适合 | 缺点 |
|---|---|---|---|---|
| **Releases 附件** | 右栏 `Releases` → 点版本 → `Assets` 下的 `.exe/.zip/.dmg` | 作者**编译好的成品** | 只想用，不想碰代码 | 版本可能旧；来路要自己判断 |
| **Download ZIP** | 绿色 `<Code>` 按钮 → `Download ZIP` | 源码**快照**（没有 `.git`，不能 `pull` 更新） | 想读代码 / 小改一下 / 交作业 | 不能更新，不能参与协作 |
| **git clone** | `<Code>` 里复制 HTTPS 地址，本地 `git clone 地址` | **完整仓库**（含全部历史） | 长期跟进、要改代码、要提 PR | 得先装 Git |

**三个常见误解：**

- **Star ≠ 下载**。Star 只是收藏 + 点赞，不会把任何文件存到你电脑上。
- **Fork ≠ 下载**。Fork 是把别人的仓库**复制一份到你自己的账号下**（网页上的副本），用来改完发 PR。
- **Download ZIP ≠ clone**。ZIP 是一张"照片"，clone 是一条"能继续长的分支"。

> 安全提醒：`.exe` 只从**官方 Releases** 下；看作者是不是项目主人、Star 量级、有没有签名。来路不明的"加速下载站""破解版"一律不碰。

---

## 5. 第四课：收藏与整理（不然找过就忘）

| 功能 | 在哪 | 作用 | 用法建议 |
|---|---|---|---|
| **Star** | 仓库页右上 | 收藏 + 给作者鼓励 | 看到有用的就点，别犹豫 |
| **Lists** | `github.com/stars/你的用户名` → 建 List | 给 Star 分类 | 建 3 个：`工具` / `学习` / `以后再看` |
| **Watch** | 仓库页右上 | 收这个仓库的通知 | 只对"我要跟进"的开；其余 Ignore |
| **Follow** | 用户主页 | 关注某个人 | 关注几个靠谱的作者，Feed 会变好看 |
| **Feed** | 左上 | 你 Star / 关注的人的动态 | 每天扫一眼，比刷短视频有用 |

**四个"逛"的入口，别混：**

| 入口 | 地址 | 解决什么 |
|---|---|---|
| Explore | `github.com/explore` | 总入口，编辑推荐 + 热门 |
| Topics | `github.com/topics` | 按**主题**找（如 `finite-element`、`live2d`） |
| Trending | `github.com/trending` | 按**时间**看今天/本周/本月最热 |
| Collections | `github.com/collections` | 官方打包的专题合集 |

---

## 6. 第五课：搜索（真正拉开差距的地方）

点搜索框（按 `/`）→ 输入关键词 → 回车。左边还能切：`Repositories` / `Code` / `Issues` / `Pull requests` / `Discussions` / `Users`。

**限定符速查（写在关键词后面，空格分隔）：**

| 限定符 | 例子 | 作用 |
|---|---|---|
| `language:` | `language:python` | 只要某个语言 |
| `topic:` | `topic:live2d` | 只要某个主题标签 |
| `stars:` | `stars:>500` | 星数门槛（过滤玩具项目） |
| `pushed:` | `pushed:>2025-06-01` | 最近还在更新 |
| `in:name` / `in:readme` | `in:readme 教程` | 限定匹配位置 |
| `license:` | `license:mit` | 按许可证过滤 |
| `user:` / `org:` | `user:torvalds` | 限定作者/组织 |
| `is:issue is:open` | `is:issue is:open label:bug` | 搜 Issue |
| `label:` | `label:"good first issue"` | 新手友好的 Issue |

**三个马上能用的组合：**

```
topic:finite-element language:python stars:>100
```
→ 找有限元的 Python 实现，过滤掉没人用的。

```
in:readme 教程 stars:>1000 pushed:>2025-01-01
```
→ 找还在维护的教程类仓库。

```
topic:awesome language:markdown stars:>1000
```
→ 找"资源清单"（下面第 9 章会讲怎么用）。

**排序**：结果页右上角可切 `Best match` / `Most stars` / `Recently updated`。找资源用 Most stars，找新东西用 Recently updated。

---

## 7. 第六课（轻量"写"）：建仓库 → 上传 → 改 README → 提交

这一步只为了让你**看懂**别人仓库里的那些按钮，不需要你会编程。

### 7.1 建第一个仓库

1. 右上 `+` → **New repository**
2. `Repository name`：`github-notes`（名字只能英文/数字/`-`/`_`）
3. 选 **Public**（公开；免费账号的私有仓库也免费，但公开才能被搜索到、才能当作品集）
4. 勾 **Add a README file**（省得建一个空壳）
5. `Create repository`

### 7.2 上传一个文件（= 一次提交）

1. 仓库页 → `Add file` → **Upload files**
2. 把本地文件拖进去（比如这份笔记）
3. 底部 `Commit changes` 里的说明写：`添加第一份学习笔记`
4. **Commit changes**

> 每一次"Commit changes" = 一个存档点。GitHub 会记下：谁、什么时候、改了什么。

### 7.3 改 README，看"存档点"长什么样

1. 点 `README.md` → 右上铅笔图标 → 改一行字
2. `Commit changes` → 写一句"补充自我介绍"
3. 回到仓库页，点文件列表上方的 `commits`（或 `History`）→ 点开刚那次提交 → 看 **Diff**：
   `+` 绿色是新增，`-` 红色是删除。
4. 想反悔：进那次提交，或点 `Revert`。

**这就是"版本控制"的全部魔法**：你随时能回到任何一个存档点，也能看到每一步改了什么。

### 7.4 Issue → 分支 → PR → Merge（可选，10 分钟）

1. `Issues` → `New issue` → 标题"补一张术语表" → 提交（这是"给自己派活"）
2. 回到 Issue 右侧 → `Create a branch`（自动建一条分支）
3. 在分支上改文件 → `Commit changes`
4. 页面会提示 `Compare & pull request` → 点它 → 写说明 → `Create pull request`
5. `Merge pull request` → 回 Issue 看：**自动关闭**了

走完这一圈，你就把第 0 章那三个词真正用了一遍。

---

## 8. 术语速查表

| 英文 | 中文 | 一句话 |
|---|---|---|
| repository / repo | 仓库 | 一个项目 |
| commit | 提交 | 一个存档点 |
| branch | 分支 | 平行草稿线 |
| main / master | 主线 | 默认分支 |
| merge | 合并 | 把分支合回主线 |
| pull request (PR) | 合并请求 | 申请把你的改动收进主线 |
| issue | 议题 | bug 报告 / 需求 / 讨论 |
| fork | 派生 | 复制别人的仓库到自己账号 |
| clone | 克隆 | 把仓库完整拉到本地（含历史） |
| release | 发布 | 作者打包的成品版本 |
| tag | 标签 | 给某个提交起的版本名（v1.0.0） |
| star | 星标 | 收藏 + 点赞 |
| watch | 关注 | 订阅通知 |
| license | 许可证 | 允许你怎么用（MIT 宽松 / GPL 传染） |
| README | 自述文件 | 项目说明书 |
| contributor | 贡献者 | 提交过代码/文档的人 |
| maintainer | 维护者 | 有权合并 PR 的人 |
| CI / Actions | 持续集成 | 自动构建/测试 |
| workflow | 工作流 | Actions 里的自动化脚本 |
| markdown | 标记语言 | README 用的写法（`#` 标题、`-` 列表） |

---

## 9. 「找资源」实战清单（你的主目标）

**先收藏这几个"清单的清单"：**

- `github.com/sindresorhus/awesome` —— 所有 Awesome 清单的总目录
- `github.com/521xueweihan/HelloGitHub` —— 中文，每月一期，专门给新手推项目（**强烈推荐从这开始**）
- `github.com/vinta/awesome-python` —— Python 生态全景
- `github.com/awesome-selfhosted/awesome-selfhosted` —— 能自己部署的软件

**判断一个项目靠不靠谱的 5 个信号：**

1. Star 量级（<50 慎用，>1000 一般有生态）
2. 最后一次提交时间（半年内活跃）
3. Open Issues 数 vs 回复情况（一堆没人回的 Issue = 弃坑或没人管）
4. License 是否明确（商用前必须看）
5. README 是否完整（有没有安装步骤、截图、常见问题）

**给新手的三个小动作：**

- 看到好项目，先 `Star` 再关页面——不然后面再也找不到。
- 想学一个方向，用 `topic:关键词` 逛 Topics 页，比乱搜准。
- 下工具前，先去 `Releases` 看**最新版本日期**和**更新日志**，别下两年前的。

---

## 10. 新手最容易踩的 6 个坑

1. **把 Star 当下载** —— 点了半天星星，本地什么都没有。
2. **下 ZIP 当安装包** —— ZIP 是源码，双击没用，得自己编译。
3. **不看 License 就商用** —— GPL 项目拿去闭源卖 = 侵权。
4. **在别人的 Issue 里问"这个怎么用"** —— Issue 是报 bug 的，问用法去 Discussions 或自己搜。
5. **公开仓库里贴 API Key / 密码** —— 一旦提交就进了历史，删掉也还在，得撤销密钥。
6. **照抄来路不明的安装命令**（`curl xxx | bash`）—— 先看清域名和内容再执行。

---

## 11. 下一步：什么时候才需要装东西

| 阶段 | 需要装 | 为什么 |
|---|---|---|
| 现在（找资源、看代码） | **什么都不用装** | 网页够用 |
| 想"改了再跑" | VS Code + Git | 编辑器 + 版本控制 |
| 不会命令行 | **GitHub Desktop** | 图形界面点鼠标提交 |
| 想长期跟进项目 | Git | `git clone` / `git pull` 更新 |

**装 Git 后只需要 4 条命令**（到时候再学也不迟）：

```bash
git clone https://github.com/owner/repo.git   # 下载完整仓库
git pull                                      # 拉取最新改动
git add . && git commit -m "说明"             # 存档
git push                                      # 推回 GitHub
```

---

## 12. 学习资源

| 类型 | 地址 | 说明 |
|---|---|---|
| 官方互动课程 | `github.com/skills` | 在 GitHub 里手把手教你用 GitHub，有徽章，**最推荐** |
| 官方文档 | `docs.github.com` | 权威，英文；搜关键词比通读强 |
| 官方入门 | `docs.github.com/get-started` | 结构化的 Getting started |
| 中文清单 | `github.com/521xueweihan/HelloGitHub` | 每月精选，新手友好 |
| 视频 | B 站搜「GitHub 入门」「Git 教程」 | 挑播放量高、有分 P 的系统课 |

---

## 附：第一小时 checklist（打印出来勾）

- [ ] 打开 `github.com/explore`，随便点 3 个仓库，只看不装
- [ ] 打开 `github.com/trending`，看今天最热
- [ ] 用 `topic:` 搜一个你感兴趣的方向
- [ ] 挑 1 个顺眼的仓库点 **Star**，去头像 → Your stars 里找到它
- [ ] 打开 1 个仓库的 **Releases** 页，分清"成品"和"源码"
- [ ] 建 1 个仓库（`github-notes`），上传这份笔记
- [ ] 改一次 README 并 Commit，打开 Diff 看一眼
- [ ] （可选）提 1 个 Issue，走完分支 → PR → Merge
