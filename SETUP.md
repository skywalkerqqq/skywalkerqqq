# 🚀 快速部署指南

## 第一步：创建 GitHub Profile 仓库

1. 登录你的 GitHub
2. 创建一个**与你 GitHub 用户名完全相同**的公开仓库
   - 例如：你的用户名是 `skywalkerqqq`，就创建 `skywalkerqqq/skywalkerqqq`
3. 勾选 "Add a README file"

## 第二步：替换占位符

在 `README.md` 中全局搜索替换：

| 占位符 | 替换为 |
|---------|--------|
| `skywalkerqqq` | 你的 GitHub 用户名 |
| `your.email@gmail.com` | 你的邮箱 |
| Twitter/LinkedIn/WhatsApp 链接 | 你自己的社交链接 |

## 第三步：上传文件

把以下文件推送到你的 profile 仓库：

```
.
├── .github/
│   └── workflows/
│       ├── grid-snake.yml       # 自动生成贪吃蛇动画（每12小时）
│       ├── Metrics.yml          # 生成 github-metrics.svg
│       └── profile-3d.yml       # 生成 3D 贡献图
├── assets/
│   ├── Bottom_up.svg            # 页首波浪动画
│   ├── Bottom_down.svg          # 页尾波浪动画
│   ├── twitter.svg              # Twitter 图标
│   ├── linkedin.svg             # LinkedIn 图标
│   └── gmail.svg                # Gmail 图标
├── profile-3d-contrib/
│   └── profile-green-animate.svg # 3D 贡献动画
├── src/
│   ├── header_.png              # 个人 Banner 图片（替换为你自己的）
│   ├── badges_hackerrank.png    # HackerRank 徽章（替换为你自己的）
│   ├── hackerrank-logo.jpg      # HackerRank Logo
│   ├── badges_1-12.png          # 徽章条（替换为你自己的）
│   ├── badges_13-24.png         # 徽章条
│   ├── badges_25-36.png         # 徽章条
│   └── badges_37-46.png         # 徽章条
├── README.md                    # 主页内容
├── LICENSE                      # MIT 许可证
└── SETUP.md                     # 本文件
```

## 第四步：启用 Workflow

### Snake 动画
1. 进入仓库 → **Settings** → **Actions** → **General**
2. Workflow permissions 设置为 **Read and write permissions**
3. 进入 **Actions** 标签页，手动运行 "Generate Snake Animation"
4. 运行成功后会在 `output` 分支生成 SVG 文件

### Metrics 插件
1. 创建 GitHub Personal Access Token（Settings → Developer settings → Personal access tokens）
2. 在仓库 Secrets 中添加 `METRICS_TOKEN`
3. 手动触发 Metrics workflow

### 3D 贡献图
1. 确保 Actions 有写入权限
2. 手动触发 GitHub-Profile-3D-Contrib workflow

## 第五步：自定义

1. **header_.png** — 替换为你自己的 Banner 图片
2. **社交链接** — 更新 README 中的 Twitter、LinkedIn、Gmail、WhatsApp
3. **HackerRank 徽章** — 替换 `src/` 下的 badges 和 hackerrank 图片
4. **Skills 表格** — 根据你的实际技术栈修改

## 主题配色

| 颜色 | 用途 |
|------|------|
| 紫蓝渐变 | 页首波浪动画 |
| #36BCF7 | 打字机文字 |
| radical 主题 | GitHub 统计卡片 |
