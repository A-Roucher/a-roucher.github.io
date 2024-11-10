
🧠 CLEAR: first multimodal benchmark to make models forget what we want them to forget

With privacy concerns rising, we sometimes need our models to "forget" specific information - like a person's data - while keeping everything else intact. Researchers just released CLEAR, the first benchmark to test how well this works with both text and images.

❌ Bad news: Current methods either fail to truly forget or end up forgetting way too much. It's like trying to remove a single ingredient from a baked cake!

✨ But there's hope: Adding simple mathematical constraints (L1 regularization) during the forgetting process significantly improves results.

🎯 Key insights:

✅ The benchmark tests forgetting on 200 fictional personas

‣ 3,770 visual Q&A pairs

‣ 4,000 textual Q&A pairs

‣ Additional real-world tests

🛑 Most current forgetting methods don't work well with both text and images

‣ They either remember what they should forget

‣ Or they forget too much unrelated information

✨ Simple mathematical constraints work surprisingly well

‣ L1 regularization prevents excessive forgetting

‣ Works especially well with the LLMU method

👉 Read the full paper here: [https://huggingface.co/papers/2410.18057](https://huggingface.co/papers/2410.18057)

![image.png](attachments/Posts/CLEAR/image.png)