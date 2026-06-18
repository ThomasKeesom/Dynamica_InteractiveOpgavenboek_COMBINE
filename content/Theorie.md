# Theorie: Rigid bodies

After having discussed dynamics of point masses, we now turn to the analysis of rigid bodies.  
In this textbook we focus on the planar kinematics of rigid bodies in the $xy$-plane. 
That means that the point masses in the rigid body all move in the  $xy$\nobreakdash-plane with $z=0$. 
However, we note that much of the presented theory is also applicable in 3D and unless explicitly indicated, 
e.g. with a subscript $_{2D}$, the equations in this chapter are also valid in 3D.

'''{card} Rigid body
:header: **Concept**

A rigid body is an object that is undeformable.
'''

Every point mass $m_i$ in the rigid body can be identified by a position vector $\V{r}_{i}$. Since the body is rigid and undeformable, the distance between every two point masses in the rigid body is constant which relates their dynamics by the following \emph{relative constraint equation}:
$$ |\V{r}_{i/j}| = |\V{r}_{i}-\V{r}_{j}| = \mathrm{~constant} $$ (eq:rigbodconstraint)
In the next section we discuss how the orientation and position of a rigid body can be specified.

## Orientation and position

[Figure 1?]
 
The first step in the kinematic analysis of a rigid body is to have a unique description of its position and orientation. In planar kinematics, we fully determine the position of a rigid body by fixing the position vectors of 2 points in the rigid body that can be freely chosen, like points $A$ and $B$ of the rectangle in \figref{fig:rigbodor}.

If we know position vectors $\V{r}_A$ and $\V{r}_B$ the position and orientation of the rigid body is fully determined. This requires four coordinates: $x_A, y_A, x_B$ and $y_B$. However, because we know the distance between the points, we can use constraint equation\index{Constraints} \ref{eq:rigbodconstraint} to reduce this to 3 coordinates, namely $x_A, y_A$ and $\phi_{B/A}$, where $\phi_{B/A}$ is the angle\index{Angle} the relative position vector\index{Relative position} $\V{r}_{B/A}$ makes with the $x$-axis\index{Axis}\footnote{Note that with this definition $\phi_{B/A}\ne \phi_B-\phi_A$ in contrast to the definition in \sref{sec:vecmagang}.}. With $x_A, y_A$ we can determine $\V{r}_A$, and with $\phi_{B/A}$ and knowledge of the distance $|\V{r}_{B/A}|$ we can determine $\V{r}_{B/A}$:

    $$\V{r}_{A,2D} &=& x_A \ui + y_A \uj$$
    $$\V{r}_{B/A,2D} &=& |\V{r}_{B/A}|\cos \phi_{B/A} \ui + |\V{r}_{B/A}|\sin \phi_{B/A} \uj$$

Now we determine $\V{r}_{B}$ from the 3 coordinates by adding these two vectors as shown in \figref{fig:rigbodor}.

    $$\V{r}_{B}&=&\V{r}_{A} + \V{r}_{B/A} $$
    $$\V{r}_{B,2D}&=&(x_A+|\V{r}_{B/A}|\cos \phi_{B/A})\ui + (y_A+|\V{r}_{B/A}|\sin \phi_{B/A})\uj (eq:rrigbod2D2)$$
    
## General motion

 In general, as shown in \figref{fig:rigbodvelgen}, the motion of a point in a rigid body is a sum of translational and rotational motion. By combining these respective equation terms, we obtain the most general equation and important equation for the velocity in a rigid body:

$$\V{v}_{B}= \V{v}_{A} + \V{\omega}_\UL{F} \times \V{r}_{B/A} (eq:geneqrigbodvel)$$

We note that this equation is valid in 3D and for any choice of the points $A$ and $B$ \emph{as long as both points move along with the rigid body}. However, a smart choice of point $A$ can simplify the analysis.

## Angular acceleration of a rigid body
'''{card}  Acceleration vector in a rigid body
:header: **Concept**

The general vector expression for the acceleration vector of a point $B$ in a rigid body that has translational and rotational acceleration:
'''
   
$$\V{a}_{B} = \V{a}_{A} + \V{\alpha}_\UL{F} \times \V{r}_{B/A} + \V{\omega}_\UL{F} \times (\V{\omega}_\UL{F} \times \V{r}_{B/A}) (eq:accvecrigbod) $$

This equation shows that the acceleration of a point $B$ on a rigid body consists of three contributions.
