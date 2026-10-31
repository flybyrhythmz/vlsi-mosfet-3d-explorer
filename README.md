# ⚡ VLSI & MOSFET 3D Interactive Lab

An interactive, three-dimensional engineering visualizer and educational platform for semiconductor physics, MOSFET device operation, CMOS digital logic, and industrial chip manufacturing.

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)
![Chart.js](https://img.shields.io/badge/Chart.js-v4.4-orange?logo=chartdotjs)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v3.4-38bdf8?logo=tailwindcss)

---

## 🌟 Live Demo (GitHub Pages)

Deploy instantly with GitHub Pages:
1. Go to **Settings** &rarr; **Pages** in this repository.
2. Under **Build and deployment**, select **Branch: main** and folder **/ (root)**.
3. Click **Save**. Your site will be live at:
   `https://flybyrhythmz.github.io/vlsi-mosfet-3d-explorer/`

---

## 🔬 Key Features

### 1. 3D MOSFET Device & Carrier Flow Simulation
- **Volumetric Silicon Stack**: 3D interactive models of P-substrate, heavily doped $N^+$ Source and Drain diffusion wells, thin High-k gate oxide ($HfO_2$), polysilicon/metal gate, and tungsten contact vias.
- **Dynamic Inversion Channel & Pinch-Off**: Real-time channel tapering and pinch-off zone rendering as Gate-to-Source ($V_{GS}$) and Drain-to-Source ($V_{DS}$) voltages vary.
- **Charge Carrier Drift Dynamics**: 360+ animated electron particles drifting from Source to Drain with field-dependent velocity, plus conventional current ($I_D$) indicators.
- **Physical Overlays**:
  - Depletion region depth variation with Body Bias ($V_{BS}$).
  - Fixed ionized acceptor ions ($N_A^-$) in the space-charge layer.
  - 3D Electric field vectors ($E_y$ gate field, $E_x$ lateral drift field).
- **Interactive Tools**: 3D layer exploding slider, cross-section cutaway view, camera presets (Isometric, Top/Layout, Side Cross-Section), and clickable component inspector.
- **Synchronized SPICE Curves**: Live $I_D$ vs. $V_{DS}$ output characteristic family of curves with active operating point marker and mathematical formula tracking.

### 2. Exact 12-Step Semiconductor Foundry Stepper
Step-by-step 3D wafer cross-section covering the full commercial manufacturing flow:
1. **RCA Chemical Cleaning**: SC-1 & SC-2 wet bench surface conditioning.
2. **Twin-Well Ion Implantation**: P-well and N-well formation with thermal drive-in.
3. **Shallow Trench Isolation (STI)**: Trench etch, liner oxide, TEOS CVD fill, and CMP planarization.
4. **$V_{th}$ Adjustment Implantation**: Channel stop and retrograde well implants.
5. **High-k Gate Dielectric**: Atomic Layer Deposition (ALD) of 1.2nm $HfO_2$.
6. **Metal / Polysilicon Gate Stack**: CVD work-function setting metal deposition.
7. **Photolithography & Gate RIE**: EUV (13.5nm) scanner pattern transfer and plasma etch.
8. **Self-Aligned LDD Implantation**: Low-energy shallow implants to suppress Hot Carrier Injection.
9. **Sidewall Spacer Formation**: Conformal $Si_3N_4$ deposition and directional anisotropic dry etch.
10. **Deep Source/Drain Implants & RTA**: Heavy doping activation via 1050°C millisecond laser spike annealing.
11. **Self-Aligned Silicidation (Salicide)**: Low-resistance Nickel Silicide ($NiSi$) formation.
12. **Multi-Level Copper Dual-Damascene BEOL**: Tungsten plugs, low-k dielectric, and 12–16 copper routing layers.

### 3. Fabrication Technologies & Industry Benchmark Matrix
- **Comparative Analysis**: Bulk Planar CMOS, Fully Depleted SOI (FD-SOI), 3D FinFET (Tri-Gate), Gate-All-Around (GAAFET / Nanosheet), SiGe BiCMOS, and GaN/SiC Power semiconductors.
- **Interactive Industry Selector**: Tailored architectural recommendations for Data Center AI/HPC, Automotive ECUs & ADAS radar, 5G/6G RF Front-Ends, Ultra-Low-Power Edge IoT, Aerospace Rad-Hard systems, and EV Traction Inverters.

### 4. 3D CMOS Inverter & Silicon Layout
- Twin-well layout with NMOS in P-substrate and PMOS in N-well, connected to $V_{DD}$, $GND$, common input gate ($V_{in}$), and output ($V_{out}$).
- Sweep input voltage to observe complementary pull-up/pull-down switching, crowbar short-circuit current ($I_{DD}$), and the Voltage Transfer Characteristic (VTC) curve.

### 5. 3D Energy Band Diagram Visualizer
- Visualizes Conduction ($E_C$), Intrinsic ($E_i$), Valence ($E_V$), and Fermi ($E_F$) energy bands bending in 3D under applied gate bias.
- Real-time transitions: Accumulation &rarr; Flatband &rarr; Depletion &rarr; Strong Inversion.

### 6. Interactive VLSI Knowledge Quiz
- 5-question engineering assessment testing intuition on saturation criteria, CMOS power advantages, body effect, short-channel effects, and self-aligned fabrication.

---

## 🚀 Quick Start (Local Setup)

Simply clone this repository and open `index.html` in any modern web browser:

```bash
git clone https://github.com/flybyrhythmz/vlsi-mosfet-3d-explorer.git
cd vlsi-mosfet-3d-explorer
# Open in browser:
open index.html        # macOS
xdg-open index.html   # Linux
start index.html      # Windows
```

No build step or Node.js environment is required. All 3D and charting dependencies load via standard CDNs.

---

## 🛠️ Technology Stack
- **3D Graphics Engine**: Three.js (WebGL) + OrbitControls
- **2D Data Plotting**: Chart.js v4.4
- **UI Framework & Styling**: Tailwind CSS
- **Physics Solver**: Custom real-time analytical SPICE model (Shockley + body effect + channel length modulation)

---

## 📄 License
This project is open-source under the [MIT License](LICENSE).
