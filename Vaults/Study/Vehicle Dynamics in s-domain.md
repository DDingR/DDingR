## 1. Summary
The systems in s-domain are represented as follows:
$$
G^{A_y}_{\delta_1}(s)
= 
G^{A_y}_{\delta_1}(0)
\cdot
\tfrac{1+(1+\lambda_1)T_1s+(1+\lambda_2)T_ss^2}{1+\tfrac{2\zeta}{\omega_n}s + \tfrac{1}{\omega_n^2}s^2}
$$
and
$$
G^{r}_{\delta_1}(s)
=
G^{r}_{\delta_1}(0)\cdot\tfrac{1+(1+\lambda_r)T_r s}{1+\tfrac{2\zeta}{\omega_n}s+\tfrac{1}{\omega_n^2}s^2}
$$
where
$$
G^{A_y}_{\delta_1} (0) 
=
\tfrac{(1-k)V_x^2}{L(1+KV_x^2)}
,\quad
\lambda_1:= \tfrac{L}{l_2}\cdot\tfrac{k}{1-k},\quad T_1:=\tfrac{l_2}{V_x} 
,\quad
\lambda_2:= \tfrac{C_1+C_2}{C_2}\cdot\tfrac{k}{1-k},\quad T_2:=\tfrac{I_z}{LC_2}
$$
and
$$
G^{r}_{\delta_1} (0) 
:= 
\tfrac{(1-k)V_x}{L(1+KV_x^2)}
,\quad
\lambda_r 
:=
\tfrac{l_1C_1-l_2C_2}{l_1C_1}\cdot\tfrac{k}{1-k}
,\quad
T_r
:=
\tfrac{l_1m}{LC_2}V_x
$$
and
$$
K=\tfrac{C_2l_2-C_1l_1}{C_1C_2L^2}m
.
$$
> Note that when $k=0$, i.e. for the case of FWS, the perturbation terms by proportional RWS $\lambda_j,\ j\in\{1,2,r\}$, are removed.


## 2. Derivation
### 2.1. Lateral Acceleration
With small steering angle and constant longitudinal velocity assumptions, the vehicle dynamics can be represented as follows:
$$
\begin{aligned}
mV_x (\ddtt \beta +r)
=&
F_1+F_2 = 
C_1
\left(
\delta_1-\left(\beta+\tfrac{l_1 r}{V_x}\right)
\right)
+
C_2
\left(
\delta_2-\left(\beta-\tfrac{l_2 r}{V_x}\right)
\right)
\\
I_z\ddtt r 
=&
l_1 F_1 - l_2 F_2
=
\left(
l_1\cdot
C_1
\left(
\delta_1-\left(\beta+\tfrac{l_1 r}{V_x}\right)
\right)
-
l_2\cdot
C_2
\left(
\delta_2-\left(\beta-\tfrac{l_2 r}{V_x}\right)
\right)
\right)
.
\end{aligned}
$$
In other words,
$$
\begin{aligned}
\ddtt \beta + \tfrac{C_1+C_2}{mV_x}\beta + \left( 1 + \tfrac{l_1C_1-l_2C_2}{mV^2_x}\right) r
=&
\tfrac{C_1+C_2k}{mV_x}\delta_1
\\
\ddtt r + \tfrac{l_1^2C_1+l_2^2C_2}{I_zV_x}r + \tfrac{l_1C_1-l_2C_2}{I_z}\beta
=&
\tfrac{l_1C_1-l_2C_2k}{I_z}\delta_1
\end{aligned}
$$

^2928ef

Using Laplace transformation [[#^2928ef]] can be represented as follows: 
$$
a_1 \beta + a_2r = a_3\delta_1,\quad b_1 r + b_2 \beta = b_3 \delta_1
$$
where
$$
\begin{aligned}
a_1 = s+\tfrac{C_1+C_2}{mV_x}
,\quad
a_2 = 1 + \tfrac{l_1C_1-l_2C_2}{mV^2_x}
,\quad 
a_3 = \tfrac{C_1+C_2k}{mV_x}
\\
b_1 = s+ \tfrac{l_1^2C_1+l_2^2C_2}{I_zV_x}
,\quad
b_2 = \tfrac{l_1C_1-l_2C_2}{I_z}
,\quad
b_3 = \tfrac{l_1C_1-l_2C_2k}{I_z}
.
\end{aligned}
$$
Then the transfer functions are
$$
\tfrac{\beta(s)}{\delta_1(s))} = \tfrac{a_3b_1-a_2b_3}{a_1b_1-a_2b_2}
,\quad 
\tfrac{r(s)}{\delta_1(s)} = \tfrac{a_3b_2-a_1b_3}{a_2b_2-a_1b_1}
.
$$

^e35df3

The transfer function of lateral acceleration to the real steering angle can be represented as follows:
$$
G^{A_y}_{\delta_1}(s):=
\tfrac{A_y(s)}{\delta_1(s)} = V_x\left(s\tfrac{\beta}{\delta_1}+\tfrac{r}{\delta_1}\right) 
=
\tfrac{V_x}{a_1b_1-a_2b_2}
\left(
s(a_3b_1-a_2b_3)-(a_3b_2-a_1b_3)
\right)
.
$$
First, numerator of the transfer function is obtained. Each multiplication terms are represented as follows:
$$
\begin{aligned}
a_3b_1-a_2b_3
=&
\left(\tfrac{C_1+C_2k}{mV_x}\right) s 
+
\tfrac{(l_1^2C_1+l_2^2C_2)(C_1+C_2k)}{mI_zV_x^2}
-
\tfrac{l_1C_1-l_2C_2k}{I_z}
-
\tfrac{(l_1C_1-l_2C_2)(l_1C_1-l_2C_2k)}{mI_zV_x^2}
\\
=&
\left(\tfrac{C_1+C_2k}{mV_x}\right) s 
-
\tfrac{l_1C_1-l_2C_2k}{I_z}
+
\tfrac{L^2 C_1C_2}{mI_zV_x^2}
+
\tfrac{Ll_1C_1C_2}{mI_zV_x^2}(k-1)
\end{aligned}
$$
and
$$
\begin{aligned}
a_3b_2-a_1b_3
=&
\tfrac{(C_1+C_2k)(l_1C_1-l_2C_2)}{mI_zV_x}
-
\left(\tfrac{l_1C_1-l_2C_2k}{I_z}\right) s 
-
\tfrac{(C_1+C_2)(l_1C_1-l_2C_2k)}{mI_zV_x}
\\
=&
-
\left(\tfrac{l_1C_1-l_2C_2k}{I_z}\right) s 
+
\tfrac{LC_1C_2}{mI_zV_x}(k-1)
.
\end{aligned}
$$
Then we have
$$
\begin{aligned}
s(a_3b_1-a_2b_3)& - (a_3b_2-a_1b_3)
=
\\
&\left(\tfrac{C_1+C_2}{mV_x}+\tfrac{C_2}{mV_x}(k-1)\right)s^2
+
\left(\tfrac{L^2C_1C_2}{mI_zV_x^2}+\tfrac{Ll_1C_1C_2}{mI_zV_x^2}(k-1)\right)s
-
\tfrac{LC_1C_2}{mI_zV_x}(k-1)
\end{aligned}
$$

To transform into a standard form of robust control, we use the following equality
$$
\tfrac{a+b(k-1)}{c(k-1)}
=
\tfrac{b-a}{c} \left(1+\tfrac{a}{a-b}\tfrac{k}{1-k}\right)
.
$$
Then the numerator of the transfer function is
$$
V_x
\left(
s(a_3b_1-a_2b_3)-(a_3b_2-a_1b_3)
\right)
= 
V_x
\left(
-
\tfrac{LC_1C_2}{mI_zV_x}(k-1)
\cdot
\left(
1+(1+\lambda_1)T_1 s + (1+\lambda_2)T_2 s^2
\right)
\right)
$$

where
$$
\begin{aligned}
\lambda_1:= \tfrac{L}{l_2}\cdot\tfrac{k}{1-k},\quad T_1:=\tfrac{l_2}{V_x} 
\\
\lambda_2:= \tfrac{C_1+C_2}{C_2}\cdot\tfrac{k}{1-k},\quad T_2:=\tfrac{I_z}{LC_2}
.
\end{aligned}
$$
Second, the steady state value of the transfer function is obtained. 
$$
a_1b_2-a_2b_2 = (\cdot)s^2+(\cdot\cdot)s + \tfrac{L^2C_1C_2}{mI_zV_x^2}-\tfrac{l_1C_1-l_2C_2}{I_z}
.
$$
Then, the steady state value can be obtained as follows
$$
G^{A_y}_{\delta_1} (0) = 
V_x
\cdot
\left(-
\tfrac{LC_1C_2(k-1)}{mI_zV_x}/
\left(
\tfrac{L^2C_1C_2}{mI_zV_x^2}-\tfrac{l_1C_1-l_2C_2}{I_z}
\right)
\right)
=
\tfrac{(1-k)V_x^2}{L(1+KV_x^2)}
$$
where
$$
K:=\tfrac{C_2l_2-C_1l_1}{C_1C_2L^2}m
.
$$
Finally, the transfer function is
$$
G^{A_y}_{\delta_1}(s)
= 
G^{A_y}_{\delta_1}(0)
\cdot
\tfrac{1+(1+\lambda_1)T_1s+(1+\lambda_2)T_ss^2}{1+\tfrac{2\zeta}{\omega_n}s + \tfrac{1}{\omega_n^2}s^2}
$$
where the natural frequency and damping ratio are determined according to the system definitions.
### 2.2. Yaw rate
From [[#^e35df3]] the transfer function can be obtained as follows:
$$
G^{r}_{\delta_1}(s):=\tfrac{r(s)}{\delta_1(s)}
=
G^{r}_{\delta_1}(0)\cdot\tfrac{1+(1+\lambda_r)T_r s}{1+\tfrac{2\zeta}{\omega_n}s+\tfrac{1}{\omega_n^2}s^2}
$$
where
$$
G^{r}_{\delta_1} (0) 
:= 
\tfrac{(1-k)V_x}{L(1+KV_x^2)}
,\quad
\lambda_r 
:=
\tfrac{l_1C_1-l_2C_2}{l_1C_1}\cdot\tfrac{k}{1-k}
,\quad
T_r
:=
\tfrac{l_1m}{LC_2}V_x
.
$$

