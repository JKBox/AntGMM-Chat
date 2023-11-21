# AntGMM-Chat

## Approach

AntGMM-Chat is a multimodal method trained on a variety of multimodal datasets, which benefits many different tasks.

AntGMM-Chat has a total of 8B parameters. The visual encoder, dubbed as AntGMM-Encoder, is a transformer-based model with ~1B parameters. The LLM, namely LLaMA2-7B-ZH shares the same structure with LLaMA2-7B. Before multi-modal training, we first pre-train the visual encoder as well as the LLM respectively using in-house visual and multilingual data, where the visual encoder is trained from scratch and the LLM is initialized with LLaMA2-7B pre-trained weights. After that, we freeze LLaMA2-7B-ZH and update the rest parameters of the whole model in multimodal training process.

## Model architecture

<div align="center">
<img src=assets/framework.jpg style="zoom:40%">
