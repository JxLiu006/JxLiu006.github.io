# 个人网站 Design —— JxLiu

**版本：** v1.0
**日期：** 2026-07-24
**技术栈：** Jekyll + Minimal Mistakes 主题
**模版仓库：** https://github.com/mmistakes/minimal-mistakes

## 1. 页面区块与浏览顺序

### 导航栏（masthead，始终固定于页面顶部）

`
首页 | About | Skills & Interests | Projects | Contact
`

- 当前页面高亮
- 移动端自动折叠为汉堡菜单

### 浏览顺序（自上而下）

1. **首页（/）** — 访问者首先看到一句话定位 + 简短自我介绍，下设三个方向快速摘要（金融科技 / Agent / 效率与决策），可点击跳转到对应详情页
2. **About（/about/）** — 详细个人背景、学习方向、兴趣来源，2-3 个段落
3. **Skills & Interests（/skills/）** — 技术栈列表 + 感兴趣方向列表
4. **Projects（/projects/）** — 项目入口框架，含占位卡片 + "更多项目即将更新"提示
5. **Contact（/contact/）** — 公开联系方式

### 作者侧边栏（author sidebar）

- 所有页面默认显示（author_profile: true）
- 包含：头像占位图、姓名、一句话简介、社交图标链接
- 桌面端显示在内容左侧，移动端折叠至底部或隐藏

## 2. 颜色、字体与整体风格

- **主题皮肤：** minimal_mistakes_skin: "default"（干净、专业、内容优先）
- **字体：** 使用 Minimal Mistakes 默认字体栈（sans-serif），不额外引入字体
- **整体风格：** 极简、信息密度适中，适合技术展示与项目交流场合
- **颜色：** 保留 default 皮肤的原始配色，不额外自定义颜色变量

## 3. 桌面端与移动端要求

### 桌面端（≥768px）

- 两栏布局：左侧作者侧边栏 + 右侧主要内容
- 导航栏横向展开所有菜单项
- 所有页面内容完整显示，无截断

### 移动端（375px 起）

- 导航栏折叠为汉堡菜单
- 两栏切换为单栏，侧边栏内容移至底部或隐藏
- 无水平滚动条、无文字溢出、无元素重叠
- 按钮和链接的点击区域适应触控操作

## 4. 关键文件分别负责什么

| 文件 | 负责内容 |
|------|----------|
| _config.yml | 网站全局配置：标题、描述、作者信息、社交链接、皮肤、插件启用 |
| _data/navigation.yml | 导航菜单条目与 URL 定义 |
| index.html | 首页，使用 home 布局（Front Matter 控制） |
| about.md | 关于我页面 |
| skills.md | 能力与兴趣页面 |
| projects.md | 项目入口页面 |
| contact.md | 联系方式页面 |
| assets/css/ | 主题样式文件（SCSS 编译产物，一般不动） |
| _layouts/ | 页面布局模板（保留不动，通过 Front Matter 选择） |
| _includes/ | 组件片段（masthead、author-profile、footer 等） |

## 5. 保留模板的哪些部分，修改哪些部分

### 保留不动

- 全部 _layouts/ 目录（布局模板）
- 全部 _includes/ 目录（组件片段，除非需要微调）
- 全部 _sass/ 目录（样式源文件）
- 全部 assets/css/ 和 assets/js/（编译后的静态资源）
- Gemfile、Rakefile、package.json（构建配置）
- .editorconfig、.gitattributes、.gitignore（工具配置）

### 修改的部分

- _config.yml — 写入个人信息、站点标题、社交链接、启用皮肤
- _data/navigation.yml — 替换为本站导航（首页 / About / Skills / Projects / Contact）
- index.html — 替换 Front Matter 和内容
- 新增 about.md、skills.md、projects.md、contact.md（五个页面）

## 6. 图片和外部素材的来源与许可

- 头像/logo：使用 Minimal Mistakes 默认占位头像（主题自带），不引入外部图片
- 社交图标：使用 Font Awesome 图标（主题内置），无需额外引入
- 项目截图 / 外部素材：本期无，后续用户自行添加
- 所有素材均来源于主题内置资源，无需额外许可

## 7. 修订历史

| 版本 | 日期 | 变更说明 |
|------|------|----------|
| v1.0 | 2026-07-24 | 根据作业说明补充完善后定稿 |
