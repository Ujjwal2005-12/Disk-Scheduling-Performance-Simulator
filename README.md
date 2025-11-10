Disk Scheduling Performance Simulator

A comprehensive C-based simulator to analyze and compare the performance of major Disk Scheduling Algorithms with realistic workload patterns.

📘 Overview

The Disk Scheduling Performance Simulator is designed to evaluate and visualize how different disk scheduling algorithms perform under various I/O workloads.
It calculates and compares total head movement, average seek time, and determines the best-performing algorithm for the given input or workload.

⚙️ Algorithms Implemented
Algorithm	Description
FCFS (First Come First Serve)	Processes requests in the order they arrive. Simple but may cause high seek times.
SSTF (Shortest Seek Time First)	Chooses the request closest to the current head position. Reduces total seek time but can cause starvation.
SCAN (Elevator Algorithm)	Moves the head in one direction until the end, then reverses. Provides better performance balance.
C-SCAN (Circular SCAN)	Moves the head in one direction and jumps to the beginning after reaching the end. Uniform wait time.
LOOK	Similar to SCAN, but the head only goes as far as the last request in each direction.
C-LOOK	Circular version of LOOK — wraps around to the lowest request instead of disk start.
🧩 Features

✅ Supports custom input sequences
✅ Provides real-world workload simulations (sequential, random, mixed)
✅ Displays tabular performance summary
✅ Highlights best-performing algorithm automatically
✅ Modular and extensible code
✅ Uses clean menu-driven CLI

🧮 Performance Metrics

Each algorithm is evaluated based on:

Total Head Movement → Total distance the disk arm travels.

Average Seek Time → Total head movement divided by number of requests.

Example Output:

==================== PERFORMANCE SUMMARY ====================
| Algorithm | Total Movement | Avg Seek Time |
|------------|----------------|---------------|
| FCFS       |            590 |         59.00 |
| SSTF       |            321 |         32.10 |
| SCAN       |            350 |         35.00 |
| C-SCAN     |            370 |         37.00 |
| LOOK       |            330 |         33.00 |
| C-LOOK     |            315 |         31.50 |
=============================================================
🏆 Best Performing Algorithm: C-LOOK (Min Total Movement = 315)

🧠 Workload Simulation Patterns
Pattern	Description	Use Case
Sequential	Requests in increasing order	Video playback, media streaming
Random	Randomly distributed requests	Web servers, user-driven I/O
Mixed	Combination of sequential and random	Database and file systems
🖥️ How to Run
🔧 Compilation
gcc disk_simulator.c -o disk_simulator

▶️ Execution
./disk_simulator

🧭 Menu Options
==== DISK SCHEDULING PERFORMANCE SIMULATOR ====
1. Custom Sequence
2. Simulate Workload
0. Exit
Choice:

🧑‍💻 Example Run

Input:

1
Enter number of requests: 8
Enter request sequence: 176 79 34 60 92 11 41 114
Enter disk size: 200
Enter initial head: 50


Output:

🏆 Best Performing Algorithm: SSTF (Min Total Movement = 321)

📂 Project Structure
📦 Disk-Scheduling-Simulator
 ┣ 📜 disk_simulator.c        # Main source code
 ┣ 📜 README.md               # Project documentation
 ┗ 📜 sample_output.txt       # Example simulation results (optional)
