# Devoir de Mathématiques #


## Question 1 : ##

Soit $c \in \mathbb{R}$
, on note $E  = \{(x,y) \in \mathbb{R^2} \ | \ f(x,y) = c \}$

Comme  {c} est un fermé de $\mathbb{R}$ et par continuité de $f$, $f^{-1}(\{c\})$ est un fermé de $\mathbb{R^2}$.

Montrons maintenant que $E$ est borné : 

Comme, $f(x,y) \underset{||(x,y)|| \to + \infin} \to + \infin$

Ainsi, il existe $b$, $b \in \mathbb{R_+}$, tel que :

$\forall (x,y) \in \mathbb{R^2}, ||(x,y)|| \geqslant b \implies f(x,y) \gt c$.

$\forall (x,y) \in E, ||(x,y)|| \le b$.

Donc $E$ est borné. Ainsi, $E$ est un fermé borné de $\mathbb{R^2}$, donc un compact de $\mathbb{R^2}$.

## Question 2 : ##

-----

## Question 3 : ##
 
On définit $g : \mathbb{R^3} \to \mathbb{R^2}$ par :

$g :(x_1,x_2,t) \mapsto (f(x_1,x_2)-c, \ p(x_1,x_2)-t)$

On veut appliquer le $Théorème\ des\ fonctions\ implicites$ à la fonction $g$ :

- $g$ est continuement differentiable car $f$ l'est par definition et $p$ est un polynome en les coordonnées.
- le determinant de la jacobienne
  
   $\partial_x g(x_1,x_2,t) = \begin{pmatrix} 
  \partial_1f(x_1,x_2)&\partial_2f(x_1,x_2)\\
  \frac{\partial_1f(\vec x_0)}{||\nabla f(\vec x_0)||}&-\frac{\partial_1f(\vec x_0)}{||\nabla f(\vec x_0)||}\\
  \end{pmatrix}$ 


  vaut -||$\nabla f(\vec x_0)|| \ne 0$ en $x_0$, ainsi par continuité du gradient ( $f$ continuement differentiable), il existe un ouvert $U$ de $\mathbb{R^2}$ tq:
  - $(x_0,y_0) \in U$   


  - $\forall \vec x \in U,  \ ||\nabla f(\vec x)|| \ne 0$, donc  $\partial_x g(\vec x,t)$ inversible dans U
- enfin, on choisit un $\delta > 0,$ et on restreint $g$ à
   $W = U\times ]-\delta,\delta[$, on a donc  $(x_0,y_0,0) \in W$ et qui annule $g$


Ainsi par le $théorème \ des \ fontions \  implicites$ :
  - il existe des voisinages $U'$ de $\vec x_0$, $V de \ 0$ (du type $]- \epsilon,\epsilon[$], où $0<\epsilon \le \delta$) tel que $U' \times V \subset W$ et une unique fonction implicite $\gamma : V \longrightarrow \mathbb{R^2}$, continuement différentiable, telle que $\forall (t, \vec x)\in V \times U'$ :
  
  $g(\vec x,t)=0  \Leftrightarrow (f( \vec x) = c \ \ et \ t=p(\vec x))  \Leftrightarrow \gamma(t)=\vec x$ d'où le résultat escompté.

## Question 4 : ##

- La suite du théoreme des fonctions implicites nous donne l'expression de $\gamma'$ :
$\forall t\in ]-\epsilon,\epsilon[$ :
$d\gamma(t) = \gamma'(t) =-(\partial_xg(\gamma(t), t))^{-1}$ . $\partial_tg(\gamma(t), t)$ 
 = $\frac{||\nabla f(\vec xo)||}{A} \begin{pmatrix}
\partial_2 f(\vec x)\\
-\partial_1 f(\vec x)
\end{pmatrix}$
avec $A =\partial_1f(\vec x_0) \partial_1f(\vec x) + \partial_2f(\vec x_0) \partial_1f(\vec x) \ne 0$ d'apres la question precedente.

- De plus, si $\gamma'(t) = 0$, le gradient de $f$ en $\vec x$ est nul. Donc quitte à réduite l'intervalle de definition de $\gamma$, en utilisant le fait que $||\nabla f(\vec x_0)||$ $\ne 0$, àl'aide de la continuité du gradient, on peut trouver un ouvert $]\epsilon',\epsilon'[$ inclus dans $]\epsilon,\epsilon[$ où $\gamma'$ est non nul.
On aurait pu s'y restreindre dès le debut.

- et directement :
$<\gamma'(t),\nabla f(\gamma(t))> \ =B*(\partial_1f(\vec x)\partial_2f(\vec x)-\partial_1f(\vec x)\partial_2f(\vec x))=0$
Donc  $\gamma'(t) \perp \nabla f(\gamma(t))$
