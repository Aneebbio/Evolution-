# Evolution-
# 🧬 Project Genesis: The Evolution Exam

## 📖 The High Concept
At first glance, this is a 1st-person 3D survival simulation. You start as a microscopic organism and must eat, survive, and evolve through geological eras. 

**The Twist:** You are not actually an animal. You are a futuristic student taking a high-stakes "Biotic History & Adaptability Exam." The goal isn't just to survive; it's to reach a **Neurological Threshold** (Sentience) through any biological path possible. When you reach maximum intelligence, the 3D world "glitches" out, revealing the simulation and grading your evolutionary creativity.

## 🎮 Core Gameplay Loop
1. **Spawn:** Enter the world in First-Person view.
2. **Survive & Hunt:** Navigate the 3D terrain, avoid predators, and consume resources to earn **Evolution Points (EP)**.
3. **Extinction:** Die from environmental hazards, predators, or era-ending cataclysms (like meteors).
4. **The Gene Lab:** Spend EP on a branching Tech Tree to alter your DNA (speed, size, intelligence, wings, etc.).
5. **Respawn:** Re-enter the simulation as the next generation.



## ⌨️ Controls
* **Movement:** `WASD` or `Arrow Keys`
* **Sprint:** Hold `Shift` (Drains Stamina/Energy)
* **Jump:** `Spacebar`
* **Flight:** Hold `Shift` + press `Spacebar` (Requires unlocking Wings/Flight genes)
* **Interact:** `Left Click` (Bite/Eat/Use Tool depending on intelligence level)

---

## 📂 Project Architecture & Folders

This project is built for the web using **Three.js** and vanilla JavaScript. It is modular, meaning the core engine, the game world, and the "Exam Twist" UI are kept completely separate.

```text
/evolution-exam-game
│
├── index.html           # The main entry point and UI canvas
├── style.css            # HUD styles and "Simulation Glitch" animations
├── README.md            # You are here!
│
├── /assets/             
│   ├── /models/         # 3D assets for creatures and terrain
│   └── /audio/          # Ambient nature sounds and futuristic UI blips
│
└── /src/                # Core Game Logic
    ├── main.js          # The Master Game Loop (requestAnimationFrame)
    │
    ├── /core/           
    │   ├── Engine.js       # Three.js setup (Scene, Camera, Renderer, Lighting)
    │   ├── Input.js        # Keyboard/Mouse listener & Flight State Machine
    │   └── StateManager.js # Controls game states (Playing, Dead, Upgrading, Exam_Passed)
    │
    ├── /entities/       
    │   ├── Player.js       # Player physics, camera height, and stamina logic
    │   ├── DNA.js          # The active genome (stats, unlocked parts, intelligence level)
    │   └── Spawner.js      # Procedurally generates food and AI predators
    │
    ├── /world/          
    │   ├── Biome_Micro.js  # Era 1: The Primordial Soup
    │   ├── Biome_Macro.js  # Era 2: The Open Surface / Dinosaur Era
    │   └── EraManager.js   # Triggers extinction events and swaps biomes
    │
    └── /meta/           
        ├── HUD.js          # First-person overlays (Vitals, Targeting Reticle)
        ├── TechTree.js     # The Gene Lab UI for spending EP
        └── ExamSystem.js   # The secret script monitoring Intelligence to trigger the twist ending
