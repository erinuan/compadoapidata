# Compado 数据报告

Compado clickid-report API 数据可视化页面。

## 功能

- 按日期查询 Compado 广告数据
- 分 campaign_id 展示回收、转化、RPC
- 开关「看kw」展示/隐藏分关键词的明细数据
- 自动翻页拉取所有数据

## GitHub Pages 访问

https://erinuan.github.io/compadoapidata/

## API 说明

接口：`https://api.compado.com/adsense/clickid-report`

参数：
- `user` / `password` — API 凭证
- `start_date` / `end_date` — 日期范围（YYYY-MM-DD）
- `page` — 页码

⚠️ Compado API 不支持 CORS，前端直接调用会被浏览器拦截。
当前方案已配置 GitHub Actions（compado-fetch.yml）定时拉取数据生成 JSON 文件，页面读取静态 JSON 避免跨域问题。
