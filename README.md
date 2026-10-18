# 13ft for 懒猫微服

自托管的「文章正文提取」阅读器，中文界面由上游自带（`app/locales/zh.json`）。

- 上游：https://github.com/wasi-master/13ft（MIT）
- 镜像：`ghcr.io/wasi-master/13ft:1.3.0`
- 包名：`cloud.lazycat.app.13ft`
- 端口：5000，服务名 `app`，路由 `/` → `http://app:5000`
- 中文：通过环境变量 `LOCALE=zh` 启用上游原生中文

## 构建

本仓库用 ca-x/lazycat-github-action 固定提交构建，推 tag 或手动 `workflow_dispatch` 触发。
官方商店发布开关在 `.github/lazycat-action.yml` 的 `stores.official.enabled`。
