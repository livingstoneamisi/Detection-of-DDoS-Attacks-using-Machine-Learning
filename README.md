Sure, here's the README.md file with the specified structure maintained:

```markdown
# Detection of DDoS attacks on SDN network using Machine Learning

This repository contains the code and resources for detecting DDoS (Distributed Denial of Service) attacks on Software-Defined Networking (SDN) using Machine Learning techniques. The project involves the setup of a local SDN network, simulation of normal and DDoS traffic, creation of a dataset, development of machine learning models, and deployment for real-time attack detection.

## Project Overview

In this project, we aim to detect DDoS attacks on an SDN network by leveraging machine learning models trained on a locally generated dataset. The key components of the project include:

1. **Network Setup**: A local SDN network is designed and deployed using Mininet to simulate network traffic and attacks.

2. **Traffic Generation**: Normal and DDoS traffic is generated using tools like `iperf` and `hping3` to create a diverse dataset.

3. **Dataset Creation**: The generated traffic is used to create a dataset comprising both normal and attack traffic samples.

4. **Machine Learning Model Development**: Various machine learning models, including K-Nearest Neighbors (K-NN), Support Vector Machines (SVM), Random Forest (RF), and Deep Learning (DL), are developed using RapidMiner for comparative analysis.

5. **Model Selection**: Based on performance metrics, the Random Forest (RF) model is selected as the best-performing model for detecting DDoS attacks.

6. **Instructions**: Detailed instructions are provided for generating normal and DDoS traffic, as well as for deploying and using the trained model for real-time attack detection.

## Repository Structure

- `generate_normal_traffic/`: Contains scripts for generating normal network traffic.
- `generate_ddos_traffic/`: Includes scripts for generating DDoS attack traffic.
- `mininet/`: Contains scripts and configurations for setting up the SDN network using Mininet.
- `model_training/`: Includes code and resources for training machine learning models using RapidMiner.
- `README.md`: This file, providing an overview of the project and instructions for usage.
- `LICENSE`: The license information for the repository.

## Usage

To replicate the experiment and utilize the DDoS detection model, follow these steps:

### Generating Normal traffic:
- Run command `ryu-manager collect_normal_traffic.py` in `generate_normal_traffic` folder.
- Run command `service openvswitch-switch start`.
- Run command `sudo python generate_normal_traffic.py` in `generate_normal_traffic` folder.
- Restart PC.

### Generating DDoS traffic:
- Run command `ryu-manager collect_ddos_traffic.py` in `generate_ddos_traffic` folder.
- Run command `service openvswitch-switch start`.
- Run command `sudo python generate_ddos_traffic.py` in `generate_ddos_traffic` folder.
- Restart PC.

### Detecting Attacks and Normal Traffic:
- Run command `service openvswitch-switch start`.
- Run command `ryu-manager Detection.py` in `mininet` folder.
- Run command `sudo python3 SDN.py` in `mininet` folder.
- After the above command in the same terminal, run command `xterm h1 h6 h13 h17`.

### Normal traffic:
- Ping `10.0.0.15` on node `h17`, then ping `10.0.0.4` on `h6`.
- Go to `h13` and execute various commands (e.g., `cd`, `ls`, `clear`, `git clone`, `wget`, etc.).
- Stop the traffic.

### DDoS traffic:
- Execute DDoS attack commands on the specified nodes using `hping3`.

For detailed instructions, refer to the sections above and the provided scripts.


```

