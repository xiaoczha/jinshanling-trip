# 金山岭家庭出行 Proposal

这是一个纯静态、mobile-first 的单页 Proposal，适合部署为 GitHub Pages Project Site。

## 文件

- `index.html`：完整页面，CSS / JS 均内嵌，上传一个文件即可运行
- `.nojekyll`：告诉 GitHub Pages 直接发布静态文件
- `README.md`：本说明

## 推荐仓库名

`jinshanling-trip`

部署后的地址：

`https://xiaoczha.github.io/jinshanling-trip/`

## 最简单的 GitHub 网页部署方式

1. 登录 GitHub，点击 **New repository**。
2. Repository name 填：`jinshanling-trip`
3. 建议设为 **Public**（GitHub Free 的 Pages 用公共仓库最简单）。
4. 创建仓库后点击 **Add file → Upload files**。
5. 上传本目录中的：
   - `index.html`
   - `.nojekyll`
   - `README.md`
6. Commit 到 `main`。
7. 进入仓库 **Settings → Pages**。
8. **Build and deployment → Source** 选择 `Deploy from a branch`。
9. Branch 选择 `main`，Folder 选择 `/(root)`，点击 **Save**。
10. 部署完成后打开：
    `https://xiaoczha.github.io/jinshanling-trip/`

以后更新页面，只需要替换 `index.html` 并 commit；GitHub Pages 会重新发布。

## 如果你习惯 Git 命令行

```bash
git clone https://github.com/xiaoczha/jinshanling-trip.git
cd jinshanling-trip

# 把 index.html / .nojekyll / README.md 放到这里

git add .
git commit -m "Add Jinshanling family trip proposal"
git push
```

## 实时天气

页面使用 Open-Meteo 的公开天气 API：

- 默认位置：阿那亚·金山岭（约 `40.690811, 117.428039`）
- 页面打开后读取实时天气和未来预报
- 点击“使用我的当前位置”后，浏览器会请求定位权限
- GitHub Pages 使用 HTTPS，符合浏览器 Geolocation 安全上下文要求
- 用户拒绝定位，不影响页面其他功能

当前页面把 `2026-08-17` 至 `2026-08-19` 作为优先显示的旅行日期；如果日期已不在天气 API 的预测窗口内，会自动显示最近三天。

## 微信使用

部署完成后，把页面 URL 发到微信即可：

`https://xiaoczha.github.io/jinshanling-trip/`

建议实际测试一次微信内置浏览器的：
1. 页面排版
2. 实时天气
3. “使用我的当前位置”的定位授权

不同系统版本对定位权限弹窗可能略有差异。

## 后续结构建议

如果后面增加完整版攻略和长图，可保持同一仓库：

```text
jinshanling-trip/
├── index.html              # Proposal / 首页
├── guide.html              # 完整攻略
├── quick.html              # 手机速查页（可选）
├── assets/
│   └── images/
│       ├── quick-01.png
│       └── quick-02.png
├── .nojekyll
└── README.md
```

这样：
- Proposal：`/jinshanling-trip/`
- 完整攻略：`/jinshanling-trip/guide.html`
- 长图：直接保存在手机相册，也可以网页查看

## 数据说明

旅行安排基于 2026-08-15 的家庭约束和公开资料整理。景区开放、索道、课程、天气等动态信息，应以出发当天官方信息为准。
