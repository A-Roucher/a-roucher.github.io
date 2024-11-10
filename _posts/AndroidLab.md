---
title: AndroidLab
toc: true
categories: 
- AI news
tags:
  - Artificial Intelligence
  - LLMs
---

AndroidLab: First ever systematic benchmark for Android mobile agents shows that small, fine-tuned open models can power a JARVIS system on your smartphone 📱🔥

A team from Tsinghua University just released AndroidLab, the first systematic framework to evaluate and train Android mobile agents that works with both text-only and multimodal models.

They show that fine-tuning small open-source models can significantly boost performance, matching that of much bigger closed models like GPT-4o.

The team built:

📊 A reproducible benchmark with 138 tasks across 9 apps to evaluate mobile agents systematically

📝📱 A framework supporting both text-only (via XML) and visual (via marked screenshots) interfaces

✅ An instruction dataset of 10.5k operation traces for training mobile agents

Key insights:

- 📈 Fine-tuning improves performance BY A LOT: Open-source model Llama-3.1-8B improves from 2% to 24% success rate after training, nearly reaching GPT-4o performance although it’s much smaller
- ⚙️ Text-only agents match multimodal ones: XML-based agents achieve similar performance to screenshot-based multimodal agents.

![Capture d’écran 2024-11-08 à 10.38.55.png](Capture_decran_2024-11-08_a_10.38.55.png)