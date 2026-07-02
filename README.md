# 甄嬛传后宫人物星图

一个可部署到 GitHub Pages 的纯静态网页 MVP。页面用 `HTML + CSS + JavaScript` 实现，无后端、无数据库、无构建工具，直接打开 `index.html` 即可运行。

## 功能

- 深色宇宙风格关系星图
- 100+ 人物 / 对象节点与大量关系线
- 默认聚焦甄嬛
- 拖拽旋转视图、滚轮缩放
- 点击节点查看右侧详情
- 搜索姓名、位份、阵营、职位、称号、宫殿
- 按阵营 / 类型筛选
- 底部展示关系最多的重要节点
- 支持桌面和手机屏幕

## 本地打开

直接双击 `index.html`，或在浏览器中打开该文件。

如果希望用本地服务预览，也可以在项目目录运行：

```bash
python3 -m http.server 8000
```

然后访问：

```text
http://localhost:8000
```

## 部署到 GitHub Pages

1. 新建一个 GitHub 仓库。
2. 上传 `index.html`、`README.md`、`.nojekyll`。
3. 进入仓库的 `Settings`。
4. 打开 `Pages`。
5. 在 `Build and deployment` 中选择 `Deploy from a branch`。
6. 分支选择 `main`，目录选择 `/root`。
7. 保存后等待 GitHub Pages 生成访问地址。

## 数据结构

页面内置了两类数据：

- `nodes`：人物 / 对象节点，包含 `id`、`name`、`alias`、`category`、`rank`、`role`、`bio` 等字段。
- `edges`：关系线，包含 `source`、`target`、`relation`、`event`。

后续可以直接在 `index.html` 中扩充节点和关系。
