# Towards-Model-Free-Conformance-Checking

### Usage of this repository
This repository is supposed to help to reproduce the work in the paper "Towards Model-Free Conformance Checking: Assessing Trace Conformance Based on Few Annotated Variants". With
this work, we aim to move towards model-free conformance checking and enable managers to apply conformance checking even if no process model is available. We evaluated various anomaly detection algorithms and used the heuristic miner algorithm as baselines. Additionally, we proposed a novel approach that uses three conforming input traces for conformance checking.

data
- contains all the event logs, process models and input traces used

notebooks:
- contains all the experimental results for approaches BINet, DAPNN, H+A, OHE, and EMB 


### Process Discovery Baseline (H+A)
An intuitive approach to model-free conformance checking would be first to discover a process model and then perform traditional trace alignments. We use the heuristics miner with default noise parameters to discover a process model from the event log and use the PM4Py trace alignment implementation to perform model-free conformance checking. We visualized the ground truth and the discovered process model for log 12A:

<div style="display: flex; justify-content: center; align-items: flex-start;">
  <div style="text-align: center; margin: 0 20px;">
    <img src="images/12A_discovered_model.png" alt="Discovered Model" style="width: 800px; height: auto;"/>
    <div>Fig. 1: 12A Discovered Model</div>
  </div>
  <div style="text-align: center; margin: 0 20px;">
    <img src="images/12A_ground_truth_model.png" alt="Ground Truth Model" style="width: 800px; height: auto;"/>
    <div>Fig. 2: 12A Ground Truth Model</div>
  </div>
</div>








### References
[1] Lahann, J., Pfeiffer, P., Fettke, P.: Lstm-based anomaly detection of process instances: benchmark and tweaks. In: ICPM. pp. 229–241. Springer (2022)

[2] Nolle, T., Luettgen, S., Seeliger, A., Mühlhäuser, M.: Binet: Multi-perspective business process anomaly classification. Inf Syst 103, 101458 (2019)

### Python packages
python version:	3.9
- pm4py
- scipy
- sklearn
- tensorflow
- numpy
- pandas
