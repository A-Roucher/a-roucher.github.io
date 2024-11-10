---
title: 
toc: true
categories: 
- AI news
tags:
  - Artificial Intelligence
  - LLMs
---


Anthropic just released a chunk improvement technique that vastly improves RAG performance! 🔥

Crash reminder: Retrieval Augmented Generation (RAG) is a widely-used technique for improving your LLM chatbot's answers to user questions.

It goes like this: instead of generating an LLM answer straight away, it just adds a previous step called Retrieval, that retrieves relevant documents from your knowledge base through semantic search, and just appends the top K documents to the prompt. ➡️ As a result, the LLM answer is grounded in context.

⛔️ The difficulty with this retrieval step is that when you split your documents into chunks that will be retrieved, you lose context. So importance chunks could be missed.

💡 Anthropic has just released a blog post that shows that you can use one LLM call to generate a bit of context for each chunk. Then you embed together the original chunk + this bit of added context, so that the embedding is much more representative of the document in its context!

🤔 Isn't that crazy expensive? Well it would have been before, but not so much anymore with their new Prompt caching feature that makes duplicating thousands of requests with the same prompt much less expensive. They give an indicative price tag of only $1.02 per million chunks processed!

✅ And this vastly improves performance on their benchmark!

Read their blog post 👉 [https://www.anthropic.com/news/contextual-retrieval](https://www.anthropic.com/news/contextual-retrieval)

![image.png](attachments/Posts/Anthropic’s%20Contextual%20RAG/image.png)