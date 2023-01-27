---
layout: default_math
---

Using neural networks to solve PDEs. 

Learning to Accelerate Partial Differential Equations via Latent Global Evolution 
Wu, Maruyama, Leskovec

Latent Vector 
* There is a latent vector $z^k$ at each time step $k$. 
* The dimension of the latent vector is $d_z$, which does not depend on the time step $k$. (So the dimension of the latent vector is the same at each time step).
* The latent vector $$z^k$$ presumably has much lower dimension than the original vector $$U^k$$. The original vector has one component for each cell.  
Encoding 
* The function $q$ maps the original vector $U^k$ to the latent vector $z^k$. 
* So $$q$$ performs dimension reduction. 
* There are many methods of dimension reduction, such as PCA. 
* Neural network encoders are one among many methods of dimension reduction. 
* When we reduce the dimension, there is usually some property that we want to preserve. In this case the property is that we want to be able to recover the solution to the original PDE. 
