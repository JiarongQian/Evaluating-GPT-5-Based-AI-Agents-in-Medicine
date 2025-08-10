<h1>
  <span style="font-size: 2em; vertical-align: middle;">Medical Agent Benchmark:</span>
  <span style="font-size: 2em; vertical-align: middle;">Evaluating GPT-5-Based AI Agents in Medicine</span>
</h1>

## 👨‍💻 Authors

Zhiling Yan, Jiarong Qian, Shaohui Zhang, Kai Zhang, Wei Liu, Quanzheng Li, Lifang He, Jing Huang, Lichao Sun  
Lehigh University, 
University of Pennsylvania,
Harvard Medical School,
Massachusetts General Hospital,
Mayo Clinic


## 🌟 Introduction

MedABench evaluates GPT-5-based models and systems on medical diagnosis tasks. The homepage logo and title reflect the MedASI branding. The landing page包含：

- Teaser figure：Overview of the Diagnosis dataset and model evaluation（198 cases，11 body systems，9 imaging modalities；对比不同 GPT-5/ChatGPT 配置对准确率的影响）。
- Introduction 标题两侧的 `nurse (1).png` 与 `nurse.png` 图标。
- Diagnosis Dataset 模块，包含两张数据集示例图的轮播。
- Leaderboard 表格：仅保留三列（Model、Result、Accuracy (%)），行固定为 10 个模型配置。

## 📊 Leaderboard（固定结构）

三列：
- Model
- Result（例如 `55/198`）
- Accuracy (%)（例如 `27.77`）

当前展示的 10 个模型：
1. GPT-5  
2. GPT-5 Web Search  
3. GPT-5 Thinking  
4. GPT-5 Thinking (quick)  
5. GPT-5 Thinking Web Search  
6. GPT-5 Thinking (quick) Web Search  
7. GPT-5 Pro  
8. GPT-5 Pro Web Search  
9. ChatGPT Agent  
10. Deep Research

示例已填：
- GPT-5: Result `55/198`，Accuracy `27.77`
- GPT-5 Pro: Result `63/198`，Accuracy `31.77`

## 📦 Project Structure

```
.
├── static/
│   ├── css/              # 样式（Bulma、自定义 index.css）
│   ├── images/           # 图标与图片资源（含 MedASI_logo、nurse 图标等）
│   ├── js/               # 轮播与交互（bulma-carousel、index.js）
├── index.html            # 主页面
├── README.md             # 本说明
```

## 🔗 Links

- Website: 可部署至 GitHub Pages 或 Hugging Face Spaces（静态站点，无需后端）
- Paper: 待补（按钮已预留）
- Code: 待补（按钮已预留）

## 🚀 部署到 GitHub Pages

1) 新建仓库并推送：
```
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
```

2) 打开仓库 Settings → Pages：
- Build and deployment: 选择 “Deploy from a branch”
- Branch 选 `main`，Folder 选 `/ (root)`
- 保存，几分钟后访问 `https://<your-username>.github.io/<repo>/`

## 🛠 技术栈

- Bulma + bulma-carousel/bulma-slider（静态轮播与样式）
- jQuery（初始化轮播）
- 纯前端静态站点，所有资源使用相对路径（`static/...`）

## 📄 License

基于 Academic Project Page Template（Nerfies）修改，保留原模板声明。

