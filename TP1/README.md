# La méthode de Dichotomie

Cette méthode repose sur les hypothèses suivantes :

   - Il existe une solution sur un intervalle [a,b]
   - La fonction <img src="https://render.githubusercontent.com/render/math?math=f(x)"> est monotone (croissante ou décroissante) sur l'intervalle [a,b]
 Sous ces deux hypothèses, l'inégalité suivante est vérifiée :
<img src="https://render.githubusercontent.com/render/math?math=f(a)*f(b)<0">
 ## Principe de la méthode de Dichotomie
 La figure ci-dessous illustré le principe de la méthode de Dichotomie :
 
<p align="center">
  <img src="https://github.com/JihedMasri/TP_Analyse_Numerique/blob/main/TP1/dicho.JPG?raw=true" alt="dicho"/>
</p>

On calcule c par l’expression :
<img src="https://render.githubusercontent.com/render/math?math=c=\frac{a+b}{2}">

 - Si <img src="https://render.githubusercontent.com/render/math?math=f(c)=0"> la solution est égale à c, alors arrêter la recherche.
 - mettre à jours l'intervalle [a, b] telle que :
 - [ ] Si <img src="https://render.githubusercontent.com/render/math?math=f(a)*f(c)<0">, la solution se trouve dans l'intervalle [a,c] alors on prend b=c
 - [ ] Si <img src="https://render.githubusercontent.com/render/math?math=f(a)*f(s)<0">, la solution se trouve dans l'intervalle [c,b] alors on prend a=c
 - On recommence le calcul de c itérativement jusqu'à ce que : <img src="https://render.githubusercontent.com/render/math?math=|b-a|<\epsilon">
 ## La condition d’arrêt
 Le nombre d'itération dépend de la précision voulue ainsi que l'intervalle initial [a,b] soit :
 <img src="https://render.githubusercontent.com/render/math?math=N\geqslant\frac{log{(b-a)}-log{(2\epsilon)}}{log{(2)}}">
 


# La méthode de point fixe

Il faut réécrire l’équation <img src="https://render.githubusercontent.com/render/math?math=f(x)=0"> sous la forme <img src="https://render.githubusercontent.com/render/math?math=x=g(x)"> avec la condition de convergence <img src="https://render.githubusercontent.com/render/math?math=|g(x)|<1">

 ## Principe de la méthode de point fixe
La figure ci-dessous illustré le principe de la méthode de point fixe :

<p align="center">
  <img src="https://github.com/JihedMasri/TP_Analyse_Numerique/blob/main/TP1/ptfixe.JPG?raw=true" alt="ptfixe"/>
</p> 

 - Le principe de la méthode du point fixe correspond à la recherche du point d'intersection entre les deux fonctions :
       
 - [ ] la première fonction est la droite y = x
 - [ ] la deuxième fonction est y = <img src="https://render.githubusercontent.com/render/math?math=g(x)">
 - On choisit initialement un point <img src="https://render.githubusercontent.com/render/math?math=x_0">, qui sera la première estimée de la solution
 - on calcul <img src="https://render.githubusercontent.com/render/math?math=x_0">, cette dernière valeur sera considérée comme étant la deuxième estimée de la solution soit <img src="https://render.githubusercontent.com/render/math?math=x_1=g(x_0)"> a son tour, cette dernière valeur sera injectée dans la fonction <img src="https://render.githubusercontent.com/render/math?math=g(x)"> et ainsi de suite jusqu'à la satisfaction d'un critère d'arrêt.
 
 ## La condition d’arrêt
Le critère d'arrêt soit <img src="https://render.githubusercontent.com/render/math?math=|x_1-x_0 |<\epsilon">
 
# Principe de la méthode de Newton

Le principe de cette méthode est illustré sur la figure ce dessous où : On choisit une première estimée <img src="https://render.githubusercontent.com/render/math?math=x_0">, la second estimée est <img src="https://render.githubusercontent.com/render/math?math=x_1"> déterminée par l'intersection de la ligne tangente de la fonction <img src="https://render.githubusercontent.com/render/math?math=f(x)">  au point <img src="https://render.githubusercontent.com/render/math?math=(x_1,f(x_1))"> et la droite y = 0. La troisième estimée est déterminée par l'intersection de la ligne tangente de la fonction <img src="https://render.githubusercontent.com/render/math?math=f(x)"> au point <img src="https://render.githubusercontent.com/render/math?math=(x_2;f(x_2))"> et la droite y = 0, et ainsi de suite.

<p align="center">
  <img src="https://github.com/JihedMasri/TP_Analyse_Numerique/blob/main/TP1/newton.JPG?raw=true" alt="newton"/>
</p>
 - [ ] L’algorithme de Newton-Raphson est :<img src="https://render.githubusercontent.com/render/math?math=x_{i%2B1}=x_i - \frac{f(x_i)}{f'(x_i)}"> 

 
 ## La condition d’arrêt
 Le critère d'arrêt soit <img src="https://render.githubusercontent.com/render/math?math=|x_{i%2B1}-x_i|<\epsilon">
