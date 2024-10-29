# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

**Answer:**

Do this with subsitution. 

$T(n)$ = $T\left(\frac{n}{13}\right) + 5$

= $T\left(\frac{n}{13^2}\right) + 5(2)$

= $T\left(\frac{n}{13^i}\right) + 5(i)$

For $i = \log_{13} n :$

$T(1) + 5\log_{13} n$ 

= log n 

= $Theta(log n)$ is the answer

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

**Answer:**

Attempt to use the Master theorem method. I am following this website's Master Theorem method. https://www.programiz.com/dsa/master-theorem

Therom method = T(n) = $aT\left(\frac{n}{b}\right) + f(n)$

We have: 

$T(n)$ = $13T\left(\frac{n}{13}\right) + 5$

a = 13 

b = 13

f(n) = 5

Step 2: Need to solve $log_{a} b$

$log_{13} 13$ = 1 

Step 3: Compare the f(n) to $log_{a} b$

f(n) = 5 

$n^{log_{a} b}$ = $n^1$ = _n_

Since f(n) is $O(n^{1 - &#949;)$, the Master theorm states $T(n) = Theta(n^{log_{a} b})$

Which will give us T(n) = $Theta(n^1)$ = $Theta(n)$ 

Answer = $Theta(n)$


3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

**Answer:**
