This project implements and compares classical search & pathfinding algorithms:
✨ BFS | ⚡ UCS | 🌟 A* | 🔺 Hill Climbing
It also supports dynamic replanning 🌀 when obstacles appear in the grid!

📂 Project Structure
├── 📁 logs/              → Log files & snapshots from dynamic replanning
├── 🗺️ maps/              → Grid maps (small, medium, large, dynamic)
├── 📊 results/           → Experiment results (CSV)
├── ⚙️ src/               → Core source code
│   ├── 🤖 planners/      → Algorithms: BFS, UCS, A*, Hill Climbing
│   ├── 🛠️ utils/         → Visualization & helper functions
│   ├── ▶️ main.py        → Run algorithms on chosen map
│   ├── 🔄 dynamic_runner.py → Handles dynamic replanning
│   └── 📜 map_loader.py  → Map loading logic
├── 📈 make_plots.py      → Generate performance plots
├── 🧪 run_experiments.py → Run all algorithms across all maps
└── 📘 README.md          → Project documentation

⚙️ Installation
1️⃣ Clone the repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2️⃣ Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate     # On Linux/Mac
venv\Scripts\activate        # On Windows

3️⃣ Install dependencies
pip install -r requirements.txt


If requirements.txt is missing, install manually:

pip install numpy matplotlib

▶️ Running the Program
🔹 Run a single algorithm on a map
python src/main.py --map maps/small.txt --algo astar


Available options for --algo:
bfs | ucs | astar | hill

🔹 Run dynamic replanning
python src/dynamic_runner.py --map maps/dynamic.txt --algo astar


🌀 Simulates obstacles appearing dynamically and replans the path in real time.

🔹 Run all experiments
python run_experiments.py


📊 Results saved in: results/results.csv

🔹 Generate plots
python make_plots.py


📈 Creates visual comparisons (path length, cost, runtime, nodes expanded).

📊 Example Output

✔ Logs stored in logs/
✔ Snapshots of grids saved step-by-step
✔ Final results in results/results.csv

✅ Requirements

🐍 Python 3.10+

📦 Libraries: numpy, matplotlib