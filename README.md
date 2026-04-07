# 📰 政经要闻早报（云端版）

每天自动运行，生成早报并推送到微信。

## 🚀 快速部署

### 1. 准备微信推送
1. 访问 [Server酱官网](https://sct.ftqq.com/)
2. 用 GitHub 账号登录
3. 获取 SendKey（类似 `SCTxxxxxxxxxxxxx`）

### 2. 创建 GitHub 仓库
1. 创建新仓库 `morning-report`
2. 上传本项目所有文件
3. 进入仓库 Settings → Secrets → New repository secret
4. 添加 `SEND_KEY`，值为上一步获取的 SendKey

### 3. 启用 Actions
- 首次推送后，GitHub 会自动创建分支并运行
- 可以在 Actions 页面查看运行日志

## ⏰ 运行时间
- 自动：每天 23:45 UTC（即北京时间 7:45）
- 手动：点击仓库 Actions → "政经要闻早报" → Run workflow

## 📱 推送效果
每天会收到两条微信推送：
1. 摘要版（300字以内，快速浏览）
2. 详情版（完整早报）

## 🛠️ 自定义
- 修改 `main.py` 中的新闻源逻辑
- 调整 `.github/workflows/morning-report.yml` 中的定时任务
