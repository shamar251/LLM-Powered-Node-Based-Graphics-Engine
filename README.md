# LLM-Powered-Node-Based-Graphics-Engine


This is an experimental graphics engine that allows users to generate and manipulate node-based visual scenes using natural language prompts.

By combining the power of Large Language Models (LLMs) with a visual programming interface, PromptGraph turns English instructions into structured, editable graphs — enabling a new way to build scenes, animations, and logic without writing code.

---

## 🚀 Features

- ✍️ **Natural Language Prompting**  
  Describe what you want using simple English — the engine handles the rest.

- 🧱 **Node-Based Visual Editor**  
  Generated nodes are placed in an interactive canvas. Drag, connect, or modify them in real-time.

- 🔁 **Prompt-to-Graph Parser**  
  A custom parser interprets LLM output into structured commands for the engine.

- 🧠 **LLM Integration**  
  Powered by lightweight open-source models like Mistral, Phi, or Gemma. Local inference or API options supported.

- 🧪 **Fine-Tuning Ready (LoRA/QLoRA)**  
  Improve the model's understanding of your scene domain with low-cost fine-tuning.

---

## 🖼 Example Prompt

```

Place a spinning red cube next to a green sphere. Add a light source above them.

````

### ➡️ LLM Output (JSON)

```json
{
  "nodes": [
    { "id": "1", "type": "cube", "color": "red", "position": [0, 0], "animation": "spin" },
    { "id": "2", "type": "sphere", "color": "green", "position": [1, 0] },
    { "id": "3", "type": "light", "position": [0.5, 1], "intensity": 1 }
  ]
}
````

### ➡️ Visual Result

An automatically generated node scene rendered in the editor.

---

## 🛠️ Tech Stack

| Area             | Tool / Library                                     |
| ---------------- | -------------------------------------------------- |
| UI & Editor      | React, Tailwind, React Flow                        |
| LLM Backend      | Mistral, Phi-2, or Gemma via Ollama / Transformers |
| State Management | Zustand                                            |
| Graphics Engine  | Three.js or Custom ECS (WIP)                       |
| LLM Tuning       | LoRA / QLoRA                                       |

---

## 📦 Installation

```bash
# Clone the repo
git clone https://github.com/yourusername/promptgraph.git
cd promptgraph

# Install dependencies
npm install

# Start the dev server
npm run dev
```

> ⚠️ To use LLM features locally, install [Ollama](https://ollama.com/) or configure a HuggingFace API key.

---

## 📁 Project Structure

```
/src
 ┣ /components      → UI + Node editor
 ┣ /llm             → Prompt handling + model output
 ┣ /parser          → Converts LLM output to graph commands
 ┣ /engine          → Node instantiation + scene updates
 ┣ /data            → Sample prompt-output pairs
```

---

## 🧪 Roadmap

* [x] Prompt input + structured output
* [x] JSON → Node parser
* [x] Node canvas editor (React Flow)
* [ ] Scene rendering in 2D/3D (WebGL or Three.js)
* [ ] Editable node attributes (color, behavior, animation)
* [ ] LoRA fine-tuning support
* [ ] Export/import scenes
* [ ] Voice input & sketch support (Phase 3)

---

## 👩‍💻 Contributing

Pull requests are welcome! Whether it’s improving prompts, adding a new node type, or optimizing the parser — open a discussion or issue and let's build.

---

## 📄 License

MIT © 2025 Shamariah Ogu

---

## 🙌 Acknowledgements

Inspired by the intersection of:

* Natural Language Interfaces
* Node-based Programming
* Creative Coding & Visual Scripting

Special thanks to open-source LLMs like [Mistral](https://mistral.ai/), [Phi](https://www.microsoft.com/en-us/research/project/phi-2/), and the React Flow ecosystem.

---

## 🌐 Demo / Preview

Coming soon... Stay tuned!

Follow progress [on Twitter](https://twitter.com/sha2510).
