# GxxM2 — 传奇 GXX 引擎源码库（林婉儿 fork 维护版）

> 本仓库为 **林婉儿**（GitHub: [wanerlin](https://github.com/wanerlin)）从上游 fork 的维护副本。
> 上游仓库：[Mufeisi/GxxM2](https://github.com/Mufeisi/GxxM2)

## 📌 这是什么

一套完整的 **GXX 引擎源码**（Pascal / Delphi 编写），包含服务端与客户端全套模块：

- `Source/` — 主引擎源码
  - `M2Engine/` — 游戏引擎核心
  - `GameCenter/` — 游戏中心服务
  - `DBServer/` — 数据库服务
  - `LoginGate/`、`LoginSrv/`、`RunGate/`、`SelGate/` — 网关与登录服务
  - `Client-HGE/` — HGE 客户端引擎
  - `Common/` — 公共库
- `GXX.CSharp/` — C# 重制版（含 `GXX.slnx` 解决方案、`docs/`、`tests/`、`tools/`）
- `Component/` — 组件库
- `Common/` — 公共资源

## 🔄 如何与上游保持同步

本 fork 的 `main` 分支与上游 `Mufeisi/GxxM2` 的 `main` 保持关联。
如需拉取上游最新更新：

```bash
# 1. 添加上游为 remote（首次执行）
git remote add upstream https://github.com/Mufeisi/GxxM2.git

# 2. 抓取上游所有分支
git fetch upstream

# 3. 合并上游 main 到本地
#    （如果本地有专属改动，建议用 rebase 保持历史干净）
git checkout main
git merge upstream/main
# 或：git pull --rebase upstream main

# 4. 推送到本仓库
git push origin main
```

## 📂 分支策略

- `main` — 与上游同步的基线分支（不直接改业务逻辑）
- 后续新增的修改建议开独立分支（`dev-*` / `feature-*`），经测试后再合入

## 👤 维护

- 维护者：**林婉儿**（wanerlin）
- 说明：仅供技术研究与学习使用