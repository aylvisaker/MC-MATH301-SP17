---
layout: post
title: "Chapter 1 Notes"
categories: [notes]
tags: [notes]
description: Course prerequisites.
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
* An **order** on a set $S$ is a relation (which we denote by $<$) with the following two properties:
	* If $x,y\in S$ then one and only one of the following holds:
		* $x<y$
		* $y<x$
		* $x=y$
	*If $x,y,z\in S$, $x<y$, and $y<z$, then $x<z$.
* The relations $\leq, >, \geq$ can be defined in terms of $<$ and have all of the properties you would expect.
* An **ordered set** is a set on which an order can be defined. For example $\mathbb{Q}$ is an ordered set when $r<s$ is taken to mean that $s-r$ is positive.
* Suppose $S$ is an ordered set and $E\subset S$. If there is some $\beta\in S$ such that $x\leq\beta$ for every $x\in E$, then we say that $E$ is **bounded above** and that $\beta$ is an **upper bound**.
* **Bounded below** and **lower bound** are defined analogously.
* Suppose $S$ is an ordered set and $E\subset S$ has an upper bound. Suppose that there is some $\alpha\in S$ such that:
	* $\alpha$ is an upper bound for $E$, and
	* if $\gamma<\alpha$ then $\gamma$ is not an upper bound for $E$.
	then we say $\alpha$ is the **least upper bound** of $E$, or the **supremum** of $E$.
* If $\alpha$ is the supremum of $E$, we write $\alpha=\sup E$.
* The **greatest lower bound**, or **infimum**, is defined analogously and denoted $\alpha=\inf E$.

### Examples
* Let $A = \\{x\in\mathbb{Q}^{+}\mid x^2<2\\}$ and $B = \\{x\in\mathbb{Q}^{+}\mid x^2>2\\}$. Then $A$ has no least upper bound and $B$ has no greatest lower bound. We prove the former. Let $p$ be an upper bound for $A$, and let $q = p-\frac{p^2-2}{p+2}$. It is straightforward to show that $q\in\mathbb{Q}$. Since $p\in B$ (think about that), it follows that $p^2-2>0$, so $q<p$. Now consider

$$q^2-2=\left(\frac{2p+2}{p+2}\right)^2-2=\frac{(4p^2+8p+4)}{(p+2)^2}-\frac{2p^2+8p+8}{(p+2)^2}=\frac{2(p^2-2}{(p+2)^2}$$

since $q^2-2>0$, we conclude $q\in B$. Therefore $q$ is an upper bound for $A$, which is both rational and smaller than $p$. Given an arbitrary upper bound, we have constructed a smaller upper bound. Surely this means there can be no *least* upper bound.
* Let $A = \\{x\in\mathbb{Q}\mid x<0\\}$ and $B=\\{x\in\mathbb{Q}\mid x\leq 0\\}$. Then $\sup A = \sup B = 0$, and $0\in B$, but $0\notin A$.
* Let $A = \\{\frac1n\mid n\in\mathbb{Z}^{+}\\}$. Then $\sup A = 1\in A$ and $\inf A = 0\notin A$.