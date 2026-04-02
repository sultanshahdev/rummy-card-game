# ♠️♦️ Rummy Card Game (C++)

A terminal-based **human vs. computer** Rummy-style card game simulation focused on hand-value strategy, showdowns, and score survival.

[![Top Language](https://img.shields.io/github/languages/top/sultanshahdev/rummy-card-game?style=for-the-badge)](https://github.com/sultanshahdev/rummy-card-game)
[![Repo Size](https://img.shields.io/github/repo-size/sultanshahdev/rummy-card-game?style=for-the-badge)](https://github.com/sultanshahdev/rummy-card-game)
[![Stars](https://img.shields.io/github/stars/sultanshahdev/rummy-card-game?style=for-the-badge)](https://github.com/sultanshahdev/rummy-card-game/stargazers)
[![License](https://img.shields.io/badge/License-Not%20specified-lightgrey?style=for-the-badge)](#-license)

**Quick Links:** [Install](#-getting-started) • [Usage](#️-usage) • [Contributing](#-contributing)

---

## Table of Contents

- [📌 About](#-about)
- [✨ Features](#-features)
- [🧱 Tech Stack](#-tech-stack)
- [📂 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [🛠️ Usage](#️-usage)
- [🧪 Testing](#-testing)
- [⚙️ Configuration](#️-configuration)
- [🗺️ Roadmap](#️-roadmap)
- [🤝 Contributing](#-contributing)
- [🙏 Credits / Attribution](#-credits--attribution)
- [📄 License](#-license)
- [🙌 Support](#-support)

---

## 📌 About

This project implements a simplified Rummy/Score-style card game in C++ where you compete against a computer player in the terminal.

**Who it’s for:**
- C++ beginners learning classes, structs, and game loops
- Students building console game projects
- Anyone who wants a lightweight card-game simulation

**Core use cases:**
- Play short strategy rounds against AI
- Learn turn-based game logic and scoring systems
- Study deck shuffling, card replacement, and showdown mechanics

---

## ✨ Features

- 🃏 52-card deck generation and shuffle
- 👤🤖 Human vs. computer gameplay
- 🎯 Hand-value minimization strategy
- ⚔️ Showdown mechanic with penalty rules
- 📊 Score tracking until target score elimination
- 😏 Computer taunts and turn “thinking” delay
- 🎨 ANSI-colored terminal output and splash screen

---

## 🧱 Tech Stack

- **Language:** C++ (C++11 standard)
- **Runtime:** Native console application
- **Standard library usage:** iostream, string, algorithm, random/cstdlib, thread, chrono
- **Build tool:** `g++` (manual compile command)

---

## 📂 Project Structure

```text
rummy-card-game/
├── README.md
└── RummyRoyale (Project Source File).cpp
```

| Path | Purpose |
|---|---|
| `RummyRoyale (Project Source File).cpp` | Full game implementation (Card, Deck, Player, GameManager, `main`) |
| `README.md` | Project documentation |

---

## 🚀 Getting Started

### Prerequisites

- C++ compiler with C++11 support (e.g., `g++`)
- Terminal/console environment

### Installation

```bash
git clone https://github.com/sultanshahdev/rummy-card-game.git
cd rummy-card-game
```

### Environment setup

No `.env` setup is required.

### Run locally

```bash
g++ -std=c++11 -pthread "RummyRoyale (Project Source File).cpp" -o rummy
./rummy
```

For Windows (MinGW), for example:

```bash
g++ -std=c++11 -pthread "RummyRoyale (Project Source File).cpp" -o rummy.exe
rummy.exe
```

> **Assumption:** The source uses `system("CLS")` to clear the screen (Windows-specific). On non-Windows systems, game logic should still run, but screen clearing may not behave as intended.

---

## 🛠️ Usage

Typical gameplay flow:

1. Start the executable.
2. Enter a **target score** (elimination threshold).
3. On each turn, choose:
   - `1` to replace one of your 4 cards
   - `2` to call a showdown
4. Continue until either you or the computer reaches the target score.

### Game rules (implemented behavior)

- Each player holds 4 cards.
- Replace actions swap one chosen card with a new card from deck.
- Showdown scoring:
  - If player calls showdown with value **>= computer**, player gets **+30 penalty**
  - Otherwise, computer gains points from its hand value
- First to hit/exceed target score loses.

---

## 🧪 Testing

**Not applicable** (no automated test suite or lint configuration detected in repository files).

---

## ⚙️ Configuration

No configuration files or environment variables are currently required.

---

## 🗺️ Roadmap

- [ ] Split game logic into multiple `.h/.cpp` files
- [ ] Add input validation and safer error handling
- [ ] Replace `system("CLS")` with cross-platform screen handling
- [ ] Add deterministic RNG mode for reproducible gameplay
- [ ] Add automated tests for scoring and showdown rules
- [ ] Add CI workflow for build checks

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch  
   `git checkout -b feature/your-change`
3. Commit with clear messages  
   `git commit -m "feat: improve showdown validation"`
4. Push your branch and open a Pull Request

Recommended:
- Keep changes focused and small
- Preserve existing gameplay behavior unless intentionally changed
- Update README when gameplay/build commands change

---

## 🙏 Credits / Attribution

- Project implementation and repository content by the repository author(s)/contributors.
- Game concept based on classic Rummy/Score-style card gameplay mechanics.
- Preserve existing source headers and notices in `RummyRoyale (Project Source File).cpp` when redistributing modified versions.

---

## 📄 License

> **Assumption:** No license file was detected in the current repository tree snapshot.

License is **not specified** in the inspected files.  
Maintainers should add a `LICENSE` file to define usage and distribution terms clearly.

---

## 🙌 Support

- ⭐ Star this repository if you found it useful
- 🍴 Fork it to build your own variant
- 🐛 Report bugs or suggest features via Issues:  
  https://github.com/sultanshahdev/rummy-card-game/issues
