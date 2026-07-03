# Release Index

用于汇总需要持续关注的开源项目、工具、模型或数据集的 release logs，重点关注 LLM training、post-training、agentic SLLM、推理服务以及 Ascend/NPU 生态相关工具链更新。

## Weekly Release Logs

| Week     | File                       | Notes |
| -------- |----------------------------| ----- |
| 2026-W27 | `release-logs/2026-W01.md` | 初始化示例 |

## Tracked Projects / Tools

| Name                                     | Repository / Website                               | Release Page / Change Source                                               | Type                             | Tracking Reason                                                                 | Status   |
| ---------------------------------------- | -------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------------------- | -------- |
| verl                                     | https://github.com/verl-project/verl               | https://github.com/verl-project/verl/releases                              | Framework / RL Training          | 跟踪 LLM RL post-training、RLHF、agentic training、rollout、tool calling 及训练后优化相关能力更新 | Tracking |
| vLLM                                     | https://github.com/vllm-project/vllm               | https://github.com/vllm-project/vllm/releases                              | Library / Inference Engine       | 跟踪高吞吐 LLM inference、serving、rollout、KV cache、scheduler 以及训练-推理联动能力变化            | Tracking |
| PyTorch                                  | https://github.com/pytorch/pytorch                 | https://github.com/pytorch/pytorch/releases                                | Framework                        | 跟踪底层训练框架、分布式训练、编译器、算子、性能优化和硬件兼容性更新                                              | Tracking |
| Transformers                             | https://github.com/huggingface/transformers        | https://github.com/huggingface/transformers/releases                       | Library / Model Framework        | 跟踪主流模型架构、tokenizer、training/inference API、模型加载方式和兼容性变化                          | Tracking |
| MindSpeed-LLM                            | https://gitcode.com/Ascend/MindSpeed-LLM           | https://gitcode.com/Ascend/MindSpeed-LLM/tags                              | Framework / Distributed Training | 跟踪 Ascend 生态下的大语言模型分布式预训练、指令微调、后训练、模型转换和工具链更新                                   | Tracking |
| MindSpeed                                | https://gitcode.com/Ascend/MindSpeed               | https://gitcode.com/Ascend/MindSpeed/tags                                  | Library / Acceleration           | 跟踪 Ascend NPU 上的大模型训练加速、并行策略、算子优化、内存优化和性能变化                                     | Tracking |
| vLLM Ascend                              | https://github.com/vllm-project/vllm-ascend        | https://github.com/vllm-project/vllm-ascend/releases                       | Plugin / Inference Backend       | 跟踪 vLLM 在 Ascend NPU 上的适配、版本兼容、安装要求、bug fix 和性能变化                               | Tracking |
| vLLM Ascend Docs                         | https://docs.vllm.ai/projects/ascend/en/main/      | https://docs.vllm.ai/projects/ascend/en/main/user_guide/release_notes.html | Documentation / Release Notes    | 跟踪 vLLM Ascend 官方文档中的 release notes、版本矩阵、安装说明和兼容性要求                             | Tracking |
| torch_npu / Ascend Extension for PyTorch | https://github.com/Ascend/pytorch                  | https://github.com/Ascend/pytorch/tags                                     | Plugin / PyTorch Backend         | 跟踪 PyTorch 与 Ascend NPU 的适配、算子支持、版本匹配、性能优化和兼容性变化                                | Tracking |
| verl-ascend-recipe                       | https://github.com/verl-project/verl-ascend-recipe | https://github.com/verl-project/verl-ascend-recipe/pulls                   | Recipe / Ascend Support          | 跟踪 verl 在 Ascend NPU 上的训练 recipe、环境配置、适配脚本、已知问题和使用方案更新                          | Tracking |

## Tracking Rules

1. 如果项目有正式 GitHub Releases，优先跟踪 Releases 页面。
2. 如果项目没有稳定的 Releases 页面，则跟踪 tags、release notes、documentation updates、important PRs/MRs 或主分支关键提交。
3. 每周只记录与团队研究、训练环境、推理服务、模型适配或实验复现直接相关的变更。
4. 不需要逐条复制完整 release notes，应提取对团队有实际影响的变化。
5. 当某个 release 影响依赖版本、硬件适配、训练流程、推理性能或实验结果可复现性时，在周记录中标记为 `Important`。
