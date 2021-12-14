# Methode d'intégration numérique

- [ ] [Introduction](#Introduction)
- [ ] [But](#But)
  - [Méthode de Réctangle](#Méthode_de_Réctangle)
  - [Méthode des Trapézes](#Méthode_des_trapèzes)
  - [Méthode de Simpson](#Méthode_de_simpson)
  - [Méthode des Points Milieux](#Méthode_des_points_milieux)
- [ ] [Conclusion](#Conclusion)

## Introduction
L'intégration est l'un des problèmes les plus importants rencontrés en analyse. En fait, on rencontre souvent des intégrations, dont le calcul par des méthodes analytiques est très compliqué voire impossible, car il n'y a pas d'expression analytique de la primitive de la fonction à intégrer. Dans ces cas, des méthodes composées peuvent être appliquées pour évaluer la valeur d'une intégrale donnée. La plupart des méthodes d'intégration numérique fonctionnent sur le même principe.

## But
Le but de ce chapitre est d’aborder le calcul général de l’intégrale d’une fonction <img src="https://render.githubusercontent.com/render/math?math=f(x)"> sur un domaine fini délimité par des bornes finies a et b

<img src="https://render.githubusercontent.com/render/math?math=\int_a^b f(x) \,dx">

## Méthode_de_Réctangle

<img src="https://render.githubusercontent.com/render/math?math=I(f)=\frac{(b-a)}{n} \sum_{k=0}^{n-1} f(a+k\frac{(b-a)}{n})">

Cette méthode, très élémentaire, basée sur les sommes de Cauchy-Riemann (approchant l'aire sous une courbe) et appliquée à une fonction f continue, permet le calcul approché d'intégrales 


<p align="center">
  <img src="https://github.com/JihedMasri/TP_Analyse_Numerique/blob/main/TP3/rectangle.gif?raw=true" alt="rectangle"/>
</p>
## Méthode_des_trapèzes:

<img src="https://render.githubusercontent.com/render/math?math=I(f)=\frac{(b-a)}{n} (\frac{f(a)+f(b)}{2}+\sum_{k=1}^{n-1} f(a+k\frac{(b-a)}{n}) )">
la méthode des trapèzes est une méthode pour le calcul numérique d'une intégrale ,s'appuyant sur l'interpolation linéaire par intervalles le principe est d'assimiler la région sous la courbe représentative d'une fonction f définie sur un segment [a,b] à un trapèze et d'en calculer l'aire  

## Méthode_de_simpson:

<img src="https://render.githubusercontent.com/render/math?math=I(f)=\frac{(\frac{(b-a)}{n})}{6} ({f(a)+f(b)}+2\sum_{k=1}^{n-1} f(a+k\frac{(b-a)}{n})+4\sum_{k=0}^{n-1} f(a+(k+\frac{1}{2})\frac{(b-a)}{n})">
 la méthode de Simpson,<i>du nom de Thomas Simpson, est une technique de calcul numérique d'une intégrale cette méthode utilise l'approximation d'ordre 2 de f par un polynôme quadratique prenant les mêmes valeurs que f aux points d'abscisse a et b 

## Méthode_des_points_milieux:
  
<img src="https://render.githubusercontent.com/render/math?math=I(f)=\frac{(b-a)}{n} \sum_{k=0}^{n-1} f(a+(k+\frac{1}{2})\frac{(b-a)}{n})">

Le principe est d'approcher l'intégrale de la fonction f par l'aire d'un rectangle de base le segment [a,b] et de hauteur  
<img src="https://render.githubusercontent.com/render/math?math=f\left ( \frac{a+b}{2} \right )">
ce qui donne : 

<img src="https://render.githubusercontent.com/render/math?math=R = (b-a)f\left ( \frac{a+b}{2} \right )">
  
Cette aire est aussi celle du trapèze de base [a,b] et dont le côté opposé est tangent au graphe de f en <img src="https://render.githubusercontent.com/render/math?math=C = \frac{a+b}{2}">
ce qui explique sa relative bonne précision
## Conclusion:  
  
Le tableau suivant résume les performances théoriques de chaque méthode :
  
| Nom de la Méthode  | Degré du polynôme  | Nombre de points  |  Degré d’exactitude (ordre)| Degré d’erreur globale |Degré d’erreur finale|
|---|---|---|---|---|---|
| Rectangle |  0 | 1  | 0  | 2  | 1  |
| Point Milieu  |  0 | 1  | 1  | 3  |  2 |
| Trapèze  |  1 |  2 |  1 | 3  | 2  |
| Simpson  |  2 | 3  |  3 | 5  | 4  |
  			
	
