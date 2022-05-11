---
layout:     post
title:      The Column Space of A Contains All Vectors Ax
subtitle:   
date:       2022-03-26
author:     Ambition
header-img: 
catalog: true
tags:
    - Math
    - Linear Algebra
    - Machine Learning
---

# The Column Space of A Contains All Vectors Ax

## The rightway of a Matrix multiply a Vector

$$
A = \begin{bmatrix} 2 & 1 & 3\\ 3 & 1 & 4\\ 5 & 7 & 12\\ \end{bmatrix} , \boldsymbol x = \begin{bmatrix} x_1\\ x_2\\ x_3\\ \end{bmatrix}
$$
$$
A \boldsymbol x =
  \begin{bmatrix} 2 & 1 & 3\\ 3 & 1 & 4\\ 5 & 7 & 12\\ \end{bmatrix} 
  \begin{bmatrix} x_1\\ x_2\\ x_3\\ \end{bmatrix} = 
  x_1  \begin{bmatrix} 2\\ 3\\ 5\\ \end{bmatrix} +
  x_2  \begin{bmatrix} 1\\ 1\\ 7\\ \end{bmatrix} +
  x_3  \begin{bmatrix} 3\\ 4\\ 12\\ \end{bmatrix}
$$

  - The combination of vector produce a vector.

  - Thinking matrix as a whole thing.

### Think about all combinations of the columns of $A$

* All $A \boldsymbol x$ give us a big banch of vectorx, that collection of vectors is called the column space of $A$. It's a space, in other words, that's the keyword there, the column space of $A$.

* In this case, we got a plane.

* The below column space is a **line** ($A$ is rank 1 matrix): 
  $$
  A = \begin{bmatrix} 1 & 2 & 3\\ 1 & 2 & 3\\ 1 & 2 & 3\\ \end{bmatrix} \\
  C(A) = line \\
  rank(A) = 1
  $$

- The rank is sort of the dimension of the column space

### Matrices with two factor

* Basis for the column space ($C$)

$$
A = CR = \begin{bmatrix} 2 & 1 & 3\\ 3 & 1 & 4\\ 5 & 7 & 12\\ \end{bmatrix} \\
C = \begin{bmatrix} 2 & 1\\ 3 & 1\\ 5 & 7\\ \end{bmatrix} \\
R = \begin{bmatrix} 1 & 0 & 1\\ 0 & 1 & 1\\ \end{bmatrix}
$$

1. The column rank is 2
2.  column rank = row rank = 2, and why?

### What's the row rank, what's the row space?

* All combinations of the row is **row space**

* Two ways to get the row space

  * transpose the matrix, and to get row space, we need to get transpose matrix's column space

    $R(A) = C(A^T)$

  * the basis for the row space is $R= \begin{bmatrix} 1 & 0 & 1\\ 0 & 1 & 1\\ \end{bmatrix}$
  
  * the conditions to be basis
  
    * Independent
    * the combinations produce all the rows
  
  * Range?

### The factorization of matrix

1. $A = CR$

2. > If you have a giant matrix, like size 10 to the 5th, you can't put that into fast memory. It's a mess. How do you deal with a matrix of size 10 to the 5th, when you cannot deal with all the entries?
   >
   > How do you sample a matrix?
   >
   > you want to get some typical columns.

   $A\boldsymbol x, x = rand(m, 1)$

   $A(BC\boldsymbol x)$

   $A = CUR^\prime$, $R^\prime$ is the rows of $A$

## Matrix multiply a Matrix

* Dot product

$$
AB = \begin{bmatrix}  &  & \\ - & - & -\\  &  & \\ \end{bmatrix} 
  \begin{bmatrix}  & | & \\  & | & \\  & | & \\ \end{bmatrix}
$$

* New way
  $$
  AB = \begin{bmatrix} | \\ col \ K \\ | \\ \end{bmatrix} 
    \begin{bmatrix} - & row \ K & - \\ \end{bmatrix}
  $$
  

