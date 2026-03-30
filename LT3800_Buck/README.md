# 01 :  LT3800 Synchronous Buck Converter
**12V → 3.3V / 2A @ 200kHz**

---

## Results Summary

| Parameter | Result | Target | Verdict |
|-----------|--------|--------|---------|
| Output ripple | 4.2mV pk-pk | <30mV | ✅ 7× margin |
| Load step dip | 28mV | <30mV | ✅ met |
| Recovery time | 7.55µs | :  | ✅ ~1.5 cycles |
| Full-load efficiency | 95.8% | >90% | ✅ met |
| Crossover frequency | 34.1kHz | Fsw/5–10 | ✅ met |
| Phase margin | 77.6° | >45° | ✅ comfortable |

---

## What This Demonstrates

- Real Digikey component selection with datasheet parameter extraction
- MLCC DC bias derating :  100µF nominal → 72µF effective at 3.3V, component selection adjusted
- LTspice transient simulation with real parasitics (DCR, ESR) modelled explicitly
- LT3800 subcircuit limitations identified, documented and resolved
- Analytical efficiency model with per-contributor loss breakdown
- Type II compensation design from transfer function :  no black-box tools
- Bode plot from small-signal averaged model :  cycle-by-cycle SPICE incompatibility explained

---

## Contents

```
01-buck-converter/
├── schematics/
│   ├── lt3800_buck_main.asc        ← main schematic (transient sims)
│   ├── lt3800_buck_efficiency.asc  ← ideal switch variant (efficiency)
│   └── lt3800_buck_bode.asc        ← loop injection variant (AC analysis)
├── waveforms/
│   ├── startup_ripple.png
│   └── load_step.png
├── analysis/
│   ├── lt3800_buck_analysis.ipynb  ← run this to reproduce all plots
│   ├── efficiency_curve.png
│   └── bode_plot.png
└── report.pdf                      ← full 6-page deliverable
```

## How To Reproduce

```bash
pip install numpy matplotlib jupyter
jupyter notebook analysis/lt3800_buck_analysis.ipynb
```

---

*Sample deliverable :  [hire me on Fiverr](#) for a custom analysis of your design.*
