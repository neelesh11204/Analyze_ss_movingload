# Analyze_ss_movingload
Beam Analysis Under Moving Loads
This Python script calculates shear forces and bending moments in a simply supported beam subjected to two moving point loads. The analysis provides key structural insights including support reactions, maximum bending moment, and shear force values at various critical positions along the beam.

📌 Features
Calculates maximum reactions at supports A and B.

Determines bending moment when the first load (W1) is at the beam's start.

Calculates shear force when the center of the load system is at mid-span.

Identifies maximum shear force and maximum bending moment and their positions on the beam.

Supports custom inputs for beam length, load magnitudes, and distance between loads.

🧮 How It Works
The loads move along the beam in small increments (dx = 0.1 m).

For each position, it computes:

Support reactions using the principles of static equilibrium.

Bending moment at mid-span.

Shear force just right of the mid-span.

Results are displayed in a concise analysis report.

🛠️ Function Definitions
analyze_beam(L, W1, W2, x)
L: Total length of the beam (in meters)

W1, W2: Point loads (in kN)

x: Distance between the two loads (in meters)

frange(start, stop, step)
Floating-point range generator to simulate continuous motion of loads.

🚀 Usage
Run the script and provide the required inputs when prompted:

bash
Copy
Edit
$ python beam_analysis.py
Enter beam length L (m): 10
Enter load W1 (kN): 20
Enter load W2 (kN): 30
Enter distance between W1 and W2 (m): 2
The output will include a beam analysis report with all relevant shear and moment data.

📋 Sample Output
vbnet
Copy
Edit
===== Beam Analysis Report =====
Max Reaction at A: 31.0 kN
Max Reaction at B: 34.0 kN
BM_01 (W1 at L=0): 0.0 kNm
SF_01 (center of load at L/2): 32.5 kN
SF_max: 32.5 kN at 5.0 m from A
BM_max: 68.75 kNm at 5.0 m from A
✅ Dependencies
Python 3.x

No external libraries required

📂 File Structure
bash
Copy
Edit
beam_analysis/
│
├── beam_analysis.py     # Main script
└── README.md            # Documentation
