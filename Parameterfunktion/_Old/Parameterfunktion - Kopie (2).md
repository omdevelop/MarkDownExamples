# Parameterformen

## 1. Zweidimensionale Parameterfunktion

Zwei reellwertige Funktionen $x(p) = f_x(p)$ und $y(p) = f_y(p) $ mit $ p \in \R $ sind als Abbildung
von $ \R $ nach $ \R $ definiert: 

$f_x(p) : \R \to \R $ und $f_y(p) : \R \to \R $ .

Die Parameterfunktion $\vec{P(p)} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix}$ mit $p \in \R $ wird damit eine reellwertige Abbildung $\R \to \R \times  \R$ . 
Falls $p$ normiert im Intervall $p \in [0, \varepsilon, 1]$ mit Schrittweite $\epsilon \in (0, 1) \in \R$ heisst  $\vec{P(p)}$ normierte Parameterfunktion.







## 2. Parameterfunktion: Gerade / Strecke

Wahl der Zwei-Punkte-Form einer Geraden mit den gegebenen Punkten $P_0$ und $P_1$ :

$P_0 = (x_0, y_0)$ mit $x_0, y_0 \in \R$ und $P_1 = (x_1, y_1)$ mit $x_1, y_1 \in \R$ 

Die Parameterfunktion einer Geraden ergibt sich über die Zwei-Punkte-Form:

$ \vec{P(p)}_{gerade} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0)p + x_0 \\ (y_1 - y_0)p + y_0 \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion einer Gerade ergibt eine Strecke:

$ \vec{P(p)}_{strecke} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0)p + x_0 \\ (y_1 - y_0)p + y_0 \end{pmatrix}$ $p \in [0  .. 1]$



## 3. Parameterfunktion: Kreis / Kreisbogen

Wahl der Zwei-Winkel-Form eines Kreises mit den gegebenen Winkeln $\alpha_0$ und $\alpha_1$ :

$\alpha_0 \in [0 .. N \cdot  2 \pi]$ und $\alpha_1 \in [0 .. N \cdot 2 \pi]$ und $N \in \N_0$ .

( $\alpha_0 < \alpha_1$ : positiver Drehsinn, $\alpha_0 > \alpha_1$ : negativer Drehsinn )

Bei gegebenem Kreismittelpunkt $P_m = (x_m, y_m)$  und Kreisradius $R > 0 \in \R$  ergibt sich die Parameterfunktion des Kreises:

$ \vec{P(p)}_{kreis} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion eines Kreises ergibt einen Kreisbogen:

$ \vec{P(p)}_{kreisbogen} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in [0  .. 1]$



## 4. Parameterfunktion: Ellipse / Ellipsenbogen

Wahl der Zwei-Winkel-Form einer Ellipse mit den gegebenen Winkeln $\alpha_0$ und $\alpha_1$ :

$\alpha_0 \in [0 .. N \cdot  2 \pi]$ und $\alpha_1 \in [0 .. N \cdot 2 \pi]$ und $N \in \N_0$ .

( $\alpha_0 < \alpha_1$ : positiver Drehsinn, $\alpha_0 > \alpha_1$ : negativer Drehsinn )

Bei gegebenem Ellipsenmittelpunkt $P_m = (x_m, y_m)$  und grosser Halbachse $A > 0 \in \R$ und kleiner Halbachse $B > 0 \in \R$ ergibt sich die Parameterfunktion der Ellipse:

$ \vec{P(p)}_{ellipse} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} x_m + A \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + B \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion eines Kreises ergibt einen Kreisbogen:

$ \vec{P(p)}_{ellipsenbogen} = \begin{pmatrix} x(p) \\ y(p) \end{pmatrix} = \begin{pmatrix} x_m + A \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + B \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in [0  .. 1]$



## 5. Theorie Kubischer Spline

Mit der Vier-Punkte-Form eines kubischen Splines ergibt sich mit den gegebenen Randpunkten

$P_0 = (x_0, y_0)$  mit $x_0, y_0 \in \R$ und $P_1 = (x_1, y_1)$  mit $x_1, y_1 \in \R$ 

und den Randsteigungen

 $ S_0 \big|_{P_0} = \begin{pmatrix} s_{0x} \\ s_{0y} \end{pmatrix} = \begin{pmatrix} \dfrac{d f_x(p)}{dp} \\ \dfrac{d f_y(p)}{dp} \end{pmatrix} $ und $ S_1 \big|_{P_1} = \begin{pmatrix} s_{1x} \\ s_{1y} \end{pmatrix}$ 





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



























