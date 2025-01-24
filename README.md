# aigc_interview_note

# llm aigc 相关知识及面试题

本仓库为大模型面试相关概念，由本人参考网络资源整理，欢迎阅读，如果对你有用，麻烦点一下 `🌟 star`，谢谢！

<!-- 为了在低资源情况下，学习大模型，进行动手实践，创建 [tiny-llm-zh](https://github.com/wdndev/tiny-llm-zh)仓库，旨在构建一个小参数量的中文大语言模型，该项目已部署，可以在如下网站上体验：[ModeScope Tiny LLM](https://www.modelscope.cn/studios/wdndev/tiny_llm_92m_demo/summary)。 -->

其他学习资源推荐：

- tiny-llm: 实现一个简单 llm，模型架构：整体模型架构采用开源通用架构，包括：RMSNorm，RoPE，MHA 等
  实现细节：实现大模型两阶段训练及后续人类对齐，即：分词(Tokenizer) -> 预训练(PTM) -> 指令微调(SFT) -> 人类对齐(RLHF, DPO)-> 测评 -> 量化 -> 部署。
- tiny-rag: 实现一个简单的 RAG 系统，支持多路召回、重排等功能，快速了解搜索相关内容
- tiny-rlhf: 实现一个简单的 rlhf，包括 actor model、reference model、reward model、critic model4 个模型的更新迭代

<!-- - [AI 工程师八股](https://github.com/wdndev/ai_interview_note) : 包含深度学习、机器学习、推荐系统、搜索系统等通用知识 -->

## 在线阅读

在线阅读链接：[aigc_interview_notes]()

## 注意：

- ✍️ 公众号会整理 LLM、AIGC 的入门笔记、论文学习笔记、一线大厂面经等

 <img src=https://github.com/user-attachments/assets/27aaff49-132c-4e0e-9718-a975e7d426cf width = "130" height = "130" alt="weixin" />

欢迎关注加入知识星球，会不定期更新 AIGC 相关知识，以及一些面试、业务落地经验：
<img src=https://github.com/user-attachments/assets/74d0f245-e7ca-42f9-a486-f51849e4f610 width = "500" height = "700" alt="weixin" />

## 目录

- [首页](/)
- [LLM 基础](/1.数据篇/)
  - [1. 数据篇](/1.数据篇/)
    - [1.1 数据来源](/1.数据篇/1.1数据来源/1.1数据来源.md)
  - [1.2 数据预处理](/1.数据篇/)
    - [1.2.1 质量过滤](/1.数据篇/1.2数据预处理/1.2数据预处理.md)
    - [1.2.2 敏感内容过滤](/1.数据篇/1.2数据预处理/1.2数据预处理.md)
    - [1.2.3 冗余去重](/1.数据篇/1.2数据预处理/1.2数据预处理.md)
    - [1.2.4 tokenizer 分词](/1.数据篇/1.2数据预处理/1.2数据预处理.md)
  - [1.3 面试题](/1.数据篇/1.3面试题/1.3面试题.md)
- [2.大模型架构](/2.大模型架构篇/)
  - [2.1 基础知识](/2.大模型架构篇/)
  - [2.2 因果解码器](/2.大模型架构篇/)
    - [1.位置编码](/2.大模型架构篇/2.4位置编码/2.4位置编码.md)
    - [2.layer_normalization](/2.大模型架构篇/2.4位置编码/2.4位置编码.md)
    - [3.激活函数](/02.大语言模型架构/6.激活函数/6.激活函数.md "6.激活函数")
  - [2.3 注意力](/02.大语言模型架构/)
    - [Self Attention](/2.大模型架构篇/2.3attention/2.3.1self%20attention.md)
    - [MHA](/2.大模型架构篇/2.3attention/2.3.2MHA.md)
    - [MQA](/2.大模型架构篇/2.3attention/2.3.3MQA.md)
    - [GQA](/2.大模型架构篇/2.3attention/2.3.4GQA.md)
    - [MLA](/2.大模型架构篇/2.3attention/2.3.5MLA.md)
    - [小结](/2.大模型架构篇/2.3attention/2.3.6小结.md)
  - [2.4 llama 系列](/2.大语言模型架构/)
    - [llama 系列模型](/2.大模型架构篇/2.1llama系列/2.1llama系列.md)
  - [2.5 MoE](/2.大语言模型架构/)
    - [MoE 经典论文](/02.大语言模型架构/1.MoE论文/1.MoE论文.md "1.MoE论文")
  - [2.6 面试题](/2.大模型架构篇/2.5面试题/面试题.md)
- [3.分布式训练](/3.分布式训练/)
  - [3.1 基础知识](/3.分布式训练/)
    - [3.1.1.数据并行](/3.分布式训练/3.1基础知识/3.1.1数据并行/数据并行.md)
    - [3.1.2.流水线并行](/3.分布式训练/3.1基础知识/3.1.2流水线并行/流水线并行.md)
    - [3.1.3.张量并行](/3.分布式训练/3.1基础知识/3.1.3张量并行/张量并行.md)
    - [3.1.4.序列并行](/04.分布式训练/5.序列并行/5.序列并行.md "5.序列并行")
    - [3.1.5.多维度混合并行](/04.分布式训练/6.多维度混合并行/6.多维度混合并行.md "6.多维度混合并行")
    - [3.1.6.自动并行](/04.分布式训练/7.自动并行/7.自动并行.md "7.自动并行")
    - [3.1.7.moe 并行](/04.分布式训练/8.moe并行/8.moe并行.md "8.moe并行")
    - [3.1.8.总结](/04.分布式训练/9.总结/9.总结.md "9.总结")
  - [3.2 DeepSpeed](/3.分布式训练/3.2DeepSeed/)
    - [deepspeed 介绍](/3.分布式训练/3.2DeepSeed/DeepSeed.md)
  - [3.3 Megatron](/3.分布式训练/3.3Megatron/Megatron.md)
  - [3.4 面试题](/3.分布式训练/3.4面试题/面试题.md)
  <!-- - [4.5 一些有用的文章](/04.分布式训练/)
  - [4.6 一些题目](/04.分布式训练/)
    - [1.分布式训练题目](/04.分布式训练/分布式训练题目/分布式训练题目.md "分布式训练题目")
    - [2.显存问题](/04.分布式训练/1.显存问题/1.显存问题.md "1.显存问题") -->
- [4.RLHF](/4.RLHF)
  - [4.1 基础知识](/4.RLHF)
    - [策略梯度（pg）](/4.强化学习/策略梯度（pg）/策略梯度（pg）.md "策略梯度（pg）")
  - [4.2 DPO](/4.RLHF/4.2DPO/DPO.md)
  - [4.3 PPO](/4.RLHF/4.3PPO/PPO.md)
  - [4.3 面试题](/4.RLHF//4.4面试题/面试题.md)
- [5.有监督微调](/05.有监督微调/)
  - [5.1 理论](/05.有监督微调/)
    - [1.基本概念](/05.有监督微调/1.基本概念/1.基本概念.md "1.基本概念")
    - [2.prompting](/05.有监督微调/2.prompting/2.prompting.md "2.prompting")
    - [3.adapter-tuning](/05.有监督微调/3.adapter-tuning/3.adapter-tuning.md "3.adapter-tuning")
    - [4.lora](/05.有监督微调/4.lora/4.lora.md "4.lora")
    - [5.总结](/05.有监督微调/5.总结/5.总结.md "5.总结")
  - [5.2 微调实战](/05.有监督微调/)
    - [llama2 微调](/05.有监督微调/llama2微调/llama2微调.md "llama2微调")
- [6.大模型推理](/6.大模型推理篇/)

  - [6.1 推理框架](/6.大模型推理篇/6.1推理框架/推理框架.md)

    <!-- - [1.vllm](/06.推理/1.vllm/1.vllm.md "1.vllm")
    - [2.text_generation_inference](/06.推理/2.text_generation_inference/2.text_generation_inference.md "2.text_generation_inference")
    - [3.faster_transformer](/06.推理/3.faster_transformer/3.faster_transformer.md "3.faster_transformer")
    - [4.trt_llm](/06.推理/4.trt_llm/4.trt_llm.md "4.trt_llm") -->

  - [6.2 推理优化技术](/6.大模型推理篇/6.2推理优化/推理优化.md)
  - [6.3 量化](/6.大模型推理篇/6.3量化/量化.md)
  - [6.4 面试题](/6.大模型推理篇/6.4面试题/面试题.md)

- [7.检索增强 RAG](/7.RAG/)
  - [7.1 RAG 概述](/7.RAG/7.1RAG概述/rag概述.md/)
  - [7.2 高级 RAG](/7.RAG/7.2高级RAG/高级rag.md)
  - [7.3 RAG 实践](/7.RAG/7.3RAG实践/rag实践.md)
  - [7.4 面试题](./7.RAG/7.4面试题/面试题.md)
- [98.相关课程](/98.相关课程/)
- [99.参考资料](/99.参考资料/)
