<<<<<<< HEAD
# Medical Agent Benchmark: Evaluating GPT-5-Based AI Agents in Medicine
=======
<h1>
  <span style="font-size: 2em; vertical-align: middle;">Medical Agent Benchmark:</span>
  <span style="font-size: 2em; vertical-align: middle;">Evaluating GPT-5-Based AI Agents in Medicine</span>
</h1>
>>>>>>> 35853d90cb9e99095a305bf307435c2914573944

## Overview

<<<<<<< HEAD
This project presents a comprehensive evaluation of GPT-5-based AI agents in medical diagnosis tasks. We systematically assess the performance of a hierarchy of OpenAI models and systems, from base large language models to autonomous agents, to understand the impact of incremental capabilities on clinical intelligence.
=======
Zhiling Yan, Jiarong Qian, Shaohui Zhang, Kai Zhang, Wei Liu, Quanzheng Li, Lifang He, Jing Huang, Lichao Sun  
Lehigh University, 
University of Pennsylvania,
Harvard Medical School,
Massachusetts General Hospital,
Mayo Clinic

>>>>>>> 35853d90cb9e99095a305bf307435c2914573944

## Authors

<<<<<<< HEAD
- **Zhiling Yan**
- **Jiarong Qian** 
- **Shaohui Zhang**
- **Kai Zhang**
- **Wei Liu**
- **Quangzheng Li**
- **Lifang He**
- **Jing Huang**
- **Lichao Sun**
=======
MedABench evaluates GPT-5-based models and systems on medical diagnosis tasks. The homepage logo and title reflect the MedASI branding. The landing page包含：
>>>>>>> 35853d90cb9e99095a305bf307435c2914573944

**Affiliations:** Harvard Medical School/Massachusetts General Hospital, Mayo Clinic, Lehigh University, University of Pennsylvania

## Introduction

Large language models (LLMs) are increasingly being augmented with reasoning and tool-use capabilities, creating a spectrum of AI systems from simple chatbots to autonomous agents. This rapid evolution has fueled visions of Artificial Super Intelligence (ASI) revolutionizing medicine, yet the true gap between current systems and this future remains unquantified.

Our analysis spans from the base large language model (e.g., GPT-5) to models enhanced with reasoning, web search, a deep research function, and a fully autonomous agent. We show that while augmenting models with external information tools improves data retrieval, it does not consistently translate to superior diagnostic accuracy and can introduce new error vectors.

This work provides a crucial benchmark of OpenAI's model ecosystem, establishing a rigorous methodology for evaluating the true clinical readiness of increasingly complex AI systems and guiding their responsible integration into healthcare.

## Dataset

We evaluate on **HealthBench**, a publicly available benchmark introduced by OpenAI for Human Health tasks. The dataset contains 198 diagnosis cases distributed across 11 body systems:

- **Cardiovascular**: 40 cases
- **Digestive**: 35 cases  
- **Respiratory**: 34 cases
- **Skeletal**: 31 cases
- **Nervous**: 22 cases
- **Reproductive**: 9 cases
- **Endocrine**: 9 cases
- **Integumentary**: 7 cases
- **Lymphatic**: 5 cases
- **Muscular**: 4 cases
- **Urinary**: 2 cases

Each case has a unique identifier and an open-ended, reasoning-style diagnostic question paired with medical images spanning CT, MRI, X-ray, PET, pathology images, EEG/ECG recordings, charts, and real-world photographs, together with a clinically validated ground-truth diagnosis.

## Leaderboard

The following table shows the performance of different GPT-5 models on the diagnosis dataset:

| Category | Model | Result | Accuracy (%) |
|----------|-------|---------|--------------|
| **LLL** | GPT-5 | 55/198 | 27.77 |
| | GPT-5 Pro | 63/198 | 31.77 |
| | GPT-5 Thinking | - | - |
| | GPT-5 Thinking (quick) | - | - |
| **Web-Search** | GPT-5 Web Search | - | - |
| | GPT-5 Pro Web Search | - | - |
| | GPT-5 Thinking Web Search | - | - |
| | GPT-5 Thinking (quick) Web Search | - | - |
| **Agent** | ChatGPT Agent | - | - |
| | Deep Research | - | - |

## Project Structure

```
GPT-5/
├── index.html              # Main webpage
├── README.md               # This file
├── static/
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript files
│   ├── images/            # Project images and icons
│   └── pdfs/              # PDF documents
```

## Features

- **Interactive Image Carousel**: Dataset visualization with sliding images
- **Responsive Design**: Built with Bulma CSS framework
- **Modern UI**: Clean, professional interface for medical AI research
- **Comprehensive Evaluation**: Systematic assessment of GPT-5 model hierarchy

## Deployment

This is a static HTML website that can be deployed to various platforms:

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to Settings > Pages
3. Select source branch (usually `main` or `master`)
4. Your site will be available at `https://username.github.io/repository-name`

### Alternative Platforms
- **Vercel**: Drag and drop deployment
- **Netlify**: Git-based deployment
- **Hugging Face Spaces**: For ML/AI projects
- **Cloudflare Pages**: Fast global deployment

## Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Styling with Bulma framework
- **JavaScript**: Interactive features and carousel functionality
- **Bulma**: Modern CSS framework for responsive design

## Contributing

This project evaluates the performance of AI models in medical diagnosis. For questions or contributions, please refer to the research methodology and evaluation criteria outlined in the main webpage.

## License

This project is for research and educational purposes. Please ensure compliance with relevant data privacy and medical research regulations when using the HealthBench dataset.

---

*This benchmark aims to establish a rigorous methodology for tracking progress and guiding the responsible development of AI towards a future of safe and reliable super-intelligence in medicine.*

