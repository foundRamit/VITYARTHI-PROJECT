# 🚀 Pathfinding Algorithms in Python

This project implements and compares **classical search & pathfinding algorithms** with support for **dynamic replanning** when obstacles appear in the grid.

✨ Algorithms:
- 🔹 Breadth-First Search (**BFS**)
- ⚡ Uniform Cost Search (**UCS**)
- 🌟 A* Search (**A***)
- 🔺 Hill Climbing

🌀 Features:
- Dynamic obstacle handling (replanning in real time)
- Visualizations & step-by-step logs
- Experiment results with performance metrics

---

## 📂 Project Structure
```
├── 📁 logs/              → Log files & snapshots from dynamic replanning
├── 🗺️ maps/              → Grid maps (small, medium, large, dynamic)
├── 📊 results/           → Experiment results (CSV)
├── ⚙️ src/               → Core source code
│   ├── 🤖 planners/      → Algorithms: BFS, UCS, A*, Hill Climbing
│   ├── 🛠️ utils/         → Visualization & helpers
│   ├── ▶️ main.py        → Run algorithms on chosen map
│   ├── 🔄 dynamic_runner.py → Handles dynamic replanning
│   └── 📜 map_loader.py  → Map loading logic
├── 📈 make_plots.py      → Generate performance plots
├── 🧪 run_experiments.py → Run all algorithms across all maps
└── 📘 README.md          → Project documentation
```

---

## ⚙️ Installation

1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2️⃣ Create a virtual environment (recommended)
```bash
python -m venv venv
# On Linux/Mac
source venv/bin/activate
# On Windows
venv\Scripts\activate
```

3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, install manually:
```bash
pip install numpy matplotlib
```

---

## ▶️ Running the Program

### 🔹 Run a single algorithm on a map
```bash
python src/main.py --map maps/small.txt --algo astar
```

Available options for `--algo`:
```
bfs | ucs | astar | hill
```

### 🔹 Run dynamic replanning
```bash
python src/dynamic_runner.py --map maps/dynamic.txt --algo astar
```
🌀 Simulates obstacles appearing dynamically and replans the path in real time.

### 🔹 Run all experiments
```bash
python run_experiments.py
```
Results are saved in:
```
results/results.csv
```

### 🔹 Generate plots
```bash
python make_plots.py
```
📈 Creates visual comparisons:
- Path length
- Path cost
- Runtime
- Nodes expanded

---

## 📊 Example Output
✔ Logs stored in `logs/`  
✔ Snapshots of grids saved step-by-step  
✔ Final results in `results/results.csv`  

---

## ✅ Requirements
- 🐍 Python 3.10+
- 📦 Libraries: `numpy`, `matplotlib`

---

## 📌 Example Results (from `results.csv`)
| Map         | Algorithm | Path Length | Cost | Nodes Expanded | Time (s) |
|-------------|-----------|-------------|------|----------------|----------|
| small.txt   | BFS       | 18          | 17   | 89             | 0.0      |
| small.txt   | UCS       | 18          | 17   | 279            | 0.0015   |
| small.txt   | A*        | 18          | 17   | 100            | 0.0      |
| small.txt   | Hill      | 18          | 17   | 18             | 0.0      |

---

💡 This project is great for understanding and **comparing search strategies** in AI, and how they behave in both static and dynamic environments.
