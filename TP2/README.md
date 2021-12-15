# TP2 
## Interpolation polynomiale

[//]: # (how to add latex in markdown https://gist.github.com/a-rodin/fef3f543412d6e1ec5b6cf55bf197d7b)

**Polynome d'interpolation de Lagrange** 
> Soient <img src="https://render.githubusercontent.com/render/math?math=(x_0,y_0), \ldots,(x_k,y_k),\ldots ,(x_n,k_n)">  ,  n+1 points deux à deux distincts, le polynôme d'interpolation de Lagrange associés à ces points supports est défini par :
<img src="https://render.githubusercontent.com/render/math?math=\displaystyle P_n(x)=\sum_{k=0}^{n%2B1} y_kL_k(x)">

avec


<img src="https://render.githubusercontent.com/render/math?math=L_{0}(x)=\displaystyle\frac{(x-x_1)(x-x_2)\ldots(x-x_{n})}{(x_0-x_1)(x_0-x_2)\ldots(x_0-x_{n})}">

et 


<img src="https://render.githubusercontent.com/render/math?math=L_{k}(x)=\displaystyle\frac{(x-x_1)(x-x_2)\ldots(x-x_{k-1})(x-x_{k%2B1})\ldots(x-x_{n})}{(x_k-x_0)(x_k-x_1)\ldots(x_k-x_{k-1})(x_k-x_{k %2B 1})\ldots(x_k-x_{n})}">


 pour 
 
 <img src="https://render.githubusercontent.com/render/math?math=k\in \{1,\ldots,n\}">

#  LE PHÉNOMÈNE DE RUNGE


en Analyse numérique la  **Le phénomène de Runge**  il est un problème avec tous les interpolation polynomiale de noeuds espacés régulièrement polynômes degré de haut. Elle consiste à augmenter l'amplitude d'erreur dans le voisinage des limites.

Il a été découvert par Carl Runge alors qu'il est en train d'étudier le comportement d'erreur interpolation polynomiale  pour approximatif plusieurs fonctions.

<p align="center">
  <img src="https://github.com/JihedMasri/TP_Analyse_Numerique/blob/main/TP2/runge.png?raw=true" alt="runge"/>
</p>

 - La courbe rouge est la fonction Runge, la courbe bleue est un polynôme du cinquième degré, et la courbe verte est un neuvième polynôme d'ordre. Le rapprochement, au voisinage de la limite, se détériore avec l'augmentation de qualité.

## PROBLÈME
Runge a constaté que cette interpoler fonction dans un ensemble de points  à égale distance gamme  , avec polynôme  qualité  , l'interpolation résultant oscille dans amplitude vers les extrémités de la plage (dans ce cas  et  ).
Vous pouvez également prouver que l'erreur tend vers l'infini
## SOLUTION
Le Runge montre que contre-il ne convient pas d'utiliser polynômes de degré élevé de noeuds équidistants pour interpoler une fonction. Cependant, il est possible d'obtenir un schéma d'interpolation dont l'erreur diminue à mesure que le nombre de noeuds à l'aide de la nœuds de Chebyshev alternativement à des points équidistants
