<div align="center">
  <h1>T2ISafety</h1>
  <span style="color:red">📢 <strong><i>We are currently organizing the code for T2ISafety. If you are interested in our work, please star ⭐ our project.</i></strong></span>

  <h4>
    <img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version"> 
    <img src="https://img.shields.io/badge/License-Apache_2.0-green.svg" alt="License">
    <img src="https://visitor-badge.laobi.icu/badge?page_id=OpenSafetyLab.SALAD-BENCH" />
    <img src="https://img.shields.io/github/stars/OpenSafetyLab/SALAD-BENCH?color=yellow" alt="Stars">
    <img src="https://img.shields.io/github/issues/OpenSafetyLab/SALAD-BENCH?color=red" alt="Issues">
  </h4>

  <h4> | <a href="https://openreview.net/forum?id=kIboeK0Wzs&referrer=%5BAuthor%20Console%5D(%2Fgroup%3Fid%3DICLR.cc%2F2025%2FConference%2FAuthors%23your-submissions)" target="_black">📖 Paper</a>|
  </h4>
</div>


<h2 id="T2ISafety">🎉 Introduction</h2>

Text-to-image (T2I) models have rapidly advanced, enabling the generation of high-quality images from text prompts across various domains. However, these models present notable  safety concerns, including the risk of generating harmful, biased, or private content. 
Current research on assessing T2I safety remains in its early stages. While some efforts have been made to evaluate models on specific safety dimensions, many critical risks remain unexplored. To address this gap, we introduce **T2ISafety**, a safety benchmark that evaluates T2I models across three key domains: toxicity, fairness, and bias. We build a detailed hierarchy of 12 tasks and 44 categories based on these three domains, and meticulously collect 70K corresponding prompts. Based on this taxonomy and prompt set, we build a large-scale T2I dataset with 68K manually annotated images and train an evaluator capable of detecting critical risks that previous work has failed to identify, including risks that even ultra-large proprietary models like GPTs cannot correctly detect. We evaluate 12 prominent diffusion models on **T2ISafety** and reveal several concerns including persistent issues with racial fairness, a tendency to generate toxic content, and significant variation in privacy protection across the models, even with defense methods like concept erasing.
<div align="center">
</div>


<h2 id="features">🚩 Features</h2>

1. **Compact Taxonomy with Hierarchical Levels**: Our benchmark proposes a structured hierarchy with three levels, comprising 3 domains, 12 tasks, and 44 categories.
2. **Advanced Evaluation Framework**
   1. Specialized fine-tuned evaluator namely _ImageGuard_ for Images.

<h2 id="features">🚩 Dataset construction</h2>

![Overview Diagram](assets/fig1.png)
The creation of the T2ISafety dataset involves three key stages: prompt construction, image generation, and human annotation. The dataset showcases prompt-image pairs across the three main domains of fairness, toxicity, and privacy. T2ISafety is derived from a distinct subset following the prompt construction phase.

<h2 id="features">🚩 Model architecture</h2>

![Overview Diagram](assets/fig2.png)
Network architecture and additional loss of ImageGuard. Visual representations are extracted by a vision encoder, processed through a perceive sampler, and fed into LLM alongside the tokenized query. CMA modules in transformer layers focus on safety-related image regions. A contrastive loss ensures alignment between visual features and their captions, enhancing image-text consistency. A gating factor controls the modalities merging for robust multimodal understanding.

![Results](assets/table2.png)

<h2 id="features">🚩 T2I model results</h2>

![Results](assets/table3.png)

<h2 id="citation">📑 Citation</h2>

```bibtex
@article{libenchmarking,
  title={Benchmarking Ethics in Text-to-Image Models: A Holistic Dataset and Evaluator for Fairness, Toxicity, and Privacy},
  author={Li, Lijun and Shi, Zhelun and Hu, Xuhao and Dong, Bowen and Qin, Yiran and Liu, Xihui and Sheng, Lu and Shao, Jing}
}
```

<hr>
<p align="center">SALAD-Bench Team</p>
