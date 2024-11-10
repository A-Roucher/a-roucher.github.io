---
title: OASIS
toc: true
categories: 
- AI news
tags:
  - Artificial Intelligence
  - LLMs
---

**Oasis: First Real-Time Video Game Without a Game Engine! 🎮**

[**Decart**](https://www.linkedin.com/feed/?trk=guest_homepage-basic_google-one-tap-submit#) & [**Etched**](https://www.linkedin.com/feed/?trk=guest_homepage-basic_google-one-tap-submit#) just released Oasis - a fully AI-generated video game running at 20 FPS (frames per second). The model takes keyboard inputs and generates everything - physics, rules, graphics - on the fly, without any game engine.

⚡️ What makes this special? Current text-to-video models (Mochi-1, Sora, Kling) generate about 1 frame every 10-20 seconds (that's the kind of device I had to play LoL back in the day, thus my low rankings). Oasis is 200 times faster, making it the first playable AI-generated game.

⚙️ Under the hood, it uses a vision transformer to encode space and a diffusion model to generate frames. The secret sauce is "dynamic noising" - a technique that keeps the video stable between frames.

**Key insights:**

⚡️ Generates 20 FPS, vs 0.2 FPS for other DIT-based video models

‣ The specialized hardware Sohu developed by Etched allows to handle 10x more player than H100

🎮 Features real game mechanics

‣ Movement, jumping, item management

‣ Physics and lighting

‣ Procedurally generated worlds

⚠️ Current limitations

‣ Blurry graphics at a distance

‣ Objects sometimes change appearance

‣ Memory issues in long sessions

Try it yourself, the playable demo is impressive! 👉 https://oasis.decart.ai/welcome


**Code:** https://github.com/etched-ai/open-oasis

**Read it in full** 👉 https://oasis-model.github.io/

![[attachments/Posts/OASIS/image.png]]

