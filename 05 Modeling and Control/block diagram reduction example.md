status :: #green 

# Block diagram reduction example 1

\#block-diagram #example

Take the following block diagram:

![block_diagram_reduc1.svg](images/block_diagram_reduc1.svg)

Since there is no clear [feedback](General%20feedback.md) loop, we wish to rearange some things first. Using what we know from [block diagram algebra](block%20diagram%20algebra.md) (eg. rule 9) we can make "remove" $H_1$ from the loop created by $H_2$, $G_2$ and $G_2$. This gives the following adjustment: 

![block_diagram_reduc2.svg](images/block_diagram_reduc2.svg)

Now we see that $H_1$ and $1/G_3$ are connected in series, meaning we can use [block diagram algebra](block%20diagram%20algebra.md) rule 1, allowing us to combine the two blocks by multiplying them. We also see that $H_2$, $G_2$ and $G_2$ is now a [feedback](General%20feedback.md) loop, thus we can also use rule 3.

![block_diagram_reduc3.svg](images/block_diagram_reduc3.svg)

Now we have another simple series connection between $G_1$ and the large feedback reduction from before. These are simply multiplied together as before.

For the next reduction we have two parallel feedback paths, which we can reduce by manipulating the terms in the feedback path. We wish to combine the two parallel feedbacks (*notice, one is positive, one is negative*) into a single negative feedback path. This means we will have to invert the contents of the one that is not already negative, that is $H_1/G_3$. To this, we will add $1$ which will be the existing negative feedback path. This gives: 

![block_diagram_reduc4.svg](images/block_diagram_reduc4.svg)

Once again we have a negative feedback loop, which means we can once again use [block diagram algebra](block%20diagram%20algebra.md) rule 3. 

![block_diagram_reduc5.svg](images/block_diagram_reduc5.svg)

Now it obviously does not make sense to use a block diagram, since nothing is visualized particularly well. It makes more sense to simply define the contents of the single block as the [Transfer Function](Transfer%20Function.md) of the system, thus:

$$
H(s) = \frac{C(s)}{R(s)} = \frac{\frac{G_1G_2G_3}{1+G_2G_3H_2}}{1+\frac{G_1G_2G_3}{1+G_2G_3H_2}\cdot\left(1-\frac{H_1}{G_3}\right)} 
$$

***Example done***
