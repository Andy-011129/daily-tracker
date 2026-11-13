Daily Tracker 2.0 更新内容
- 四个项目名称可编辑，每项最多 12 个字符。
- 颜色可从蓝、绿、橙、紫、红五种中选择。
- 可开启每日开始提醒，默认 09:00，也可修改时间。
- 停止实验、英语口语或信息输入时，自动切换到其它活动。
- 其它活动是默认兜底计时，点击自身不会停止；选择其他项目即可切换。

更新 GitHub Pages：打开仓库 -> Add file -> Upload files，将 index.html、sw.js、manifest.webmanifest 上传并覆盖同名文件，提交 Commit changes。图标无需更换。

iOS 提醒限制：网页应用在前台运行时才会检查 09:00/23:00 提醒，不能保证关闭或后台时准时通知。数据保存在本机 localStorage，清除 Safari 网站数据可能丢失。
