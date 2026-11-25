# 古筝社团招新网站（work2.html）

一个基于纯 HTML + CSS + 少量 JavaScript 的古筝社团招新静态网站，根据课程上机作业 `work2` 的要求制作，包含背景音乐、导航跳转、活动安排表格、风采展示（图片/视频/音频）、社员故事与在线报名表单。

## 文件结构

```
guzheng-club-website/
├── index.html          # GitHub Pages 入口，自动跳转到 work2.html
├── work2.html          # 招新主页面（核心交付文件）
├── club_intro.html     # 活动安排专题页（从主页面可跳转，含返回链接）
├── music.mp3           # 背景音乐（左上角点击播放）
├── movie.mp4           # 风采展示视频
├── movie.mp3           # 视频配套音频
├── h3.png / h4.png / h5.png   # 风采展示图片：初识古筝 / 雅集现场 / 舞台展演（点击跳转专题页）
└── README.md           # 本说明文档
```

## 功能对照（作业 7 项要求）

1. **背景音乐**：页面左上角固定按钮，点击切换播放 / 暂停（`music.mp3`，循环播放）。
2. **导航跳转**：顶部五个锚点链接——社团简介｜活动安排｜风采展示｜社员故事｜在线报名，每个版块底部均有“返回顶部”。
3. **古筝简介**：完整社团介绍文案。
4. **活动安排表格**：标题跨 4 列（`colspan=4`）、表头居中，且“新成员见面会”与“古筝基础教学公开课”通过 `rowspan` 合并在同一教室（艺术楼 301），满足跨多行跨多列要求。
5. **风采展示**：三张与文案匹配的国风配图（`h3/h4/h5.png` 分别对应初识古筝 / 雅集现场 / 舞台展演，点击可跳转专题页）+ 视频（`movie.mp4`）+ 配套音频（`movie.mp3`）。
6. **社员故事**：完整社员故事文案，含返回顶部。
7. **在线报名表**：十个字段全部置于 `<table>` 中（姓名 / 性别 / 出生日期 / 手机邮箱 / 乐器基础 / 兴趣方向 / 年级下拉 / 自我介绍 / 服从安排 / 提交+重填）。

## 本地预览

- 方式一：直接用浏览器打开 `work2.html`。
- 方式二（推荐，避免个别浏览器对本地音频/视频的限制）：在文件夹内启动本地服务器，例如：
  ```bash
  python -m http.server 8000
  ```
  然后访问 `http://localhost:8000/work2.html`。
- 注意：媒体文件（mp3 / mp4 / jpg）必须与 HTML 位于同一目录，否则无法加载。

## 提交到 GitHub

```bash
cd guzheng-club-website
git init
git add .
git commit -m "feat: 古筝社团招新网站 work2"
git branch -M main
git remote add origin <你的仓库地址>
git push -u origin main
```

## 开启 GitHub Pages

仓库设置 → Pages → Source 选择 `main` 分支 `/ (root)`，保存后访问
`https://<用户名>.github.io/<仓库名>/`，`index.html` 会自动跳转到招新主页。

> 说明：报名表单的 `action="/cgi-bin/post-information"` 为作业示例地址，仅前端展示，未对接后端。
