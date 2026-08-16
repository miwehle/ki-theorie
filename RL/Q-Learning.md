# Q-Learning

**Umgebung** definiert durch Funktion:

$(s, a) \mapsto (s', r)$

Dabei:
	s, s': state; a: action; r: reward.
## Q-Funktion

$Q$ = Qualität bei Berücksichtigung der Zukunft

$Q(s, a)$ = wie gut im Zustand s die Aktion a ist

**TD-Target**
$y = r + \gamma \max_{a'} Q(s', a')$

*Greedy-Algorithmus*
In jedem Zustand s:
- Wähle $argmax_a Q(s, a)$
- $Q(s, a)$ += lr $\cdot$ td_error
- s = s' 

**TD-Error**
 td_error = $y - Q(s, a)$


**Q-LEARNING(Q, α, γ, ε)**
```
1  for each episode
2     initialize state s  
3     while s is not terminal  
4        if RANDOM(0, 1) < ε  
5           a ← RANDOM-ACTION(s)  
6        else a ← arg max_b Q[s, b]  
7        take action a  
8        observe reward r and next state s'  
9        δ ← r + γ max_b Q[s', b] − Q[s, a]  
10      Q[s, a] ← Q[s, a] + αδ  
11      s ← s'
```

## Beispiel

Die Matrix stellt eine Umgebung dar mit Reward in jeder Zelle:

$$
R =
\begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 5 & 0 & 0 \\
0 & 0 & -20 & 0 \\
0 & 50 & 0 & 0
\end{pmatrix}
$$

Mögliche Aktionen: hoch, runter, links, rechts.

### Lauf

Start in Zelle (0,1), also über der 5, und lr = 0.5:
$$
Q_D^{(0)} =
\begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$

$$
Q_D^{(1)} =
\begin{pmatrix}
0 & 2.5 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$

$$
Q_D^{(2)} =
\begin{pmatrix}
0 & 2.5 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$

$$
Q_D^{(3)} =
\begin{pmatrix}
0 & 2.5 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 25 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$
## Exploration


[^1]: "Learning a guess from a guess"
