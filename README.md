# xy的小小世界（可安装 App / PWA）

把本目录下的 6 个文件**原样上传到 GitHub 仓库根目录**，即可生成一个可「添加到手机主屏幕」的离线 App。

## 文件说明
- `index.html`：应用本体（所有功能都在这一个文件里）
- `manifest.webmanifest`：PWA 安装清单
- `sw.js`：离线缓存（Service Worker）
- `icon-192.png` / `icon-512.png` / `icon-maskable-512.png`：应用图标

> 路径全部用相对路径（`./`、`start_url:"."`），所以无论部署在 `用户名.github.io` 还是 `用户名.github.io/仓库名` 子路径都能正常安装。

## 部署到 GitHub Pages（免费、自动 HTTPS）
1. 登录 GitHub，新建一个 **Public** 仓库（名字随意，如 `gk-app`）。
2. 把本目录里的 6 个文件**直接上传到仓库根目录**（可用网页拖拽上传，或用 GitHub Desktop）。
3. 进入仓库 **Settings → Pages**（左侧边栏，或 Settings 里的 Pages 标签）。
4. Source 选择 **Deploy from a branch**，Branch 选 **main**（或 master），文件夹选 **/ (root)**，点 **Save**。
5. 等待 1–2 分钟，访问 `https://<你的用户名>.github.io/<仓库名>/`。
6. 用**手机浏览器**打开该地址 → 点浏览器菜单 **「添加到主屏幕」** → 桌面出现图标，点开即全屏 App，断网也能用。

## 更新应用
直接覆盖仓库里的 `index.html`（其余文件一般不用动），GitHub Pages 会自动重新发布。
若手机端没立即更新，可在手机浏览器里刷新一次，或长按图标「移除」后重新添加到主屏幕。

## 私有化（可选）
不想要公开仓库，可在第 2 步把仓库设为 **Private**（GitHub 免费账户支持私有仓库的 Pages，仅你自己能访问部署地址）。
