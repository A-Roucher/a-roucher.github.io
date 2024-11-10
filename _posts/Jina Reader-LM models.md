---
title: Jina Reader-LM models
toc: true
categories: 
* AI news
* 
* 
tags:
  - AI
  - LLM
---


Tags: New models

**Extracting your HTML webpages to markdown is now possible end-to-end with a simple LLM! 👏**

Jina just released Reader-LM, that handles the whole pipeline of extracting markdown from HTML webpages. 

A while ago, Jina had released a completely code-based deterministic program to do this extraction, based on some heuristics : e.g., “if the text is in a <p> tag, keep it, but if it’s hidden behind another, remove it”.

🤔 But they received complaints from readers: some found it too detailed, other not enough, depending on the pages. 

➡️ So they decided, maybe heuristics were not enough: instead, they tried to train a LLM to do the complete extraction. This LLM does not need to be very strong,but it should handle a very long context: it’s a challenging, “shallow-but-wide” architecture.

Technical insights:

2️⃣ models: Reader-LM-0.5B and 1.5B

⚙️ Two stages of training: first, short and simple HTML to get the basics, then ramp up to longer and harder HTML up to 128k tokens

🔎 Use contrastive search for decoding: this empirically reduces “repeating output” issues

➡️ Their models beat much larger models at HTML extraction 🔥

🤗 Weights available on HF (sadly cc-by-nc license)