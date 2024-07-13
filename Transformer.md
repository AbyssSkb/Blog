---
title: Transformer 发展简史
date: 2024-6-20 12:00:00
tags: [AI, Transformer]
---
## 前言
高二下学期，一次偶然的机会，我接触到了 AI。当时的我加入到了一位好朋友的行列中，一起学习机器学习。机器学习（Machine Learning）是一门人工智能的科学，该领域的主要研究对象是人工智能，特别是如何在经验学习中改善具体算法的性能。 在那段快乐的时光，我接触到了许多机器学习领域的知识。在听完吴恩达的机器学习课程后，我开始接触深度学习。深度学习（Deep Learning）是机器学习的分支，是一种以人工神经网络为架构，对资料进行表征学习的算法。 很快，一起学习 AI 的队伍扩充到了 3 人。依稀记得，在晚自习课间，我们仨在机房讨论反向传播的原理。你或许难以想象，当我们手搓出一个可以实现任意层隐藏层的普通神经网络时，内心是多么的喜悦。高二结束之际，随着 GPT-3.5 的爆火，人工智能逐渐走进大众的视野。在高三的闲暇时间，我接触到了 Transformer，被其巧妙的结构所迷住，而这也是写这篇文章的原因之一。	

## 发展历史	
在自然语言处理（NLP）领域中，机器翻译（Machine Translation）任务自提出起就备受关注，许多模型都对其发出了挑战，RNN就是其中一个典型代表。RNN（Recurrent Neural Network）在网络结构上进行了创新，引入了循环神经元，从而使输入和输出没有长度限制，且具有序列性，能够较好地完成机器翻译任务。但其结构上有一个致命缺陷，把单词按照序列顺序不断输入神经网络中，这使其难以捕捉长距离的依赖关系，同时也难以实现并行化，在处理长序列时速度较慢。虽然后续有人在此基础上进行改进后提出了 LSTM（Long Short-Term Memory）和 GRU（Gated Recurrent Unit），通过引入门机制，提高了 RNN 在处理长序列和复杂时间依赖关系上的性能，但其基本网络结构仍未改变，依旧存在局限性。

2017 年，Google 团队 Vaswani 等人在论文《Attention is All You Need》中提出了 Transformer，该模型创新性地引入了自注意力机制（Self-Attention）以及多头注意力机制（Multi-Head Attention），能够并行处理一段序列，理解其中不同位置单词之间的联系。2018 年，OpenAI提出了 GPT（Generative Pre-trained Transformer）模型，其先在大量无标签的文本数据集上进行自监督预训练，然后在具体要学习的任务上进行微调，在许多数据集上的指标均取得了巨大突破。同年 Google 团队 Devlin 等人提出了 BERT（Bidirectional Encoder Representations from Transformers），该模型使用了双向编解码器，进一步提高了理解上下文的能力，以掩码语言模型 (MLM) 为任务在大量文本数据集上进行自监督预训练后，在对应任务的数据集上微调即可表现出优异的性能。

2020 年，Alexey Dosovitskiy 等人提出了 ViT（Vision Transformer），标志着 Transformer 开始应用于计算机视觉领域。ViT 将一幅图像分割成许多块，经过线性变换投影到高维空间后排成一条序列作为 Transformer 的输入，在 ImageNet 数据集上对图像分类取得了与卷积神经网络（CNN）相媲美的结果，证明了 Transformer 在视觉任务上的潜力。在目标检测任务上，Nicolas Carion 等人随后提出了 DETR（Detection Transformer），直接输出目标的类别和准确位置不再需要用传统的锚框（Anchor Box）和非极大值抑制（Non-Maximum Suppression），真正意义上实现了端对端（End-to-End）。由于 Transformer 相比于传统卷积神经网络来说结构较为复杂，计算复杂度高，不太适用于对延迟要求较高的实时目标检测任务（Real-Time Object Detection）中，对此百度于 2024 年提出了 RT-DETR（Real-Time Detection Transformer），采用了一种高效地混合编码器，减少了计算复杂度。

2020年后，多模态 Transformer 模型开始兴起。2021年，OpenAI 提出了 CLIP（Contrastive Language-Image Pre-training），通过对图像和文本数据进行联合训练，实现了跨模态的视觉和语言理解能力。同时，OpenAI 提出了 DALL-E，支持从文本描述生成图像。

## 回顾与展望
Transformer 诞生之初主要是为了解决机器翻译问题，经过后人的不懈努力，其通用性不断提高，如今已应用于自然语言处理的方方面面，如 OpenAI 推出的基于 Transformer 的语音识别模型 Whisper 能够提取出音频中的文字，支持绝大多数语言。2023 年是生成式 AI 的爆发之年，OpenAI 推出了迭代产品 GPT-4，Google 推出了 Gemini 系列，国内基于 Transformer 的 AI 大模型也层出不穷，如百度文心一言、阿里云的通义千问等。除了自然语言处理，Transformer 也渗透到计算机视觉领域，在许多任务上均达到了 SOTA（State-of-the-Arts）。

未来，我相信 Transformer 在其他方面的应用会得到进一步的挖掘，不只是局限于自然语言处理和计算机视觉，还可以拓展到天气预测、物质结构预测、证明数学定律等方面。注意力机制让 Transformer 拥有了理解事物的能力，未来基于 Transformer 的大模型在理解真实世界上的能力会得到进一步提高，如能够理解物理规律、人们的行为、人们的心理。OpenAI 推出的基于 Transformer 的大模型 GPT-4 涌现出的强大能力让人们看到了 AGI（通用人工智能）的希望，加速了人类对 AGI 的探索，我们或许即将迎接一个新世界的到来。

## 结语
了解 Transformer 的发展史，能帮助我们更好地梳理整个 Transformer 体系，进而深入和系统地学习，还能让我们看到未来，AI 可能会对人们日常生活的哪些方面产生影响。最后，感谢一直陪伴我学AI的伙伴 `zhz` 和 `yyc`，没有他们，我学习 AI 的道路上会失去很多快乐。
