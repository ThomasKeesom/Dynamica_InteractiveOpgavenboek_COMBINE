## Rigid bodies

After having discussed dynamics of point masses, we now turn to the analysis of rigid bodies.  In this lecture we focus on the planar kinematics of rigid bodies in the $xy$-plane. That means that the point masses in the rigid body all move in the  $xy$\nobreakdash-plane with $z=0$. However, we note that much of the presented theory is also applicable in 3D and unless explicitly indicated, e.g. with a subscript $_{2D}$, the equations in this lecture are also valid in 3D.

```{card} Rigid Body
:header: Concept
:footer: footer

A rigid body is an object that is undeformable.
```
 Every point mass $m_i$ in the rigid body can be identified by a position vector $r_{i}$. Since the body is rigid and undeformable, the distance between every two point masses in the rigid body is constant which relates their dynamics by the following relative constraint equation:

$$
    |\vec{r}_{i/j}| = |\vec{r}_{i}-\vec{r}_{j}| = \mathrm{~constant} (eq:rigbodconstraint)
$$

In the next section we discuss how the orientation and position of a rigid body can be specified.

## Orientation and position


![](Figures/RIGIDB~4.PDF)

```{figure} Figures/RIGIDB~4.PDF
:label: eq:rigbodconstraint
:width: 70%
:align: center

A sketch of a rigib body with important variables
```

*Figuur: The orientation of a rigid body in the 2D $xy$-plane can uniquely be described by a position vector $\vec{r}$*

<!-- fig:rigbodor -->

 
The first step in the kinematic analysis of a rigid body is to have a unique description of its position and orientation. In planar kinematics, we fully determine the position of a rigid body by fixing the position vectors of 2 points in the rigid body that can be freely chosen, like points $A$ and $B$ of the rectangle in \figref{fig:rigbodor}.

If we know position vectors $r_{A}$ and $r_{B}$ the position and orientation of the rigid body is fully determined. This requires four coordinates: $x_{A}$, $y_{A}$, $x_{B}$ and $y_{B}$. However, because we know the distance between the points, we can use constraint equation (eq:rigbodconstraint) to reduce this to 3 coordinates, namely $x_{A}$, $y_{A}$ and $\phi_{B/A}$, where $\phi_{B/A}$ is the angle the relative position vector $r_{B/A}$ makes with the $x$-axis. With $x_{A}, y_{A}$ we can determine $r_{A}$, and with $\phi_{B/A}$ and knowledge of the distance $|r_{B/A}|$ we can determine $r_{B/A}$:

$$
\begin{aligned}
% label: eq:2Dkinrigbod
    \vec{r}_{A,2D} = x_A \ui + y_A \hat{j} \\
    \vec{r}_{B/A,2D} = |\vec{r}_{B/A}|\cos \phi_{B/A} \ui + |\vec{r}_{B/A}|\sin \phi_{B/A} \uj
\end{aligned}
$$

Now we determine $\vec{r}_{B}$ from the 3 coordinates by adding these two vectors as shown in \figref{fig:rigbodor}.

$$
\begin{aligned}
% label: eq:rrigbod2D
    \vec{r}_{B}=\vec{r}_{A} + \vec{r}_{B/A} \\
    \vec{r}_{B,2D}=(x_A+|\vec{r}_{B/A}|\cos \phi_{B/A})\ui + (y_A+|\vec{r}_{B/A}|\sin \phi_{B/A})\uj
    % label: eq:rrigbod2D2
\end{aligned}
$$


## Velocities in a rigid body

\begin{derivation}
Velocity of a point $B$ in a rigid body
\end{derivation}
By taking the time derivative of the position vector $\vec{r}_{B}$ in \eqref{eq:rrigbod2D}, we can determine the velocity vector of point $B$ in the rigid body as follows:


$$
\begin{aligned}
% label: eq:vrigbod2D
    \vec{v}_{B,2D}=\Dd{}{t} \vec{r}_{B} = 
    \Dd{}{t} \vec{r}_{A} + \Dd{}{t} \vec{r}_{B/A} \\
    =\vec{v}_A+\dot{\phi}_{B/A}|\vec{r}_{B/A}|\left( -\sin \phi_{B/A}\ui + \cos \phi_{B/A}\uj\right) \\
    =\vec{v}_A+\dot{\phi}_{B/A}|\vec{r}_{B/A}| \vech{\phi}_A % label: eq:vrigbod2Dtot
\end{aligned}
$$


In the last step we used \eqref{eq:vhthcyl} to replace the terms in brackets by $\vech{\phi}_A$, which represents the unit vector at point $B$ of a cylindrical coordinate system with origin $A$, which is why we add the subscript $A$ to the unit vector. The velocity of point $B$ in \eqref{eq:vrigbod2Dtot} can be split up in two parts: a vector $\vec{v}_{B,\mathrm{trans}}$ related to translation and a  vector $\vec{v}_{B,\mathrm{rot}}$ related to rotation:


$$
\begin{aligned}
% label: eq:vrigbod2D2
    \vec{v}_{B}= \vec{v}_{B,\mathrm{trans}} + \vec{v}_{B,\mathrm{rot}}\\
   \vec{v}_{B,\mathrm{trans}}  = \vec{v}_{A} \\
   \vec{v}_{B,\mathrm{rot},2D}  = \dot{\phi}_{B/A}|\vec{r}_{B/A}| \vech{\phi}_A % label: eq:vrigbod2D2rot
\end{aligned}
$$


In Figs. \ref{fig:rigbodveltrans}, \ref{fig:rigbodvelrot} and \ref{fig:rigbodvelgen} we show these three velocity vectors $\vec{v}_{B,\mathrm{trans}}$,  $\vec{v}_{B,\mathrm{rot}}$ and $\vec{v}_{B}$. Let us first discuss two special types of rigid body motion: pure translation and pure rotation. 


![](Figures/RigidBodVeltrans.pdf)

*Figuur: Pure translation of a rigid body: $\phi_{B/A*

<!-- fig:rigbodveltrans -->

 

![](Figures/RigidBodVelrot.pdf)

*Figuur: Pure rotation of a rigid body: $\vec{r*

<!-- fig:rigbodvelrot -->



![](Figures/RigidBodVelgen.pdf)

*Figuur: General motion of a rigid body: a combination of rotation and translation.*

<!-- fig:rigbodvelgen -->


### Pure translation
When the angle $\phi_{B/A}$ is kept constant, like in \figref{fig:rigbodveltrans}, all points in the rigid body move with the same velocity vector:

$$
\vec{v}_{B}=\vec{v}_{B,\mathrm{trans}}=\vec{v}_A
$$

This type of motion is called \emph{pure translation}.
The rotational component of velocity is zero, as follows from \eqref{eq:vrigbod2D2rot} and $\dot{\phi}_{B/A}$=0. It is important to note that pure translation can happen along any path curve $\vec{r}_A(s)$, even a circular 
path. The word translation thus only means that the shape of the path is identical for all points in the rigid body because $\phi_{B/A}$ is constant.

### Pure rotation
When the position vector of a point in the rigid body is constant in time, and all other points make circular paths around it, e.g. because it rotates around an axle at that position, the motion of the rigid body is a \emph{pure rotation}.  We choose point $A$ to be the point with constant position vector $\vec{r}_A$, as shown in \figref{fig:rigbodvelrot}. Then according to \eqref{eq:vrigbod2D2rot} the velocity vector of point $B$ is given by:

$$
\vec{v}_{B}=\vec{v}_{B,\mathrm{rot},2D}=\dot{\phi}_{B/A}|\vec{r}_{B/A}| \vech{\phi}_A
$$

To facilitate the analysis of rotations and generalise it to 3D, we now define the angular velocity $\omega$ and angular velocity vector $\vec{\omega}$.

### Angular velocity of a rigid body

The kinematics of a rigid body is closely linked to the time derivative $\dot{\phi}_{B/A}(t)$, which is defined as its angular velocity.

\begin{definition} Angular velocity of a rigid body\\
    The time derivative $\dot{\phi}_{B/A}$ is the angular velocity $\omega_\UL{F}$ of the rigid body:
\end{definition}

$$
\omega_\UL{} \equiv \dot{\phi}_{B/A}
$$

The unit of angular velocity is $\unit[]{rad/s}$. Interestingly, the angular velocity $\omega_\UL{F}$ of the rigid body is independent of the choice of the points $A$ and $B$ on the rigid body and is therefore a general property of a rigid body as can be shown as follows.
\begin{concept} Independency of angular velocity \\
    The angular velocity $\omega_\UL{F}$ of a rigid body is independent of the choice of points $A$ and $B$ on the rigid body.
\end{concept}
\begin{derivation}
    This can be proven by drawing two relative position vectors between points $A-D$ on the rigid body, $\vec{r}_{B/A}$ and $\vec{r}_{D/C}$. Then the angular velocities of these straight lines $\dot{\phi}_{B/A}$ and $\dot{\phi}_{D/C}$ has to be the same, otherwise the rigid body would deform. This can be demonstrated by rotating the rigid body by a full 360 $^\circ$ circle: then all points need to make a circle in the same time and therefore have the same angular velocity.
\end{derivation}

 Note that the angular velocity $\omega_\UL{F}$ of a rigid body is different from the \emph{orbital} angular velocity $\omega_{o}$ of a single point mass around an axis. Orbital angular velocity can depend on the position of the rotation axis or origin (\sref{sec:circmotion}). To distinguish angular velocity of a rigid body from orbital angular velocity, the angular velocity of a rigid body is therefore sometimes called its \emph{spin} angular velocity.

### Angular velocity vector
It can be seen in \figref{fig:rigbodvelrot} that for pure rotation all points in the rigid body move in circular paths around point $A$. The velocity vector $\vec{v}_B$ and all other points in the rigid body, lie in the plane of those circles. To describe that plane we define the angular velocity vector to be perpendicular to that plane.

\begin{concept} Angular velocity vector \\
    The angular velocity vector $\vec{\omega}_\UL{}$ of a rigid body is a vector with magnitude $|\omega|=|\dot{\phi}_{B/A}|$ and a direction that is perpendicular to the plane in which the rigid body rotates. Its direction can be determined using the right hand rule.
\end{concept}
The angular velocity vector (unit $\unit[]{rad/s}$) of a rigid body that rotates in the $xy$ plane is:

$$
% label: eq:angvel2D
    \vec{\omega}_{2D}=\omega_\UL{F} \vech{k} = \dot{\phi}_{B/A} \vech{k}
$$

The direction of the vector can be determined using the right-hand rule by curving the fingers of your right-hand around the curved arrow in \figref{fig:rigbodvelrot}, which indicates the direction of rotational motion. Then your thumb points in the $\vech{k}$ direction, in agreement with \eqref{eq:angvel2D}.

### Determining velocities with the angular velocity vector

From \figref{fig:rigbodvelrot} we see that the velocity vector $\vec{v}_{B,\mathrm{rot}}$ lies in the plane in which the rigid body moves. It is therefore perpendicular to $\vec{\omega}_\UL{F,2D}$. It is also perpendicular to the vector $\vec{r}_{B/A}$, since this vector is the radius of the circular motion. To obtain a vector that is perpendicular to two other vectors we take the cross product of these vectors:

\begin{concept}
    Rotational velocity equation \\
    The rotational velocity of a point $B$ in a rigid body is given by:
\end{concept}

$$
% label: eq:rotvelomega
    \vec{v}_{B,\mathrm{rot}} = \vec{\omega}_\UL{F} \times \vec{r}_{B/A}
$$
 

For the 2D case, where $\vec{\omega}_{2D}=\dot{\phi}_{B/A} \vech{k}$ and $\vec{r}_{B/A}=|\vec{r}_{B/A}| \vech{\rho}_A$, it is straightforward to check the correctness of this equation by comparison with \eqref{eq:vrigbod2D2rot} and by using that $\vech{k} \times \vech{\rho}_A = \vech{\phi}_A$ as follows from the right-hand rule.

### General motion
 In general, as shown in \figref{fig:rigbodvelgen}, the motion of a point in a rigid body is a sum of translational and rotational motion. By combining Eqs. (\ref{eq:vrigbod2D2}) and (\ref{eq:rotvelomega}) we obtain the most general equation and important equation for the velocity in a rigid body:
 
$$
% label: eq:geneqrigbodvel
     \vec{v}_{B}= \vec{v}_{A} + \vec{\omega}_\UL{F} \times \vec{r}_{B/A}
$$

We note that this equation is valid in 3D and for any choice of the points $A$ and $B$ \emph{as long as both points move along with the rigid body}. However, a smart choice of point $A$ can simplify the analysis.

## Angular acceleration of a rigid body

After having determined the velocity vector of a point in a rigid body, it is now of interest to also determine the acceleration vector of the points in the rigid body. We take the time derivative of \eqref{eq:geneqrigbodvel}, and use the product rule on the vector cross product to determine the acceleration vector $\vec{a}_{B}$ in a rigid body.

$$
\begin{aligned}
% label: eq:rbacceleration
    \Dd{}{t} \vec{v}_{B}=\Dd{}{t} \vec{v}_{A} + \Dd{\vec{\omega}_\UL{F}}{t} \times \vec{r}_{B/A} + \vec{\omega}_\UL{F} \times \Dd{\vec{r}_{B/A}}{t} \\
    % label: eq:rbacceleration2
    \vec{a}_{B} = \vec{a}_{A} + \vec{\alpha}_\UL{F} \times \vec{r}_{B/A} + \vec{\omega}_\UL{F} \times \vec{v}_{B,\mathrm{rot}}
\end{aligned}
$$

In this derivation we used that $\Dd{\vec{r}_{B/A}}{t}=\vec{v}_{B,\mathrm{rot}}$ as follows from \eqref{eq:vrigbod2D} and \eqref{eq:vrigbod2D2}, and defined the angular acceleration vector $\vec{\alpha}_\UL{F}$ of the rigid body as follows. 


![](Figures/RigidBodAccgen2.pdf)

*Figuur: Acceleration components in a rigid body. The acceleration vector $\vec{a*

<!-- fig:rigbodaccgen -->


\begin{definition} Angular acceleration vector \\
The angular acceleration vector $\vec{\alpha}$ of a rigid body is the time derivative of its angular velocity vector.
\end{definition}

$$
\vec{\alpha}_{\UL{F}} \equiv  \Dd{\vec{\omega}_\UL{F}}{t}
$$

We note that in planar kinematics this expression can be simplified:

$$
\vec{\alpha}_{\UL{F}2D} = \dot{\omega}_{\UL{F}}\vech{k}=\alpha_{\UL{F}} \vech{k}
$$

The unit of angular acceleration is $\unit[]{rad/s^2}$. We now substitute \eqref{eq:rotvelomega} in \eqref{eq:rbacceleration2} and obtain the general expression for the acceleration.
\newpage
\begin{concept} Acceleration vector in a rigid body \\
The general vector expression for the acceleration vector of a point $B$ in a rigid body that has translational and rotational acceleration:
\end{concept}

$$
\vec{a}_{B} = \vec{a}_{A} + \vec{\alpha}_\UL{F} \times \vec{r}_{B/A} + \vec{\omega}_\UL{F} \times (\vec{\omega}_\UL{F} \times \vec{r}_{B/A})
% label: eq:accvecrigbod
$$


This equation shows that the acceleration of a point $B$ on a rigid body consists of three contributions that are shown in \figref{fig:rigbodaccgen}.

\begin{enumerate}
    \item The translational acceleration $\vec{a}_{B,
\mathrm{trans}}=\vec{a}_{A}$ due to the acceleration of point $A$.
    \item The angular acceleration $\vec{a}_{B,
\mathrm{ang}}=\vec{\alpha}_\UL{F} \times \vec{r}_{B/A}$ due to the angular acceleration vector.
\item The centripetal acceleration $\vec{a}_{B,
\mathrm{cptl}}=\vec{\omega}_\UL{F} \times (\vec{\omega}_\UL{F} \times \vec{r}_{B/A})$, due to the angular velocity vector $\vec{\omega}_\UL{F}$.
\end{enumerate}

\subsubsection{Acceleration in planar kinematics}

In planar kinematics we can simplify the expressions for the angular acceleration somewhat. By using that $\vec{\alpha}_\UL{F,2D}=\alpha_\UL{F} \vech{k}$ we find:


$$
\vec{a}_{B,\mathrm{ang,2D}}=\vec{\alpha}_\UL{F} \times \vec{r}_{B/A}=\alpha_\UL{F} \vech{k} \times |\vec{r}_{B/A}|\vech{\rho}_A = \alpha_\UL{F} |\vec{r}_{B/A}| \vech{\phi}_A
$$


The vector $\vec{\omega}$ is always perpendicular to the $xy$\nobreakdash-plane, such that $\vec{\omega}_\UL{F} \times \vec{r}_{B/A}=\omega_\UL{F}|\vec{r}_{B/A}|\vech{\phi}_A$ and:


$$
\vec{a}_{B,\mathrm{cptl,2D}} =\vec{\omega}_\UL{F} \times (\vec{\omega}_\UL{F} \times \vec{r}_{B/A})=-{\omega}^2 \vec{r}_{B/A}
$$


This shows that the centripetal component of acceleration always points towards point $A$, the centre of rotation. Note that a similar result for the centripetal acceleration term was obtained in \eqref{eq:centripetal}. Combining the three terms we obtain for the planar kinematics of a rigid body the following equation:

$$
\vec{a}_{B,2D} = \vec{a}_{A} + \alpha_\UL{F} |\vec{r}_{B/A}| \vech{\phi} - {\omega}^2 \vec{r}_{B/A}
$$


For completeness we repeat the most important equations for analysing the kinematics of a rigid body:


$$
\begin{aligned}
% label: eq:velrotrbfinal
    \vec{v}_B = \vec{v}_{A} + \vec{\omega}_\UL{F} \times \vec{r}_{B/A} \\
    \vec{a}_B = \vec{a}_{A} + \vec{\alpha}_\UL{F} \times \vec{r}_{B/A}   + \vec{\omega}_\UL{F} \times \left(\vec{\omega}_\UL{F} \times \vec{r}_{B/A}\right) % label: eq:accrotrbfinal\\
    \vec{v}_{B,2D} = \vec{v}_{A} + \omega_\UL{F}|\vec{r}_{B/A}|\vech{\phi}_A \\
    % label: eq:a2drigbody
    \vec{a}_{B,2D} =  \vec{a}_{A} + \alpha_\UL{F} |\vec{r}_{B/A}|\vech{\phi}_A  - \omega^2_\UL{F} \vec{r}_{B/A}
\end{aligned}
$$



\begin{prex}[eo]
\label{ex:fallingsquare}
As an example of the kinematic methods for rigid bodies, consider the square $F$ in \figref{fig:rigbodex}. The \cm{} of the square falls with a velocity $\vec{v}_G=-1 ~\uj~\unit[]{m/s}$ and acceleration $\vec{a}_G=-1~ \uj~\unit[]{m/s^2}$. At the same time the angular velocity and acceleration of the square are $\vec{\omega}_\UL{F}=1 ~\uk~\unit[]{rad/s}$ and $\vec{\alpha}_\UL{F}=1 ~\uk~\unit[]{rad/s^2}$. The question is: \emph{Determine the velocity and acceleration vectors of point $B$.}

To solve this problem, we can use Eqs. (\ref{eq:velrotrb}) and (\ref{eq:accrotrb}). Instead of point $A$ we choose point $G$ as reference point, because we have a lot of information on $G$. Then we determine the vector $\vec{r}_{B/G}=(3.5\ui -0.5\uj) \unit[]{m}$ from the figure. Now we use \eqref{eq:velrotrb} to obtain:

$$
\begin{aligned}
\vec{v}_B = [-1\uj +1\uk \times (3.5\ui -0.5\uj)] ~\unit[]{m/s} \\
     = (0.5\ui + 2.5\uj) ~\unit[]{m/s}
\end{aligned}
$$


And using \eqref{eq:accrotrb} we obtain:

$$
\begin{aligned}
\vec{a}_B = [-1\uj +1\uk \times (3.5\ui -0.5\uj)- 1^2 (3.5\ui - 0.5\uj)] ~\unit[]{m/s^2} \\
     = [(0.5\ui + 2.5\uj) - 1 (3.5\ui - 0.5\uj)] ~\unit[]{m/s^2} \\
     = (-3\ui + 3\uj) ~\unit[]{m/s^2}
\end{aligned}
$$

\end{prex}


![](Figures/RigidBodRotEx.pdf)

*Figuur: Example \ref{ex:fallingsquare*

<!-- fig:rigbodex -->

