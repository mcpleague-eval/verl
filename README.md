<div align="center">
  Hi, everyone! 
    verl is a RL training library initiated by <b>ByteDance Seed team</b> and maintained by the verl community.
    <br>
    <br>
</div>

<div align="center">

<a href="https://deepwiki.com/volcengine/verl"><img src="https://devin.ai/assets/deepwiki-badge.png" alt="Ask DeepWiki.com" style="height:20px;"></a>
[![GitHub Repo stars](https://img.shields.io/github/stars/volcengine/verl)](https://github.com/volcengine/verl/stargazers)
[![Twitter](https://img.shields.io/twitter/follow/verl_project)](https://twitter.com/verl_project)
<a href="https://join.slack.com/t/verlgroup/shared_invite/zt-2w5p9o4c3-yy0x2Q56s_VlGLsJ93A6vA"><img src="https://img.shields.io/badge/Slack-verl-blueviolet?logo=slack&amp"></a>
<a href="https://arxiv.org/pdf/2409.19256"><img src="https://img.shields.io/static/v1?label=EuroSys&message=Paper&color=red"></a>
[![Documentation](https://img.shields.io/badge/documentation-blue)](https://verl.readthedocs.io/en/latest/)
<a href="https://raw.githubusercontent.com/eric-haibin-lin/verl-community/refs/heads/main/WeChat.JPG"><img src="https://img.shields.io/badge/-green?logo=wechat&amp"></a>

</div>

![seed logo](https://github.com/user-attachments/assets/c42e675e-497c-4508-8bb9-093ad4d1f216)

<h1 style="text-align: center;">verl: Volcano Engine Reinforcement Learning for LLMs</h1>

verl is a flexible, efficient and production-ready RL training library for large language models (LLMs).

verl is the open-source version of **[HybridFlow: A Flexible and Efficient RLHF Framework](https://arxiv.org/abs/2409.19256v2)** paper.

verl is flexible and easy to use with:

- **Easy extension of diverse RL algorithms**: The hybrid-controller programming model enables flexible representation and efficient execution of complex post-training dataflows. Build RL dataflows such as GRPO, PPO in a few lines of code.

- **Seamless integration of existing LLM infra with modular APIs**: Decouples computation and data dependencies, enabling seamless integration with existing LLM frameworks, such as FSDP, Megatron-LM, vLLM, SGLang, etc

- **Flexible device mapping**: Supports various placement of models onto different sets of GPUs for efficient resource utilization and scalability across different cluster sizes.

- Ready integration with popular HuggingFace models

verl is fast with:

- **State-of-the-art throughput**: SOTA LLM training and inference engine integrations and SOTA RL throughput.

- **Efficient actor model resharding with 3D-HybridEngine**: Eliminates memory redundancy and significantly reduces communication overhead during transitions between training and generation phases.

</p>

## News
- [2025/07] The [ReTool](https://arxiv.org/pdf/2504.11536) recipe is fully open sourced. [Blog](https://www.notion.so/verl-reTool-recipe-Using-multi-round-conversations-and-code-sandboxing-to-improve-the-math-of-large-23a8b5b7feba80b386b2e5b5e3c1cde0)
- [2025/07] The first verl meetup will be held at ICML Vancouver on July 16th! Please [join us](https://lu.ma/0ek2nyao) if you are at ICML! (onsite only)
- [2025/07] verl keynote at [AWS AI Hours Singapore](https://pages.awscloud.com/aws-ai-hours-sg.html#agenda) on 7/8, verl & verl-agent project updates at [Agent for SWE meetup](https://lu.ma/e498qhsi) by LF AI & Data Singapore on 7/11.
- [2025/06] verl with Megatron backend enables large MoE models such as [DeepSeek-671b and Qwen3-236b](https://verl.readthedocs.io/en/latest/perf/dpsk.html).
- [2025/06] verl team will provide latest project updates at [PyTorch Day China](https://www.lfasiallc.com/pytorch-day-china/) on June 7th. Meet our dev team in Beijing!
- [2025/04] [Seed-Thinking-v1.5](https://github.com/ByteDance-Seed/Seed-Thinking-v1.5/blob/main/seed-thinking-v1.5.pdf) tech report is released! Trained with verl, Seed-Thinking-v1.5 achieves 86.7 on AIME 2024, 55.0 on Codeforces and 77.3 on GPQA, demonstrating excellent reasoning abilities in STEM and coding. Beyond reasoning tasks, the method demonstrates notable generalization across diverse domains.
- [2025/03] [DAPO](https://dapo-sia.github.io/) is the open-sourced SOTA RL algorithm that achieves 50 points on AIME 2024 based on the Qwen2.5-32B pre-trained model, surpassing the previous SOTA achieved by DeepSeek's GRPO (DeepSeek-R1-Zero-Qwen-32B). DAPO's training is fully powered by verl and the reproduction code is available in `recipe/dapo` now.
<details><summary> more... </summary>
<ul>
  <li> [2025/04] [VAPO](https://arxiv.org/pdf/2504.05118) (value-based augmented PPO) paper covers our latest RL method for reasoning models. Trained from Qwen-32B-base model, VAPO achieves 60.4 on AIME 2024, outperforming DAPO-32B.</li>
  <li>[2025/05] [PF-PPO](https://arxiv.org/abs/2409.06957), accepted to ICML 2025, is now supported in verl! PF-PPO enhances policy learning efficiency and robustness by filtering potentially noisy reward signals and reusing high-quality experiences via a replay buffer.</li>
  <li>[2025/04] We will give a tutorial about latest post-training techniques and programming guide for verl at [ICLR 2025 Expo](https://iclr.cc/virtual/2025/calendar?filter_events=Expo+Talk+Panel&filter_rooms=), [SCI-FM workshop](https://open-foundation-model.github.io/) and [LMSys afterparty](https://lu.ma/d23nyynm). Talk materials available [here](https://github.com/eric-haibin-lin/verl-community/tree/main/iclr25). </li>
  <li>[2025/03] verl v0.3.0.post1 is released! See [release note](https://github.com/volcengine/verl/releases/) for details. It achieves [~1.4x speedup](https://tongyx361.github.io/blogs/posts/verl-intro/#/verl-flexible-and-efficient-rl-for-llms) compared to prev versions.</li>
  <li>[2025/05] verl will be presented at [A2M Shanghai](https://a2m.msup.com.cn/home/?aid=4488&city=shanghai) on 5/16 - 5/17.</li>
  <li>[2025/05] verl will be presented at [GOSIM x PyTorch Day 2025](https://paris2025.gosim.org/). See you in Paris! </li>
  <li>[2025/03] We introduced the programming model of verl at the [vLLM Beijing Meetup](https://mp.weixin.qq.com/s/n77GibL2corAtQHtVEAzfg) and [verl intro and updates](https://github.com/eric-haibin-lin/verl-community/blob/main/slides/verl-lmsys-meetup.pdf) at the [SGLang-LMSYS Org Meetup](https://lu.ma/ntjrr7ig) in Sunnyvale mid-March.</li>
  <li>[2025/03] We will present verl(HybridFlow) at EuroSys 2025. See you in Rotterdam!</li>
  <li>[2025/02] verl v0.2.0.post2 is released!</li>
  <li>[2025/02] We presented verl in the <a href="https://lu.ma/ji7atxux">Bytedance/NVIDIA/Anyscale Ray Meetup</a>. See you in San Jose!</li>
  <li>[2025/01] [Doubao-1.5-pro](https://team.doubao.com/zh/special/doubao_1_5_pro) is released with SOTA-level performance on LLM & VLM. The RL scaling preview model is trained using verl, reaching OpenAI O1-level performance on math benchmarks (70.0 pass@1 on AIME).</li>
  <li>[2024/12] verl is presented at Ray Forward 2024. Slides available <a href="https://github.com/eric-haibin-lin/verl-community/blob/main/slides/Ray_Forward_2024_%E5%B7%AB%E9%94%A1%E6%96%8C.pdf">here</a></li>
  <li>[2024/12] The team presented <a href="https://neurips.cc/Expo/Conferences/2024/workshop/100677">Post-training LLMs: From Algorithms to Infrastructure</a> at NeurIPS 2024. <a href="https://github.com/eric-haibin-lin/verl-data/tree/neurips">Slides</a> and <a href="https://neurips.cc/Expo/Conferences/2024/workshop/100677">video</a> available.</li>
  <li>[2024/10] verl is presented at Ray Summit. <a href="https://www.youtube.com/watch?v=MrhMcXkXvJU&list=PLzTswPQNepXntmT8jr9WaNfqQ60QwW7-U&index=37">Youtube video</a> available.</li>
  <li>[2024/08] HybridFlow (verl) is accepted to EuroSys 2025.</li>
</ul>   
</details>

## Key Features

- **FSDP**, **FSDP2** and **Megatron-LM** for training.
- **vLLM**, **SGLang** and **HF Transformers** for rollout generation.
- Compatible with Hugging Face Transformers and Modelscope Hub: [Qwen-3](https://github.com/volcengine/verl/blob/main/examples/grpo_trainer/run_qwen3-8b.sh), Qwen-2.5, Llama3.1, Gemma2, DeepSeek-LLM, etc
- Supervised fine-tuning.
- Reinforcement learning with [PPO](examples/ppo_trainer/), [GRPO](examples/grpo_trainer/), [ReMax](examples/remax_trainer/), [REINFORCE++](https://verl.readthedocs.io/en/latest/examples/config.html#algorithm), [RLOO](examples/rloo_trainer/), [PRIME](recipe/prime/), [DAPO](recipe/dapo/), [DrGRPO](recipe/drgrpo), [KL_Cov & Clip_Cov](recipe/entropy) etc.
  - Support model-based reward and function-based reward (verifiable reward) for math, [coding](https://github.com/volcengine/verl/tree/main/recipe/dapo), etc
  - Support vision-language models (VLMs) and [multi-modal RL](examples/grpo_trainer/run_qwen2_5_vl-7b.sh) with Qwen2.5-vl, Kimi-VL
  - [Multi-turn with tool calling](https://github.com/volcengine/verl/tree/main/examples/sglang_multiturn)
- LLM alignment recipes such as [Self-play preference optimization (SPPO)]](https://github.com/volcengine/verl/tree/main/recipe/sppo)
- Flash attention 2, [sequence packing](examples/ppo_trainer/run_qwen2-7b_seq_balance.sh), [sequence parallelism](examples/ppo_trainer/run_deepseek7b_llm_sp2.sh) support via DeepSpeed Ulysses, [LoRA](examples/sft/gsm8k/run_qwen_05_peft.sh), [Liger-kernel](examples/sft/gsm8k/run_qwen_05_sp2_liger.sh).
- Scales up to 671B models and hundreds of GPUs with [expert parallelism](https://github.com/volcengine/verl/pull/1467)
- Multi-gpu [LoRA RL](https://verl.readthedocs.io/en/latest/advance/ppo_lora.html) support to save memory.
- Experiment tracking with wandb, swanlab, mlflow and tensorboard.

...(content truncated for brevity)...

We are HIRING! Send us an [email](mailto:haibin.lin@bytedance.com) if you are interested in internship/FTE opportunities in RL for agents.


hello world
