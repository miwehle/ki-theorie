

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