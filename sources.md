# 来源与证据等级

本资料按“官方事实、官方自报结果、独立研究”区分，不把它们混为一谈。

## 官方来源

- **[O1] Qwen3.8-Max: A New Bar for Coding and Cowork**（Qwen Team，2026-08-03）
  https://qwen.ai/blog?id=qwen3.8
  用于：模型规模/激活参数、RL 环境与奖励设计、官方 benchmark 全表、各项评测脚注、权重发布时间表述。
  原始文章接口（包含该篇记录，文章标题为 `Qwen3.8-Max: A New Bar for Coding and Cowork`）：
  https://qwen.ai/api/v2/article/retrieval?language=en-US&path=qwen3.8&type=qwen_ai

- **[O2] QwenCloud: Qwen3.8-Max model page**
  https://www.qwencloud.com/models/qwen3.8-max
  用于：API 可用性、2.4T MoE、1M context、输入输出模态和内置工具。

- **[O3] Alibaba Cloud Model Studio: supported web-search models**
  https://help.aliyun.com/en/model-studio/web-search
  用于：`qwen3.8-max`/`qwen3.8-max-preview` 的当前 API 型号可用性。

- **[O4] Qwen3 Technical Report**（Qwen Team，2025）
  https://arxiv.org/abs/2505.09388
  用于：旧版 Qwen3 的 n-gram/LCS 去污染规则背景。该报告不能替代 Qwen3.8-Max 的训练数据审计。

## 独立研究

- **[R1] Soft Contamination Means Benchmarks Test Shallow Generalization**（Spiesberger et al.，2026，预印本）
  https://arxiv.org/abs/2602.12413
  用于：解释为什么精确 n-gram 去重不能排除语义重复，以及为什么 benchmark 高分不必然是 OOD 泛化证据。论文的受控实验涉及 Qwen3-8B-base，不是 Qwen3.8-Max 的污染检测。

## 第三方材料（时间快照）

- **[E1] Trilogy AI: Qwen 3.8 Max Benchmark: How It Compares With Kimi K3**（2026-07-19）
  https://trilogyai.substack.com/p/qwen-38-max-benchmark-how-it-compares
  用于：一个明确披露 harness、冻结输入、限制条件和盲评方式的单次外部工作流试验；不是通用排行榜。

- **[G1] QwenLM/qwen-code Issue #7332**（2026-07-20，已关闭）
  https://github.com/QwenLM/qwen-code/issues/7332
  用于：记录 preview 的 thinking-only 参数与 agent/harness 兼容性问题；不作为模型能力分数。

- **[C1] LINUX DO：Qwen3.8目前只有淌口水的水平**（2026-07-19）
  https://linux.do/t/topic/2614704?tl=en
  用于：两个实际任务的用户负样本，供后续转写为回归用例。

- **[C2] LINUX DO：qwen3.8 preview(qwen studio)这思考有点离谱了吧**（2026-07-20）
  https://linux.do/t/topic/2621929?tl=en
  用于：推理链长度、完成条件和工具适配的社区观测。

- **[C3] LINUX DO：qwen3.8 有点强啊！？**（2026-07-20）
  https://linux.do/t/topic/2617632?tl=en
  用于：短前端 demo 与同帖相互矛盾反馈的样本，不作能力排名。

- **[C4] LINUX DO：Qwen3.8 max preview 用量、套餐、价格、折扣分析**（2026-07-19）
  https://linux.do/t/topic/2614659?tl=en
  用于：用户成本推算线索，不替代官方价格。

- **[T1] Telegram：@linuxdoit 公开转发频道**（采集于 2026-08-04）
  https://t.me/s/linuxdoit?before=366453
  用于：发现与追溯公开 LINUX DO 转发；与原帖非独立样本。

- **[U1] Reddit：Qwen 3.8 Max Review - Good technical ability, judgement defaults to laziness instead of ambition**（2026-07-29 附近）
  https://www.reddit.com/r/Qwen_AI/comments/1va3v8j/qwen_38_max_review_good_technical_ability/
  用于：困难任务的需求覆盖与擅自降级风险线索。

- **[U2] Reddit：I built a complete Docker backup infrastructure with the new Qwen3.8-Max model**（2026-07-20）
  https://www.reddit.com/r/Qwen_AI/comments/1v174i8/i_built_a_complete_docker_backup_infrastructure/
  关联公开项目：https://github.com/Revolutionnnn/Docker-Vault
  用于：真实项目正向案例；作者明确保留了人工引导、review 和测试，不可将其直接归因于模型。

## 读取规则

1. [O1] 的数字是厂商自报；除非存在同配置的独立复现，不应写成“已经独立证实”。
2. [O2]/[O3] 证明当前产品和 API 功能，不证明 benchmark 能力。
3. [R1] 证明的是评测方法风险，不是对 Qwen3.8-Max 的具体指控。
4. [E1]、[G1]、[C1] 至 [C4]、[T1]、[U1] 和 [U2] 是不同强度的第三方时间快照；其版本、端点和配置不能默认相同，也不能按帖数加权投票。
