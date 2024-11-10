---
title: 
toc: true
categories: 
- AI news
tags:
  - Artificial Intelligence
  - LLMs
---


**🌟 Cohere releases Aya 8B & 32B: SOTA multilingual models for 23 languages.**

@Cohere just dropped two great models: great on generalist use, they specifically shine on 23 non-english languages.

How did they pull that multilingual magic?

🔄 Using synthetic data:

- Synthetic data has been said to cause model-collapse after too much training
- Cohere has introduced “data arbitrage” to prevent this by strategically sampling from a pool of several teacher models instead of one single teacher
- First train a model pool for each different groups of languages, and employ an internal Reward Model named “Arbiter” to evaluate and select the optimal generation. Then only the best generation is kept as the final completion for each prompt
- Particularly effective for multilingual setting, where no single teacher model performs in all languages : here “Multilingual Arbitrage” singlehandedly improves win rates of the 8B model vs Gemma-2-9B by 10 points!

🧩 Rather than struggling to find the right mix of data in training a single model for multilingual use, just train language specific models then merge them!

- Maximize diversity between merged checkpoints by training each on different language families.
- Experimented fancy techniques (SLERP, TIES, DARE-TIES) but found out weighted averaging to be the most consistent!
- Merging had 3x more gains at high 35B scale vs the 8B scale - consistent with literature findings that merging is more effective at scale

⚡️ Performance: Automatic evaluations on Arena-Hard-Auto dataset:

- [**Aya Expanse 8B**](https://huggingface.co/CohereForAI/aya-expanse-8b) beats models from its weight class such as Gemma 2 9B, Llama 3.1 8B, and the recent Ministral 8B, with win rates ranging from 60.4% to 70.6%
- [**Aya Expanse 32B**](https://huggingface.co/CohereForAI/aya-expanse-32b) outperforms Gemma 2 27B, Mistral 8x22B, and Llama 3.1 70B, a model more than 2x its size
- But this performance eval comes from only one benchmark! Let’s wait for Open-LLM-Leaderboard

Read more in their in-depth blog post 👉 [https://huggingface.co/blog/aya-expanse](https://huggingface.co/blog/aya-expanse)

LI Format:

🌟🌎 Cohere releases Aya 8B & 32B: SOTA multilingual models for 23 languages !

[**Cohere**](https://www.linkedin.com/feed/#) just dropped two great models: great on generalist use, they specifically shine on 23 non-english languages. How did they pull that multilingual magic?

🔄 𝗧𝗿𝗮𝗶𝗻 𝗼𝗻 𝘀𝘆𝗻𝘁𝗵𝗲𝘁𝗶𝗰 𝗱𝗮𝘁𝗮:

• Synthetic data has been said to cause model-collapse after too much training

• Cohere has introduced "data arbitrage" to prevent this by strategically sampling from a pool of several teacher models instead of one single teacher

• First train a model pool for each different groups of languages, and employ an internal Reward Model named "Arbiter" to evaluate and select the optimal generation. Then only the best generation is kept as the final completion for each prompt

➡️ This process is particularly effective for multilingual setting, where no single teacher model performs in all languages : here "Multilingual Arbitrage" singlehandedly improves win rates of the 8B model vs Gemma-2-9B by 10 points!

🧩 𝗨𝘀𝗲 𝗺𝗼𝗱𝗲𝗹 𝗺𝗲𝗿𝗴𝗶𝗻𝗴: Rather than struggling to find the right mix of data in training a single model for multilingual use, just train language specific models then merge them!

• Maximize diversity between merged checkpoints by training each on different language families.

• Experimented fancy techniques (SLERP, TIES, DARE-TIES) but found out weighted averaging to be the most consistent!

➡️ Merging had 3x more gains at high 35B scale vs the 8B scale - consistent with literature findings that merging is more effective at scale

⚡️ 𝗚𝗿𝗲𝗮𝘁 𝗽𝗲𝗿𝗳𝗼𝗿𝗺𝗮𝗻𝗰𝗲: Automatic evaluations on Arena-Hard-Auto dataset:

➡️ Aya Expanse 8B beats models from its weight class such as Gemma 2 9B, Llama 3.1 8B, and the recent Ministral 8B, with win rates ranging from 60.4% to 70.6%

➡️ Aya Expanse 32B outperforms Gemma 2 27B, Mistral 8x22B, and Llama 3.1 70B (2x its size)

• ⚠️ But this performance eval comes from only one benchmark! Let's wait for Open-LLM-Leaderboard

🔒 Open weights, but CC-by-NC non-commercial license.

Read more in their in-depth blog post 👉 https://huggingface.co/blog/aya-expanse

![aya\_expanse\_image.png](aya_expanse_image.png)