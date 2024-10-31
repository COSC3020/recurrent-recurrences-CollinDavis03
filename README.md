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

= $\theta(log n)$ is the answer

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

Since f(n) is $O(n^{1 - &#949;})$, the Master theorm states $T(n) = Theta(n^{log_{a} b})$

Which will give us T(n) = $\theta(n^1)$ = $\theta(n)$ 

Answer = $\theta(n)$


3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

**Answer:**

Use the Master theorem again. 

a = 13

b = 13

f(n) = 2n

Step 2: solve $log_{a} b$

$log_{13} 13$ = 1 

Step 3: Compare f(n) to $log_{a} b$ 

f(n) = 2n 

$n^{log_{a} b}$ = $n^1$ = _n_

f(n) is in the same order as log 

Step 4: Solve 

$T(n) = (n^{log_{a} b} * log n)$

Since $n^{log_{13} 13} = n$ 

Answer = $\theta(n log n)$ is the answer 


## Sources 
The only thing I used was the link I mentioned earlier to learn about the master theorem a little more and how and when it is used. Other than that I did the rest of the solving myself. I spoke with the TA, who assisted me with the notation needed for the problem. 

## Plagarism Statement 
“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
