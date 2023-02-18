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

Let's guess how they train the neural network. 
* What is the training data? What is the loss function?  
* For an autoencoder, the forward pass involves applying the encoder then the decoder. The loss function compares the reconstructd output to the original output. When we optimize the loss function, we find parameter values that tend to make the reconstructed output similar to the original output. 
    * Let's think about what would happen if you used linear functions to encode and decode. Then think about what the advantage is and limitations if you use nonlinear functions. 
* For a differential equation, do we want the solution to be accurate at every time step, or do we only care whether it is accurate in the final time step?  If we care about accuracy at every time step, the loss function can compare the reconstructed output to the "true" output at each time step, where the "true" output comes from finite differences. Something like this $$\sum_{n = 1}^N \sum_{k = 1}^K \lVert \mathcal{U}^{k} - g^{(k)}(U^0_{(n)}  \rVert $$, where 
* One option is that the training data is $$\{(U^k, z^k)_k\}$$.  