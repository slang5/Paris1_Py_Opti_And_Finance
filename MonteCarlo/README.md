## Monte Carlo, Optimisation et Finance
Dans le domaine de la finance, les méthodes de Monte Carlo sont cruciales pour estimer les prix des options et évaluer le risque associé. Nous allons explorer différentes approches pour estimer le prix des options, notamment l'utilisation de variables antithétiques et de variables de contrôle
### Informations connues 
Expression de la valeur intrinsèque d'un call, Prix du sous-jacent à l'échéance selon une distribution normale, Valeur attendue via Monte Carlo, Valeur selon Black & Scholes

### Question (certaines ne sont pas traitées)
- Estimation Monte Carlo de l'option Call ATM
  - Utiliser Monte Carlo pour approximer la valeur d'un call et fournir un intervalle de confiance.
  - Paramètres : Call, ATM, 1an, S0=10, sigma=20%, rf=3%
  - Comparer les résultats avec ceux obtenus via la formule de Black & Scholes, avec 2^15 échantillons.

- Utiliser une variable antithétique
  - Améliorer l'approximation de la valeur d'un call en réduisant la variance des estimations Monte Carlo.
  - Méthodologie : Implanter une variable antithétique pour recalculer le prix du call
  - Test avec le même call sur un échantillon de 2^15 valeurs
  
- Estimer la valeur d'un Put
  - Approximer la valeur d'un Put par Monte Carlo avec et sans variable antithétique
 
- Estimer par Monte Carlo la valeur d'un Call OTM
  - Paramètres : Call, OTM, 1an, S0=10, K=15, sigma=20%, rf=3%
  - Comparer Monte Carlo et Black and Scholes

- Utiliser la méthode "importance sampling" pour recalculer la valeur d'un call OTM (non traité)
  - Paramètres : échantillon de 2^15 prix de sous-jacents à l'échéance dont la croissance moyenne est de 50% par an
