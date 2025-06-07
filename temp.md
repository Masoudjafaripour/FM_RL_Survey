## 🧠 Table of Contents

* [Datasets](#datasets)

* [LLM/VLM as Agent](#llmvlam-as-agent)

  * [Parametric Methods](#parametric-methods)

    * See: Table of Parametric LLM/VLM Agents
  * [Non-Parametric Methods](#non-parametric-methods)

    * See: Table of Non-Parametric LLM/VLM Agents

* [LLM/VLM as Planner](#llmvlam-as-planner)

  * [Comprehensive Planning](#comprehensive-planning)

    * See: Table of Comprehensive Planning Approaches
  * [Incremental Planning](#incremental-planning)

    * See: Table of Incremental Planning Approaches

* [LLM/VLM as Reward](#llmvlam-as-reward)

  * [Reward Function](#reward-function)

    * See: Table of Reward Function Approaches
  * [Reward Model](#reward-model)

    * See: Table of Reward Model Approaches

---

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
