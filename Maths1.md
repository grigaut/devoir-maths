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
 
## Question 8 ##

Soit deux points du plan $P_1=(p_{1x},p_{1y})$ et $P_2=(p_{2x},p_{2y})$, et deux vecteurs directeurs $u_1=\begin{pmatrix}
u_{1x}\\
u_{1y}
\end{pmatrix}$
et $u_2=\begin{pmatrix}
u_{2x}\\
u_{2y}
\end{pmatrix}$.

On cherche a lier les points $P_1$ et $P_2$ par un arc parametré $\gamma$ binomial du type : 

pour $t\in \mathbb{R}$,  $\gamma(t)=\begin{pmatrix}
a+bt+ct^{2}\\
d+et+ft^{2}
\end{pmatrix}$ vérifiant :
 - $\gamma(0)=P_1 \Leftrightarrow \begin{pmatrix}
a\\
d
\end{pmatrix}$ = $\begin{pmatrix}
p_{1x}\\
p_{1y}
\end{pmatrix}$ $\newline$
 $\gamma(1)=P_2 \Leftrightarrow \begin{pmatrix}
a+b+c\\
d+e+f
\end{pmatrix}$ = $\begin{pmatrix}
p_{2x}\\
p_{2y}
\end{pmatrix}$
- $\exist(\lambda,\mu) \in (\mathbb{R^{*}_{+}})^{2}$ tel que: $\newline$ 
  - $\gamma'(0)=\lambda u_1 \Leftrightarrow \begin{pmatrix}
b\\
e
\end{pmatrix}$ = $\begin{pmatrix}
\lambda u_{1x}\\
\lambda u_{1y}
\end{pmatrix}$ 
  - $\gamma'(0)=\lambda u_1 \Leftrightarrow \begin{pmatrix}
b+2c\\
e+2f
\end{pmatrix}$ = $\begin{pmatrix}
\mu u_{2x}\\
\mu u_{2y}
\end{pmatrix}$ 

On a donc 8 équations pour 8 inconnues (en comptant $\lambda$ et $\mu$ qui ne semblent pas forcement arbitraire)
On resoût le systeme et on obtient les resultats suivant :
$\newline$
$a=p_{1x}$
$\newline$
$d=p_{1y}$
$\newline$
$b=\lambda u_{1x}$
$\newline$
$e=\lambda u_{1y}$
$\newline$
$c=p_{2x}-p_{1x}-\lambda u_{1x}$
$\newline$
$f=p_{2y}-p_{1y}-\lambda u_{1y}$
$\newline$
avec $\lambda = 2\frac{det(\vec {P_1P_2}, \vec u_2)}{det(\vec u_2,\vec u_1)}$

De la on peut en deduire plusieurs contraintes :

Comme $\lambda$ ne peut etre nul si on veut respecter les conditins sur les derivées, on a:
- $P_1$ et $P_2$ ne peuvent être confondus.

Pour que $\lambda$ soit bien définit
- $\vec u_1$ et $\vec u_2$ ne peuvent pas être des vecteurs nuls (mais le sujet les definit comme tel)
- il faut que $\vec u_1$ et $\vec u_2$ ne soient pas parrallels . Cela semble logique ''car on travaille avec une parametrisation polynomiale''


