## Awesome LLM- and VLM-Integrated Reinforcement Learning [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

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

### Table of Parametric LLM/VLM Agents

| Method                           | Model(s)               | FT  | RL Role                  | Metrics          | Code                                                                 |
| -------------------------------- | ---------------------- | --- | ------------------------ | ---------------- | -------------------------------------------------------------------- |
| AGILE \[Feng et al., 2024]       | Meerkat, Vicuna-1.5    | ✓\* | $\pi_l, v_l, \text{rft}$ | acc, rew         | [Link](https://github.com/bytarnish/AGILE)                           |
| Retroformer \[Yao et al., 2024]  | GPT-3, GPT-4, LongChat | ✓   | $\pi_l, \text{rft}$      | sr, se           | -                                                                    |
| TWOSOME \[Tan et al., 2024]      | Llama                  | ✓\* | $\pi_l, v_l, \text{rft}$ | sr, rew, gen, se | [Link](https://github.com/WeihaoTan/TWOSOME)                         |
| POAD \[Wen et al., 2024]         | CodeLlama, Llama 2     | ✓\* | $\pi_l, v_l, \text{rft}$ | rew, gen, se     | [Link](https://github.com/morning9393/ADRL)                          |
| GLAM \[Carta et al., 2023]       | FLAN-T5                | ✓   | $\pi_l, v_l, \text{rft}$ | se, gen          | [Link](https://github.com/flowersteam/Grounding_LLMs_with_online_RL) |
| Zhai et al. \[Zhai et al., 2024] | LLaVA-v1.6-Mistral     | ✓\* | $\pi_l, v_l, \text{rft}$ | sr               | [Link](https://github.com/RL4VLM/RL4VLM)                             |

### Table of Non-Parametric LLM/VLM Agents

| Method                            | Model(s)                    | FT | RL Role                | Metrics          | Code                                            |
| --------------------------------- | --------------------------- | -- | ---------------------- | ---------------- | ----------------------------------------------- |
| ICPI \[Brooks et al., 2023]       | Codex                       | ×  | $\pi_l, v_l, \tau_\pi$ | rew, gen         | [Link](https://github.com/ethanabrooks/icpi)    |
| Reflexion \[Shinn et al., 2023]   | GPT-3, GPT-3.5-Turbo, GPT-4 | ×  | $\pi_l, \tau_\pi$      | sr, acc          | [Link](https://github.com/noahshinn/reflexion)  |
| REMEMBERER \[Zhang et al., 2023a] | GPT-3.5                     | ×  | $\pi_l, v_l, \tau_\pi$ | sr, rob          | [Link](https://github.com/OpenDFM/Rememberer)   |
| ExpeL \[Zhao et al., 2024]        | GPT-3.5-Turbo, GPT-4        | ×  | $\pi_l, \tau_\pi$      | sr, gen          | [Link](https://github.com/LeapLabTHU/ExpeL)     |
| RLingua \[Chen et al., 2024]      | GPT-4                       | ×  | $\pi_g, v_g, \tau_\pi$ | sr, se           | -                                               |
| Xu et al. \[Xu et al., 2024]      | GPT-3.5-Turbo               | ×  | $\pi_l, v_l$           | sr, rob          | -                                               |
| LangGround \[Li et al., 2024]     | GPT-4                       | ×  | $\pi_l$                | sr, gen, se, int | [Link](https://github.com/romanlee6/langground) |

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

### Table of Comprehensive Planning Approaches

| Method                                | Model(s)      | FT | RL Role      | Metrics          | Code                                                 |
| ------------------------------------- | ------------- | -- | ------------ | ---------------- | ---------------------------------------------------- |
| SayTap \[Tang et al., 2023]           | GPT-4         | ×  | $\pi_g, v_g$ | sr, acc          | -                                                    |
| LgTS \[Shukla et al., 2024]           | Llama 2       | ×  | $\pi_g, v_g$ | sr, se           | -                                                    |
| PSL \[Dalal et al., 2024]             | GPT-4         | ×  | $\pi, v$     | sr, gen, se      | [Link](https://github.com/planseqlearn/planseqlearn) |
| LLaRP \[Szot et al., 2024]            | Llama         | ×  | $\pi_g, v_g$ | sr, gen, rob, se | [Link](https://github.com/apple/ml-llarp)            |
| LMA3 \[Colas et al., 2023]            | GPT-3.5-Turbo | ×  | $\pi_g$      | gen, exp         | -                                                    |
| When2Ask \[Hu et al., 2024]           | Vicuna        | ×  | $\pi, v$     | sr               | -                                                    |
| Inner Monologue \[Huang et al., 2022] | GPT-3, PaLM   | ×  | $\pi, v$     | sr, rob, al      | -                                                    |

### Table of Incremental Planning Approaches

| Method                           | Model(s)              | FT  | RL Role                            | Metrics           | Code                                                                          |
| -------------------------------- | --------------------- | --- | ---------------------------------- | ----------------- | ----------------------------------------------------------------------------- |
| SayCan \[Ichter et al., 2022]    | PaLM                  | ×   | $\pi_l, v_l, \text{rft}$           | sr, rob           | [Link](https://github.com/google-research/google-research/tree/master/saycan) |
| LLM4Teach \[Zhou et al., 2024]   | ChatGLM-Turbo, Vicuna | ×   | $\pi, v$                           | sr, se            | [Link](https://github.com/ZJLAB-AMMI/LLM4Teach)                               |
| AdaRefiner \[Zhang and Lu, 2024] | Llama 2, GPT-4        | ✓\* | $\pi_l, v_l, \tau_\pi$             | sr, rew, gen, exp | [Link](https://github.com/PKU-RL/AdaRefiner)                                  |
| BOSS \[Zhang et al., 2023b]      | Llama                 | ×   | $\pi_l, v_l, \text{rft}, \tau_\pi$ | sr, gen, rob, se  | -                                                                             |
| Text2Motion \[Lin et al., 2023]  | Codex, GPT-3.5        | ×   | $\pi, v$                           | sr, gen, int      | -                                                                             |


| Method                                                                          | Strategy    | Code |
| ------------------------------------------------------------------------------- | ----------- | ---- |
| [SayCan](https://github.com/google-research/google-research/tree/master/saycan) | Incremental | ✅    |
| [AdaRefiner](https://github.com/PKU-RL/AdaRefiner)                              | Incremental | ✅    |
| [Inner Monologue](https://arxiv.org/abs/2212.01599)                             | Hybrid      | -    |

---

## 🎯 LLM/VLM as Reward

**Reward Function**: Text2Reward, Eureka, Zeng et al.
**Reward Model**: VLM-RM, MineCLIP, RL-VLM-F

### Table of Reward Function Approaches

| Method                          | Model(s) | FT | RL Role            | Metrics         | Code                                              |
| ------------------------------- | -------- | -- | ------------------ | --------------- | ------------------------------------------------- |
| Text2Reward \[Xie et al., 2024] | GPT-4    | ×  | $\pi, \text{ref}$  | sr, se, al      | [Link](https://github.com/xlang-ai/text2reward)   |
| Zeng et al. \[2024]             | GPT-4    | ×  | $\pi, \tau_\pi$    | sr, se          | -                                                 |
| Eureka \[Ma et al., 2024]       | GPT-4    | ×  | $\pi, v, \tau_\pi$ | sr, gen, se, al | [Link](https://github.com/eureka-research/Eureka) |

### Table of Reward Model Approaches

| Method                           | Model(s)           | FT  | RL Role      | Metrics          | Code                                               |
| -------------------------------- | ------------------ | --- | ------------ | ---------------- | -------------------------------------------------- |
| Kwon et al. \[2023]              | GPT-3              | ×   | $\pi, v$     | acc, se, al      | -                                                  |
| PREDILECT \[Holk et al., 2024]   | GPT-4              | ×   | $\pi$        | rew, se, al      | -                                                  |
| ELLM \[Du et al., 2023]          | Codex, GPT-3       | ×   | $\pi_l, v_l$ | sr, gen, se, exp | -                                                  |
| RL-VLM-F \[Wang et al., 2024]    | Gemini-Pro, GPT-4V | ×   | $\pi, v$     | sr, rew, se      | [Link](https://github.com/yufeiwang63/RL-VLM-F)    |
| VLM-RM \[Rocamonde et al., 2024] | CLIP               | ×   | $\pi, v$     | sr, al           | [Link](https://github.com/AlignmentResearch/vlmrm) |
| MineCLIP \[Fan et al., 2022]     | CLIP               | ✓\* | $\pi_l, v_l$ | sr, gen, se, al  | [Link](https://github.com/MineDojo/MineDojo)       |

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
