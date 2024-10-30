I wanted to write a few notes to give the best intuition I can about some of the algebraic structures we discussed today. I'll use LaTeX for some of the symbols, namely

$\mathbb{R}$: the set of real numbers
$\mathbb{C}$: the set of complex numbers 

# Review: Definition of a Field 

I'm going to skip writing this part for now, and trust that we can fill it in later. Let's just agree that $\mathbb{R}$ is a field. 

[This is an example of an edit to test versioning on this markdown file]

# Key Idea: Polynomials over a Field, Roots, and Irreducibility

A polynomial over a field is a polynomial whose coefficients are in the field.  
A root of a polynomial $p(x)$ is a field element $r$ which satisfies $p(r) = 0$. 

Let's say we have a polynomial $f(x) = x^2 - 1$. The roots are 1 and -1. 

What if the polynomial doesn't have any roots in the field? Consider $q(x) = x^2 + 1$. This doesn't have any roots in $\mathbb{R}$, but we could just make one up, call it $i$, and add it to the field. This is called a \textit{field extension}. 

Of course, once we add $i$, we need to add more elements: $1+i$, $38i$, etc. (If we don't, the structure won't be closed under addition or multiplication -- when we add a new element, we need to make sure that we still can add it or multiply it by anything we've had before). Of course, we've built the field of complex numbers.

The key Idea here is: take a field, find a polynomial with no root in the field, add a new element to be the root, and take whatever else happens. 

# Key Idea: Vector Spaces and Componentwise Operations

When we think of an element of a vector spa d, we probably think of a vector as a tuple of numbers. For instance, a familiar example would be $\mathbb{R}^2$, the two-dimensional vector space over $\mathbb{R}$ consisting of ordered pairs of the form $(a,b)$ with addition given componentwise: $(a,b) + (c,d)$ is equal to $(a+c, b+d)$. 

Vector Spaces are always defined over fields (for reasons that we won't get into at the moment). Vector Spaces are different from fields, in that they don't naturally come with multiplication between elements (you can multiply a vector by a \textit{scalar} -- an element of the underlying field). No worry -- it's not hard to define multiplication to be \textit{componentwise}: $(a,b) \cdot (c,d) = (a \cdot c, b \cdot d)$. With these componentwise operations, $\mathbb{R}^2$ is a ring, but not a field. 

# Key Idea: Identifying Vector Spaces with Field Extensions

It's natural to represent imaginary numbers as points in the plane. This is because both a complex number $a+bi$ and a vector $(x,y) \in \mathbb{R}^2$ are specified by a pair of real numbers. 

Just like $\mathbb{R}^2$, the field $\mathbb{C}$ is a two-dimensional vector space! It isn't really different to talk about $a+bi$ or $(a,b)$. In fact, we could write $a+bi$, as $(a,b)$ -- we'd just need to be careful that we didn't make the mistake of using the wrong multiplication.

Connection to Finite Fields 

I don't have time to write out all the details tonight, but these ideas carry over to finite fields and vector spaces as well. We start with a field $\mathbb{F}_p$ with $p$ elements ($p$ is a prime). 

To get a field $\mathbb{F}_{p^2}$ with $p^2$ elements, we take a degree-2 polynomial that has no roots in $\mathbb{F}_p$. 

For instance, let's try $\mathbb{F}_3$. To build $\mathbb{F}_9$, we take the polynomial $p(x) = x^2 + 1$ over $\mathbb{F}_3$. This equation has no roots, so we give it one: let's say $\alpha$ is a root of $p(x)$, so $\alpha^2 + 1 = 0$. We add $\alpha$ to the field, as well as anything that it needs to have addition and multiplication remain defined. In the end, everything has the for $a + b\alpha$, where $a,b \in \mathbb{F}_3$. This gives 9 elements. When we multiply, we use the fact that $\alpha^2 + 1 = 0$ or $\alpha^2 = 2$. For instance, if we multiply $\alpha + 1$ by $\alpha + 2$, it looks like this: 
$(\alpha + 1)(\alpha + 2) = \alpha^2 + 3 \alpha + 2 = 2 + 0 + 2 = 1$. So $\alpha + 1$ and $\alpha + 2$ are multiplicative inverses. 

The comparison with $\mathbb{F}_p^2$ is the same as the comparison of $\mathbb{C}$ with $\mathbb{R}^2$: the elements correspond and it's almost natural to think about switching the same point to a different algebraic structure. 
