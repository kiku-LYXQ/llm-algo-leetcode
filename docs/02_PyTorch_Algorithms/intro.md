# Chapter 2: PyTorch 算法实战

## 🎯 本章概览

本章聚焦 PyTorch 级别的大模型实现，按“基础算子 -> 模型架构 -> 微调与训练技术 -> 对齐技术 -> 反向传播与显存优化 -> 核心推理优化 -> 高级推理优化 -> 分布式与扩展”组织。

### 快速入口

- [2.1 基础算子](./2_1.md)
- [2.2 模型架构](./2_2.md)
- [2.3 微调与训练技术](./2_3.md)
- [2.4 对齐技术](./2_4.md)
- [2.5 反向传播与显存优化](./2_5.md)
- [2.6 核心推理优化](./2_6.md)
- [2.7 高级推理优化](./2_7.md)
- [2.8 分布式与扩展](./2_8.md)
- [Chapter 1 导学](../01_Hardware_Math_and_Systems/intro.md)
- [Chapter 3 导学](../03_CUDA_and_Triton_Kernels/intro.md)
- [使用指南](../guide.md)
- [维护与发布手册](../maintenance.md)

### 学习组划分

| 学习组 | 题目范围 | 主题 | 难度 |
|:---|:---|:---|:---|
| **2.1: 基础算子** | 00-04 | Transformer 组件 | Easy-Medium |
| **2.2: 模型架构** | 05-08 | 模型组装 | Medium |
| **2.3: 微调与训练技术** | 09-11 | SFT / LoRA / 调度器 | Medium |
| **2.4: 对齐技术** | 12-13 | RLHF / DPO | Medium-Hard |
| **2.5: 反向传播与显存优化** | 14 | Autograd / Backward | Hard |
| **2.6: 核心推理优化** | 15-17 | FlashAttention / Decoding / PagedAttention | Hard |
| **2.7: 高级推理优化** | 18-20 | Speculative / Radix / Quantization | Hard |
| **2.8: 分布式与扩展** | 21-25 | Checkpointing / ZeRO / Parallelism | Hard |

### 环境边界（代码审计版）

- **整体定位：CPU-first**
- **大多数 notebook**：可在 CPU 环境下完成学习和 correctness 验证
- **已确认需要 GPU 的 notebook**：`21_Gradient_Checkpointing`，其测试会读取真实 CUDA 显存峰值
- **学习建议**：为了保持体验一致，建议所有学习者使用同一套 Python 环境；GPU 作为后段实验和真实性能验证的增强条件，而不是 Chapter 2 的统一门槛

### 学习建议

- 新手先看 **2.1 -> 2.2 -> 2.3**
- 关注训练与对齐的同学看 **2.3 -> 2.4 -> 2.5**
- 关注推理与规模化的同学看 **2.6 -> 2.7 -> 2.8**

### 前置页面

- [1A 基础数学](../01_Hardware_Math_and_Systems/01_Data_Types_and_Precision.md)
- [1B 硬件架构](../01_Hardware_Math_and_Systems/03_GPU_Architecture_and_Memory.md)
- [1C 系统与编译](../01_Hardware_Math_and_Systems/08_Programming_Models_CUDA_Triton.md)

### 后续页面

- [2.1 基础算子](./2_1.md)
- [2.4 对齐技术](./2_4.md)
- [2.5 反向传播与显存优化](./2_5.md)
- [2.6 核心推理优化](./2_6.md)
- [2.8 分布式与扩展](./2_8.md)
- [3.1 Triton 基础](../03_CUDA_and_Triton_Kernels/intro.md)

### 题目与测试

章节题目的占位初始化、答案验证和本地测试方式，统一以 [维护与发布手册](../maintenance.md) 和 [使用指南](../guide.md) 为准。
