# 南山区无人机3D路径规划

基于 Cesium 的三维无人机航线规划可视化系统，展示南山区低空航线的空间约束与规划逻辑。

## 页面

| 页面 | 说明 |
|------|------|
| [index.html](index.html) | 门户首页，案例入口 |
| [cesium_3d.html](cesium_3d.html) | 3D 地图展示（建筑体块 / 禁飞区 / 飞行路径 / 无人机飞行模拟） |
| [algorithm.html](algorithm.html) | 算法原理（26 向 A\* 多目标优化，含公式与核心代码） |

## 案例数据

| 案例 | 建筑体块 | 路径节点 | 航线长度 |
|------|---------|---------|---------|
| 小型无人机 | 1530 | 1104 | 8.7 km |
| 微型无人机复杂环境 | 596 | 691 | 2.6 km |

## 算法

26 向 A\* 多目标优化：禁飞区 + 噪音敏感区 + TKE 湍流 + 航向约束 + 3D 避障。详见 [algorithm.html](algorithm.html)。

## 部署

纯静态页面，无构建步骤。可用于 GitHub Pages / Cloudflare Pages：

- **GitHub Pages**：将本目录推送到仓库，开启 Pages（分支或 /docs 目录均可）
- **Cloudflare Pages**：上传本目录或连接仓库自动部署

> 注意：3D 地图与算法页依赖外部 CDN（jsdelivr / cesium.com / unpkg）加载 Cesium 与 MathJax，部署到境外平台（GitHub Pages）后加载更稳定；地图底图来自 ArcGIS Online 卫星影像。
