\part{Rigid Body Dynamics}
\label{part:rigbod}
# Kinematics of Rigid Bodies
\label{chapter:kinematicsrigbodies}

%Reconsider naming of v_rot and a_ang (same name?)
%Verbindingsvergelijkingen in kinematica starre lichamen
%Wat betekent het ‘meebewegen’ van een punt (hoeft niet in het starre lichaam te liggen).
%Hoe punten A en B kiezen voor kinematica?
%Formule 9.80: accenten op rho en phi in subscripts coriolis componenten.

## Rigid bodies

After having discussed dynamics of point masses\index{Point mass}, we now turn to the analysis of rigid bodies\index{Rigid body}.  In this \lecn{} we focus on the planar kinematics\index{Planar kinematics} of rigid bodies in the $xy$-plane. That means that the point masses in the rigid body all move in the  $xy$\nobreakdash-plane with $z=0$. However, we note that much of the presented theory is also applicable in 3D and unless explicitly indicated, e.g. with a subscript\index{Subscript} $_{2D}$, the equations in this \lecn{} are also valid in 3D.

> **Concept – Rigid body**
>
> A rigid body is an object that is undeformable.
 Every point mass $m_i$ in the rigid body can be identified by a position vector\index{Position vector} $\V{r}_{i}$. Since the body is rigid and undeformable, the distance\index{Distance} between every two point masses in the rigid body is constant which relates their dynamics by the following \emph{relative constraint equation} (see \sref{sec:relconstraints}):
\begin{equation}
\label{eq:rigbodconstraint}
    |\V{r}_{i/j}| = |\V{r}_{i}-\V{r}_{j}| = \mathrm{~constant}
\end{equation}
In the next section we discuss how the orientation and position of a rigid body can be specified.

## Orientation and position

![The orientation of a rigid body in the 2D $xy$\nobreakdash-plane can uniquely be described by a position vector $\V{r](Figures/RigidBodOrientation.pdf)

*Figuur: The orientation of a rigid body in the 2D $xy$\nobreakdash-plane can uniquely be described by a position vector $\V{r*

<label id="fig:rigbodor"></label>
 
The first step in the kinematic analysis\index{Kinematic analysis} of a rigid body is to have a unique description of its position and orientation. In planar kinematics, we fully determine the position of a rigid body by fixing the position vectors of 2 points in the rigid body that can be freely chosen, like points $A$ and $B$ of the rectangle in \figref{fig:rigbodor}.

If we know position vectors $\V{r}_A$ and $\V{r}_B$ the position and orientation of the rigid body is fully determined. This requires four coordinates: $x_A, y_A, x_B$ and $y_B$. However, because we know the distance between the points, we can use constraint equation\index{Constraints} \ref{eq:rigbodconstraint} to reduce this to 3 coordinates, namely $x_A, y_A$ and $\phi_{B/A}$, where $\phi_{B/A}$ is the angle\index{Angle} the relative position vector\index{Relative position} $\V{r}_{B/A}$ makes with the $x$-axis\index{Axis}\footnote{Note that with this definition $\phi_{B/A}\ne \phi_B-\phi_A$ in contrast to the definition in \sref{sec:vecmagang}.}. With $x_A, y_A$ we can determine $\V{r}_A$, and with $\phi_{B/A}$ and knowledge of the distance $|\V{r}_{B/A}|$ we can determine $\V{r}_{B/A}$:
\begin{eqnarray}
\label{eq:2Dkinrigbod}
    \V{r}_{A,2D} &=& x_A \ui + y_A \uj \\
    \V{r}_{B/A,2D} &=& |\V{r}_{B/A}|\cos \phi_{B/A} \ui + |\V{r}_{B/A}|\sin \phi_{B/A} \uj
\end{eqnarray}
Now we determine $\V{r}_{B}$ from the 3 coordinates by adding these two vectors as shown in \figref{fig:rigbodor}.
\begin{eqnarray}
\label{eq:rrigbod2D}
    \V{r}_{B}&=&\V{r}_{A} + \V{r}_{B/A} \\
    \V{r}_{B,2D}&=&(x_A+|\V{r}_{B/A}|\cos \phi_{B/A})\ui + (y_A+|\V{r}_{B/A}|\sin \phi_{B/A})\uj
    \label{eq:rrigbod2D2}
\end{eqnarray}

## Velocities in a rigid body

### Afleiding

*Velocity of a point $B$ in a rigid body*
By taking the time derivative\index{Time derivative} of the position vector $\V{r}_{B}$ in \eqref{eq:rrigbod2D}, we can determine the velocity vector\index{Velocity} of point $B$ in the rigid body as follows:

\begin{eqnarray}
\label{eq:vrigbod2D}
    \V{v}_{B,2D}&=&\Dd{}{t} \V{r}_{B} = 
    \Dd{}{t} \V{r}_{A} + \Dd{}{t} \V{r}_{B/A} \\
    &=&\V{v}_A+\dot{\phi}_{B/A}|\V{r}_{B/A}|\left( -\sin \phi_{B/A}\ui + \cos \phi_{B/A}\uj\right) \\
    &=&\V{v}_A+\dot{\phi}_{B/A}|\V{r}_{B/A}| \Vh{\phi}_A \label{eq:vrigbod2Dtot}
\end{eqnarray}

In the last step we used \eqref{eq:vhthcyl} to replace the terms in brackets by $\Vh{\phi}_A$, which represents the unit vector\index{Unit vector} at point $B$ of a cylindrical coordinate system\index{Cylindrical coordinates} with origin $A$, which is why we add the subscript $A$ to the unit vector. The velocity of point $B$ in \eqref{eq:vrigbod2Dtot} can be split up in two parts: a vector $\V{v}_{B,\mathrm{trans}}$ related to translation and a  vector $\V{v}_{B,\mathrm{rot}}$ related to rotation\index{Rotational motion}:

\begin{eqnarray}
\label{eq:vrigbod2D2}
    \V{v}_{B}&=& \V{v}_{B,\mathrm{trans}} + \V{v}_{B,\mathrm{rot}}\\
   \V{v}_{B,\mathrm{trans}}  &=& \V{v}_{A} \\
   \V{v}_{B,\mathrm{rot},2D}  &=& \dot{\phi}_{B/A}|\V{r}_{B/A}| \Vh{\phi}_A \label{eq:vrigbod2D2rot}
\end{eqnarray}

In Figs. \ref{fig:rigbodveltrans}, \ref{fig:rigbodvelrot} and \ref{fig:rigbodvelgen} we show these three velocity vectors $\V{v}_{B,\mathrm{trans}}$,  $\V{v}_{B,\mathrm{rot}}$ and $\V{v}_{B}$. Let us first discuss two special types of rigid body motion\index{Motion}: pure translation\index{Pure translation} and pure rotation\index{Pure rotation}. 

![Pure translation of a rigid body: $\phi_{B/A](Figures/RigidBodVeltrans.pdf)

*Figuur: Pure translation of a rigid body: $\phi_{B/A*

<label id="fig:rigbodveltrans"></label>
 
![Pure rotation of a rigid body: $\V{r](Figures/RigidBodVelrot.pdf)

*Figuur: Pure rotation of a rigid body: $\V{r*

<label id="fig:rigbodvelrot"></label>

![General motion of a rigid body: a combination of rotation and translation.](Figures/RigidBodVelgen.pdf)

*Figuur: General motion of a rigid body: a combination of rotation and translation.*

<label id="fig:rigbodvelgen"></label>

### Pure translation
When the angle $\phi_{B/A}$ is kept constant, like in \figref{fig:rigbodveltrans}, all points in the rigid body move with the same velocity vector:
\begin{equation}
\V{v}_{B}=\V{v}_{B,\mathrm{trans}}=\V{v}_A    
\end{equation}
This type of motion is called \emph{pure translation}.
The rotational component of velocity is zero, as follows from \eqref{eq:vrigbod2D2rot} and $\dot{\phi}_{B/A}$=0. It is important to note that pure translation can happen along any path curve\index{Path curve} $\V{r}_A(s)$, even a circular 
path. The word translation thus only means that the shape of the path is identical for all points in the rigid body because $\phi_{B/A}$ is constant.

### Pure rotation
When the position vector of a point in the rigid body is constant in time, and all other points make circular paths around it, e.g. because it rotates around an axle at that position, the motion of the rigid body is a \emph{pure rotation}.  We choose point $A$ to be the point with constant position vector $\V{r}_A$, as shown in \figref{fig:rigbodvelrot}. Then according to \eqref{eq:vrigbod2D2rot} the velocity vector of point $B$ is given by:
\begin{equation}
\V{v}_{B}=\V{v}_{B,\mathrm{rot},2D}=\dot{\phi}_{B/A}|\V{r}_{B/A}| \Vh{\phi}_A   
\end{equation}
To facilitate the analysis of rotations and generalise it to 3D, we now define the angular velocity\index{Angular velocity} $\omega$ and angular velocity vector $\V{\omega}$.

### Angular velocity of a rigid body

The kinematics\index{Kinematics} of a rigid body is closely linked to the time derivative $\dot{\phi}_{B/A}(t)$, which is defined as its angular velocity.

> **Definitie – Angular velocity of a rigid body**
>
> The time derivative $\dot{\phi}_{B/A}$ is the angular velocity $\omega_\UL{F}$ of the rigid body:
\begin{equation}
    \omega_\UL{} \equiv \dot{\phi}_{B/A}
\end{equation}
The unit of angular velocity is $\unit[]{rad/s}$. Interestingly, the angular velocity $\omega_\UL{F}$ of the rigid body is independent of the choice of the points $A$ and $B$ on the rigid body and is therefore a general property of a rigid body as can be shown as follows.
> **Concept – Independency of angular velocity**
>
> The angular velocity $\omega_\UL{F}$ of a rigid body is independent of the choice of points $A$ and $B$ on the rigid body.
### Afleiding

*This can be proven by drawing two relative position vectors between points $A-D$ on the rigid body, $\V{r}_{B/A}$ and $\V{r}_{D/C}$. Then the angular velocities of these straight lines $\dot{\phi}_{B/A}$ and $\dot{\phi}_{D/C}$ has to be the same, otherwise the rigid body would deform. This can be demonstrated by rotating the rigid body by a full 360 $^\circ$ circle: then all points need to make a circle in the same time and therefore have the same angular velocity.*

 Note that the angular velocity $\omega_\UL{F}$ of a rigid body is different from the \emph{orbital} angular velocity $\omega_{o}$ of a single point mass around an axis. Orbital angular velocity can depend on the position of the rotation axis or origin (\sref{sec:circmotion}). To distinguish angular velocity of a rigid body from orbital angular velocity\index{Orbital angular velocity}, the angular velocity of a rigid body is therefore sometimes called its \emph{spin} angular velocity.

### Angular velocity vector
It can be seen in \figref{fig:rigbodvelrot} that for pure rotation all points in the rigid body move in circular paths around point $A$. The velocity vector $\V{v}_B$ and all other points in the rigid body, lie in the plane of those circles. To describe that plane we define the angular velocity vector to be perpendicular to that plane.

> **Concept – Angular velocity vector**
>
> The angular velocity vector $\V{\omega}_\UL{}$ of a rigid body is a vector with magnitude $|\omega|=|\dot{\phi}_{B/A}|$ and a direction that is perpendicular to the plane in which the rigid body rotates. Its direction can be determined using the right hand rule.
The angular velocity vector (unit $\unit[]{rad/s}$) of a rigid body that rotates in the $xy$ plane is:
\begin{equation}
\label{eq:angvel2D}
    \V{\omega}_{2D}=\omega_\UL{F} \Vh{k} = \dot{\phi}_{B/A} \Vh{k}
\end{equation}
The direction of the vector can be determined using the right-hand rule\index{Right-hand rule} by curving the fingers of your right-hand around the curved arrow in \figref{fig:rigbodvelrot}, which indicates the direction of rotational motion. Then your thumb points in the $\Vh{k}$ direction, in agreement with \eqref{eq:angvel2D}.

### Determining velocities with the angular velocity vector

From \figref{fig:rigbodvelrot} we see that the velocity vector $\V{v}_{B,\mathrm{rot}}$ lies in the plane in which the rigid body moves. It is therefore perpendicular to $\V{\omega}_\UL{F,2D}$. It is also perpendicular to the vector $\V{r}_{B/A}$, since this vector is the radius of the circular motion\index{Circular motion}. To obtain a vector that is perpendicular to two other vectors we take the cross product\index{Cross product} of these vectors:

> **Concept – Rotational velocity equation**
>
> The rotational velocity of a point $B$ in a rigid body is given by:
\begin{equation}
\label{eq:rotvelomega}
    \V{v}_{B,\mathrm{rot}} = \V{\omega}_\UL{F} \times \V{r}_{B/A}
\end{equation} 

For the 2D case, where $\V{\omega}_{2D}=\dot{\phi}_{B/A} \Vh{k}$ and $\V{r}_{B/A}=|\V{r}_{B/A}| \Vh{\rho}_A$, it is straightforward to check the correctness of this equation by comparison with \eqref{eq:vrigbod2D2rot} and by using that $\Vh{k} \times \Vh{\rho}_A = \Vh{\phi}_A$ as follows from the right-hand rule.

### General motion
 In general, as shown in \figref{fig:rigbodvelgen}, the motion of a point in a rigid body is a sum of translational and rotational motion. By combining Eqs. (\ref{eq:vrigbod2D2}) and (\ref{eq:rotvelomega}) we obtain the most general equation and important equation for the velocity in a rigid body:
 \begin{equation}
 \label{eq:geneqrigbodvel}
     \V{v}_{B}= \V{v}_{A} + \V{\omega}_\UL{F} \times \V{r}_{B/A}
 \end{equation}
We note that this equation is valid in 3D and for any choice of the points $A$ and $B$ \emph{as long as both points move along with the rigid body}. However, a smart choice of point $A$ can simplify the analysis.

## Angular acceleration of a rigid body

After having determined the velocity vector of a point in a rigid body, it is now of interest to also determine the acceleration vector\index{Acceleration} of the points in the rigid body. We take the time derivative of \eqref{eq:geneqrigbodvel}, and use the product rule\index{Product rule} on the vector cross product to determine the acceleration vector $\V{a}_{B}$ in a rigid body.
\begin{eqnarray}
\label{eq:rbacceleration}
    \Dd{}{t} \V{v}_{B}&=&\Dd{}{t} \V{v}_{A} + \Dd{\V{\omega}_\UL{F}}{t} \times \V{r}_{B/A} + \V{\omega}_\UL{F} \times \Dd{\V{r}_{B/A}}{t} \\
    \label{eq:rbacceleration2}
    \V{a}_{B} &=& \V{a}_{A} + \V{\alpha}_\UL{F} \times \V{r}_{B/A} + \V{\omega}_\UL{F} \times \V{v}_{B,\mathrm{rot}}
\end{eqnarray}
In this derivation we used that $\Dd{\V{r}_{B/A}}{t}=\V{v}_{B,\mathrm{rot}}$ as follows from \eqref{eq:vrigbod2D} and \eqref{eq:vrigbod2D2}, and defined the angular acceleration vector\index{Angular acceleration} $\V{\alpha}_\UL{F}$ of the rigid body as follows. 

![Acceleration components in a rigid body. The acceleration vector $\V{a](Figures/RigidBodAccgen2.pdf)

*Figuur: Acceleration components in a rigid body. The acceleration vector $\V{a*

<label id="fig:rigbodaccgen"></label>

> **Definitie – Angular acceleration vector**
>
> The angular acceleration vector $\V{\alpha}$ of a rigid body is the time derivative of its angular velocity vector.
\begin{equation}
    \V{\alpha}_{\UL{F}} \equiv  \Dd{\V{\omega}_\UL{F}}{t}
\end{equation}
We note that in planar kinematics this expression can be simplified:
\begin{equation}
    \V{\alpha}_{\UL{F}2D} = \dot{\omega}_{\UL{F}}\Vh{k}=\alpha_{\UL{F}} \Vh{k}
\end{equation}
The unit of angular acceleration is $\unit[]{rad/s^2}$. We now substitute \eqref{eq:rotvelomega} in \eqref{eq:rbacceleration2} and obtain the general expression for the acceleration.
\newpage
> **Concept – Acceleration vector in a rigid body**
>
> The general vector expression for the acceleration vector of a point $B$ in a rigid body that has translational and rotational acceleration:
\begin{equation}    
\V{a}_{B} = \V{a}_{A} + \V{\alpha}_\UL{F} \times \V{r}_{B/A} + \V{\omega}_\UL{F} \times (\V{\omega}_\UL{F} \times \V{r}_{B/A})
\label{eq:accvecrigbod}
\end{equation}

This equation shows that the acceleration of a point $B$ on a rigid body consists of three contributions that are shown in \figref{fig:rigbodaccgen}.

\begin{enumerate}
    \item The translational acceleration $\V{a}_{B,
\mathrm{trans}}=\V{a}_{A}$ due to the acceleration of point $A$.
    \item The angular acceleration $\V{a}_{B,
\mathrm{ang}}=\V{\alpha}_\UL{F} \times \V{r}_{B/A}$ due to the angular acceleration vector.
\item The centripetal acceleration $\V{a}_{B,
\mathrm{cptl}}=\V{\omega}_\UL{F} \times (\V{\omega}_\UL{F} \times \V{r}_{B/A})$, due to the angular velocity vector $\V{\omega}_\UL{F}$.
\end{enumerate}

\subsubsection{Acceleration in planar kinematics}

In planar kinematics\index{Planar kinematics} we can simplify the expressions for the angular acceleration somewhat. By using that $\V{\alpha}_\UL{F,2D}=\alpha_\UL{F} \Vh{k}$ we find:

\begin{equation}
    \V{a}_{B,\mathrm{ang,2D}}=\V{\alpha}_\UL{F} \times \V{r}_{B/A}=\alpha_\UL{F} \Vh{k} \times |\V{r}_{B/A}|\Vh{\rho}_A = \alpha_\UL{F} |\V{r}_{B/A}| \Vh{\phi}_A
\end{equation}

The vector $\V{\omega}$ is always perpendicular to the $xy$\nobreakdash-plane, such that $\V{\omega}_\UL{F} \times \V{r}_{B/A}=\omega_\UL{F}|\V{r}_{B/A}|\Vh{\phi}_A$ and:

\begin{equation}
    \V{a}_{B,\mathrm{cptl,2D}} =\V{\omega}_\UL{F} \times (\V{\omega}_\UL{F} \times \V{r}_{B/A})=-{\omega}^2 \V{r}_{B/A}
\end{equation}

This shows that the centripetal component of acceleration always points towards point $A$, the centre of rotation. Note that a similar result for the centripetal acceleration term was obtained in \eqref{eq:centripetal}. Combining the three terms we obtain for the planar kinematics of a rigid body\index{Rigid body} the following equation:
\begin{equation}
    \V{a}_{B,2D} = \V{a}_{A} + \alpha_\UL{F} |\V{r}_{B/A}| \Vh{\phi} - {\omega}^2 \V{r}_{B/A}
\end{equation}

For completeness we repeat the most important equations for analysing the kinematics of a rigid body:

\begin{eqnarray}
    \label{eq:velrotrbfinal}
    \V{v}_B &=& \V{v}_{A} + \V{\omega}_\UL{F} \times \V{r}_{B/A} \\
    \V{a}_B &=& \V{a}_{A} + \V{\alpha}_\UL{F} \times \V{r}_{B/A}   + \V{\omega}_\UL{F} \times \left(\V{\omega}_\UL{F} \times \V{r}_{B/A}\right) \label{eq:accrotrbfinal}\\
    \V{v}_{B,2D} &=& \V{v}_{A} + \omega_\UL{F}|\V{r}_{B/A}|\Vh{\phi}_A \\
    \label{eq:a2drigbody}
    \V{a}_{B,2D} &=&  \V{a}_{A} + \alpha_\UL{F} |\V{r}_{B/A}|\Vh{\phi}_A  - \omega^2_\UL{F} \V{r}_{B/A}  
\end{eqnarray}


\begin{prex}[eo]
\label{ex:fallingsquare}
As an example of the kinematic methods for rigid bodies, consider the square $F$ in \figref{fig:rigbodex}. The \cm{} of the square falls with a velocity $\V{v}_G=-1 ~\uj~\unit[]{m/s}$ and acceleration $\V{a}_G=-1~ \uj~\unit[]{m/s^2}$. At the same time the angular velocity and acceleration of the square are $\V{\omega}_\UL{F}=1 ~\uk~\unit[]{rad/s}$ and $\V{\alpha}_\UL{F}=1 ~\uk~\unit[]{rad/s^2}$. The question is: \emph{Determine the velocity and acceleration vectors of point $B$.}

To solve this problem, we can use Eqs. (\ref{eq:velrotrb}) and (\ref{eq:accrotrb}). Instead of point $A$ we choose point $G$ as reference point, because we have a lot of information on $G$. Then we determine the vector $\V{r}_{B/G}=(3.5\ui -0.5\uj) \unit[]{m}$ from the figure. Now we use \eqref{eq:velrotrb} to obtain:
\begin{eqnarray}
    \V{v}_B &=& [-1\uj +1\uk \times (3.5\ui -0.5\uj)] ~\unit[]{m/s} \\
     &=& (0.5\ui + 2.5\uj) ~\unit[]{m/s}
\end{eqnarray}

And using \eqref{eq:accrotrb} we obtain:
\begin{eqnarray}
    \V{a}_B &=& [-1\uj +1\uk \times (3.5\ui -0.5\uj)- 1^2 (3.5\ui - 0.5\uj)] ~\unit[]{m/s^2} \\
     &=& [(0.5\ui + 2.5\uj) - 1 (3.5\ui - 0.5\uj)] ~\unit[]{m/s^2} \\
     &=& (-3\ui + 3\uj) ~\unit[]{m/s^2}
\end{eqnarray}
\end{prex}

![Example \ref{ex:fallingsquare](Figures/RigidBodRotEx.pdf)

*Figuur: Example \ref{ex:fallingsquare*

<label id="fig:rigbodex"></label>
