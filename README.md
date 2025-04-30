This repository contains the experiments, logs, and analysis scripts for evaluating three congestion control algorithms using Pantheon and Mahimahi. 

Experiment Summary
**Protocols compared:**

CUBIC
BBR
Copa
Test durations: 60 seconds per run

**Network environments simulated**:

Low-latency / High-bandwidth: 50 Mbps, 10 ms RTT
High-latency / Low-bandwidth: 1 Mbps, 200 ms RTT

**Metrics collected:**

Throughput over time
RTT statistics (average, 95th percentile)
Packet loss rate

**Requirements:**

Linux OS or WSL
Python 3.x
Pantheon (cloned from https://github.com/StanfordSNR/pantheon)
Mahimahi

**Python packages:**
pip3 install matplotlib pandas numpy

**Running the Experiments Run Pantheon using:**

bash Copy Edit bash run_test_scenario.sh my_results_50mbps_10ms bash run_test_scenario.sh my_results_1mbps_200ms and Generate Graphs from Logs From the root of the repo, run:
 python3 analysis_scripts/plot_throughput.py 
 python3 analysis_scripts/plot_rtt.py 
 python3 analysis_scripts/plot_loss.py 
 python3 analysis_scripts/generate_tradeoff_plot.py
 
 This will create .png images in the graphs/ folder
