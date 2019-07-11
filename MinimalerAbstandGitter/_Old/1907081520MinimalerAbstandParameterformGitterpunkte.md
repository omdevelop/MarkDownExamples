# Minimaler Abstand einer Parameterform zu diskreten Gitterpunkten

Gegeben sei die Parameterform $$ \boxed{ P(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} }$$ mit $$ t\in \R $$ und $$ t $$ normiert auf das Intervall $$ t \in (0, \varepsilon, 1] $$ und den beiden reellwertigen Funktionen $$ \boxed{ x(t) = f_x(t) } $$ und $$ \boxed{ y(t) = f_y(t) } $$ .

Weiterhin bilden sich die diskreten Gitterpunkte $$ \boxed{ G_{ij} = \begin{pmatrix} u_i , v_i \end{pmatrix} } $$ definiert durch die 

Ortsauflösungen $$ 0 < dX \in \R <= 1 $$ und  $$ 0 < dY \in \R <= 1 $$ 

mit $$ i \in [0, 1, N_i] \in \N $$ und $$ j \in [0, 1, N_j] \in \N $$  mit $$ u_i = i \cdot dX $$ und $$ v_i = i \cdot dY $$ .

<img src=".\image\PunkteParameterkurve.png" alt="drawing" width="50%"/>


Gesucht ist das zu einem Gitterpunkt $$ G_{ij} $$ zugehörige $$ t_{min} $$ mit der minimalen Distanz $$ D $$ entsprechend:

$$ D = \sqrt { (x(t) -u_i)^2 + (y(t) - v_i)^2 } =: \sqrt{S} $$  und damit

$$ \boxed{ S = (x(t) -u_i)^2 + (y(t) - v_i)^2) }$$

Die notwendigen Bedingungen für ein minimales Abstands-$$ S_{min} $$ folgen:

$$ \frac{\partial S}{\partial t} = 0 = \frac{\partial}{\partial t} [ (x(t) -u_i)^2 + (y(t) - v_i)^2 ] $$

$$ 0 = \frac{\partial}{\partial t} (x(t) -u_i)^2 + \frac{\partial}{\partial t}(y(t) - v_i)^2 ] $$

$$ 0 =2 (x(t) -u_i) \frac{\partial x(t)}{\partial t} + 2 (y(t) -v_i) \frac{\partial y(t)}{\partial t}  $$

$$ \boxed{ 0 =(x(t) -u_i) \frac{\partial x(t)}{\partial t} + (y(t) -v_i) \frac{\partial y(t)}{\partial t} } $$

<img src=".\image\PunkteOptimalerWeg.png" alt="drawing" width="50%"/>







































