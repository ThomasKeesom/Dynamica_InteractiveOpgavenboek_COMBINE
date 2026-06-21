## Rigid bodies

After having discussed dynamics of point masses, we now turn to the analysis of rigid bodies.  In this lecture we focus on the planar kinematics of rigid bodies in the $xy$-plane. That means that the point masses in the rigid body all move in the  $xy$-plane with $z=0$. However, we note that much of the presented theory is also applicable in 3D and unless explicitly indicated, e.g. with a subscript $_{2D}$, the equations in this lecture are also valid in 3D.

```{card} Rigid Body
:header: Concept
:footer: footer

A rigid body is an object that is undeformable.
```
Every point mass $m_i$ in the rigid body can be identified by a position vector $r_{i}$. Since the body is rigid and undeformable, the distance between every two point masses in the rigid body is constant which relates their dynamics by the following relative constraint equation:

$$
    |\vec{r}_{i/j}| = |\vec{r}_{i}-\vec{r}_{j}| = \mathrm{~constant} 
$$

In the next section we discuss how the orientation and position of a rigid body can be specified.

## Orientation and position

![](figures/RIGIDB~4.PDF)

```{figure} Figures/RIGIDB~4.PDF
:label: eq:rigbodconstraint
:width: 70%
:align: center

A sketch of a rigib body with important variables
```

*Figuur: The orientation of a rigid body in the 2D xy-plane can uniquely be described by a position vector r.*

<!-- fig:rigbodor -->

The first step in the kinematic analysis of a rigid body is to have a unique description of its position and orientation. In planar kinematics, we fully determine the position of a rigid body by fixing the position vectors of 2 points in the rigid body that can be freely chosen, like points $A$ and $B$ of the rectangle in Figure 1.

If we know position vectors $r_{A}$ and $r_{B}$ the position and orientation of the rigid body is fully determined. This requires four coordinates: $x_{A}$, $y_{A}$, $x_{B}$ and $y_{B}$. However, because we know the distance between the points, we can use constraint equation (eq:rigbodconstraint) to reduce this to 3 coordinates, namely $x_{A}$, $y_{A}$ and $\phi_{B/A}$, where $\phi_{B/A}$ is the angle the relative position vector $r_{B/A}$ makes with the $x$-axis. With $x_{A}, y_{A}$ we can determine $r_{A}$, and with $\phi_{B/A}$ and knowledge of the distance $|r_{B/A}|$ we can determine $r_{B/A}$:

$$
\begin{aligned}
% label: eq:2Dkinrigbod
    \vec{r}_{A,2D} = x_A \hat{i} + y_A \hat{j} \\
    \vec{r}_{B/A,2D} = |\vec{r}_{B/A}|\cos \phi_{B/A} \hat{i} + |\vec{r}_{B/A}|\sin \phi_{B/A} \hat{j}
\end{aligned}
$$

Now we determine $\vec{r}_{B}$ from the 3 coordinates by adding these two vectors as shown in \figref{fig:rigbodor}.

$$
\begin{aligned}
% label: eq:rrigbod2D
    \vec{r}_{B}=\vec{r}_{A} + \vec{r}_{B/A} \\
    \vec{r}_{B,2D}=(x_A+|\vec{r}_{B/A}|\cos \phi_{B/A})\hat{i} + (y_A+|\vec{r}_{B/A}|\sin \phi_{B/A})\hat{j}
    % label: eq:rrigbod2D2
\end{aligned}
$$


## Velocities in a rigid body
 In general, the motion of a point in a rigid body is a sum of translational and rotational motion. By combining their respective equations, we obtain the most general equation and important equation for the velocity in a rigid body:
 
$$
% label: eq:geneqrigbodvel
     \vec{v}_{B}= \vec{v}_{A} + \vec{\omega} \times \vec{r}_{B/A}
$$

We note that this equation is valid in 3D and for any choice of the points $A$ and $B$ as long as both points move along with the rigid body. However, a smart choice of point $A$ can simplify the analysis.

## Angular acceleration of a rigid body

After having determined the velocity vector of a point in a rigid body, it is now of interest to also determine the acceleration vector of the points in the rigid body. We take the time derivative of $v_{B}$, and use the product rule on the vector cross product to determine the acceleration vector $\vec{a}_{B}$ in a rigid body.

![](figures/RI6CDF~1.PDF)

*Figuur: Acceleration components in a rigid body. The acceleration vector a.*

<!-- fig:rigbodaccgen -->

The unit of angular acceleration is $rad/s^2$. We substitute in $\omega \times r_{B/A}$ for the left over rotational velocity term and obtain the general expression for the acceleration.

$$
\vec{a}_{B} = \vec{a}_{A} + \vec{\alpha} \times \vec{r}_{B/A} + \vec{\omega} \times (\vec{\omega} \times \vec{r}_{B/A})
% label: eq:accvecrigbod
$$

This equation shows that the acceleration of a point $B$ on a rigid body consists of three contributions that are shown in Figure 2: translational, angular and centriputal acceleration.






