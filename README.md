# Hey, I'm Kate 👋

**AI Engineer** • Former Particle Physicist ⚛️ • Former Risk Modeler 📈

I've spent my whole career looking inside systems that would rather stay
opaque — first particle collisions, then risk models, now neural networks.

> The models talk to us all day. **I want to be able to affect them back.**

So I build tools that make neural networks less mysterious — because
interpretability shouldn't stay in research papers, it belongs in
production. (And in zombie games. And in mushroom generators. You'll see.)

The house rules, in every repo: each experiment ships with a **placebo
control**, its **negative results stay published**, and when a finding
turns out to be about my own instrument instead of the model, that page
says so. Half the fun is the honest notes.

### Naming things is 10% of the work and 90% of the joy

[`the-paper-that-remembers-itself`](https://github.com/moudrkat/paper-remembers) ·
[`steeropathy`](https://github.com/moudrkat/steeropathy) ·
[`multi-shroomed-bandit`](https://multi-shroomed-bandit.streamlit.app) ·
[`once-upon-256-dim`](https://once-upon-256-dim.streamlit.app) ·
[`sample-me-softly-with-this-prompt`](https://sample-me-softly-with-this-prompt.streamlit.app) ·
[`the-shroomifier`](https://shroomrier.streamlit.app) ·
[`attack-on-applepear`](https://attack-on-applepear.streamlit.app)

(Every one of those is a real, running project. I trained several of them
on my laptop CPU, because why not.)

## 💥 Come say hi in my collision chamber

My personal site is a chat with a tiny LLM running entirely in your browser, and every answer it generates renders as a real particle collision. Click the event below to fire your own question into the chamber:

[![One question fired into the chamber: the model answers while its layers, attention heads and logit-lens flips render as a real collision.](media/detektor.gif)](https://unt1l1f1nd-detektor.static.hf.space)

## 🚀 How my projects fit together

> One engine for looking inside a model, one factory for the directions it steers with, and the experiments that run on both. **Click any box to open its repo.**

```mermaid
flowchart TD
    hd["🧭 <b>hidden-directions</b><br/>turn a behavior into a vector —<br/>inject it, bake it into the weights,<br/>or catch a bake"]
    bs(["🧠 <b>brainscope</b><br/>watch a model think: an OpenAI-compatible server<br/>with a live view into the residual stream<br/>— logit lens · attention · J-lens · live steering"])
    st["🕹️ <b>steeropathy</b><br/>agents that talk through activations<br/>and J-space, never text — moods, concepts,<br/>a zombie outbreak fought by mind-reading"]
    tm["⚖️ <b>in-two-minds</b><br/>catch an agent hesitating between two tools,<br/>in its activations before it commits"]

    hd -->|"directions &<br/>baked personas"| bs
    bs -->|"hosts the model,<br/>captures activations"| st
    bs -->|"hosts the model,<br/>captures activations"| tm
    st -.->|"steers with"| hd

    click hd "https://github.com/moudrkat/hidden-directions"
    click bs "https://github.com/moudrkat/brainscope"
    click st "https://github.com/moudrkat/steeropathy"
    click tm "https://github.com/moudrkat/in-two-minds"

    classDef engine fill:#1f6feb,stroke:#1158c7,color:#ffffff;
    classDef exp fill:#8957e5,stroke:#6e40c9,color:#ffffff;
    class bs,hd engine;
    class st,tm exp;
```

**The two blue boxes are the instrument.** [brainscope](https://github.com/moudrkat/brainscope) hosts any Hugging Face model and streams its internals to the browser; [hidden-directions](https://github.com/moudrkat/hidden-directions) makes the steering vectors — and bakes them into weights, then audits for the bake. **The two purple boxes are experiments run under that lens.** [steeropathy](https://github.com/moudrkat/steeropathy) wires agents together through activations instead of text; [in-two-minds](https://github.com/moudrkat/in-two-minds) catches an agent hesitating between tools before it commits.

---

### 🔬 Also on the bench

Smaller, self-contained ways to look inside:

- 📜 [paper-remembers](https://github.com/moudrkat/paper-remembers) — Hopfield's 1982 paper, running live: rub out any part of the page and watch it rebuild itself
- 🎬 [green-room](https://github.com/moudrkat/green-room) — a multi-character agent has already cast the scene before it writes a word of dialogue; see it in the activations, then recast it
- 🎭 [sixteen-voices](https://github.com/moudrkat/sixteen-voices) — how a tiny transformer encodes writing style, through LoRA adapters and attention heads
- 👁️ [show-me-your-attention](https://github.com/moudrkat/show-me-your-attention) — attention maps and neuron activations over your own prompt
- 💥 [detektor](https://github.com/moudrkat/detektor) — the collision chamber above, open source (SmolLM2 in your browser, no server)
- 🖼️ [jepa-demo](https://github.com/moudrkat/jepa-demo) — I-JEPA & V-JEPA 2 hands-on, no GPU needed, with a visual deep-dive article
- 🍄 [Mushroom-generator](https://github.com/moudrkat/Mushroom-generator) — a VAE growing mushrooms, with latent-space walks and the decoder taken apart layer by layer
- 🍎 [Applepear](https://github.com/moudrkat/Applepear) — apples vs pears in a tiny CNN, activations and grad-CAM included
- ⚙️ [Minimize_me](https://github.com/moudrkat/Minimize_me) — race TensorFlow optimizers across loss landscapes

### 🃏 And off the bench

- 🎨 [personal-rembrandt](https://github.com/moudrkat/personal-rembrandt) — you can't build a personal brand, so build a personal Rembrandt: paste your bio, GPT-2 reads it in your browser, and its activations repaint his 1659 self-portrait — the brand-safe words sink into shadow. Teaches you very little about the model and a lot about Rembrandt
- 🛏️ [go-to-damn-bed](https://github.com/moudrkat/go-to-damn-bed) — a Claude Code skill that sends you to bed like a mom sends naughty children: it saves your work into TOMORROW.md, then counts to three. It never says what happens at three
- 👑 [KingOfDiamonds](https://github.com/moudrkat/KingOfDiamonds) — the King of Diamonds game from *Alice in Borderland*, played by LLMs in character, recursive strategic thinking and all
- 🗨️ [paralel-discordverse](https://github.com/moudrkat/paralel-discordverse) — your company's Discord gets a parallel universe, populated entirely by fictional colleagues
- 🧮 [least-squares-method](https://github.com/moudrkat/least-squares-method) — code archaeology: a printed Pascal listing, photographed page by page and revived on Turbo Pascal 5.5

---

None of it is perfect. *That's kind of delightful.*
