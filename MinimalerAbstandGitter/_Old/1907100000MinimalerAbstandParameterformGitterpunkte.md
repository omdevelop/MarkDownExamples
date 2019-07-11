# Minimaler Abstand einer Parameterform zu diskreten Gitterpunkten (2D)

## 1. Theorie allgemeine Parameterfunktion

Gegeben sei die Parameterform $$ \boxed{ \vec{P(t)} = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} }$$ mit $$ t\in \R $$ und $$ t $$ normiert auf das Intervall $$ t \in (0, \varepsilon, 1] $$ und den beiden reellwertigen Funktionen $$ \boxed{ x(t) = f_x(t) } $$ und $$ \boxed{ y(t) = f_y(t) } $$ .

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

Nachbarpunkte (mit Unterschied von $$ dx = \{-1, 0, +1\} $$ und/oder $$ dy = \{-1, 0, +1\} $$) ergeben dann die diskrete Bahnkurve $$ B_k = \{ (u_k, v_k)  \} $$ mit $$ k \in \{ 0, 1, N_B \} $$ mit $$ N_B + 1 $$ Interpolations- bzw. Bearbeitungspunkten.

<img src=".\image\PunkteOptimalerWeg.png" alt="drawing" width="50%"/>



## 2. Theorie Gerade

Wahl der Zwei-Punkte-Form einer Geraden mit den gegebenen Punkten 

$$ P_0 = (x_0, y_0) $$ und $$ P_1 = (x_1, y_1) $$ und mit

$ \vec{P(t)} = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0) t + x_0 \\ (y_1 - y_0)t + y_0 \end{pmatrix}$

eingesetzt in

$$ 0 =(x(t) -u_i) \frac{\partial x(t)}{\partial t} + (y(t) -v_j) \frac{\partial y(t)}{\partial t} $$

$$ 0 =( (x_1 - x_0) t + x_0 -u_i) \frac{\partial x(t)}{\partial t} + ( (y_1 - y_0) t + y_0 -v_i) \frac{\partial y(t)}{\partial t} $$

$$ \dfrac{\partial x(t)}{\partial t} = \dfrac{\partial  [(x_1 - x_0) t + x_0]}{\partial t} = (x_1 - x_0)$$

$$ \dfrac{\partial y(t)}{\partial t} = \dfrac{\partial  [(y_1 - y_0) t + y_0]}{\partial t} = (y_1 - y_0)$$

$$ \Rightarrow $$ Bestimmung $$ t_{min} $$:

$$ 0 =( (x_1 - x_0) t_{min} + x_0 -u_i)  (x_1 - x_0) + ( (y_1 - y_0) t_{min} + y_0 -v_j)  (y_1 - y_0) $$

$$ 0 = t_{min}[(x_1 - x_0)(x_1 - x_0) + (y_1 - y_0)(y_1 - y_0)] + (x_0 -u_i)(x_1 - x_0) + (y_0 -v_j)(y_1 - y_0) $$

$$ 0 = t_{min} [(x_1 - x_0)^2 + (y_1 - y_0)^2] + (x_0 -u_i)(x_1 - x_0) + (y_0 -v_j)(y_1 - y_0) $$

$$ t_{min} [(x_1 - x_0)^2 + (y_1 - y_0)^2] = - (x_0 -u_i)(x_1 - x_0) - (y_0 -v_j)(y_1 - y_0) $$

$$ \boxed{ t_{min} = - \dfrac{ (x_0 -u_i)(x_1 - x_0) + (y_0 -v_j)(y_1 - y_0)}{(x_1 - x_0)^2 + (y_1 - y_0)^2}} $$

$$ t_{min} $$ abhängig vom Start/Endpunkt der Gerade $$ P_0 = (x_0, y_0) $$ und $$ P_1 = (x_1, y_1) $$ und dem gewähltem Gitterpunkt $$ G_{ij} = (u_i, v_j) $$.





## 3. Theorie Kreisbogen

Wahl der Zwei-Winkel-Form eines Kreisbogens mit den gegebenen Winkeln 

$$ \alpha_0 \in [0 .. 2 \pi) $$ und $$ \alpha_1 \in (0..2 \pi] $$ und dem Kreismittelpunkt $$ P_m = (x_m, y_m) $$  und mit

$ \vec{P(t)} = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0) \end{pmatrix}$ ,

$$ \dfrac{\partial x(t)}{\partial t} = \dfrac{\partial  [x_m + R \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0)]}{\partial t} $$ 

$$ \dfrac{\partial x(t)}{\partial t} = - R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0)$$ 

$$ \dfrac{\partial y(t)}{\partial t} = \dfrac{\partial  [y_m + R \cdot sin((\alpha_1 - \alpha_0)t + \alpha_0)]}{\partial t} $$ 

$$ \dfrac{\partial y(t)}{\partial t} = + R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t + \alpha_0)$$ 


eingesetzt in $$ 0 =(x(t_{min}) -u_i) \dfrac{\partial x(t_{min})}{\partial t} + (y(t_{min}) -v_j) \dfrac{\partial y(t_{min})}{\partial t} $$ :

$$ \begin{equation} \begin{split} 0 = [x_m + R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) -u_i] [- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [y_m + R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) - v_j] [+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \end{split} \end{equation} $$

$$ \begin{equation} \begin{split} 0 = [(x_m -u_i) + R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ] [- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [(y_m - v_j) + R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] [+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \end{split} \end{equation} $$

$ \begin{equation} \begin{split} 0 = + [R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ][- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ + [x_m -u_i][- R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)][+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [y_m - v_j][+ R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ \end{split} \end{equation} $ $ \begin{equation} \begin{split} 0 = - [R \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) ][R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ - [x_m -u_i][R \cdot (\alpha_1 - \alpha_0) \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [R \cdot sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)][R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)]  \\\ + [y_m - v_j][R \cdot (\alpha_1 - \alpha_0) \cdot cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)] \\\ \end{split} \end{equation} $ $ \begin{equation} \begin{split} 0 = - (\alpha_1 - \alpha_0)R^2 cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) \\\ - (x_m -u_i)(\alpha_1 - \alpha_0) R sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)  \\\ + (\alpha_1 - \alpha_0) R^2 sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0) cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)  \\\ + (y_m - v_j)(\alpha_1 - \alpha_0) R cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0) \\\ \end{split} \end{equation} $$ $ \begin{equation} \begin{split} 0 = - (\alpha_1 - \alpha_0)R^2 - \dfrac{(x_m -u_i)(\alpha_1 - \alpha_0)R}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)}  \\\ + (\alpha_1 - \alpha_0) R^2 + \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0)R} {sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} \end{split} \end{equation} ​ 

$ \begin{equation} \begin{split} \dfrac{(x_m -u_i)(\alpha_1 - \alpha_0)R}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} = \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0)R} {sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} \end{split} \end{equation} $

$ \begin{equation} \begin{split} \dfrac{sin((\alpha_1 - \alpha_0)t_{min} + \alpha_0)}{cos((\alpha_1 - \alpha_0)t_{min} + \alpha_0)} = \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)}  \end{split} \end{equation} $

$ tan((\alpha_1 - \alpha_0)t_{min} + \alpha_0) = \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)} $

 (\alpha_1 - \alpha_0)t_{min} + \alpha_0 = \arctan\left[ \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0) }{(x_m -u_i)(\alpha_1 - \alpha_0)} \right] $

$ \boxed{ t_{min} = \frac{\arctan \left[ \dfrac{ (y_m - v_j)(\alpha_1 - \alpha_0)}{(x_m -u_i)(\alpha_1 - \alpha_0)} \right] - \alpha_0}{(\alpha_1 - \alpha_0)}} $

$ t_{min} $ unabhängig vom Kreisradius $ R $, allein bestimmt vom Start/Endwinkel $ \alpha_0, \alpha_1 $ , Kreismittelpunkt $ P_m = (x_m, y_m) $ des Kreisbogens und dem gewähltem Gitterpunkt $ G_{ij} = (u_i, v_j) $.



## 4. Theorie Ellipsenbogen





## 5. Theorie Kubischer Spline

<u>Gegeben:</u>

Zwei Randpunkte $ P_0 = (x_0, y_0) $ und $ P_1 = (x_1, y_1) $ , alle $ \in \R^2 $, welche untereinander nicht deckungsgleich sind.

Zwei Steigungen an den Randpunkten $ P_0 $ und $ P_1 $ : 

 $ S_0 \big|_{P_0} = \begin{pmatrix} s_{0x} \\ s_{0y} \end{pmatrix} $ und $ S_1 \big|_{P_1} = \begin{pmatrix} s_{1x} \\ s_{1y} \end{pmatrix}$ .

Für Berechnungen der Randsteigungen $S_0$ und $S_1$ vergleiche **Anhang - Berechnung der Randsteigung**!

<u>Gesucht</u>: 

die Polynom-Koeffizienten $ a_x , b_x , c_x , d_x \in \R $ und $ a_y , b_y , c_y , d_y \in \R $ 

mit $ t \in \left[ 0 .. 1\right] \in \R $ in

$ f_x(t) = a_x t^3 + b_x t^2 + c_x t + d_x $

$ f_y(t) = a_y t^3 + b_y t^2 + c_y t + d_y $

derart, dass 

$ S = \min\limits_t = \left[ x(t) -u_i \right]^2 + \left[ y(t) - v_j \right]^2  $ 

(für einen Gitterpunkt $G_{ij} = (x_i, y_j) $ wird :

 $ \Leftrightarrow 0 = \left[ f_x(t_{min}) -u_i \right] \dfrac{\partial f_x(t_{min})}{\partial t} + \left[f_y(t_{min}) -v_j \right] \dfrac{\partial f_y(t_{min})}{\partial t} $ 

Zu bestimmen sind 8 Koeffizienten $ a_x , b_x , c_x , d_x,  a_y , b_y , c_y , d_y $ mit 8 Bestimmungsgleichungen. 

<u>Bestimmung der Spline-Koeffizienten:</u>

$ \dfrac{\partial f_x(t)}{\partial t} = 3a_x t^2 + 2b_x t + c_x $

$ \dfrac{\partial^2 f_x(t)}{\partial t^2} = 6a_x t + 2b_x $

$ \dfrac{\partial f_y(t)}{\partial t} = 3a_y t^2 + 2b_y t + c_y $

$ \dfrac{\partial^2 f_y(t)}{\partial t^2} = 6a_y t + 2b_y $

Der gesuchte Spline $ P(t) $ muss durch die Punkte $ P_0 $ und $ P_1 $ laufen:

$ f_x(0) = x_0 = d_x $   (1)

$ f_y(0) = y_0 = d_y $   (2)

$ f_x(1) = x_2 = a_x + b_x + c_x + d_x $   (3)

$ f_y(1) = y_2 = a_y + b_y + c_y + d_y $   (4)

Der gesuchte Spline $ P(t) $ muss stetig an $ S_0 \big|_{P_0} $ und $ S_2 \big|_{P_2} $ anschliessen:

$ \dfrac{\partial f_x(t)}{\partial t} \big|_{x_0} = c_x = S_{0x} $   (5)

$ \dfrac{\partial f_x(t)}{\partial t} \big|_{x_2} =  3a_x + 2b_x + c_x  = S_{2x} $   (6)

$ \dfrac{\partial f_y(t)}{\partial t} \big|_{y_0} = c_y = S_{0y} $   (7)

$ \dfrac{\partial f_y(t)}{\partial t} \big|_{y_2} =  3a_y + 2b_y + c_y  = S_{2y} $   (8)





































## Anhang

### Berechnung der Randsteigungen

Bei den untersuchten Parameterfunktionen $\vec{P(t)}$ in $\R^2$ geben die, falls vorhanden, Randparameterfunktionen die notwendigen Steigungen 

$S_{0} = \begin{pmatrix} 
\dfrac{\partial f_x(t)}{\partial t} \big|_{x_0} \\ 
\dfrac{\partial f_y(t)}{\partial t} \big|_{y_0}
\end{pmatrix}$ und  $S_{1} = \begin{pmatrix} 
\dfrac{\partial f_x(t)}{\partial t} \big|_{x_1} \\ 
\dfrac{\partial f_y(t)}{\partial t} \big|_{y_1}
\end{pmatrix}$

Beispiel Steigung einer angrenzende Geraden:

$ \vec{S_G} = \begin{pmatrix} 
x_1 - x_0 \\ 
y_1 - y_0
\end{pmatrix} $

Beispiel Steigung eines angrenzenden Kreises:



$ \vec{S_G} = \begin{pmatrix} 

(\alpha_1 - \alpha_0)  \\ 
y_1 - y_0
\end{pmatrix} $



























