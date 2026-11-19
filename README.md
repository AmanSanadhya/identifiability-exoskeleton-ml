# wearable_diag

Structural / sensitivity check: can sensor, interface (strap) and actuator changes in a 1-DoF wearable elbow joint be told apart when the wearer's impedance and load are unknown? Simulation only, placeholder parameters.

Start with `CLAUDE.md` (full context), then `PROMPT.md` (paste into Claude Code in VS Code).

## Setup (VS Code)

1. Unzip, then **File > Open Folder** on `wearable_diag`.
2. Terminal: `python -m venv .venv`, activate it (`source .venv/bin/activate`, Windows `.venv\Scripts\activate`), then `pip install -e ".[dev]"`.
3. In VS Code choose the `.venv` interpreter (Ctrl/Cmd+Shift+P, "Python: Select Interpreter").
4. `pytest -q` (15 tests), then `python scripts/run_structural_check.py` (about 6 s). Open `results/REPORT.md`, `results/isolability.png`, `results/hci.png`.

## What the output means

- **detect**: sigma of a typical change in the outputs.
- **isolable**: the part of that no combination of other changes can imitate.
- **sin**: isolable / detect; small means nearly collinear (confusable).
- **HCI**: human confounding index; near 0 means a human change can imitate it.
- **Robustness table**: verdict with each sensor removed. A flip means the conclusion depends on that sensor.

Local and linearized; absolute sigma is optimistic. Read `docs/MODEL.md` (known weaknesses) and `docs/FIRST_RUN_NOTES.md` before trusting anything.

## Not done yet

Parameter-perturbation sweep, combined faults, nonlinear fit study on real pairs, classical FDI baseline, robust-controller baseline, hardware. See `CLAUDE.md`, "Good next tasks".
