# Language models to learn to think and play chess
Read the full article here: [From Text to Tactics: Reinforcing Chess Reasoning in a Language Model](https://www.linkedin.com/pulse/text-tactics-reinforcing-chess-reasoning-language-model-reza-bonyadi-s8eqf)

This repository demonstrates how to teach a large language model (LLM) to play chess—and explain its moves—through reinforcement learning. By framing each problem as a textual prompt with an XML‐like structure (<reasoning>...</reasoning><answer>...</answer>), the model gradually learns to produce high‐quality “chain‐of‐thought” explanations alongside legitimate chess moves.

A key component is the custom reward function that scores each output based on (1) correct format, (2) move validity, (3) move legality, and (4) Stockfish’s engine evaluation of the resulting position. This multi-step reward guides the model from simply complying with the XML format to ultimately proposing stronger, more strategic moves.

The training leverages Generative-Rewards Policy Optimization (GRPO), an RL algorithm tailored for large language models. However, the concepts here could be adapted to other techniques (like PPO or DPO). By tying reward signals to both how the model organizes its “thought” text and what move it selects, we effectively teach the LLM to “think out loud” in a way that converges on good chess decisions.

Feel free to explore the code, tweak the hyperparameters, or even integrate a different chess engine for deeper analysis. This setup also provides a starting point for other domains where an LLM must yield structured reasoning plus a final decision, all evaluated in real time.

See details here: XXX
