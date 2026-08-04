# Qwen3.8-Max 研究资料包

更新时间：2026-08-04（Asia/Singapore）

许可证：[MIT](LICENSE)。第三方实测、LinuxDo 与公开 Telegram 讨论将以可追溯的增量提交持续补充。

## 范围与结论

这里的“Qwen3.8”指 **Qwen3.8-Max**，不是 2025 年发布的 **Qwen3-8B**。

- Qwen3.8-Max 于 2026-08-03 正式发布；官方披露为 2.4T 参数、95B 激活参数的 MoE，并称后续一周会发布权重。[O1]
- 正式模型 ID 为 `qwen3.8-max`；`qwen3.8-max-preview` 的历史体验单独标注，绝不作为正式版的实测结论。[O2]
- 现有分数表很有竞争力，尤其是多模态、文档/办公、部分长程编码和工具任务；但截至本文档更新时间，主要证据仍是厂商发布的结果，不能把它直接等同于独立、同一 harness 下的排名。
- 官方公开的训练信息重点是“真实环境 + 可验证奖励”的后训练 RL 方案；没有公开完整技术报告、预训练数据来源/截止日期、去污染审计、数据混合比例或 RL 的完整超参数。因此无法仅凭官方材料判断其 benchmark 是否干净，更不能据此断言它在真实业务中的泛化能力。

## 文件索引

| 文件 | 内容 |
| --- | --- |
| `benchmark-assessment.md` | 官方分数的重点摘录、评测条件和可相信的边界。 |
| `training-and-contamination.md` | 已公开训练思路、数据污染风险，以及能与不能作出的推断。 |
| `validation-plan.md` | 用私有/新鲜任务验证真实能力、规避 benchmark 过拟合的可执行方案。 |
| `qwen3.8-max-current.md` | 正式版与 preview 的强制版本切分、正式版当前规格和第三方证据状态。 |
| `third-party-evidence.md` | 独立试验、LinuxDo、公开 Telegram、GitHub 与 Reddit 的分级证据台账。 |
| `sources.md` | 官方页面、原始 API 记录和论文链接。 |

## 推荐使用方式

不要把“某一项高分”当作采购或模型路由结论。先用相同的 agent harness、工具权限、超时、推理预算和 token 上限，将 Qwen3.8-Max 与候选模型跑在你的冻结私有任务集上；再将结果拆成：任务成功率、可复现测试通过率、人工返工率、时延、token/工具成本和失败模式。详见 `validation-plan.md`。

引用标记见 `sources.md`。
