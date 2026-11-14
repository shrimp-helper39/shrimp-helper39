# 📥 yt-dlp 视频下载小抄

yt-dlp 常用命令合集（通用版）。把 `<网址>` 换成视频链接即可。

## 基础

```bash
# 看一个视频都有哪些画质
yt-dlp -F <网址>

# 下最高画质，合并成 mp4
yt-dlp -f "bv*+ba/b" --merge-output-format mp4 <网址>

# 指定保存目录
yt-dlp -P <目录> <网址>
```

## 只下音频

```bash
yt-dlp -x --audio-format mp3 <网址>
```

## 播放列表

```bash
# 只下列表里的第 1、3、5 条
yt-dlp --playlist-items 1,3,5 <列表网址>
```

## 需要登录的站点

```bash
# 用浏览器导出的 cookies 文件过验证
yt-dlp --cookies cookies.txt <网址>
```

## 走代理

```bash
yt-dlp --proxy http://127.0.0.1:<端口> <网址>
```

## YouTube 专用提醒

```bash
# 新版 YouTube 需要 JS 运行时解签名，装好 Node.js 后加上这个参数
yt-dlp --js-runtimes node <网址>
```

## 字幕

```bash
yt-dlp --write-subs --sub-langs "zh.*,en.*" <网址>
```
