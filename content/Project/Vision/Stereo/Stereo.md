---
title: Stereo Vision
alias: Stereo Vision
---

## Backward Projection

- Can we obtain 3D information from an image?

> [!info]- 3D to 2D
> 
> $$
> \begin{align*}
>   u = f_{x} = \frac{x}{z} + p_{x}\\ \\
>   v = f_{y} = \frac{y}{z} + p_{y}
> \end{align*}
> $$

> [!info]- 2D to 3D
> 
> $$
> \begin{gather*}
>   x = \frac{z}{f_{x}} (u - p_{x})\\ \\
>   y = \frac{z}{f_{y}} (v - p_{y})\\ \\
>   z > 0
> \end{gather*}
> $$

---

## Stereo Vision

> [!abstract] Basic Principle: Triangulation
> 
> - Gives reconstruction as intersection of two rays
> 
> > [!check] Requirements
> > 
> > - Camera calibration
> > - Correspondence

> [!NOTE] Stereo Image Rectification
> 
> - Reproject image planes onto a common plane parallel to the line between optical centers
> 
> $$
> \begin{matrix}
>   \displaystyle u_{l} = f_{x} \frac{x}{z} + p_{x} & \hspace{2cm} & \displaystyle u_{r} = f_{x} \frac{x - b}{z} + p_{x} \\ \\
>   \displaystyle v_{l} = f_{y} \frac{y}{z} + p_{y} & \hspace{2cm} & \displaystyle v_{r} = f_{y} \frac{y}{z} + p_{y}
> \end{matrix}
> $$

> [!NOTE] Depth & Disparity
> 
> - Depth is inversely proportional to Disparity
> - For the same depth, Disparity is proportional to Baseline
> 
> > [!cite]- 1
> > 
> > $$
> > \begin{matrix}
> >   \displaystyle v_{l} = f_{y} \frac{y}{z} + p_{y} & \hspace{1cm} & \displaystyle v_{r} = f_{y} \frac{y}{z} + p_{y} \\ \\
> >   \searrow & & \swarrow \\
> >   & v_{l} = v_{r}
> > \end{matrix}
> > $$
> 
> > [!cite]- 2
> > 
> > $$
> > \begin{matrix}
> >   \displaystyle u_{l} = f_{x} \frac{x}{z} + p_{x} & \hspace{1cm} & \displaystyle u_{r} = f_{x} \frac{x - b}{z} + p_{x} \\ \\
> >   \searrow & & \swarrow
> > \end{matrix}
> > $$
> > 
> > $$
> > \begin{matrix}
> >   \displaystyle u_{l} - u_{r} = \frac{f_{x}}{z} (x - (x - b)) = \frac{f_{x}}{z} b \\ \\
> >   \displaystyle z = \frac{f_{x} b}{u_{l} - u_{r}}, \quad \begin{align*} & \footnotesize z : \textsf{Depth} \\ & \footnotesize u_{l} - u_{r} : \textsf{Disparity} \end{align*}
> > \end{matrix}
> > $$

> [!NOTE] Depth and Disparity in Your Eyes!
