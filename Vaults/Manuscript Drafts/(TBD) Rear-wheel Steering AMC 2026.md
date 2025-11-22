*Myeongseok Ryu, Kyunghwan Choi*
## 1. Introduction


### 1.1. Contributions
- 

## 2. Problem Formulation
Consider the following simplified 2-DOF vehicle dynamics system:
$$
\begin{aligned}
mv_x (\ddtt \beta+r)
&=
F_1 + F_2
\\
I_z\ddtt r
&=
F_1l_1-F_2l_2
,
\end{aligned}
$$
where ...
The lateral tire forces are defined as functions of the tire slip angles as follows:
$$
F_1
:=
C_1
\left(
\delta - \left(\beta+\tfrac{l_1 r}{v_x}\right)
\right)
,\text{ and }
F_2
:=
C_2
\left(
- \beta+\tfrac{l_2 r}{v_x}
\right)
,
$$
where $C_1:=C_1(\cdots)$ and $C_2:=C_2(\cdots)$ are functions of the states.

> [!assumption]
> Tire functions are functions of the selected states, i.e. $\beta, r$. 

The control objectives of this study can be listed as follows:
- 

## 3. Main Results

We define two systems as follows:
$$
\begin{aligned}
\ddtt \mv{x}
&=
\mv{f}(\mv{x},\mv{p}%(\mv{x})
,\mv{u})
,
\\
\ddtt \widehat{\mv{x}}
&=
\mv{f}(\widehat{\mv{x}},\widehat{\mv{p}}%({\mv{x}})
,\mv{u})
,
\end{aligned}
$$
where $\mv{x}$-system is actual system with actual parameter $\mv{p}$ and $\widehat{\mv{x}}$-system is estimated system with estimated parameter $\widehat{\mv{p}}$. The system function $\mv{f}:=...$ is Lipschitz continuous function such that $\norm{\mv{f}(\mv{x})-\mv{f}(\mv{y})} \le L \norm{\mv{x}-\mv{y}}$ for some positive constant $L$.
Finally, the error dynamics can be obtained as follows:
$$
\begin{aligned}
\ddtt \mv{e}:=\ddtt(\widehat{\mv{x}}-\mv{x})
&=
\mv{f}(\widehat{\mv{x}},\widehat{\mv{p}})
-
\mv{f}(\mv{x},\mv{p})
\\

\end{aligned}
$$
To obtain LTV formulation, we use state-dependent coefficient (SDC) formulation which is defined as follows:
$$

$$
### 3.1. Application to Vehicle System

$$
\pptfrac{\mv{f}}{\mv{x}}
=
\begin{bmatrix}
\tfrac{1}{mv_x}
\left(-C_1-C_2\right)
&
\tfrac{1}{mv_x}
\left(-C_1\tfrac{l_1}{v_x}+C_2\tfrac{l_2}{v_x}-1\right)
\\
\tfrac{1}{I_z}
\left(-C_1l_1+C_2l_2\right)
&
\tfrac{1}{I_z}
\left(-C_1\tfrac{l_1^2}{v_x}-C_2\tfrac{l_2^2}{v_x}\right)
\end{bmatrix}
$$

$$
\pptfrac{\mv{f}}{\mv{C}}
=
\begin{bmatrix}
\tfrac{1}{mv_x}
\left(
\delta-\left(\beta+\tfrac{l_1 r}{v_x}\right)
\right)
&
\tfrac{1}{mv_x}
\left(
-\beta+\tfrac{l_2r}{v_x}
\right)
\\
\tfrac{1}{I_z}
\left(\delta-\left(\beta+\tfrac{l_1 r}{v_x}\right)\right)l_1
&
-
\tfrac{1}{I_z}
\left(-\beta+\tfrac{l_2 r}{v_x}\right) l_2
\end{bmatrix}
$$


## 4. Simulation

## 5. Conclusion

