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

## 读取规则

1. [O1] 的数字是厂商自报；除非存在同配置的独立复现，不应写成“已经独立证实”。
2. [O2]/[O3] 证明当前产品和 API 功能，不证明 benchmark 能力。
3. [R1] 证明的是评测方法风险，不是对 Qwen3.8-Max 的具体指控。
