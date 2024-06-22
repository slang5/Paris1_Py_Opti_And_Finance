# Optimization of a stopping strategy

## Informations données
Soit le prix d'un actif pour un $S_0$ donné à la période n+1 est 
$$\ S_{n+1} = S_n \exp \left( -\frac{1}{2} \sigma^2 \Delta t + \sigma \sqrt{\Delta t} \epsilon_{n+1} \right) \$$ 

On a aussi la moyenne du cours en 0 et n : $\ A_n = \frac{S_0 + S_1 + \cdots + S_n}{n+1} \$

## Objectifs 
- Ecrire une fonction qui produit une matrice de taille $(nb_{traj}, N+1)$ avec $nb_{traj}$ valeurs de S_n compris entre 0 et N
  - Les paramètres sont : S0, sigma, dt, N, nb_traj, seed
- Une fonction qui prend en input l'output de la fonction précédente et transforme chaque entité selon la formule $A_n$ qui donnera ainsi le cours moyen de chaque trajectoire depuis $n=0$
- Faire une fonction qui approxime la valeur de $E(A_{n}/S_{n})$ à partir des trajectoires simulées par la première fonction, on peut aussi fournir un intervalle de confidence de cette distribution
- Question mathématique : Quelle est la valeur théorique de $E(A_{n}/S_{n})$
- Réaliser un exemple avec $\ S_0 = 10, \sigma = 0.2, \Delta t = \frac{1}{252}, N = 22. \$, il peut être utile de réaliser des graphiques

- On considère $\alpha>=1$ avec $$\tau_\alpha = \min \left( \min \\{ n \in \\{ 0, \ldots, N \\}, A_n \geq \alpha S_n \\}, N \\right)$$
- Réaliser une fonction qui retourne $E(A_{\tau_a}/S_{\tau_\alpha})$ à la période $\tau_\alpha$
- Produire une méthode qui chercher à maximiser $E(A_{\tau_a}/S_{\tau_a})$ selon la valeur de $\alpha$
