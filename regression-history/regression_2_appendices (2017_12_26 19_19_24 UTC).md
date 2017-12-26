# Appendix A
Proof that the solution to
$$
\min_{f(X_i)} E[u_i^2] \leftrightarrow \min_{f(X_i)} E[(Y_i-f(X_i))^2]
$$
is  $f(X_i)=E[Y_i \mid X_i]$. $$\square$$ Taking the first-order condition:
$$
\begin{aligned}
 \frac{d E[(Y_i-f(X_i))^2]}{df(X_i)} &=0 \\ E[\frac{d (Y_i-f(X_i))^2}{df(X_i)}] &=0 \\ E[\frac{Y_i^2 -2Y_if(X_i)+f(X_i)^2}{df(X_i)}] &= 0 \\ E[-2Y_i+2f(X_i)] &=0 \\ E[-2Y_i+2f(X_i) \mid X_i] &=0 \\ -2E[Y_i \mid X_i] + 2f(X_i) &=0 \\ f(X_i) &= E[Y_i \mid X_i] \qquad \blacksquare
\end{aligned}
$$


# Appendix B
Proof that the solution to
$$$
\min_{\beta_0, \beta_1} E[(e_i + u_i)^2] \leftrightarrow \min_{\beta_0, \beta_1} E[(Y_i  - \beta_0 -\beta_1 X_i)^2] 
$$$

is 
$$
\begin{aligned}
\beta_0 &= \bar{y}- \beta_1\bar{x} \\
\beta_1 &= \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2}
\end{aligned}
$$
$\square$ Let
$$
L = \sum_{i=1}^n (y_i - \beta_1 - \beta_2 x_i)^2
$$
<div style="page-break-after: always;"></div>


We solve:
$$
\begin{aligned}
&\min_{\beta_1, \beta_2} L \\
&\leftrightarrow 

\begin{cases}
\frac{dL}{d \beta_1} =0 \qquad \text{Call this }(a) \\

\frac{dL}{d \beta_2} =0 \qquad \text{Call this }(b)
\end{cases} \\

&\leftrightarrow \begin{cases}
\sum_{i=1}^n(\frac{d(y_i-\beta_1-\beta_2x_i)^2}{d \beta_1}) =0 \qquad \qquad \text{derivative of a sum}\\
(b)\end{cases} \\

&\leftrightarrow \begin{cases}\sum_{i=1}^n-2(y_i-\beta_1-\beta_2x_i) =0 \\

(b)\end{cases}\\&\leftrightarrow \begin{cases}\beta_1 = \bar{y} - \beta_2\bar{x} \\

(b)\end{cases}\\\\ \\

&\leftrightarrow \begin{cases}(a) \\

 \sum_{i=1}^n(\frac{d(y_i-\beta_1-\beta_2x_i)^2}{d \beta_2}) =0 \qquad \qquad \text{derivative of a sum}\end{cases} \\

 &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n-2x_i(y_i-\beta_1-\beta_2x_i) =0\end{cases} \\

 &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n-2x_i(y_i-\bar{y}+\beta_2\bar{x}-\beta_2x_i) =0 \qquad \qquad \text{substitute }\beta_1
 
 \end{cases} \\
 
  &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n x_i(y_i-\bar{y}+\beta_2\bar{x}-\beta_2x_i) =0\qquad \qquad \text{divide by -2}\end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n x_i(y_i-\bar{y}) +\sum_{i=1}^n \beta_2 x_i(\bar{x} - x_i) =0 \qquad \qquad \text{rearrange}\end{cases} \\
 
 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n x_i(y_i-\bar{y}) =\sum_{i=1}^n \beta_2 x_i(x_i - \bar{x}) \qquad \qquad \text{rearrange}\end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n (x_i-\bar{x})(y_i-\bar{y}) =\sum_{i=1}^n \beta_2 (x_i - \bar{x})^2 \qquad \qquad \text{by fact A} \end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

           \beta_2  = \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \qquad \qquad \text{rearrange}\end{cases}


          \\ \\

          &\leftrightarrow \begin{cases}\beta_1 = \bar{y} - \beta_2\bar{x} \\

           \beta_2  = \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \end{cases}
\end{aligned}
$$

Thus we write:
$$
\begin{aligned} \hat{\beta_1} &= \bar{y} - \hat{\beta_2}\bar{x} \\

 \hat{\beta_2}  &= \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \ \ \blacksquare \end{aligned}
$$

Fact A is proven here:
$$
\begin{aligned}
\sum_{i=1}^n (x_i-\bar{x})(y_i-\bar{y}) &= 
\sum_{i=1}^n(x_iy_i - x_i\bar{y} -\bar{x}y_i +\bar{x}\bar{y})  \\
&= \sum_{i=1}^n(x_iy_i) -\bar{y}\sum_{i=1}^n(x_i) -  \bar{x}\sum_{i=1}^n(y_i) + n\bar{x}\bar{y} \\
&= \sum_{i=1}^n(x_iy_i) -n\bar{y}\bar{x} - n\bar{y}\bar{x} + n\bar{x}\bar{y} \\
&= \sum_{i=1}^n(x_iy_i) -n\bar{y}\bar{x}  \\

&= \sum_{i=1}^n(x_iy_i) -\sum_{i=1}^ny_i\bar{x} & &= \sum_{i=1}^n(x_iy_i) -\sum_{i=1}^nx_i\bar{y}  \\

&= \sum_{i=1}^n y_i(x_i-\bar{x}) \qquad\text{factorise y\_i} & &= \sum_{i=1}^n x_i(y_i-\bar{y}) \qquad\text{factorise x\_i}\\
\end{aligned}
$$

A special case of fact A is:
$$
\sum_{i=1}^n (x_i-\bar{x})^2 =\sum_{i=1}^n x_i(x_i-\bar{x})
$$

# Appendix C
Proof that
$$
\begin{aligned}
\min_{\beta} U'U
& \leftrightarrow \beta = (X'X)^{-1} X'Y \\
\end{aligned}
$$
Where
$$
Y=X\beta+U
$$

and where
$$
Y = \begin{bmatrix}
  y_1 \\
  y_2 \\
  \vdots \\
  y_n
\end{bmatrix}
\qquad
X = \begin{bmatrix}
  1& x_{1,1} & x_{2,1} & \cdots & x_{K,1}\\
  1& x_{1,2} & x_{2,2} & \cdots & x_{K,2}\\
  \vdots &\vdots & \vdots & \ddots & \vdots \\
  1& x_{1,n} & x_{2,n} & \cdots & x_{K,n}
\end{bmatrix}
$$

$$
\beta= \begin{bmatrix}  \beta_0 & \beta_1 & \cdots & \beta_K \end{bmatrix}^T=\begin{bmatrix}
  \beta_0 \\
  \beta_1  \\
  \vdots \\
  \beta_K 
\end{bmatrix}

\qquad

U=\begin{bmatrix}
  u_1 \\
  u_2 \\
  \vdots \\
  u_n
\end{bmatrix}
$$

$\square$ Then
$$
U'U = \begin{bmatrix}  \sum_{i=1}^n u_i u_i
      \end{bmatrix} = SSR
$$

We can also write:
$$
\begin{aligned}
U'U &= (Y-X\beta)'(Y-X\beta) \\
&= (Y' -(X\beta)')(Y-X\beta) \\
&= Y'Y - Y'X\beta -(X\beta)'Y  +(X\beta)'(X\beta) \\
&= Y'Y - ((X\beta)'Y)' -(X\beta)'Y + \beta'X'X\beta \\
\end{aligned}
$$
Since $(X\beta)'Y$ is a scalar, it is equal to its transpose $Y'X\beta$. Thus:
$$
\begin{aligned}
U'U&= Y'Y -2Y'X\beta + \beta'X'X\beta
\end{aligned}
$$


We then solve:
$$
\begin{aligned}
\min_{\beta} U'U &\leftrightarrow 

\frac{dU'U}{d\beta}=0\\
& \leftrightarrow

\frac{dY'Y }{d\beta} -2\frac{d\ Y'X\beta}{d\beta}+ \frac{d\beta'X'X\beta}{d\beta} =0 \\
& \leftrightarrow 
0 -2(Y'X)' + (X'X+(X'X)')\beta =0 \\
& \leftrightarrow 
-2X'Y + 2X'X\beta =0 \\


& \leftrightarrow 
X'X\beta = X'Y \\
\end{aligned}
$$
Assuming that $X'X$ is invertible (since it's a square matrix, this is equivalent to $det(X'X)\neq0$), we have:
$$
\begin{aligned}
\min_{\beta} U'U
& \leftrightarrow \beta = (X'X)^{-1} X'Y  \ \ \blacksquare \\
\end{aligned} 
$$
