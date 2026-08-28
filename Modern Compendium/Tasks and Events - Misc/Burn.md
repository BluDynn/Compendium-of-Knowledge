# Discrete-Time Delta Function

## Definition

$$
\delta[n]=
\begin{cases}
1,&n=0\\
0,&n\neq0
\end{cases}
$$

## Shifted Delta

$$
\delta[n-k]
$$

Occurs at $n=k$.

## Relationship with the Unit Step

Difference of steps:

$$
\delta[n]=u[n]-u[n-1]
$$

Accumulation of deltas:

$$
u[n]=\sum_{k=0}^{\infty}\delta[n-k]
$$

General form:

$$
u[n-a]=\sum_{k=a}^{\infty}\delta[n-k]
$$

## Properties

- Sifting Property
- Even Symmetry
- Identity under Convolution

## Common Problems

### Rewrite as a sum of delta functions

Use

$$
u[n-a]=\sum_{k=a}^{\infty}\delta[n-k]
$$

Example:

$$
u[n]-u[n-3]
=
\delta[n]+\delta[n-1]+\delta[n-2]
$$

See also:
- [[Discrete-Time Unit Step Function]]
- [[Convolution]]
- [[Time Shifting]]