---
published: true
title: "[Linear Algebra][1] Vectors and linear combination"
excerpt: "Vector, Matrix, Linear Combiation"
# layout: single
# author_profile: true
# sidebar_main: true
toc: true
toc_sticky: true
use_math: true

categories:
  - Linear Algebra
tags:
  - [Vector, Linear combination, Orthogonal]

permalink: /categories/linear_algebra/1


date: 2024-02-02
last_modified_at: 2024-02-02
---

선형대수 빠른 복습을 목표로 정리해 보겠습니다. 최대한 머신 러닝과 연관이 있는 부분을 발견하면 내용을 수정하더라도 자세히 채우는 방식으로 작성하겠습니다.

#### 1. Introduction

Linear Algebra는 벡터, 행렬, 선형 변환과 방정식 계산, 그리고 고유 값 등을 배우는 학문이다. 아래와 같은 키워드들을 잘 이해하고 있으면 되었던 것 같은데...

- Vector space
- Dual space
- Matrix decomposition
- Gram-schmidt orthogonalization
- Eigen value, Eigen vector

---

#### 2. Vectors in $\mathbb{R}^{2}$
벡터는 크기와 방향을 가지고 있는 것을 의미하는 용어임

##### 2.1. Vector calculation
- Scaling

Given $\lambda \in \mathbb{R}, v=\begin{pmatrix} v_1 & v_2 \end{pmatrix}^T$

$\lambda \cdot v := \begin{pmatrix} \lambda v_1 & \lambda v_2 \end{pmatrix}^T$
{: .notice--info}

- Addition  

Given $v=\begin{pmatrix} v_1 & v_2 \end{pmatrix} ^T, u=\begin{pmatrix} u_1 & u_2 \end{pmatrix} ^T$


$v+u:=\begin{pmatrix} v_1 + u_1 & v_2 + u_2 \end{pmatrix} ^T$
{: .notice--info}

---

#### 3. Linear combination
Space $\mathbb{R}^m$이 operation $(\cdot, +)$를 포함하고 있으면 <b>vector space</b>라 할 수 있으며 <b>linear combination</b>이 가능해진다.

Given vectors $v^1, v^2, ..., v^k \in \mathbb{R}^m $ and scalars $\lambda_1, \lambda_2, ..., \lambda_k \in \mathbb{R}$

$v=\sum^{k}_{j=1} \lambda_j v^j\text{는 linear combination이다.}$
{: .notice--info}

---

#### 4. Inner product
Given $v=\begin{pmatrix} v_1 & v_2 \end{pmatrix} ^T, u=\begin{pmatrix} u_1 & u_2 \end{pmatrix} ^T$ 

$v\cdot u = \langle v, u \rangle = v_1u_1 + v_2u_2$
{: .notice--info}  

##### 4.1. Orthogonal
만약 inner product가 0이면 두 벡터는 orthogonal하다.  

If $\langle v, u \rangle =0$, then v and u are orthogonal
{: .notice--info}  


##### 4.2. Norm
Inner product가 정의됨에 따라 벡터의 크기(norm)도 측정할 수 있다.

$ \Vert v \Vert:= \sqrt{\langle v, v \rangle} $
{: .notice--info}

---

#### 5. Line

- Origin on the line L ($n$은 normal vector)

$L= \lbrace v\in\mathbb{R}^2 \| v=\lambda \cdot a~ for ~\lambda \in \mathbb{R}\rbrace$  
$\quad\;\;\;\; \lbrace v\in\mathbb{R}^2 \| \langle n, v \rangle =0 \rbrace$ 
{: .notice--info}

- Origin not on the line L  ($n$은 normal vector)

$L= \lbrace v\in\mathbb{R}^2 \| \langle n, v-p \rangle=0 \rbrace $  
$\quad\;\;\;\; \lbrace \begin{pmatrix} x & y\end{pmatrix}^T\in\mathbb{R}^2 \| n_1x+n_2y = \delta \rbrace $, where $\delta := \langle n, p \rangle $
{: .notice--info}
