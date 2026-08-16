

## Entwicklungslinie

REINFORCE → Policy Gradient mit Baseline → Actor-Critic → TRPO → PPO

## Code

### Ursprung: OpenAI Baselines

- [PPO-Webseite](https://openai.com/index/openai-baselines-ppo)
- [Git-Repo](https://github.com/openai/baselines)
- technische Basis mittlerweile etwas veraltet:
	- Projekt hat seit 7 Jahren keine Aktivität mehr
	- verwendet TensorFlow, nicht PyTorch

Auf meine Frage nach einer PyTorch Impl. von OpenAIs PPO:

> [!NOTE] [ChatGPT](https://chatgpt.com/share/6a688035-680c-83eb-ad75-bece03835ccd)
> Für dich würde ich ==CleanRLs ppo_continuous_action.py== empfehlen. Das passt gut zu deinem selbst implementierten DQN und zu kontinuierlicher Steuerung.

### SB3: PyTorch-Portierung vom DLR

[JMLR-Paper von (11/21) über SB3](https://www.jmlr.org/papers/volume22/20-1364/20-1364.pdf)

[Git-Repo vom DLR-RM](https://github.com/DLR-RM)

[User Guide](https://stable-baselines3.readthedocs.io/en/master/)

Webseiten über SB3 von den Entwicklern:
- [Adam Gleave](https://www.gleave.me/publication/2021-11-stable-baselines3/)
- [Antonin Raffin](https://araffin.github.io/post/sb3/)

### TorchRL

[Docs](https://docs.pytorch.org/rl/stable/index.html)

### CleanRL

[GitHub Repo](https://github.com/vwxyzjn/cleanrl)
Hauptmodul: [ppo_continuous_action](https://github.com/vwxyzjn/cleanrl/blob/master/cleanrl/ppo_continuous_action.py)
[Webseite](https://costa.sh) vom Entwicker

## Theorie

[Arxiv-Paper über PPO](https://arxiv.org/abs/1707.06347)

[Reinforce-Paper](https://link.springer.com/content/pdf/10.1007/BF00992696.pdf)
wichtigster konzeptioneller Vorfahre von PPO

[PyTorch Tutorial](https://docs.pytorch.org/tutorials/intermediate/reinforcement_ppo.html)

[HF Blog](https://huggingface.co/blog/deep-rl-ppo)

[Wiki](https://en.wikipedia.org/wiki/Proximal_policy_optimization)
"Since 2018, PPO was the default RL algorithm at OpenAI."

[OpenAI](https://openai.com/index/openai-baselines-ppo)

[Sutton/Barto](http://incompleteideas.net/book/RLbook2020.pdf), Policy Gradient Methods (pp. 343 ff.)

