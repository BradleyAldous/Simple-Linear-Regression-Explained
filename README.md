# Under the hood of Simple Linear Regression

Simple linear regression is a method used to estimate the relationship between two continuous (quantative) variables; one independent variable, $x$, and one dependent variable, $y$, using a straight line. This linear model follows an equation of style, $y_i = \alpha x_i + \beta + \epsilon_i$, where $\beta$ is the intercept (the value of $y_i$ when $x_i$ is 0), $\alpha$ is the regression coefficient (and determines the slope of the regression line), and $\epsilon_i$ is the difference between the actual and predicted values of $y$.

The regression line will pass through the point comprised of the mean values for $x$ and $y$.**

1. Firstly, we calculate the means, $\bar x$ and $\bar y$ of all $x$ and $y$ values.

2. Then we can calculate the difference of each value from its corresponding mean value, ($x-\bar x$) and ($y-\bar y$).

3. After this, we calculate $(x-\bar x)^2$ and $(x-\bar x)\cdot(y-\bar y)$.

4. Work out the sum of these last two values to substitute into the equation $\alpha = \frac{\sum(x-\bar x)\cdot(y-\bar y)}{\sum(x-\bar x)^2}$, to calculate $\alpha$.

5. Because the regression line passes through the point ($\bar x,\bar y$), we can substitute these mean values into the equation $y = \alpha x + \beta$ to get; $\beta = \bar y - \alpha \bar x$. Into which we can substitute in all these values to obtain $\beta$.

The dataset I'm using is:

>$(x_1, y_1), (x_2, y_2), (x_3, y_3) =  (1,7),(4,5),(7,3)$

1. Firstly, we calculate the means, $\bar x$ and $\bar y$ of all $x$ and $y$ values.

Doing this, we get:

>$\bar x = 4$ and $\bar y = 5$

2. Then we can calculate the difference of each value from its corresponding mean value, ($x-\bar x$) and ($y-\bar y$).

  x  |  y  | x-$\bar x$ |  y-$\bar y$
:-----:|:-----:|:----------:|:-----------:
   1   |   7   |     -3     |      2
   4   |   5   |      0     |      0
   7   |   3   |      3     |     -2

3. After this, we calculate $(x-\bar x)^2$ and $(x-\bar x)\cdot(y-\bar y)$.

x|y|x-$\bar x$|y-$\bar y$|x-$\bar x\cdot$x-$\bar x$|x-$\bar x\cdot$ y-$\bar y$
:-:|:-:|:-:|:-:|:-:|:-:
1|7|-3|2|9|6
4|5|0|0|0|0
7|3|3|-2|9|-6

4. Work out the sum of these last two values to substitute into the equation $\alpha = \frac{\sum(x-\bar x)\cdot(y-\bar y)}{\sum(x-\bar x)^2}$, to calculate $\alpha$.

>$\sum(x-\bar x)^2 = 18$ and $\sum(x-\bar x)\cdot(y-\bar y) = -12$

Thus:
>$\alpha = -\frac{12}{18} = -\frac{2}{3} \approx 0.667$

5. Because the regression line passes through the point ($\bar x,\bar y$), we can substitute these mean values into the equation $y = \alpha x + \beta$ to get; $\beta = \bar y - \alpha \bar x$. Into which we can substitute in all these values to obtain $\beta$.

>$\beta = 5 - \left(-\frac{2}{3}\cdot4\right) = \frac{23}{3} \approx 7.667$
