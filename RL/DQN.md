# DQN

Vorgänger: [[Q-Learning]]

## Mentales Modell

2 Netze
	Fluides Wissen
	Konsolidiertes (kristallines) Wissen

dynamisch (hektisch)
konsolidiert (ruhiger)

Replay Memory

## Formale Definition

Hauptkomponenten:
	Q-Net, Target-Net
	Replay Memory

Q-Funktion
	Zustand, Aktion -> Reward, Folgezustand

Gleichungen:
	TD error
	Soft target update


Initial: q_net = target_net


