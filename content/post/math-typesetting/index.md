---
author: Hugo Authors
title: Math Typesetting
date: 2025-03-08
description: A brief guide to setup KaTeX
---

Mathematical notation in a Hugo project can be enabled by using third party JavaScript libraries.
<!--more-->

In this example we will be using [KaTeX](https://katex.org/)

- Create a partial under `/layouts/partials/math.html`
- Within this partial reference the [Auto-render Extension](https://katex.org/docs/autorender.html) or host these scripts locally.
- Include the partial in your templates like so: $\alpha=\sum_{i=1}^n \beta_1$

### Examples

Inline math: $\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
