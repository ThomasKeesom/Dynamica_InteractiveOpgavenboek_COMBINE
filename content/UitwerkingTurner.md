# Uitwerking: Turner
Hieronder de oplossingen voor de Turner opgaven:

1. Geef de positievector $\vec{r}_A$ als functie van $L_1$ en $\phi_1$. Gebruik het $\hat{i}, \hat{j}, \hat{k}$ co\"ordinatensysteem zoals afgebeeld in het Figuur.

$$
\vec r_A
= x_A\hat{\imath}+y_A\hat{\jmath}
=\sin\varphi_1L_1\hat{\imath}-\cos\varphi_1L_1\hat{\jmath}
$$

2. Doe hetzelfde voor de positievectoren $\vec{r}_B$ en $\vec{r}_C$. Gebruik weer het $\hat{i}, \hat{j}, \hat{k}$ co\"ordinatensysteem zoals afgebeeld in het Figuur. 

$$
\vec r_B
=\Bigl(x_A+\sin\varphi_2L_2\Bigr)\hat{\imath}
+\Bigl(y_A-\cos\varphi_2L_2\Bigr)\hat{\jmath}\\
$$

$$
\vec r_C
=\Bigl(x_B+\sin\varphi_3L_3\Bigr)\hat{\imath}
+\Bigl(y_B-\cos\varphi_3L_3\Bigr)\hat{\jmath}
$$

3. Geef een uitdrukking voor de snelheidsvectoren $\vec{v}_A$, $\vec{v}_B$ en $\vec{v}_C$ als functie van $L_1$ t/m $L_3$ en $\dot{\phi}_1$ t/m $\dot{\phi}_3$. Maak gebruik van een cilindrisch co\"ordinatensysteem. 

$$
\vec v_A
=\vec v_O+\dot{\varphi}_1\lvert \vec r_{A/O}\rvert\hat \varphi_0
=\dot{\varphi}_1\lvert \vec r_{A/O}\rvert\hat \varphi_0
$$

$$
\lvert \vec r_{A/O}\rvert
=\sqrt{(\sin\varphi_1L_1)^2+(\cos\varphi_1L_1)^2}
=\sqrt{L_1^2(\sin^2\varphi_1+\cos^2\varphi_1)}
=L_1
$$

$$
\vec v_A=\dot{\varphi}_1L_1\hat \varphi_0
$$

$$
\vec v_B=\vec v_A+\dot{\varphi}_2\lvert \vec r_{B/A}\rvert\hat \varphi_A
$$

$$
\boxed{\vec v_B=\vec v_A+\dot{\varphi}_2L_2\hat q_A
=\dot{\varphi}_1L_1\hat \varphi_0+\dot{\varphi}_2L_2\hat \varphi_A}
$$

$$
\boxed{\vec v_C}=\vec v_B+\dot{\varphi}_3L_3\hat \varphi_B
=\boxed{\dot{\varphi}_1L_1\hat \varphi_0+\dot{\varphi}_2L_2\hat \varphi_A+\dot{\varphi}_3L_3\hat \varphi_B}
$$

4. Leg uit of deze snelheidsvectoren in dezelfde richting staan of niet. 

Eenheidsvectoren $\hat \varphi_0$, $\hat \varphi_A$ en $\hat \varphi_B$ staan niet noodzakelijk in dezelfde richting.
Ze staan ieder loodrecht op de staven $L_1$, $L_2$ en $L_3$ en zolang deze niet parallel lopen, staan
$\hat \varphi_0$, $\hat \varphi_A$ en $\hat \varphi_B$ juist in verschillende richtingen.

5. Als de hoeksnelheid $\dot{\phi}_2$ gelijk is aan nul, wat kun je dan zeggen over de hoek tussen $L_1$ en $L_2$?

Als $\varphi_1=\varphi_2$ op ieder moment dan $\dot{\varphi}_1=\dot{\varphi}_2$ en blijft de hoek tussen
$L_1$ en $L_2$ constant. Bovendien geldt dat $L_1$ en $L_2$ in elkaars verlengde staan en $L_1$ en $L_2$ dan als \'e\'en
staaf met lengte $L_1+L_2$ gezien kunnen worden. Punt $B$ beschrijft dan een cirkelbaan rond $O$ met straal

$$
\rho_B=L_1+L_2.
$$

$$
\vec v_B=\dot{\varphi}_1\,L_1\,\hat \varphi_0+\dot{\varphi}_2\,L_2\,\hat \varphi_A
$$

$$
\boxed{\vec v_B=\dot{\varphi}_1\,(L_1+L_2)\,\hat \varphi_0}
\qquad
(\dot{\varphi}_1=\dot{\varphi}_2,\;\hat \varphi_0=\hat \varphi_A)
$$
