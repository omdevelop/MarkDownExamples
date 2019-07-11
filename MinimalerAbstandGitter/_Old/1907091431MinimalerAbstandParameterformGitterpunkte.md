# Minimaler Abstand einer Parameterform zu diskreten Gitterpunkten (2D)

## 1. Theorie allgemeine Parameterfunktion

Gegeben sei die Parameterform $$ \boxed{ P(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} }$$ mit $$ t\in \R $$ und $$ t $$ normiert auf das Intervall $$ t \in (0, \varepsilon, 1] $$ und den beiden reellwertigen Funktionen $$ \boxed{ x(t) = f_x(t) } $$ und $$ \boxed{ y(t) = f_y(t) } $$ .

Weiterhin bilden sich die diskreten Gitterpunkte $$ \boxed{ G_{ij} = \begin{pmatrix} u_i , v_i \end{pmatrix} } $$ definiert durch die 

Ortsauflösungen $$ 0 < dX \in \R <= 1 $$ und  $$ 0 < dY \in \R <= 1 $$ 



$$ c^2 = a^2 + b^2 $$



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

Nachbarpunkte (mit Unterschied von $$ dx = \{-1, 0, +1\} $$ und/oder $$ dy = \{-1, 0, +1\} $$) ergeben dann die diskrete Bahnkurve $$ B_k = \{ (u_k, v_k)  \} $$ mit $$ k \in \{ 0, 1, N_B \} $$ mit $$ N_B + 1 $$ Interpolations- bzw. Bearbeitungspunkten.

<img src=".\image\PunkteOptimalerWeg.png" alt="drawing" width="50%"/>



## 2. Theorie Gerade

Wahl der Zwei-Punkte-Form einer Geraden mit den gegebenen Punkten 

$$ P_0 = (x_0, y_0) $$ und $$ P_1 = (x_1, y_1) $$ und mit

$$P(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0) t + x_0 \\ (y_1 - y_0)t + y_0 \end{pmatrix}$$

eingesetzt in

$$ 0 =(x(t) -u_i) \frac{\partial x(t)}{\partial t} + (y(t) -v_i) \frac{\partial y(t)}{\partial t} $$

$$ 0 =( (x_1 - x_0) t + x_0 -u_i) \frac{\partial x(t)}{\partial t} + ( (y_1 - y_0) t + y_0 -v_i) \frac{\partial y(t)}{\partial t} $$

$$ \dfrac{\partial x(t)}{\partial t} = \dfrac{\partial  [(x_1 - x_0) t + x_0]}{\partial t} = (x_1 - x_0)$$

$$ \dfrac{\partial y(t)}{\partial t} = \dfrac{\partial  [(y_1 - y_0) t + y_0]}{\partial t} = (y_1 - y_0)$$

$$ \Rightarrow $$ Bestimmung $$ t_{min} $$:

$$ 0 =( (x_1 - x_0) t_{min} + x_0 -u_i)  (x_1 - x_0) + ( (y_1 - y_0) t_{min} + y_0 -v_i)  (y_1 - y_0) $$

$$ 0 = t_{min}[(x_1 - x_0)(x_1 - x_0) + (y_1 - y_0)(y_1 - y_0)] + (x_0 -u_i)(x_1 - x_0) + (y_0 -v_i)(y_1 - y_0) $$

$$ 0 = t_{min} [(x_1 - x_0)^2 + (y_1 - y_0)^2] + (x_0 -u_i)(x_1 - x_0) + (y_0 -v_i)(y_1 - y_0) $$

$$ t_{min} [(x_1 - x_0)^2 + (y_1 - y_0)^2] = - (x_0 -u_i)(x_1 - x_0) - (y_0 -v_i)(y_1 - y_0) $$

$$ \boxed{ t_{min} = - \dfrac{ (x_0 -u_i)(x_1 - x_0) + (y_0 -v_i)(y_1 - y_0)}{(x_1 - x_0)^2 + (y_1 - y_0)^2}} $$



## 3. Theorie Kreisbogen

Wahl der Zwei-Winkel-Form eines Kreisbogens mit den gegebenen Winkeln 

$$ \alpha_0 \in [0 .. 2 \pi) $$ und $$ \alpha_1 \in (0..2 \pi] $$ und dem Kreismittelpunkt $$ P_m = (x_m, y_m) $$  und mit

$$P(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0) \end{pmatrix}$$ ,

$$ \dfrac{\partial x(t)}{\partial t} = \dfrac{\partial  [x_m + R \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0)]}{\partial t} $$ 

$$ \dfrac{\partial x(t)}{\partial t} = - R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0)$$ 

$$ \dfrac{\partial y(t)}{\partial t} = \dfrac{\partial  [y_m + R \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0)]}{\partial t} $$ 

$$ \dfrac{\partial y(t)}{\partial t} = + R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0)$$ 


eingesetzt in $$ 0 =(x(t_{min}) -u_i) \dfrac{\partial x(t_{min})}{\partial t} + (y(t_{min}) -v_i) \dfrac{\partial y(t_{min})}{\partial t} $$ :

$$ \begin{equation} \begin{split} 0 = [x_m + R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) -u_i] [- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [y_m + R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) - v_i] [+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \end{split} \end{equation} $$

$$ \begin{equation} \begin{split} 0 = [(x_m -u_i) + R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ] [- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [(y_m - v_i) + R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] [+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \end{split} \end{equation} $$

$$ \begin{equation} \begin{split} 0 = + [R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ][- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [x_m -u_i][- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)][+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [y_m - v_i][+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ \end{split} \end{equation} $$$$ \begin{equation} \begin{split} 0 = - [R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ][R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ - [x_m -u_i][R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)][R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [y_m - v_i][R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ \end{split} \end{equation} $$$$ \begin{equation} \begin{split} 0 = - (\alpha_1 - \alpha_0)R^2 cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) \\\ - (x_m -u_i)(\alpha_1 - \alpha_0) R sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)  \\\ + (\alpha_1 - \alpha_0) R^2 sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)  \\\ + (y_m - v_i)(\alpha_1 - \alpha_0) R cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) \\\ \end{split} \end{equation} $$$$ \begin{equation} \begin{split} 0 = - (\alpha_1 - \alpha_0)R^2 - \dfrac{(x_m -u_i)(\alpha_1 - \alpha_0)R}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)}  \\\ + (\alpha_1 - \alpha_0) R^2 + \dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)R} {sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} \end{split} \end{equation} $$ 

$$ \begin{equation} \begin{split} \dfrac{(x_m -u_i)(\alpha_1 - \alpha_0)R}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} = \dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)R} {sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} \end{split} \end{equation} $$

$$ \begin{equation} \begin{split} \dfrac{sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} = \dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)R}{(x_m -u_i)(\alpha_1 - \alpha_0)R}  \end{split} \end{equation} $$

$$ tan((\alpha_1 - \alpha_0)t_{min} + \alpha_0) = \dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)} $$

$$ (\alpha_1 - \alpha_0)t_{min} + \alpha_0 = \arctan (\dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)} $$

$$ \boxed{ t_{min} = \frac{\arctan [\dfrac{ (y_m - v_i)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)}] - \alpha_0}{(\alpha_1 - \alpha_0)}} $$

kann nicht sein, sieht zu einfach aus!

## 4. Theorie Ellipsenbogen



## 5. Theorie Kubischer Spline

































