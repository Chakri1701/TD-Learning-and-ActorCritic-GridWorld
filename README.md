# TD Learning and Actor-Critic in GridWorld

This repository contains the implementation of various Temporal-Difference (TD) reinforcement learning algorithms in a 4×4 GridWorld environment.  
The project compares **SARSA**, **Q-Learning**, **SARSA(λ)**, and **Actor-Critic** methods.

---

##  Author
**Chakradhar Reddi Vitta**  
Oregon State University  
ID: 934-595-987  
📧 vittac@oregonstate.edu

---

##  Overview
An agent navigates a 4×4 grid to reach the goal `(3, 3)` while avoiding fire and water cells.  
Rewards:
- +100 → Goal  
- −10 → Fire  
- −5 → Water  
- −1 → Normal move

---

##  Algorithms Implemented
| Algorithm | Type | Key Feature |
|------------|------|--------------|
| **SARSA** | On-policy TD | Stable but slow learning |
| **Q-Learning** | Off-policy TD | Fast but may fluctuate |
| **SARSA(λ)** | TD with Eligibility Traces | Fastest convergence |
| **Actor–Critic** | Policy Gradient + Value Function | Uses function approximation and softmax policy |

---

##  Parameters
| Parameter | Value |
|------------|--------|
| α (Learning Rate) | 0.1 |
| γ (Discount Factor) | 0.95 |
| ε (Exploration Rate) | 0.1 |
| λ (Eligibility Decay) | 0.8–0.9 |
| Episodes | 100 |
| Trials | 100 |

---

##  Results Summary
| Algorithm | Learning Speed | Stability | Comment |
|------------|----------------|------------|----------|
| SARSA | Slow | Stable | Smoothest reward curve |
| Q-Learning | Fast | Less stable | Quick convergence |
| SARSA(λ) | Fastest | Stable | Best overall |
| Actor-Critic | Moderate | Sensitive | Competitive but parameter-dependent |

Error bars represent variability across 100 trials — narrower = more stable learning.

---

##  Concepts Demonstrated
- Temporal Difference learning  
- On-policy vs Off-policy training  
- Eligibility traces (λ)  
- Actor–Critic with softmax policy and function approximation  
- Balancing stability vs. learning speed

---

##  Files
| File | Description |
|------|--------------|
| `mp2.py` | Full Python implementation of all algorithms |
| `MP2.ipynb` | Google Colab notebook with visualization |
| `Mini_project2.pdf` | Report and analysis |
| `Mini 2.pdf` | Parameter explanation and comparison notes |

---

##  How to Run
```bash
pip install numpy matplotlib tqdm
python mp2.py
