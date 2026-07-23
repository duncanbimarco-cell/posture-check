# 体态自测 · 部署包

纯静态网站，无后端。AI 模型与识别库已全部打包在 assets/ 内，
不依赖任何境外 CDN，中国大陆用户可正常访问。

## 部署到 GitHub Pages（免费）

1. 登录 github.com，右上角 “+” → New repository，
   仓库名建议 `posture-check`，选 Public，点 Create repository。
2. 在新仓库页面点 “uploading an existing file”，
   把本文件夹里的所有内容（index.html、assets 文件夹等）整体拖进去，
   点绿色按钮 Commit changes（模型约 9MB，上传需要一会儿）。
3. 仓库页面 → Settings → 左侧 Pages →
   Source 选 “Deploy from a branch”，Branch 选 main / root，点 Save。
4. 等 1–2 分钟，页面上方会显示你的公开网址：
   https://你的用户名.github.io/posture-check/

## 本地预览

直接双击 index.html 不行（浏览器安全限制），需要本地服务器：
在本文件夹运行 `python3 -m http.server 8000`，
然后浏览器打开 http://localhost:8000

## 更换模型精度

assets/pose_landmarker_full.task 可替换为 lite（更快）或 heavy（更准）版本。
