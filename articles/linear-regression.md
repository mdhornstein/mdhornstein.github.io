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

If $$X$$ is random, then $$P$$ is a random matrix, and $$PY$$ is a random vector. Since $$Y = X\beta + \varepsilon$, we have $$PY = P(X\beta + \varepsilon) = X\beta + P\varepsilon$$, where $$X$$ and $$\varepsilon$$ are independent. Therefore $$\text{Var}\left(PY \right) = \text{Var}\left(X\beta + \varepsilon \right) = \beta^T A \beta + \text{Var}\left( P \varepsilon \right)$$. 

Suppose we want to calculate $\text{Var}(AB)$, where $A$ and $B$ are independent scalar random variables. Then 


$$
\begin{align*}
\text{Var}\left( \overline{X}^T \widehat{\beta} \right) &= \text{Var}\left( \frac{1}{n} 1_n^T PY  \right) \\
&= \frac{1}{n^2} 1_n^T \text{Var}\left( PY \right) 1_n \\
&= 
\end{align*}
$$ 

Suppose we want to estimate the population mean, and we have a regression model (todo: cite Stanford notes, and see if we can find some other references)

If you look at a scatterplot, it's visually obvious that the fitted values vary less than the raw y-values. The fitted values are confined to the line, whereas the raw values are above and below the line. 

The raw y-values are $$X\beta + \varepsilon$$, and the fitted values are $$X \widehat{\beta}$$. 

$$
\begin{align*}
\text{Var}(PY) &= E\left[ \text{Var}(PY \mid P) \right] + \text{Var}\left( E\left[ PY \mid P \right] \right) \\
&= E\left[ \sigma^2 P \right] + \text{Var}\left( \right)
\end{align*}
$$