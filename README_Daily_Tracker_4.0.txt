Daily Tracker V4 更新说明

本次在 V3 基础上增加：
1. 日报 PNG 自动生成预览：每天 23:00 结算后，应用会根据已保存的日报数据生成图片预览；如果 23:00 时应用被 iOS 挂起或关闭，下次打开并完成补结算后生成预览。
2. 保存与分享：点击“生成 / 保存日报图片”，iPhone 支持时会调用系统分享菜单，可选择存储图像或微信；不支持文件分享时会尝试下载 PNG。电脑浏览器直接下载 PNG。
3. 历史日报：通过“查看历史日期”选择有记录的日期，预览并重新生成该日 PNG。历史日报使用结算时保存的分类名称、颜色和时长。

上传方法（GitHub Pages）：
1. 打开 GitHub 仓库 daily-tracker。
2. 进入 Add file -> Upload files。
3. 将本压缩包中的 index.html 和 sw.js 上传并覆盖仓库同名文件。其他文件（manifest.webmanifest、icon-192.png、icon-512.png 等）不要删除。
4. 点击 Commit changes，等待 GitHub Pages 部署完成。
5. iPhone 用 Safari 打开 https://andy-011129.github.io/daily-tracker/ 并刷新，再关闭并重新打开主屏幕上的 Daily Tracker。

重要说明：
- 保留原 localStorage 键 dailyTracker.v1，兼容 V2/V3 的本地数据，不主动清除记录。不要点击“清除本机数据”。
- 每日 23:00 的结算依赖网页应用运行中的检查；iOS 可能冻结/关闭后台网页。若错过 23:00，下次打开时会按 23:00 补结算并生成日报预览。
- iOS 不允许网页应用在用户没有操作的情况下可靠地将图片写入相册。日报 PNG 会自动生成预览；点击按钮后通过系统分享菜单选择“存储图像”或微信分享。
- 数据仅保存在本设备浏览器 localStorage，不会上传或跨设备同步。不要清除 Safari 网站数据、卸载或移除主屏幕网页应用，否则可能丢失本地记录。
