# README 分类映射

写入前先读取 `README.md` 确认最新结构；本文件为快速参考。

## TOC 顶层

| 领域 | TOC 标签 | 说明 |
|------|----------|------|
| AIGC | **AIGC** (AI Generated Content) | 生成式内容 |
| LLM/VLM | **LLM / VLM** | 语言/视觉语言模型 |
| CV | **CV** (Computer Vision) | 计算机视觉 |

## AIGC 子分类

| 用户可能说的 | README 章节 | 锚点 |
|-------------|-------------|------|
| GAN | Generative Adversarial Network | `#Generative-Adversarial-Network` |
| VAE | Variational Auto-Encoder | `#Variational-Auto-Encoder` |
| Diffusion / 扩散 | Diffusion Model | `#Diffusion-Model` |
| AIGC 应用 | AIGC-Applications | `#AIGC-Applications` |
| 人脸编辑 / Face Editing | AIGC-Applications → Face Editing | `#Face-Editing` |
| 换脸 / Face Swapping | AIGC-Applications → Face Swapping | `#Face-Swapping` |

## LLM / VLM 子分类

| 用户可能说的 | README 章节 | 锚点 |
|-------------|-------------|------|
| Transformer / Attention | Attention or Transformer | `#Attention-or-Transformer` |
| ViT / Vision Transformer | Vision Transformer | `#Vision-Transformer` |

## CV 子分类

| 用户可能说的 | README 章节 | 锚点 |
|-------------|-------------|------|
| Backbone / 分类网络 | Backbone | `#Backbone` |
| Detection / 检测 | Object Detection | `#Object-Detection` |
| Segmentation / 分割 | Object Segmentation | `#Object-Segmentation` |
| Tracking / 跟踪 | Object Tracking | `#Object-Tracking` |
| MOT / 多目标跟踪 | Object Tracking → Multiple Object Tracking | `#Multiple-Object-Tracking` |
| VOT / 单目标跟踪 | Object Tracking → Visual Object Tracking | `#Visual-Object-Tracking` |
| FSS / 少样本分割 | Few-Shot Segmentation | `#Few-Shot-Segmentation` |
| FSL / 少样本学习 | Few-Shot Learning | `#Few-Shot-Learning` |
| 3D Face / 三维人脸 | 3D Face Reconstruction and Facial Animation | `#3D-Face-Reconstruction-and-Facial-Animation` |
| SOD / 显著性检测 | Salient Object Detection | `#Salient-Object-Detection` |
| 3D Detection | 3D Object Detection | `#3D-Object-Detection` |
| Optimization / 优化 | Optimization | `#Optimization` |
| Survey / 综述 | Survey | `#Survey` |

## 分类选择原则

1. 优先匹配**最具体**的子分类（如 Face Editing 而非 AIGC-Applications）
2. 用户给出分类线索时优先采用，但仍需与论文内容一致
3. 无法确定时列出 2–3 个候选分类，请用户选择
4. 新建分类需用户明确指令，并同步更新 TOC 与 `##` 标题
