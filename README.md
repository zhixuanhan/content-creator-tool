# 创作灵感站 - AI干货内容生成工具

输入一个话题词，一键生成校园 & 职场干货内容。支持小红书图文、公众号长文、短视频脚本三种格式。

## 功能

- 🎓 **校园方向**：考研考公、四六级、简历、求职、论文
- 💼 **职场方向**：新人指南、面试技巧、职业规划、沟通技能
- 📱 **小红书图文**：吸睛标题 + 结构化正文 + 热门标签
- 📖 **公众号长文**：深度文章，有结构有案例
- 🎬 **短视频脚本**：开头hook + 正文 + 结尾引导互动
- ⚡ **流式输出**：实时看到生成过程
- 📋 **一键复制**：直接粘贴到目标平台
- 📜 **历史记录**：保存最近50条生成记录

## 快速开始

### 1. 安装依赖

```bash
cd content-creator-tool
npm install
```

### 2. 配置环境变量

```bash
cp .env.example .env.local
```

编辑 `.env.local`，填入你的 DeepSeek API Key：

```
DEEPSEEK_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx
```

> 💡 获取 API Key：https://platform.deepseek.com/api_keys
> DeepSeek 注册后有免费额度，之后价格也很便宜

### 3. 启动开发服务器

```bash
npm run dev
```

打开浏览器访问 http://localhost:3000

### 4. 生产部署

```bash
npm run build
npm start
```

## 部署到 Vercel（推荐，免费）

1. 把代码推到 GitHub 仓库
2. 打开 https://vercel.com ，用 GitHub 登录
3. Import 你的仓库
4. 在 Settings → Environment Variables 添加 `DEEPSEEK_API_KEY`
5. 点击 Deploy，完成！

## 部署到自己的服务器

```bash
# 安装 Node.js 18+
# clone 代码
git clone <你的仓库地址>
cd content-creator-tool
npm install
cp .env.example .env.local
# 编辑 .env.local 填入 DEEPSEEK_API_KEY

# 构建
npm run build

# 启动（推荐用 pm2）
npm install -g pm2
pm2 start npm --name "content-creator" -- start
```

## 技术栈

- **Next.js 14** (App Router)
- **Tailwind CSS** (UI)
- **DeepSeek API** (AI 内容生成)

## 后续迭代方向

- [ ] 小程序端（uni-app，复用同一套API）
- [ ] 用户登录系统
- [ ] 服务端历史记录持久化
- [ ] 创作者风格学习（上传爆款，AI学习风格）
- [ ] 选题日历（结合热点推荐话题）
- [ ] 批量生成（一个话题同时出3种格式）
- [ ] AI配图建议
