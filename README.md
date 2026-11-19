# boc-aud-monitor-cron

每 5 分钟调用一次 [中行澳元牌价监控](https://boc-aud-monitor.vercel.app) 的 `/api/check` 接口，
由它抓取中国银行最新牌价、记录历史，并在澳元下跌时向已订阅的手机发送推送提醒。

本仓库只有这一个定时任务文件，不含应用代码。校验密钥保存在仓库的 Actions Secrets 中（`CHECK_SECRET`）。
