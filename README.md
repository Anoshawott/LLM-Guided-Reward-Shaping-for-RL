# LLM-Guided Reward Shaping for Reinforcement Learning - Domain Expert LLM Shapers in Action

## **Executive Summary**

This study explored whether **Large Language Models (LLMs)** can improve reinforcement learning (RL) through **reward shaping** in a retail inventory management task. The approach combined LLM-generated shaping functions with PPO training across a three-phase pipeline:

1. **Phase 1 – Reward Function Search:** LLMs generated candidate shaping penalties, which were validated and filtered based on execution success and preliminary performance.
2. **Phase 2 – Hyperparameter Optimisation:** Top candidates were tuned with Optuna to identify their best PPO hyperparameters.
3. **Phase 3 – Cross-Evaluation:** Shaped policies were evaluated against baselines (Base PPO, Fixed Action, and Base Stock Policy) over multiple seeds and episodes.

**Key Findings:**

* **Baseline PPO performed strongly**, often matching or outperforming LLM-shaped policies.
* **LLM shaping effects were mostly negligible**, though in isolated cases it led to lower base costs.
* **Methodological choices** (e.g., short training runs, reward-based optimisation in Phase 2) may have limited the ability to detect consistent benefits.

**Conclusion:**
While LLM shaping did not consistently outperform baseline PPO in this structured environment, the **methodology is valuable**. LLMs reliably produced interpretable shaping functions and demonstrated potential as **collaborative reward engineers**. The framework provides a scalable way to inject domain knowledge and creative ideation into RL, especially promising for **complex, less-structured domains** (e.g., robotics, healthcare, resource allocation).
