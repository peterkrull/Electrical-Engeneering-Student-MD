status :: #yellow

# Transfer Function

\#transfer-function #system #modeling

Transfer functions describe the relationship between the input and output of a *system* in the [Laplace](../04%20Calculation%20Techniques/Laplace.md) domain, and is defines as follows:

$$H(s) = \frac{Y(s)}{X(s)} \Rightarrow Y(s) = H(s)\cdot X(s)$$

We see that the transfer function $H(s)$ is the output $Y(s)$ divided by the input $X(s)$. This also means that the output $Y(s)$ of any transfer function with a given input, can be calculated by multiplying the input with the tranfer function.

---

## Poles and Zeros

The #poles of a transfer function can be determined by finding the values of $s$ where the denominator is equal to $0$. Likewise, the #zeros are found when the numerator equals $0$.

\#example :: take the following transfer function:
$$H(s) = \frac{(s+5)\cdot (s-2)}{s\cdot (s-10) \cdot (s-10)} $$

Looking at the poles (look at denominator, bottom) we first see that if $s = 0$, the entire denominator will equal $0$ because of the first $s$. Likewise, we can see that both of the two parenthesis will equal $0$ if $s = 10$, meaning we have two poles here. 

Likewise for the zeros (look at numerator, top), we see that if $s = -5 \vee 2$ the numerator will equal $0$, meaning that we have zeros in $-5$ and $2$.

---

### For discrete signals

In the [discrete time domain](../05%20Signal%20Processing/discrete%20time%20domain.md) the equivalent of a transfer function is the *impulse response* 
