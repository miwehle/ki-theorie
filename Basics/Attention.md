

## Self-Attention geometrisch

Geometrisch ist Self-Attention eine **kontextabhängige Verschiebung jedes Punkts**:

$$ x_i'=\sum_j \alpha_{ij}v_j $$

Für jeden Punkt $x_i$ gilt:

- Er betrachtet alle Punkte $x_j$.
- Ähnliche oder relevante Punkte erhalten große Gewichte $\alpha_{ij}$.
- Aus deren Value-Vektoren wird ein neuer Punkt als gewichteter Mittelwert gebildet.

Anschaulich: **Jeder Punkt wird in Richtung der für ihn relevanten Punktewolke gezogen.**

Der wichtige Unterschied:

- Lineare Schicht: dieselbe feste Transformation für alle Punkte.
- Attention: für jeden Punkt eine andere Transformation, abhängig von allen anderen Punkten.

Streng genommen geschieht das Ziehen im **Value-Raum**, nicht unbedingt direkt im ursprünglichen $x$-Raum.

Obiges ist die Formulierung von [ChatGPT](https://chatgpt.com/s/t_6a82e19260d08191b386d039289c841c), folgendes ist meine:

> Attention verschiebt die Token-Repräsentation Richtung Schwerpunkt der Token-Werte.

Dabei sind die Token-Werte entsprechend Relevanz gewichtet (basierend auf $QK^\top$). [ChatGPT](https://chatgpt.com/share/6a82dfe8-4194-83eb-8167-a629187fe714):

> Attention bildet aus den Value-Vektoren einen relevanzgewichteten Schwerpunkt.


Als [Formel](https://chatgpt.com/share/6a82dfe8-4194-83eb-8167-a629187fe714):

$$ \operatorname{Attention}(q_i,K,V) = \sum_j \alpha_{ij}v_j $$
mit

$$ \alpha_{ij} = \operatorname{softmax}_j\left(\frac{q_i\cdot k_j}{\sqrt{d_k}}\right) $$
Das mentale Modell ist:
 - $q_i$ sagt, wonach Token $i$ sucht.  
 - $K$ enthält die Suchmerkmale aller Tokens.  
 - $V$ enthält die Informationen aller Tokens, aus denen anschließend gewichtet gemischt wird.