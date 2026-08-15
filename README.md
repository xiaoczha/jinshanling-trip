# 小熊一家去金山岭 · GitHub Pages

这是一个纯静态、Mobile-first 的 GitHub Pages Project Site。

## 页面结构

```text
/
├── index.html          # 新主页 / 导航页
├── guide.html          # 完整攻略
├── why.html            # Why 金山岭（原 Proposal 改造）
├── sources.html        # 资料来源与可信度说明
├── assets/
│   ├── style.css       # 统一样式 + CSS 小熊一家卡通
│   ├── app.js          # 实时天气、定位、筛选、Tab、清单等
│   └── images/         # 本轮未生成图片，目录保留给后续素材
├── .nojekyll
└── README.md
```

## 推荐仓库

仓库名：`jinshanling-trip`

上线地址：

`https://xiaoczha.github.io/jinshanling-trip/`

这是 GitHub Pages 的 **Project Site**，不会覆盖你已有的 `https://xiaoczha.github.io/` 用户主页。

## 最简单的部署方法

1. 登录 GitHub。
2. 新建仓库：`jinshanling-trip`。
3. 建议设为 **Public**。
4. 解压本 ZIP，把 ZIP 内所有文件和文件夹上传到仓库**根目录**。
5. Commit 到 `main` branch。
6. 进入仓库：`Settings -> Pages`。
7. `Build and deployment -> Source` 选择 **Deploy from a branch**。
8. Branch 选择 `main`；Folder 选择 `/(root)`。
9. Save。
10. 等待 Pages 发布完成，访问：

   `https://xiaoczha.github.io/jinshanling-trip/`

GitHub 官方说明：从 branch 发布时，可以直接选择仓库根目录 `/(root)` 作为 publishing source。项目包含 `.nojekyll`，因此这套纯 HTML/CSS/JS 不需要 Jekyll 处理。

## 后续更新

以后只需修改文件并 push/commit 到 `main`，GitHub Pages 会自动重新部署。

## 微信使用

部署后把下面地址发微信即可：

`https://xiaoczha.github.io/jinshanling-trip/`

建议在手机微信内置浏览器测试：

- 首页和 Guide 的滚动体验
- 底部固定导航
- 活动筛选
- “使用当前位置”天气按钮
- 高德地图跳转

## 实时天气

`assets/app.js` 使用 Open-Meteo：

- 默认位置：阿那亚·金山岭 `40.690811, 117.428039`
- 可点击“使用当前位置”请求手机定位
- 无需 API Key
- 拒绝定位不影响攻略
- 当前行程日期：2026-08-17 至 2026-08-19
- 如果行程日期已经超出天气 API 的预测窗口，页面自动显示最近 3 天

## 内容原则

- 固定设施：根据阿那亚官方/2026 配套资料整理。
- 园区徒步：三条经典路线结合 2026 游客资料与实走轨迹；里程存在差异的地方已明确标注。
- 角楼登高线：只有 2026 真实住客点评能确认其存在，因此网页不猜测入口/里程。
- 金山岭长城：2026 旺季运营时间与索道恢复已按公开运营通知更新。
- 临时演出、手作、瑜伽、徒步开放、商家营业等动态内容：以阿那亚 App 当天为准。

## 本地预览

在文件目录中执行：

```bash
python3 -m http.server 8000
```

浏览器打开：

`http://localhost:8000/`
