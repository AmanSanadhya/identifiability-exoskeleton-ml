# Class Overlap or Model Limit? Statistical Separability, Bayes Error and a Reject Option in a Simulated Elbow Exoskeleton

Educational notebook for PGE 383 (Subsurface Machine Learning), The University of Texas at Austin.

When classes overlap so much in the features that no model can separate them, how can we tell, and what should a workflow do? The testbed is a simulated one-joint wearable elbow exoskeleton with six causes (healthy, sensor offset, sensor drift, loose strap, weaker motor, extra load). All data is synthetic, generated inside the notebook with fixed seeds, with placeholder parameters (no real device or data).

## What is in the notebook
- a compact physics simulator and feature pipeline
- pair-by-pair separability maps at four levels of wearer variation
- learning curves, a second-seed check and an ablation to tell class overlap from small-data and model limits
- a reject option ("not sure") and an interactive simulator

## Run it
    pip install -r requirements.txt
    jupyter notebook IdentifiabilityInML_Aman_Sanadhya.ipynb

Run all cells top to bottom (several minutes). GitHub's preview shows the saved outputs, but the interactive controls need a running Jupyter kernel, so download the notebook to use them.

## Author
Aman Sanadhya, UT Austin. Portfolio: https://amansanadhya.github.io

License: MIT
