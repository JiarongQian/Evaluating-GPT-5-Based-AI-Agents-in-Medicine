# Medical Agent Benchmark: Evaluating GPT-5-Based AI Agents in Medicine

## Overview

This project presents a comprehensive evaluation of GPT-5-based AI agents in medical diagnosis tasks. We systematically assess the performance of a hierarchy of OpenAI models and systems, from base large language models to autonomous agents, to understand the impact of incremental capabilities on clinical intelligence.

## Authors

- **Zhiling Yan** - Lehigh University
- **Jiarong Qian** - Lehigh University
- **Shaohui Zhang** - Lehigh University  
- **Kai Zhang** - Lehigh University
- **Wei Liu** - Lehigh University
- **Quangzheng Li** - Lehigh University
- **Xiang Li** - Lehigh University
- **Lifang He** - Lehigh University
- **Jing Huang** - Lehigh University
- **Lichao Sun** - Lehigh University

**Affiliations:** Lehigh University, University of Pennsylvania, Mayo Clinic, Harvard Medical School, Massachusetts General Hospital

## Introduction

Large language models (LLMs) are increasingly being augmented with reasoning and tool-use capabilities, creating a spectrum of AI systems from simple chatbots to autonomous agents. This rapid evolution has fueled visions of Artificial Super Intelligence (ASI) revolutionizing medicine, yet the true gap between current systems and this future remains unquantified.

It is unclear how incremental capabilities, from web search to agentic planning, affect performance on the path towards superhuman clinical intelligence, necessitating a comprehensive, ecosystem-wide evaluation. Here, we systematically evaluate the performance of a hierarchy of OpenAI models and systems on medical diagnosis tasks.

Our analysis spans from the base large language model (e.g., GPT-5) to models enhanced with reasoning, web search, a deep research function, and a fully autonomous agent. We show that while augmenting models with external information tools improves data retrieval, it does not consistently translate to superior diagnostic accuracy and can introduce new error vectors.

This work provides a crucial benchmark of OpenAI's model ecosystem, establishing a rigorous methodology for evaluating the true clinical readiness of increasingly complex AI systems and guiding their responsible integration into healthcare. Our new evaluation platform aims to establish a rigorous methodology for tracking progress and guiding the responsible development of AI towards a future of safe and reliable super-intelligence in medicine.

## Dataset

We evaluate on **MedXpertQA**, a publicly available benchmark introduced for Human Health tasks. The dataset contains 198 diagnosis cases distributed across 11 body systems:

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

## Key Findings

Our evaluation shows that while augmenting models with external information tools improves data retrieval, this does not consistently translate to superior diagnostic accuracy. GPT-5 Pro performs best in the base LLM category with an accuracy of 31.77%.

## Leaderboard

The following table shows the performance of different GPT-5 models on the diagnosis dataset:

| Category | Model | Result | Accuracy (%) |
|----------|-------|---------|--------------|
| **LLM** | GPT-5 | 55/198 | 27.77 |
| | GPT-5 Thinking | 55/198 | 27.78 |
| | GPT-5 Thinking (quick) | 52/198 | 26.26 |
| | GPT-5 Pro | 63/198 | 31.77 |
| **Web-Search** | GPT-5 Web Search | - | - |
| | GPT-5 Thinking Web Search | - | - |
| | GPT-5 Thinking (quick) Web Search | - | - |
| | GPT-5 Pro Web Search | 78/198|40.30 |
| **Agent** | ChatGPT Agent | - | - |
| | Deep Research | - | - |

## Project Structure

```
GPT-5/
├── index.html              # Main webpage
├── README.md               # This file
├── static/
│   ├── css/               # Stylesheets
│   │   ├── bulma.min.css  # Bulma CSS framework
│   │   ├── bulma-carousel.min.css  # Carousel styles
│   │   ├── bulma-slider.min.css    # Slider styles
│   │   ├── fontawesome.all.min.css # Icon styles
│   │   └── index.css      # Custom styles
│   ├── js/                # JavaScript files
│   │   ├── bulma-carousel.js  # Carousel functionality
│   │   ├── bulma-slider.js    # Slider functionality
│   │   ├── fontawesome.all.min.js # Icon functionality
│   │   └── index.js       # Main JavaScript logic
│   ├── images/            # Project images and icons
│   │   ├── MedABench_logo.png  # MedABench logo
│   │   ├── LOGO.png           # Project logo
│   │   ├── overview.jpg       # Overview image
│   │   ├── dataset_1.jpg      # Dataset example 1
│   │   ├── dataset_2.jpg      # Dataset example 2
│   │   ├── leaderboard.png    # Leaderboard icon
│   │   ├── data.png           # Data icon
│   │   ├── hospital.png       # Hospital icon
│   │   └── nurse.png          # Nurse icon
│   └── pdfs/              # PDF documents
│       └── sample.pdf     # Sample PDF
```

## Features

- **Interactive Image Carousel**: Dataset visualization with sliding images
- **Responsive Design**: Built with Bulma CSS framework
- **Modern UI**: Clean, professional interface for medical AI research
- **Comprehensive Evaluation**: Systematic assessment of GPT-5 model hierarchy
- **Professional Table Design**: Color-coded groups with progress bar visualization
- **Multi-modal Support**: Support for various medical image formats including CT, MRI, X-ray, and more

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
- **CSS3**: Styling with Bulma framework and custom progress bars
- **JavaScript**: Interactive features and carousel functionality
- **Bulma**: Modern CSS framework for responsive design
- **Font Awesome**: Icon library
- **jQuery**: JavaScript library

## Citation

If you use this project in your research, please cite:

```bibtex
@inproceedings{tie2025mmmr,
  title={TOWARDS ARTIFICIAL SUPER INTELLIGENCE IN HEALTHCARE: EVALUATING GPT-5-BASED AI AGENTS IN MEDICINE},
  author={Zhiling Yan, Jiarong Qian, Shaohui Zhang, Kai Zhang, Lifang He, Jing Huang, Lichao Sun},
  booktitle={},
  year={2025},
}
```

## Contributing

This project evaluates the performance of AI models in medical diagnosis. For questions or contributions, please refer to the research methodology and evaluation criteria outlined in the main webpage.

## License

This project is for research and educational purposes. Please ensure compliance with relevant data privacy and medical research regulations when using the MedXpertQA dataset.

---

*This benchmark aims to establish a rigorous methodology for tracking progress and guiding the responsible development of AI towards a future of safe and reliable super-intelligence in medicine.*

