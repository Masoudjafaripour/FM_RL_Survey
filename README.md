## Awesome LLM- and VLM-Integrated Reinforcement Learning [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<img src="./images/llm_rl_taxonomy.png" width="96%" height="96%">

This repository accompanies our survey paper:

**The Evolving Landscape of LLM- and VLM-Integrated Reinforcement Learning**
\[Sheila Schoepp, Masoud Jafaripour\*, Yingyue Cao\*, Tianpei Yang, Fatemeh Abdollahi, Shadan Golestan, Zahin Sufiyan, Osmar R. Zaiane, Matthew E. Taylor]
(\*equal contribution)
**University of Alberta, Nanjing University, Alberta Machine Intelligence Institute (Amii)**
📄 \[[arXiv Paper](https://arxiv.org/abs/2502.15214)]

📌 *This work provides a systematic taxonomy and analysis of how large language models (LLMs) and vision-language models (VLMs) enhance reinforcement learning (RL) tasks.*

---

## ✨ Overview

We categorize the integration of LLMs/VLMs into RL into **three core roles**:

* **LLM/VLM as Agent**: the model acts as a parametric or non-parametric decision-maker.
* **LLM/VLM as Planner**: the model generates comprehensive or incremental plans.
* **LLM/VLM as Reward**: the model defines or generates a reward function or model.

We also discuss:

* Challenges: sample inefficiency, reward engineering, poor generalization, etc.
* Future Directions: grounding, bias mitigation, action advice, multimodal representation.

---

## 🚀 Paper Highlights

* **Unified taxonomy**: Three key roles in FM-enhanced RL: *Agent, Planner, Reward*
* **Comprehensive benchmarks**: Over 40+ recent methods categorized and compared
* **Multimodal perspective**: Includes both LLM and VLM applications across domains
* **Open challenges**: In-depth discussion of limitations and paths forward

---

## 🧠 Table of Contents

* [Datasets](#datasets)
* [LLM/VLM as Agent](#llmvlam-as-agent)
* [LLM/VLM as Planner](#llmvlam-as-planner)
* [LLM/VLM as Reward](#llmvlam-as-reward)
* [Future Research Directions](#future-research-directions)
* [Citation](#citation)

---

## 🔍 Datasets

| Dataset  | Year | Domain        | Modality        | Link                                                                            |
| -------- | ---- | ------------- | --------------- | ------------------------------------------------------------------------------- |
| MineDojo | 2022 | Minecraft     | Vision+Text     | [GitHub](https://github.com/MineDojo/MineDojo)                                  |
| SayCan   | 2022 | Robotics      | Language+Action | [GitHub](https://github.com/google-research/google-research/tree/master/saycan) |
| RL4VLM   | 2024 | Multi-task RL | Vision+Language | [GitHub](https://github.com/RL4VLM/RL4VLM)                                      |

(See paper for full list.)

---

## 🤖 LLM/VLM as Agent

**Parametric (fine-tuned)**: AGILE, TWOSOME, POAD, Retroformer, Zhai et al.
**Non-parametric**: Reflexion, ExpeL, ICPI, RLingua, REMEMBERER

| Method                                              | Type           | Code |
| --------------------------------------------------- | -------------- | ---- |
| [AGILE](https://github.com/bytarnish/AGILE)         | Parametric     | ✅    |
| [Reflexion](https://github.com/noahshinn/reflexion) | Non-parametric | ✅    |
| [TWOSOME](https://github.com/WeihaoTan/TWOSOME)     | Parametric     | ✅    |
| [ExpeL](https://github.com/LeapLabTHU/ExpeL)        | Non-parametric | ✅    |

---

## 🧭 LLM/VLM as Planner

**Comprehensive planners**: SayTap, PSL, LMA3, Inner Monologue
**Incremental planners**: SayCan, BOSS, AdaRefiner, LLM4Teach

| Method                                                                          | Strategy    | Code |
| ------------------------------------------------------------------------------- | ----------- | ---- |
| [SayCan](https://github.com/google-research/google-research/tree/master/saycan) | Incremental | ✅    |
| [AdaRefiner](https://github.com/PKU-RL/AdaRefiner)                              | Incremental | ✅    |
| [Inner Monologue](https://arxiv.org/abs/2212.01599)                             | Hybrid      | -    |

---

## 🎯 LLM/VLM as Reward

**Reward Function**: Text2Reward, Eureka, Zeng et al.
**Reward Model**: VLM-RM, MineCLIP, RL-VLM-F

| Method                                                 | Reward Type | Code |
| ------------------------------------------------------ | ----------- | ---- |
| [Text2Reward](https://github.com/xlang-ai/text2reward) | Function    | ✅    |
| [Eureka](https://github.com/eureka-research/Eureka)    | Function    | ✅    |
| [RL-VLM-F](https://github.com/yufeiwang63/RL-VLM-F)    | Model       | ✅    |
| [MineDojo](https://github.com/MineDojo/MineDojo)       | Model       | ✅    |

---

## 🧭 Future Research Directions

* **Grounding**: Bridging high-level plans with low-level controllers
* **Bias Mitigation**: Debiasing pretrained FMs for RL safety
* **Multimodal Representation**: Richer integration of language, vision, and control
* **Action Advice**: Using FMs as virtual oracles to guide agents

---

## 📚 Citation

If you find this work helpful, please consider citing our survey:

```bibtex
@article{schoepp2024llmrlsurvey,
  title={The Evolving Landscape of LLM- and VLM-Integrated Reinforcement Learning},
  author={Schoepp, Sheila and Jafaripour, Masoud and Cao, Yingyue and Yang, Tianpei and Abdollahi, Fatemeh and Golestan, Shadan and Sufiyan, Zahin and Zaiane, Osmar R. and Taylor, Matthew E.},
  journal={arXiv preprint arXiv:2502.15214},
  year={2024}
}
```

---

## 🤝 Contributing

We welcome pull requests to add missing papers, implementations, or benchmarks!

**How to contribute:**

1. Fork the repository
2. Add your paper or code to the relevant section in `README.md`
3. Use the format:
   `| [Title](Paper Link) | Category | [Code](Code Link) |`
4. Open a pull request

---

## 🗓️ Last Update

2025/05/11
