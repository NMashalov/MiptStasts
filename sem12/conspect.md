# Нейронные сети

Биологические примеры составляющие:
- Синопсисы
- Нейроны

Опыт, обучающие данные -> Нейронная -> Разрешение сложных задач

Модель нейрона:

Набор признаков $X=(X_1,...,X_d)^T \in \mathbf{R}^d$

Веса признаков $\omega = (\omega_1,..,\omega_d)^T \in \mathbf{R}^d$ - weights

Cмещение$b \in \mathbf{R}$ - /bias

Перцентрон: 

$x_1 -> w_1$ 

$x_i - > w_i$  -> $\Sigma$ _> $\sigma$ -> $y(x)$

$x_n -> w_n$ 

Выход нейрона:
$y(x) = \sigma((X,\omega) + b)$ - аналогично логистической и линейной регрессии 

$\sigma$ -функция активации, кусочно-дифференцируемая

# Однослойная полносвязная нейронная сеть:

$x_1$ -> $y_1$

$x_i$ -> ...  

$x_d$ -> $y_h$

$x = (x_1,...,x_d)$
$b = (b_1,...,b_H)$

$$W = \begin{pmatrix}
w_{11} & ... & w_{1n} \\
...\\
w_{d1} &. .. & w_{dn} \\
\end{pmatrix}$$

$y = \sigma(X^TW + b)$


Можем добавлять слои:

$H$ Нейронов -> $M$ нейронов -> y

$y=\sigma(\sigma(X^TW+b^T)W'+b^T)$

Опр: $\simga(z)$ - называется сигмоидой, еслиÖ


$$\lim_{z \xrightarrow{} -\infty}\sigma_z =0,\lim_{z \xrightarrow{} +\infty}\sigma_z =1$$


# Theorem (Цыбенко)

Если $\sigma(z)$ - непрерывная сигмоида, то $\forall$ непрерывна на $[0,1]^d$ функции f(x) $\exists$ H, $w_h \in R^d$, $w_h^1 \in R^d$

$$y=\sigma(\sigma(X^TW+b^T)W'+b^T)$$

равномерно приближает $f(x)$ с любой точностью, т.е. $|y(x)-f(x)|< \varepsilon$ $\forall \varepsilon \forall x \in [0,1]^d$ 


Минус теоремы. Нет ограничения на H :(

# Как искать параметры

$L(x)$ - ошибка модели -> $min_{\omega,b}$

Градиентный спуск:

Модель - $y^1=\sigma^1(\sigma(X^TW+b^T)W^1+(b^1)^T)$

MSE: $L = \frac{1}{n} \sum_{i=1}^n (\hat{y}_i-y_i)^2$

-> $\Theta_{k,t} = \Theta_{k,t-1} - \eta \nabla L(\Theta_{k,t-1})$














