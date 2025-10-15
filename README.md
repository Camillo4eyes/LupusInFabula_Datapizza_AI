# LupusInFabula_Datapizza_AI 
<a target="_blank" href="https://colab.research.google.com/github/Camillo4eyes/LupusInFabula_Datapizza_AI/blob/main/DatapizzaAI_lupus.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

<img width="1024" height="1024" alt="cover_image_generated_with_gemini" src="https://github.com/user-attachments/assets/7cb64af7-8df0-4611-897d-f941b79be613" />


This project simulates a full match of *Lupus in Fabula* (also known as *Werewolf*) using autonomous AI agents that interact through natural language. The game unfolds without human intervention, with a Narrator coordinating the turns and Players freely discussing, accusing, and voting according to predefined rules.

The code in this repository was written using the [Datapizza AI](https://github.com/datapizza-labs/datapizza-ai) framework.

---

## 🎮 Features

- **Autonomous gameplay** — Once started, the match progresses entirely on its own.
- **Free-form dialogue between agents** — Players speak naturally rather than following scripted responses.
- **Narrated game flow** — A dedicated Narrator handles night/day cycles, eliminations, and voting.
- **Configurable roles** — You can change the number of Wolves and Villagers by editing:

```python
NUM_WOLVES = 2
NUM_VILLAGERS = 4
```

---

## 🚀 Try It on Google Colab

👉 **Run the full simulation here:**  
https://colab.research.google.com/drive/1N2Lxl-A85vK-7Rck80vVZSm7LYgLFWu8?usp=sharing

No local setup required — just open and press **▶ Run All**.

---

## 🧠 How It Works (Overview)

- Each Player is an AI agent with a private role: **Wolf** or **Villager**.
- Wolves know each other. Villagers know nothing.
- During the **night**, wolves secretly choose a victim.
- During the **day**, all players debate and accuse freely.
- If **no new accusations occur for two consecutive turns**, an automatic **vote** is triggered.
- The Narrator ensures rule consistency and announces events.

Example of agent setup:

```python
role_msg = f"SETUP: Your secret role is: {role}."
self.adapters[ps.name].append_history(f"SYSTEM: {role_msg}")
```

---

## 📌 Current Rule Configuration

| Setting        | Value |
|----------------|-------|
| Number of Wolves | 2 |
| Number of Villagers | 4 |
| Discussion Style | Free interaction (no structured turns) |
| Voting Trigger | If no accusations for 2 rounds |

---

## 📂 Project Status

This is an experimental prototype designed for **AI social interaction research and playful simulation**. Future additions may include:

- Support for additional roles (Seer, Doctor, etc.)
- GUI interface or web deployment
- Memory persistence across games

---

## 📜 License

MIT License — free to use, modify, and expand.

---

Enjoy watching AI lie, betray, and panic like real humans. 🐺🔥
