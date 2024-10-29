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

For $i = \log_{13} n$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

**Answer:**
  
4.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

**Answer:**
