# (P3.1)

---

## (a) 상태 변수 정의

상태 변수(state variables):

- $x_1(t) = y(t)$
- $x_2(t) = \dot{y}(t)$

상태벡터:

$$
\mathbf{x}(t) = \begin{bmatrix}
x_1(t) \\
x_2(t)
\end{bmatrix}
= \begin{bmatrix}
y(t) \\
\dot{y}(t)
\end{bmatrix}
$$

---

## (b) 상태 변수로 구성된 1차 미분방정식
$$
\begin{aligned}
\dot{x}_1(t) &= x_2(t) \\
\dot{x}_2(t) &= \frac{1}{M} \left( F(t) - b x_2(t) - k x_1(t) \right)
\end{aligned}
$$

---

## (c) 상태 공간 표현

### 상태 방정식

$$
\dot{\mathbf{x}}(t) = A \mathbf{x}(t) + B u(t)
$$

### 출력 방정식

$$
y(t) = C \mathbf{x}(t) + D u(t)
$$

여기서,

- $u(t) = F(t)$: 입력
- $y(t) = x_1(t)$: 출력

---

## 행렬 형태

상태방정식을 구성하는 행렬:

$$
A = \begin{bmatrix}
0 & 1 \\
-\dfrac{k}{M} & -\dfrac{b}{M}
\end{bmatrix}, \quad
B = \begin{bmatrix}
0 \\
\dfrac{1}{M}
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
1 & 0
\end{bmatrix}, \quad
D = \begin{bmatrix}
0
\end{bmatrix}
$$

---

# (P3.3)

---

## 1. KVL 방정식:

$$
v_1(t) = L \dot{x}_1 + R x_1 + x_2 \\
\Rightarrow \dot{x}_1 = \frac{1}{L} (v_1(t) - R x_1 - x_2)
$$

## 2. KCL 방정식 (캐패시터에 흐르는 전류):

$$
\dot{x}_2 = \frac{1}{C} \left(x_1 - \frac{x_2}{R} \right)
$$

---

## 상태방정식 형태

상태 공간:

$$
\dot{\mathbf{x}}(t) = A \mathbf{x}(t) + B u(t)
$$

$$
y(t) = C \mathbf{x}(t) + D u(t)
$$

여기서:

- 

  $$
  \mathbf{x}(t)=\begin{bmatrix}
  x_1(t) \\
  x_2(t)
  \end{bmatrix}
  $$

- $u(t) = v_1(t)$
- $y(t) = x_2(t) = v_2(t)$

---

## 행렬 표현

$$
A = \begin{bmatrix}
-\dfrac{R}{L} & -\dfrac{1}{L} \\
\dfrac{1}{C} & -\dfrac{1}{RC}
\end{bmatrix}, \quad
B = \begin{bmatrix}
\dfrac{1}{L} \\
0
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
0 & 1
\end{bmatrix}, \quad
D = \begin{bmatrix}
0
\end{bmatrix}
$$

---

# (P3.5)

---

## (a) 폐루프 전달함수

### 컨트롤러:

$$
G_c(s) = \frac{s + 2}{s + 8}
$$

### 플랜트:

$$
G_p(s) = \frac{1}{s - 3} \cdot \frac{1}{s} = \frac{1}{s(s - 3)}
$$

### 개루프 전달함수:

$$
G(s) = G_c(s) \cdot G_p(s) = \frac{s + 2}{s(s - 3)(s + 8)}
$$

### 폐루프 전달함수:

$$
T(s) = \frac{G(s)}{1 + G(s)} = \frac{s + 2}{s^3 + 5s^2 - 23s + 2}
$$

---

## (b) 상태 공간 모델 (Phase Variable Form)

전달함수:

$$
T(s) = \frac{s + 2}{s^3 + 5s^2 - 23s + 2}
$$

---

### 상태공간 표현:

$$
\dot{\mathbf{x}} = A \mathbf{x} + B u, \quad y = C \mathbf{x} + D u
$$

#### 행렬 정의:

$$
A = \begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-2 & 23 & -5
\end{bmatrix}, \quad
B = \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
2 & 1 & 0
\end{bmatrix}, \quad
D = \begin{bmatrix}
0
\end{bmatrix}
$$

---

# (P3.5)

---

## (a) 폐루프 전달함수

### 컨트롤러:

$$
G_c(s) = \frac{s + 2}{s + 8}
$$

### 플랜트:

$$
G_p(s) = \frac{1}{s - 3} \cdot \frac{1}{s} = \frac{1}{s(s - 3)}
$$

### 개루프 전달함수:

$$
G(s) = G_c(s) \cdot G_p(s) = \frac{s + 2}{s(s - 3)(s + 8)}
$$

### 폐루프 전달함수:

$$
T(s) = \frac{G(s)}{1 + G(s)} = \frac{s + 2}{s^3 + 5s^2 - 23s + 2}
$$

---

## (b) 상태 공간 모델

전달함수:

$$
T(s) = \frac{s + 2}{s^3 + 5s^2 - 23s + 2}
$$

---

### 상태공간 표현:

$$
\dot{\mathbf{x}} = A \mathbf{x} + B u, \quad y = C \mathbf{x} + D u
$$

#### 행렬 정의:

$$
A = \begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-2 & 23 & -5
\end{bmatrix}, \quad
B = \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
2 & 1 & 0
\end{bmatrix}, \quad
D = \begin{bmatrix}
0
\end{bmatrix}
$$

---

# (P3.12)

---

## (a) 상태 변수 모델 (Phase Variable Form)

분모 계수:

- $( a_1 = 12 ), ( a_2 = 44 ), ( a_3 = 48 )$

분자 계수 (padding 포함):

- $( b_0 = 0 ), ( b_1 = 8 ), ( b_2 = 40 )$

---

### 상태공간 표현:

$$
\dot{\mathbf{x}} = A \mathbf{x} + B u, \quad y = C \mathbf{x} + D u
$$

#### 행렬 정의:

$$
A = \begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-48 & -44 & -12
\end{bmatrix}, \quad
B = \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
40 & 8 & 0
\end{bmatrix}, \quad
D = \begin{bmatrix}
0
\end{bmatrix}
$$

---

## (b) 상태 천이 행렬 $(\Phi(t))$

$$
\Phi(t) = e^{At}
$$

---

# (P3.17)

---

## 주어진 상태방정식

$$
\dot{\mathbf{x}}(t) = A \mathbf{x}(t) + B u(t), \quad y(t) = C \mathbf{x}(t)
$$

행렬:

$$
A = \begin{bmatrix}
1 & 1 & -1 \\
4 & 3 & 0 \\
-2 & 1 & 10
\end{bmatrix}, \quad
B = \begin{bmatrix}
0 \\
0 \\
4
\end{bmatrix}
$$

$$
C = \begin{bmatrix}
1 & 0 & 0
\end{bmatrix}, \quad
D = 0
$$

---

## 전달함수 공식

상태방정식으로부터 전달함수:

$$
G(s) = C (sI - A)^{-1} B + D
$$

---
