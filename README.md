# AgentMed: Evaluating GPT-5 AI Agents in Medicine

## Overview

This project presents a comprehensive evaluation of GPT-5 AI agents in medical diagnosis tasks. We systematically assess the performance of a hierarchy of OpenAI models and systems, from base large language models to autonomous agents, to understand the impact of incremental capabilities on clinical intelligence.

## Main Page
https://JiarongQian.github.io/AgentMed

## Authors

- **Shaohui Zhang** - University of Pennsylvania
- **Jiarong Qian** - University of Pennsylvania
- **Zhiling Yan** - Lehigh University
- **Kai Zhang** - Lehigh University
- **Yonghui Wu** - University of Florida
- **Wei Liu** - Mayo Clinic
- **Quangzheng Li** - Lehigh University
- **Xiang Li** - MGH/Harvard Medical School
- **Lifang He** - Lehigh University
- **Jing Huang** - University of Pennsylvania
- **Lichao Sun** - Lehigh University

**Affiliations:** Lehigh University, University of Pennsylvania, Mayo Clinic, Harvard Medical School, Massachusetts General Hospital, University of Florida

## Introduction

Large language models (LLMs) are increasingly being augmented with reasoning and tool-use capabilities, creating a spectrum of AI systems from simple chatbots to autonomous agents. This rapid evolution has fueled visions of Artificial Super Intelligence (ASI) revolutionizing medicine, yet the true gap between current systems and this future remains unquantified.

It is unclear how incremental capabilities, from web search to agentic planning, affect performance on the path towards superhuman clinical intelligence, necessitating a comprehensive, ecosystem-wide evaluation. Here, we systematically evaluate the performance of a hierarchy of OpenAI models and systems on medical diagnosis tasks.

Our analysis spans from the base large language model (e.g., GPT-5) to models enhanced with reasoning, web search, a deep research function, and a fully autonomous agent. We show that while augmenting models with external information tools improves data retrieval, it does not consistently translate to superior diagnostic accuracy and can introduce new error vectors.

This work provides a crucial benchmark of OpenAI's model ecosystem, establishing a rigorous methodology for evaluating the true clinical readiness of increasingly complex AI systems and guiding their responsible integration into healthcare. Our new evaluation platform aims to establish a rigorous methodology for tracking progress and guiding the responsible development of AI towards a future of safe and reliable super-intelligence in medicine.

## Dataset

Our dataset is derived from **MedXpertQA**, a publicly available benchmark introduced for Human Health tasks. The dataset contains 198 diagnosis cases distributed across 11 body systems:

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
| **LLM** | GPT-5 | 55/198 | 27.78 |
| | GPT-5 Thinking | 55/198 | 27.78 |
| | GPT-5 Thinking (quick) | 52/198 | 26.26 |
| | GPT-5 Pro | 62/198 | 31.31 |
| **Web-Search** | GPT-5 Web Search | 40/198 | 20.20 |
| | GPT-5 Thinking Web Search | 65/198 | 32.83 |
| | GPT-5 Thinking (quick) Web Search | - | - |
| | GPT-5 Pro Web Search | 78/198 | 39.39 |
| **Agent** | ChatGPT Agent | 34/102 | 33.33 |
| | Deep Research | - | - |


The following table shows the performance of different 4o/o3 models on the diagnosis dataset:
| Category | Model | Result | Accuracy (%) |
|----------|-------|---------|--------------|
| **Web-Search** | 4o Web Search | 51/198 | 25.76|
| |o3-Pro Web Search | 66/198 | 33.33 |
| | - | - | - |
| | - | - | - |


## Demos

### Case MM-94: Lumbar Spine MRI

**Question:** A 60-year-old man presents with radicular pain in the right leg, accompanied by weakness in the hip abductors and extensor hallucis longus (EHL). MRI images are provided in Figures A-C. What is the underlying cause of this patient's symptoms?

**Ground Truth:** Facet synovial cyst

**Images:** <img src="static/images/MM-94-1.png" width="100"><img src="static/images/MM-94-2.png" width="100"><img src="static/images/MM-94-3.png" width="100">

| Model | Analysis | Score |
|-------|----------|-------|
| **GPT-5** | The MRI images show a right-sided herniated disc at the L4–L5 level:<br/>• Sagittal T2-weighted MRI shows loss of disc height and focal protrusion<br/>• Axial MRI confirms herniated disc material compressing the right L5 nerve root<br/><br/>**Underlying cause:** Right posterolateral L4–L5 intervertebral disc herniation causing L5 radiculopathy. | 0 |
| **GPT-5 Web Search** | Clinical presentation strongly implicates L5 nerve root compression. MRI shows protrusion of intervertebral disc material at L4–L5 level extending into neural foramen, likely impinging on L5 nerve root.<br/><br/>**Conclusion:** L4–L5 disc herniation compressing L5 nerve root. | 0 |
| **GPT-5 Thinking** | **Right L5 radiculopathy from L4–L5 facet synovial cyst compressing the traversing L5 root.**<br/>MRI shows T2-bright extradural cyst adjacent to facet joint causing lateral recess stenosis—typical of degenerative synovial cyst. | 1 |
| **GPT-5 Thinking (Quick)** | **Right-sided L4-L5 disc herniation** causing compression of right L5 nerve root within lateral recess.<br/>**Final Diagnosis:** Right L4-L5 posterolateral disc herniation compressing right L5 nerve root. | 0 |
| **GPT-5 Pro** | **L5 radiculopathy from right L4–5 juxtafacet synovial cyst.**<br/>MRI shows fluid-filled facet joints and T2 bright extradural cyst projecting medially, narrowing lateral recess and compressing traversing L5 root. | 1 |
| **GPT-5 Pro Web Search** | Exam localizes to L5 radiculopathy. MRI shows degenerative narrowing at L4–5 with facet arthropathy and joint fluid, producing lateral recess stenosis that compresses traversing right L5 nerve root. | 0 |
| **GPT-5 Thinking Web Search** | **Right L5 radiculopathy from L4–L5 facet-joint synovial cyst compressing traversing L5 root.**<br/>Exam fits L5 root: weakness of EHL and hip abductors is classic for L5 radiculopathy. | 1 |
| **GPT-5 ChatGPT Agent** | Weakness in hip abductors and EHL = L5 radiculopathy. MRI shows fluid-intensity lesion at L4–L5 facet joint compressing L5 root. Characteristic of degenerative synovial cyst, not disc herniation. | 1 |

---

### Case MM-651: ECG Analysis

**Question:** A 33-year-old female presents with dyspnea for 5 years, palpitations, chronic cough, dry skin, hair thinning, and lower extremity edema. ECG shows bradycardia. What is the most likely diagnosis?

**Ground Truth:** Sarcoidosis

**Image:** <img src="static\images\MM-651-1.png" width="500">

| Model | Analysis | Score |
|-------|----------|-------|
| **GPT-5** | ECG shows sinus bradycardia with low voltage QRS complexes. Clinical presentation suggests **hypothyroidism with pericardial effusion**.<br/>**Key features:** Sinus bradycardia, low QRS voltage, dry skin, hair thinning, edema. | 0 |
| **GPT-5 Web Search** | Clinical presentation highly suggestive of **hypothyroidism**, most likely long-standing and severe. ECG shows sinus bradycardia, low-voltage QRS complexes, and T-wave flattening. | 0 |
| **GPT-5 Thinking** | **Primary hypothyroidism with large pericardial effusion.**<br/>She has dry skin, hair loss, edema, and marked sinus bradycardia. ECG shows low-voltage complexes consistent with pericardial effusion. | 0 |
| **GPT-5 Thinking (Quick)** | ECG shows **sinus bradycardia** with low-voltage QRS complexes. Presentation consistent with **severe hypothyroidism (myxedema)** complicated by **large pericardial effusion**. | 0 |
| **GPT-5 Pro** | **Atrial flutter with slow ventricular response (high degree AV block).**<br/>ECG shows classic saw tooth flutter waves with ventricular rate ≈50/min, explaining palpitations and dyspnea. | 0 |
| **GPT-5 Pro Web Search** | **Atrial flutter with high degree AV block (≈5:1–6:1).**<br/>ECG shows continuous flutter waves with high AV conduction ratio, giving ventricular rate near 50/min. | 0 |
| **GPT-5 Thinking Web Search** | **Severe hypothyroidism with pericardial effusion ("myxedema heart").**<br/>Exam fits hypothyroidism; hypothyroidism commonly causes slowed heart rate and low-voltage ECG changes. | 0 |
| **GPT-5 ChatGPT Agent** | ECG demonstrates sinus bradycardia. Patient shows classic features of long-standing hypothyroidism. Most likely diagnosis is **severe hypothyroidism, likely with pericardial effusion** causing respiratory symptoms. | 0 |

---

### Case MM-1764: Fundus Photography

**Question:** This patient reports experiencing transient, painless visual obscuration in the left eye. What is the most likely diagnosis?

**Ground Truth:** Cholesterol emboli

**Image:** <img src="static\images\MM-1764-1.png" width="200">

| Model | Analysis | Score |
|-------|----------|-------|
| **GPT-5** | Fundus shows multiple bright, reflective lesions along retinal arterioles, consistent with **Hollenhorst plaques**—cholesterol emboli from ipsilateral carotid artery.<br/>**Diagnosis:** Amaurosis fugax due to retinal artery embolism from carotid atherosclerotic plaque. | 1 |
| **GPT-5 Web Search** | Fundus shows numerous small yellowish flecks clustered in macular region—consistent with **drusen**, suggesting early age-related macular degeneration (AMD).<br/>**Diagnosis:** Early Age-Related Macular Degeneration (Dry AMD). | 1 |
| **GPT-5 Thinking** | **Central retinal artery occlusion (CRAO).**<br/>Fundus shows pale retina with cherry-red spot at macula, characteristic of CRAO, associated with transient monocular visual loss. | 0 |
| **GPT-5 Thinking (Quick)** | Retinal image shows **multiple yellowish refractile deposits** consistent with **Hollenhorst plaques** (cholesterol emboli).<br/>**Diagnosis:** Retinal cholesterol embolism secondary to carotid artery atherosclerosis. | 1 |
| **GPT-5 Pro** | **Retinal cholesterol embolus (Hollenhorst plaque) causing amaurosis fugax.**<br/>Fundus shows bright, refractile yellow plaque lodged in retinal arteriole near optic disc. | 1 |
| **GPT-5 Pro Web Search** | **Hollenhorst plaque causing amaurosis fugax.**<br/>Fundus shows small, bright, yellow, refractile deposits lodged in retinal arterioles—classical for Hollenhorst plaques. | 1 |
| **GPT-5 Thinking Web Search** | **Hollenhorst plaque causing amaurosis fugax.**<br/>Fundus shows small, bright, refractile yellow embolus lodged at arteriole bifurcation—typical of Hollenhorst plaque. | 1 |
| **GPT-5 ChatGPT Agent** | Fundus shows small, bright yellow–white refractile deposit lodged within retinal arteriole near optic disc. Such plaques consist of cholesterol crystals that embolize from proximal atherosclerotic lesions. | 1 |

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
@inproceedings{2025_AgentMed,
  title={AgentMed: Evaluating GPT-5 AI Agents in Medicine},
  author={Shaohui Zhang,Jiarong Qian,Zhiling Yan,Kai Zhang,Yonghui Wu,Wei Liu,Quangzheng Li,Xiang Li,Lifang He,Jing Huang,Lichao Sun},
  booktitle={},
  year={2025},
}
```

## Contributing

This project evaluates the performance of  AI models from ChatGPT in medical diagnosis. For questions or contributions, please refer to the research methodology and evaluation criteria outlined in the main webpage.

## License

This project is for research and educational purposes. Please ensure compliance with relevant data privacy and medical research regulations when using the MedXpertQA dataset.

---

*This benchmark aims to establish a rigorous methodology for tracking progress and guiding the responsible development of AI towards a future of safe and reliable super-intelligence in medicine.*

