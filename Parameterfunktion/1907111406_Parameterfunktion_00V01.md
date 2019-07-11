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

$ \vec{P(p)}_{gerade} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0)p + x_0 \\ (y_1 - y_0)p + y_0 \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion einer Gerade ergibt eine Strecke:

$ \vec{P(p)}_{strecke} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} (x_1 - x_0)p + x_0 \\ (y_1 - y_0)p + y_0 \end{pmatrix}$ $p \in [0  .. 1]$

Entsprechend die Parameterfunktionen der Steigung:

$\dfrac{\vec{dP(p)}_{gerade}}{dp} = \begin{pmatrix} \dfrac{df_x(p)}{dp} \\ \dfrac{df_y(p)}{dp} \end{pmatrix} = \begin{pmatrix}  x_1 - x_0 \\  y_1 - y_0 \end{pmatrix}$



## 3. Parameterfunktion: Kreis / Kreisbogen

Wahl der Zwei-Winkel-Form eines Kreises mit den gegebenen Winkeln $\alpha_0$ und $\alpha_1$ :

$\alpha_0 \in [0 .. N \cdot  2 \pi]$ und $\alpha_1 \in [0 .. N \cdot 2 \pi]$ und $N \in \N_0$ .

( $\alpha_0 < \alpha_1$ : positiver Drehsinn, $\alpha_0 > \alpha_1$ : negativer Drehsinn )

Bei gegebenem Kreismittelpunkt $P_m = (x_m, y_m)$  und Kreisradius $R > 0 \in \R$  ergibt sich die Parameterfunktion des Kreises:

$ \vec{P(p)}_{kreis} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion eines Kreises ergibt einen Kreisbogen:

$ \vec{P(p)}_{kreisbogen} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} x_m + R \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + R \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in [0  .. 1]$

Entsprechend die Parameterfunktionen der Steigung:

$\dfrac{\vec{dP(p)}_{kreis}}{dp} = \begin{pmatrix} \dfrac{df_x(p)}{dp} \\ \dfrac{df_y(p)}{dp} \end{pmatrix} = \begin{pmatrix} -R \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \\ +R \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$



## 4. Parameterfunktion: Ellipse / Ellipsenbogen

Wahl der Zwei-Winkel-Form einer Ellipse mit den gegebenen Winkeln $\alpha_0$ und $\alpha_1$ :

$\alpha_0 \in [0 .. N \cdot  2 \pi]$ und $\alpha_1 \in [0 .. N \cdot 2 \pi]$ und $N \in \N_0$ .

( $\alpha_0 < \alpha_1$ : positiver Drehsinn, $\alpha_0 > \alpha_1$ : negativer Drehsinn )

Bei gegebenem Ellipsenmittelpunkt $P_m = (x_m, y_m)$  und grosser Halbachse $A > 0 \in \R$ und kleiner Halbachse $B > 0 \in \R$ ergibt sich die Parameterfunktion der Ellipse:

$ \vec{P(p)}_{ellipse} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} x_m + A \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + B \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in \R$

Die normierte Parameterfunktion eines Kreises ergibt einen Kreisbogen:

$ \vec{P(p)}_{ellipsenbogen} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} x_m + A \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \\ y_m + B \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$ $p \in [0  .. 1]$

Entsprechend die Parameterfunktionen der Steigung:

$\dfrac{\vec{dP(p)}_{ellipse}}{dp} = \begin{pmatrix} \dfrac{df_x(p)}{dp} \\ \dfrac{df_y(p)}{dp} \end{pmatrix} = \begin{pmatrix} -A \cdot sin((\alpha_1 - \alpha_0)p + \alpha_0) \\ +B \cdot cos((\alpha_1 - \alpha_0)p + \alpha_0) \end{pmatrix}$



## 5. Parameterfunktion: Kubischer Spline

Mit der Vier-Punkte-Form eines kubischen Splines ergibt sich mit den gegebenen Randpunkten

$P_0 = (x_0, y_0)$  mit $x_0, y_0 \in \R$ und $P_1 = (x_1, y_1)$  mit $x_1, y_1 \in \R$ 

und den Randsteigungen

 $ S_0 \big|_{P_0} = \begin{pmatrix} s_{0x} \\ s_{0y} \end{pmatrix} = \begin{pmatrix} \dfrac{d f_x(p)}{dp} \big|_{P_0} \\ \dfrac{d f_y(p)}{dp}\big|_{P_0} \end{pmatrix}$ und $ S_1 \big|_{P_1} = \begin{pmatrix} s_{1x} \\ s_{1y} \end{pmatrix}= \begin{pmatrix} \dfrac{d f_x(p)}{dp} \big|_{P_1} \\ \dfrac{d f_y(p)}{dp}\big|_{P_1} \end{pmatrix} $ 

und den zwei Parameterfunktionen dritten Grades

$f_x(p) = a_x p^3 + b_x p^2 + c_x p + d_x$ mit $a_x , b_x , c_x , d_x \in \R$

$f_y(p) = a_y p^3 + b_y p^2 + c_y p + d_y$  mit $a_y , b_y , c_y , d_y \in \R$

$ \vec{P(p)}_{spline} = \begin{pmatrix} f_x(p) \\ f_y(p) \end{pmatrix} = \begin{pmatrix} a_x p^3 + b_x p^2 + c_x p + d_x \\  a_y p^3 + b_y p^2 + c_y p + d_y \end{pmatrix}$

mit den acht zu bestimmenden Polynomkoeffizienten $a_x , b_x , c_x , d_x$ und $a_y , b_y , c_y , d_y$ .

Entsprechend die Parameterfunktionen der Steigung:

$\dfrac{\vec{dP(p)}_{spline}}{dp} = \begin{pmatrix} \dfrac{df_x(p)}{dp} \\ \dfrac{df_y(p)}{dp} \end{pmatrix} = \begin{pmatrix} 3a_x p^2 + 2b_x p + c_x \\  3a_y p^2 + 2b_y p + c_y \end{pmatrix}$

Für Berechnungen der Randsteigungen $S_0$ und $S_1$ vergleiche **Anhang - Berechnung der Randsteigung**.



## 6. Anhang

### Berechnung der Randsteigungen

Bei den untersuchten Parameterfunktionen $\vec{P(t)}$ in $\R^2$ geben die, falls vorhanden, Randparameterfunktionen die notwendigen Steigungen 

$S_{0} = \begin{pmatrix} 
\dfrac{\partial f_x(t)}{\partial t} \big|_{x_0} \\ 
\dfrac{\partial f_y(t)}{\partial t} \big|_{y_0}
\end{pmatrix}$ und  $S_{1} = \begin{pmatrix} 
\dfrac{\partial f_x(t)}{\partial t} \big|_{x_1} \\ 
\dfrac{\partial f_y(t)}{\partial t} \big|_{y_1}
\end{pmatrix}$

Beispiel Steigung einer angrenzenden Strecke:

$ \vec{S_{strecke}} = \begin{pmatrix} \dfrac{dx(p)}{dp} \\ \dfrac{dy(p)}{dp} \end{pmatrix} = \begin{pmatrix} 
x_1 - x_0 \\ 
y_1 - y_0
\end{pmatrix} $ mit $p \in [0  .. 1]$

Beispiel Steigung eines angrenzenden Kreisbogens:

$\vec{S(p)}_{kreisbogen} = \begin{pmatrix} \dfrac{dx(p)}{dp} \\ \dfrac{dy(p)}{dp} \end{pmatrix} = \begin{pmatrix} - (\alpha_1 - \alpha_0) R \cdot sin[(\alpha_1 - \alpha_0)p + \alpha_0] \\ +(\alpha_1 - \alpha_0) R \cdot cos[(\alpha_1 - \alpha_0)p + \alpha_0] \end{pmatrix}$ mit $p \in [0  .. 1]$

Beispiel Steigung eines angrenzenden Ellipsenbogens:

$\vec{S(p)}_{ellipsenbogen} = \begin{pmatrix} \dfrac{dx(p)}{dp} \\ \dfrac{dy(p)}{dp} \end{pmatrix} = \begin{pmatrix} - (\alpha_1 - \alpha_0) A \cdot sin[(\alpha_1 - \alpha_0)p + \alpha_0] \\ +(\alpha_1 - \alpha_0) B \cdot cos[(\alpha_1 - \alpha_0)p + \alpha_0] \end{pmatrix}$ mit $p \in [0  .. 1]$



### Umrechnung von unnormierten in normierte Parameterfunktionen

$f(t) = a t^2 + b t +c$ mit $t \in \R$

$F(T) = A T^2 + B T + C$ mit $T \in [0, 1]$

alle Punkte müssen gleich sein : 

$f(t) = F(T)$

$a t^2 + b t +c = A T^2 + B T + C$ 

Drei Punkte $P_0$, $P_1$ und $P_2$ gegeben (mit $T_0 = 0$ und $T_2 = 1$) :

$P_0 = (t_0, f_0) == (T_0, F_0) = (0, C) = (0, f_0)$

$P_1 = (t_1, f_1) == (T_1, F_1)$

$P_2 = (t_2, f_2) == (T_2, F_2) = (1, A + B + C)$



$f_0 = C$

$f_1 = A T_1^2 + B T_1 + C$

$f_2 = A + B + C$

| A       | B     | C    | Inhomogen |
| ------- | ----- | ---- | --------- |
| 0       | 0     | 1    | $f_0$     |
| $T_1^2$ | $T_1$ | 1    | $f_1$     |
| 1       | 1     | 1    | $f_2$     |

| A       | B     | Inhomogen |
| ------- | ----- | --------- |
| $T_1^2$ | $T_1$ | $f_1$     |
| 1       | 1     | $f_2$     |

$D = T_1^2 - T_1$

$D_A = f_1 - T_1$

$D_B = T_1^2 - f_2$

$A = \dfrac{D_A}{D} = \dfrac{f_1 - T_1}{T_1^2 - T_1}$

$B = \dfrac{D_B}{D} = \dfrac{T_1^2 - f_2}{T_1^2 - T_1}$



Mit $f_1 = A T_1^2 + B T_1 + C$

$\Rightarrow f_1 = \dfrac{f_1 - T_1}{T_1^2 - T_1} T_1^2 + \dfrac{T_1^2 - f_2}{T_1^2 - T_1}T_1 + f_0$

$f_1(T_1^2 - T_1) = (f_1 - T_1) T_1^2 + (T_1^2 - f_2) T_1 + f_0(T_1^2 - T_1)$

$f_1 T_1^2 - f_1 T_1 = f_1 T_1^2 - T_1^3  + T_1^3 - f_2 T_1 + f_0 T_1^2 - f_0 T_1$

$0 = f_1 T_1 - f_2 T_1 + f_0 T_1^2 - f_0 T_1$

$0 =  T_1^2 (f_0) + T_1 (f_1 - f_2 - f_0)$

Lösung der quadratischen Gleichung:

$u x^2 + v x + w = 0$   $\Rightarrow$   $x_{1/2} = -\dfrac{v}{2u} \pm \sqrt{\dfrac{v^2}{4u^2} - \dfrac{w}{u}}$

hier: $u = f_0$ und $v = f_1 - f_2 - f_0$ und $w = 0$

$\Rightarrow$   $T_{1\pm} = -\dfrac{f_1 - f_2 - f_0}{2 f_0} \pm \sqrt{\dfrac{(f_1 - f_2 - f_0)^2}{4 f_0^2} - \dfrac{w}{f_0}}$

und damit

$A_{\pm} = \dfrac{f_1 - T_{1\pm}}{T_{1\pm}^2 - T_{1\pm}}$

$B = \dfrac{T_{1\pm}^2 - f_2}{T_{1\pm}^2 - T_{1\pm}}$

