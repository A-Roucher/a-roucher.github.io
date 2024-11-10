---
title: Llama 3 2 release
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

**Llama 3.2: Meta completes their Llama 3 collection of models with new 1B, 3B and 11B + 90B multimodal models (vision + text)**

- Releases a collection of 11 models:
    - Text 1B and 3B, in instruct & base versions
    - Llama-Guard 3B, in normal & int4 versions
    - Text+vision: 11B & 90B, instruct & base
    - Guard 11B vision
- Vision models trained on 6B image/text pairs
- 1B/3B trained on 9T tokens (vs 15T for Llama-3.1 series)
- “Llama 3.2 is the first Llama model to support vision tasks, with a new model architecture that integrates image encoder representations into the language model”
    - Images up to 1120x1120 resolution
- Languages:  English, German, French, Italian, Portuguese, Hindi, Spanish, Thai
- If EU based, you cannot access the weights ([link](https://huggingface.slack.com/archives/C06SSAAGJ6Q/p1726855714784769?thread_ts=1726719784.327169&cid=C06SSAAGJ6Q)), but can access some end products deployed from elsewhere
    - So it means you can still use the model in Hugging Chat and Inference Endpoints!
- 90B vision: [base LLM should be frozen so metrics on text tasks match the 70B](https://huggingface.slack.com/archives/C06SSAAGJ6Q/p1727185776040669?thread_ts=1727185119.255999&cid=C06SSAAGJ6Q)
- Scores

Score comparison vs Qwen2.5:

The 3B model is as strong as the 8B one on IFEval! This high IFEval score is very impressive for a model of this size.

| Model                | BBH   | MATH Lvl 5 | GPQA  | MUSR  | MMLU-PRO | Average |

| Meta-Llama-3.2-1B     | 4.37  | 0.23       | 0.00  | 2.56  | 2.26     | 1.88    |

| Meta-Llama-3.2-3B     | 14.73 | 1.28       | 4.03  | 3.39  | 16.57    | 8.00    |

| Meta-Llama-3.1-8B     | 25.29 | 4.61       | 6.15  | 8.98  | 24.95    | 14.00   |

![image.png](attachments/Posts/Llama%203%202%20release/image.png)

20h30 ou 19h30! voir leur heure de post !

![image.png](attachments/Posts/Llama%203%202%20release/image%201.png)

### Open letter:

In the absence of consistent rules, the EU is going to miss out on two cornerstones of AI innovation. The first are developments in ‘open’ models that are made available without charge for everyone to use, modify and build on, multiplying the benefits and spreading social and economic opportunity. Open models strengthen sovereignty and control by allowing organisations to download and fine-tune the models wherever they want, removing the need to send their data elsewhere. The second are the latest ‘multimodal’ models, which operate fluidly across text, images and speech and will enable the next leap forward in AI. The difference between text-only models and multimodal is like the difference between having only one sense and having all five of them.

But in recent times, regulatory decision making has become fragmented and unpredictable, while interventions by the European Data Protection Authorities have created huge uncertainty about what kinds of data can be used to train AI models.