---
layout: post
title: "Chapter 1 Notes"
categories: [notes]
tags: [notes]
description: Course prerequisites.
---

# Introduction
This class assumes basic familiarity with **arithmetic**, **algebra**, and **sets** (particularly the fundamental theorems of the former). The **additive identity** is \\(0\\). The **multiplicative identity** is \\(1\\). The set of **natural numbers** is \\(\\mathbb{N}\\), the smallest set that contains \\(\\{0,1\\}\\) and is closed under addition, multiplication, and exponentiation.

\\[ \mathbb{N} = \\{0,1,2,\dots\\} \\]

The **additive inverse** of a number, \\(n\\), is the number \\(-n\\). The set of  **integers** is  \\(\\mathbb{Z}\\), the smallest set that contains \\(\\mathbb{N}\\) and is closed under additive inverses, addition, subtraction, and multiplication. \\(\\mathbb{Z}\\) is not closed under exponentiation.

\\[ \mathbb{Z} = \\{\dots,-2,-1,0,1,2,\dots\\} \\]

The **multiplicative inverse** of a non-zero number, \\(n\\), is the number \\(\\frac{1}{n}\\). The **rational numbers** is  \\(\\mathbb{Q}\\), the smallest set that contains \\(\\mathbb{Z}\\) and is closed under inverses, addition, subtraction, multiplication, and non-zero division. \\(\\mathbb{Q}\\) is not closed under exponentiation.

\\[ \mathbb{Q} = \\left\\{\\frac{m}{n} \mid m,n\in\mathbb{Z},n\neq0\\right\\} \\]

**_Theorem_**. \\(\\sqrt{2}\notin\\mathbb{Q}\\).

**_Proof_**. Suppose that \\(\\sqrt{2} = x = \frac{a}{b}\\) where \\(a,b\\in\\mathbb{Z}\\) and \\(b\\neq0\\). Then let \\(y = x^2\\cdot b = 2b^2= a^2)\\). Observe that \\(a, b\\), and \\(y\\) are integers, and so by the fundamental theorem of arithmetic, have unique prime factorizations.

\\[a = \\prod\_{k=1}^{r}p\_{i\_k}^{d\_k}\\]
\\[b = \\prod\_{k=1}^{s}q\_{i\_k}^{e\_k}\\]

Now consider the prime factorization(s) of \\(y\\):

\\[y = a^2 = \\prod\_{k=1}^{r}p\_{i\_k}^{2d\_k}\\]
\\[y = 2b^2 = 2\\prod\_{k=1}^{s}q\_{i\_k}^{2e\_k}\\]

These cannot be the same because the former factorization has an even exponent on the prime \\(2\\), while the latter has an odd exponent on the prime \\(2\\). This contradicts the uniqueness part of the fundamental theorem of arithmetic for the integer \\(y\\). \\(\\Box\\)

# Ordered Sets
