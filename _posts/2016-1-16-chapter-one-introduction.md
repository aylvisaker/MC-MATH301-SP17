---
layout: post
title: "Chapter 1 Notes"
categories: [notes]
tags: [notes]
description: MC-MATH301-SP17
---

# Introduction
This class assumes basic familiarity with **arithmetic**, **algebra**, and **sets** (particularly the fundamental theorems of the former).

### Important sets

* The **additive identity** is \\(0\\). The **multiplicative identity** is \\(1\\). The set of **natural numbers** is \\(\\mathbb{N}\\), the smallest set that contains \\(\\{0,1\\}\\) and is closed under addition, multiplication, and exponentiation.
\\[ \mathbb{N} = \\{0,1,2,\dots\\} \\]

* The **additive inverse** of a number, \\(n\\), is the number \\(-n\\). The set of  **integers** is  \\(\\mathbb{Z}\\), the smallest set that contains \\(\\mathbb{N}\\) and is closed under additive inverses, addition, subtraction, and multiplication. \\(\\mathbb{Z}\\) is not closed under exponentiation.
\\[ \mathbb{Z} = \\{\dots,-2,-1,0,1,2,\dots\\} \\]

* The **multiplicative inverse** of a non-zero number, \\(n\\), is the number \\(\\frac{1}{n}\\). The set of **rational numbers** is  \\(\\mathbb{Q}\\), the smallest set that contains \\(\\mathbb{Z}\\) and is closed under inverses, addition, subtraction, multiplication, and non-zero division. \\(\\mathbb{Q}\\) is not closed under exponentiation.
\\[ \mathbb{Q} = \\left\\{\\frac{m}{n} \mid m,n\in\mathbb{Z},n\neq0\\right\\} \\]

### Gaps in the rational numbers

**_Theorem_**. \\(\\sqrt{2}\notin\\mathbb{Q}\\).

**_Proof_**. Suppose, by way of contradiction, that \\(\\sqrt{2} = x = \frac{a}{b}\\) where \\(a,b\\in\\mathbb{Z}\\) and \\(b\\neq0\\). Then let \\(y = x^2\\cdot b = 2b^2= a^2)\\). Observe that \\(a, b\\), and \\(y\\) are integers, and so by the fundamental theorem of arithmetic, have unique prime factorizations.

\\[a = \\prod\_{k=1}^{r}p\_{i\_k}^{d\_k}\\]
\\[b = \\prod\_{k=1}^{s}q\_{i\_k}^{e\_k}\\]

Now consider the prime factorization(s) of \\(y\\):

\\[y = a^2 = \\prod\_{k=1}^{r}p\_{i\_k}^{2d\_k}\\]
\\[y = 2b^2 = 2\\prod\_{k=1}^{s}q\_{i\_k}^{2e\_k}\\]

These cannot be the same because the former factorization has an even exponent on the prime \\(2\\), while the latter has an odd exponent on the prime \\(2\\). This contradicts the uniqueness part of the fundamental theorem of arithmetic for the integer \\(y\\). Our supposition that \\(\\sqrt{2}\\in\\mathbb{Q}\\) must have been incorrect. \\(\\Box\\)

### Set notation and basic definitions

* \\(x\\in S\\) means that \\(x\\) is an **element** (i.e. **member**) of \\(S\\) and \\(x\\notin S\\) means that \\(x\\) is *not* an element of \\(S\\).
* \\(\\emptyset = \\{\\}\\) is called the **empty set** and has no elements. Sets which have at least one element are called **non-empty**.
* If \\(A\\) and \\(B\\) are sets, then 
  * \\(A\\cap B = \\{x\\mid x\\in A\\text{ and } x\\in B\\}\\) is the **intersection** of \\(A\\) and \\(B\\).
  * \\(A\\cup B = \\{x\\mid x\\in A\\text{ or }  x\\in B\\}\\) is the **union** of \\(A\\) and \\(B\\). 
  * \\(A\\subset B\\) and \\(B\\supset A\\) both convey that each element of \\(A\\) is also an element of \\(B\\). We say that \\(A\\) is **contained** in  (i.e. a **subset** of) \\(B\\).
  * \\(A=B\\) means that \\(A\\subset B\\) and \\(B\\subset A\\).

# Ordered Sets
**Definition 1.5**: An **order** on a set $S$ is a relation (which we denote by $<$) with the following two properties:
* If $x,y\in S$ then one and only one of the following holds:
	* $x<y$
	* $y<x$
	* $x=y$
* If $x,y,z\in S$, $x<y$, and $y<z$, then $x<z$.

The relations $\leq, >, \geq$ can be defined in terms of $<$ and have all of the properties you would expect.

**Definition 1.6**: An **ordered set** is a set on which an order can be defined. For example $\mathbb{Q}$ is an ordered set when $r<s$ is taken to mean that $s-r$ is positive.

**Definition 1.7**: Suppose $S$ is an ordered set and $E\subset S$. If there is some $\beta\in S$ such that $x\leq\beta$ for every $x\in E$, then we say that $E$ is **bounded above** and that $\beta$ is an **upper bound**. **Bounded below** and **lower bound** are defined analogously.

**Definition 1.8**: Suppose $S$ is an ordered set and $E\subset S$ has an upper bound. Suppose that there is some $\alpha\in S$ such that:
* $\alpha$ is an upper bound for $E$, and
* if $\gamma<\alpha$ then $\gamma$ is not an upper bound for $E$.
then we say $\alpha$ is the **least upper bound** of $E$, or the **supremum** of $E$. If $\alpha$ is the supremum of $E$, we write $\alpha=\sup E$. The **greatest lower bound**, or **infimum**, is defined analogously and denoted $\alpha=\inf E$.

**Example** Let $A = \\{x\in\mathbb{Q}^{+}\mid x^2<2\\}$ and $B = \\{x\in\mathbb{Q}^{+}\mid x^2>2\\}$. Then $A$ has no least upper bound and $B$ has no greatest lower bound. We prove the former. Let $p$ be an upper bound for $A$, and let $q = p-\frac{p^2-2}{p+2}$. It is straightforward to show that $q\in\mathbb{Q}$. Since $p\in B$ (think about that), it follows that $p^2-2>0$, so $q<p$. Now consider

$$q^2-2=\left(\frac{2p+2}{p+2}\right)^2-2=\frac{(4p^2+8p+4)}{(p+2)^2}-\frac{2p^2+8p+8}{(p+2)^2}=\frac{2(p^2-2}{(p+2)^2}$$

Since $q^2-2>0$, we conclude $q\in B$. Therefore $q$ is an upper bound for $A$, which is both rational and smaller than $p$. Given an arbitrary upper bound, we have constructed a smaller upper bound. Surely this means there can be no *least* upper bound. $\Box$

**More examples**
* Let $A = \\{x\in\mathbb{Q}\mid x<0\\}$ and $B=\\{x\in\mathbb{Q}\mid x\leq 0\\}$. Then $\sup A = \sup B = 0$, and $0\in B$, but $0\notin A$.
* Let $A = \\{\frac1n\mid n\in\mathbb{Z}^{+}\\}$. Then $\sup A = 1\in A$ and $\inf A = 0\notin A$.

**Definition 1.10**: An ordered set $S$ is said to have the **least upper bound property** if every non-empty $E\subset S$ with an upper bound has a supremum.

The ordered set $\mathbb{Q}$ does not have the least upper bound property. The ordered set $\mathbb{Z}$ does have the least upper bound property.

**Theorem 1.11** If $S$ has the least upper bound property then every non-empty set which is bounded below has an infimum. One might express this by saying that $S$ also has a *greatest lower bound* property.

# Fields
**Definition 1.12**: A **field** is a set, $F$, with two operations called *addition* and *multiplication* which satisfy the field axioms. In the following, $x$, $y$, and $z$ are arbitrary elements of $F$.
* (A1) $F$ is closed under $+$. $x+y\in F$
* (A2) $+$ is commutative. $x+y=y+x$
* (A3) $+$ is associative. $(x+y)+z=x+(y+z)$
* (A4) There is an element $0\in F$ such that $0+x=x$ for every $x\in F$.
* (A5) For each $x\in F$ there is an element $-x\in F$ such that $x+(-x)=0$.
* (M1) $F$ is closed under $\cdot$. $x\cdot y\in F$
* (M2) $\cdot$ is commutative. $x\cdot y = y\cdot x$
* (M3) $\cdot$ is associative. $(x\cdot y)\cdot z = x\cdot (y\cdot z)$
* (M4) There is an element $1\in F$ such that $1\cdot x=x$ for every $x\in F$.
* (M5) For each $x\in F$ such that $x\neq 0$, there is an element $1/x=x^{-1}\in F$ such that $x\cdot x^{-1}=1$.
* (D) Multiplication distributes over addition. $x\cdot(y+z)=x\cdot y + x\cdot z$

In any field, and for any integer $n$, the expressions $x-y$, $x/y$, $x+y+z$, $xyz$, $x^n$, $nx$ have their usual intended meaning. $\mathbb{Q}$ is an example of a field. $\mathbb{Z}$ is not because its elements do not have multiplicative inverses in $\mathbb{Z}$.

**Propositions 1.14-1.16**: Let $x,y,z$ be arbitrary elements of the field $F$.
* If $x+y=x+z$ then $x=z$
* If $x+y=x$ then $y=0$
* If $x+y=0$ then $y=-x$
* $-(-x)=x$
* If $x\neq 0$ and $xy=xz$ then $y=z$
* If $x\neq 0$ and $xy=x$ then $y=1$
* If $x\neq 0$ and $xy=1$ then $y=1/x$
* If $x\neq 0$ then $1/(1/x)=x$
* $0\cdot x=0$
* If $x\neq 0$ and $y\neq 0$ then $xy\neq 0$
* $(-x)\cdot y = -(x\cdot y) = x\cdot(-y)$
* $(-x)\cdot(-y) = xy$

**Defintion 1.17**: An **ordered field** is a field which is also an ordered set, such that the following hold:
* $x+y<x+z$ when $y<z$
* $xy>0$ if $x>0$ and $y>0$

$\mathbb{Q}$ is an example of an ordered field.

**Proposition 1.18**: Let $x,y,z$ be arbitrary elements of the ordered field $F$.
* If $x>0$ then $-x<0$ and vice versa
* If $x>0$ and $y<z$ then $xy<xz$
* If $x<0$ and $y<z$ then $xy>xz$
* If $x\neq 0$ then $x^2>0$
* If $0<x<y$ then $0<1/y<1/x$

# The Real Field
**Theorem 1.19**: There exists an ordered field $\mathbb{R}$ with the least upper bound property. Moreover, $\mathbb{Q}$ is (isomorphic to) a subfield of $\mathbb{R}$. The members of this field are called the **real numbers**.

**Theorem 1.20**: Let $x$ and $y$ be arbitrary elements of $\mathbb{R}$.
* *The Archimedean Property:* If $x>0$ then there is some $n\in\mathbb{Z}^{+}$ such that $nx>y$.
* *Density of the Rationals:* If $x<y$ then there is some $p\in\mathbb{Q}$ such that $x<p<y$.
	
**Proposition 1.21**: Let $x\in\mathbb{R}$, $x>0$, and $n>0$. Then there is exactly one $y\in\mathbb{R}$ such that $y^n=x$. We usually write $y=\sqrt[n]{x}$ or $y=x^{\frac1n}$.

**We shall never use decimals, so we do not enter into a detailed discussion of them**

# The Extended Real Number System
**Definition 1.23**: The **extended real number system** consists of the real field $\mathbb{R}$ and two additional symbols, $\infty=+\infty$ and $-\infty$. The original order of $\mathbb{R}$ is preserved and for each $x\in\mathbb{R}$ we define $-\infty<x<\infty$.

In the extended reals, every non-empty set has a least upper bound (possibly $\infty$) and a greatest lower bound (possibly $-\infty$). Every real number in this system is referred to as *finite*. The extended reals *do not* form a field, but we employ the following consistent conventions for each real number $x$:
* $x+\infty=\infty$
* $x+(-\infty) = x-\infty = -\infty$
* $x/\infty=x/-\infty=0$
* If $x>0$ then $x\cdot\infty=\infty$ and $x\cdot-\infty=-\infty$
* If $x<0$ then $x\cdot\infty=-\infty$ and $x\cdot-\infty=\infty$

Note in particular that there are no consistent definitions for:
* $0\cdot\pm\infty$
* $\infty-\infty$
* $\pm\infty/\pm\infty$

# The Complex Field
**Definition 1.24**: A **complex number** is an ordered pair $(a,b)$ of real numbers.For complex numbers $x=(a,b)$ and $y=(c,d)$ we write $x=y$ precisely when $a=c$ and $b=d$. Moreover, we define:
* $x+y=(a+c,b+d)$
* $x\cdot y=(ac-ba,ad+bc)$

According to these definitions, $(0,0)$ is an additive identity and $(1,0)$ is a multiplicative identity.

**Theorem 1.25**: The complex numbers, $\mathbb{C}$ form a field.

**Theorem 1.26**: The real numbers are a subfield of the complex numbers, with $a\in\mathbb{R}$ being identified with $(a,0)\in\mathbb{C}$.

**Theorems 1.27-1.29**: The above definitions are consistent with familiar notations for complex numbers: $a+bi$. Where $i=(0,1)$, $a+bi$ is identified with $(a,b)$.

**Definition 1.30**: If $z=(a,b)=a+bi$, then $\overline{z}=(a,-b)=a-bi$, $\Re(z)=a$, and $\Im(z)=b$.

**Theorem 1.31**: If $z$ and $w$ are complex numbers, then:
* $\overline{z+w}=\overline{z}+\overline{w}$
* $\overline{zw}=\overline{z}\overline{w}$
* $z+\overline{z}=2\Re(z)$
* $z-\overline{z}=2\Im(z)$
* $z\overline{z}$ is a positive real number unless $z=0$
* If $z\in\mathbb{R}$ then $\overline{z}=z$
	
**Definition 1.32**: If $z$ is any complex number (possibly real) then $\vert z\vert = \sqrt{z\overline{z}}$.

**Theorem 1.33**: If $z$ and $w$ are complex numbers, then:
* $\vert z\vert\in\mathbb{R}$
* $\vert 0\vert=0$
* if $z\neq0$ then $\vert z\vert >0$
* $\vert\overline{z}\vert=\vert z\vert$
* $\vert zw\vert = \vert z\vert\cdot \vert w\vert$
* $\vert\Re(z)\vert \leq \vert z\vert$
* $\vert z+w\vert\leq \vert z\vert + \vert w\vert$

**Sigma notation**: When $x_1,\dots,x_n$ are complex numbers, in place of $x_1+x_2+\dots+x_n$ we write $\sum_{i=1}^n x_i$.

**Theorem 1.35 - The Schwarz Inequality**: Let $a_1,\dots,a_n$ and $b_1,\dots,b_n$ be complex numbers. Then

$$ \left\vert \sum_{i=1}^n a_i\overline{b_i} \right\vert^2 \leq \left( \sum_{i=1}^n\left\vert a_i \right\vert^2 \right) + \left( \sum_{i=1}^n\left\vert b_i \right\vert^2 \right)$$