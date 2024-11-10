---
title: Easier tool building arrives in transformers agent
toc: true
categories: 
* AI news
* 
* 
tags:
  - AI
  - LLM
---


Transformers v4.45.0 released: includes a lightning-fast method to build tools! ⚡️

During user research with colleagues [**Moritz Laurer**](https://www.linkedin.com/feed/#) and [**Joffrey THOMAS**](https://www.linkedin.com/feed/#), we discovered that the class definition currently in used to define a Tool in transformers.agents is a bit tedious to use, because it goes in great detail.

➡️  So I’ve made an easier way to build tools: just make a function with type hints + a docstring, and add a @tool decorator in front.

✅ Voilà, you’re good to go!

Read all about it in the new doc here: [https://huggingface.co/docs/transformers/main/en/agents#create-a-new-tool](https://huggingface.co/docs/transformers/main/en/agents#create-a-new-tool)

And don’t hesitate to give feedback, I’m all ears! 🤗

![image.png](attachments/Posts/Easier%20tool%20building%20arrives%20in%20transformers%20agent/image.png)