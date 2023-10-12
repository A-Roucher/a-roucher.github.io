---
title: Divide your ChatGPT costs by 10 by directly calling the API
toc: true
categories:
  - study
tags:
  - deep_learning
  - tensorflow
---

# Pourquoi une UI pour l'API GPT ?

❌ Il y a quelques mois, j'ai résilié mon abonnement à ChatGPT.

Cet outil est incroyable, surtout GPT4: quand je l'utilise pour du débuggage par exemple, je peux gagner plusieurs heures par jour. Mais 20$ par mois d'abonnement, c'est trop cher si je ne l'utilise pas régulièrement.

Mais cet été, tout a changé: GPT4 est devenu disponible par l'API d'OpenAI.

L'API, c'est une interface qui permet d'appeler des réponses des modèles OpenAI dans des programmes.
La vraie différence, c'est qu'on paye selon le nombre de mots renvoyés par GPT4 ▶ Donc le payement est adapté à l'usage.

🛠 J'ai donc juste construit une interface qui permet d'utiliser l'API OpenAI dans un notebook.

### Résultat : énorme réduction des frais

✅ Pour exactement les mêmes réponses qu'auparavant, mes frais sont tombés à moins d'1$ par jour où je l'utilise beaucoup, 0$ les autres jours.

<img src="/assets/images/2023-09-23-an-ui-for-gpt-api/usage.png">

Voilà quoi ça ressemble:

<img src="/assets/images/2023-09-23-an-ui-for-gpt-api/ui.png">

# Comment c'est construit

- L'interface est faite de simple widgets IPython.

Le coeur de la machine est cette fonction `get_user_input` de la classe `Chat`. Elle met à jour entre autres l'attribute `history`, qui est une liste des messages, chaque message étant un dictionnaire avec les clés `"role"` et `"content"`, ce qui est un format directement accepté par `openai.ChatCompletion.create()`.

```python
def get_user_input(self, b) -> None:
    message = self.user_input.value
    self.add_message("👨‍🚀 You:", message)

    self.history.append({"role": "user", "content": message})
    response = openai.ChatCompletion.create(
        model=self.model, messages=self.history, temperature=0, stream=True
    )
    collected_messages = []
    current_reply = None
    for chunk in response:
        chunk_message = chunk["choices"][0].get("delta", {}).get("content")
        if chunk_message is not None:
            collected_messages.append(chunk_message)
            current_reply = "".join(collected_messages)
            self.answer.value = sanitize_code(markdown(current_reply))
    self.answer.value = ""
    self.add_message("🤖 Bot:", current_reply)
    self.history.append({"role": "system", "content": current_reply})
    return
```

- L'option `stream=True` dans `openai.Chatcompletion` permet de recevoir en live la complétion de GPT, donc de dialoguer bien plus facilement.

# Pour l'utiliser

Clonez [ce repo](https://github.com/A-Roucher/gpt_api_ui), copiez votre [clé API OpenAI](https://platform.openai.com/account/api-keys), lancez la cellule du notebook et c'est parti !