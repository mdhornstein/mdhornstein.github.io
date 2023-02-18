--- 
layout: default_math 
--- 

If you evaluate the fitted regression model at the average 

The design matrix is $$X \in \mathbb{R}^{n \times p}$$. 

$$
\begin{align*}
\overline{X}^T \widehat{\beta} &= \left(\frac{1}{n} 1_n^T X \right) \left( (X^T X)^{-1} X^T Y \right) \\
&= \frac{1}{n} 1_n^T X(X^T X)^{-1} X^T Y \\
&= \frac{1}{n} 1_n^T PY \\
&= \frac{1}{n} \sum_{i = 1}^n \widehat{Y}
\end{align*}
$$

That property has nothing to do with least squares. It's just a property of lines. If you have points $$(x_1, y_1), (x_2, y_2), \ldots, (x_n, y_n)$$ on a line $y = ax + b$, then if you evaluate the line at the average x-value $$\overline{x}$$, the result is the average y-value $$\overline{y}$$, 

$$
\begin{align*}
\overline{x} + b &= a \left( \frac{1}{n} x_n \right) + b \\
&= \frac{1}{n} \sum_{i = 1}^n \left( ax_i + b \right) \\
&= \frac{1}{n} \sum_{i = 1}^n y_i \\
&= \overline{y}
\end{align*}
$$

So this is *purely* because of linearity of expectation. It has nothing to do with least squares. When we say that the regression line passes through $$(\overline{x}, \overline{y})$$, I had always assumed that this is a property of the fitted regression line, but it is actually true of *any* line. It's because of linearity of expectation. If you average the x's then look at the y-value, it's the same as if you averaged the y-value. For a convex function, we would have that the function passes *below* $$(\overline{x}, \overline{y})$$ by the definition of convexity (the function evaluated at a convex combo of x-values is less than the corresponding convex combo of y-values). I had never seen the connection before between this and convexity. 

If $X$ is random, then $P$ is a random matrix. 
$$
\begin{align*}
\text{Var}\left( \overline{X}^T \widehat{\beta} \right) &= \text{Var}\left( \frac{1}{n} 1_n^T PY  \right) \\
&= 
\end{align*}
$$ 