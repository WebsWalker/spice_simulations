# SPICE Circuit Simulations :  Portfolio Samples

> Sample deliverables from freelance simulation work.
> For a custom simulation of your circuit, [hire me on Fiverr](#) *(link added at launch)*.

---

## What I Deliver

| Deliverable | Format |
|-------------|--------|
| Annotated schematic | LTspice `.asc` + PNG export |
| Transient waveforms | Startup, ripple, load step |
| Efficiency analysis | Analytical model + Python plots |
| Loop stability | Bode plot with phase margin verdict |
| PDN impedance profile | Bare vs decoupled, anti-resonance analysis |
| Written report | PDF, 5–8 pages |

---

## Sample Projects

### 01 :  LT3800 Synchronous Buck Converter (12V to 3.3V / 2A)

Full switching regulator analysis:

- Real Digikey component selection with datasheet parameter extraction
- LTspice transient simulation: startup, output ripple (4.2mV pk-pk), load step (28mV / 7.55µs recovery)
- Analytical efficiency model with per-contributor loss breakdown (dominant loss: inductor DCR)
- Type II compensation design: Bode plot, Fc=34.1kHz, PM=77.6°
- MLCC DC bias derating analysis: 100µF nominal reduced to 72µF effective at 3.3V

**Tools:** LTspice XVII, Python (numpy, matplotlib), WeasyPrint

### 02 :  NUCLEO-H743ZI2 VDD_MCU PDN Analysis (3.3V @ 480MHz)

Power delivery network review of the STM32H743 3.3V rail on the MB1364 board:

- Target impedance: 165mΩ flat, DC to 500MHz
- Decoupling BOM extracted directly from ST's published MB1364 schematic (traceable)
- Three-tier decoupling strategy analysis: 4.7µF + 1µF + 12×100nF
- Impedance profile before and after decoupling
- Anti-resonance identification at each tier transition
- Verdict: target met with 68% margin across full band
- Production VRM candidate recommendations

**Tools:** Python (numpy, matplotlib), WeasyPrint

---

## Typical Use Cases

- Validating a power supply design before PCB spin
- Debugging instability or unexpected behaviour on a power rail
- PDN review before board bring-up or EMC pre-compliance
- Loop compensation design for switching regulators
- Design review documentation for customer or certification submission

---

## Turnaround and Pricing

| Package | Scope | Typical Delivery |
|---------|-------|-----------------|
| **Basic** | Schematic + key waveforms or impedance plot | 2 days |
| **Standard** | Full analysis + PDF report | 3–4 days |
| **Premium** | Parametric sweep + compensation or PDN optimisation | 5–7 days |

📩 **[View gig and order on Fiverr](#)** *(link added at launch)*

---

## About

Electrical engineer with background spanning ASIC physical design (Cadence), PCB/PDN engineering,
embedded firmware, and metrology software API design. From silicon to API.

---

## Licence

CC BY-NC 4.0 :  see LICENSE
