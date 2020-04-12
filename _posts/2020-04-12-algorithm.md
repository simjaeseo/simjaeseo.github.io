---
layout: single
title: 스트라센 알고리즘
date: 2020-04-12 09:00:00 +0900
author: simjaeseo
---

---

# 1. 알고리즘

<font size="3pt">스트라센 알고리즘을 알아보기 전, 프로그래밍을 할 때 알고리즘에서 중요하게 생각하는 두가지를 먼저 짚어보려 합니다.</font>

<br>

**(1) 시간**

<font size="3pt">input인 n이 증가할 때 시간이 증가하는 대략적인 패턴인 시간복잡도를 고려합니다.</font>

<br>

**(2) 메모리**

<font size="3pt">메모리를 적게 사용하는지, 즉 메모리를 얼마나 효율적으로 사용하는지를 고려합니다.</font>

<br>

---

# 2. 스트라센 알고리즘(Strassen Algorithm)

- ### 소개

<font size="3pt">
행렬의 곱연산은 각 원소를 곱한 후에 나온 결과들을 더해 최종행렬을 구하는 방식으로 이루어집니다. </font><br>



 <font size="3pt">행렬이 커질수록, 덧셈 뺄셈연산과 달리 행렬의 곱연산을 수행할 때 연산 속도는 기하급수적으로 증가하게 됩니다. cpu 구조상 <b><u>곱연산보단 덧셈연산이 더 빠르기때문에</u></b> 독일의 수학자 스트라센은 1969년 시간복잡도가 더 낮게 알고리즘을 보완했습니다. </font><br>



**시간복잡도 변화**

<p style="text-align:center;">
    <img align="center" width="" alt="on" src="https://user-images.githubusercontent.com/63089631/79060707-3cdffa80-7cc3-11ea-99bd-615e79ac1592.PNG">
</p>

---



- ### 원리

<font size="3pt">2 by 2 행렬 A , B 가 존재할 때, </font><br>



<font size="3pt">본래의 곱은 </font>

<p style="text-align:center;">
    <img border="4" width="400" alt="Corigin" src="https://user-images.githubusercontent.com/63089631/79060900-479b8f00-7cc5-11ea-9809-5ab7b98eb8d3.PNG">
</p>

<font size="3pt">으로 총 8번의 곱셈, 4번의 덧셈의 연산과정을 거칩니다.</font>

<br>

<font size="3pt">하지만,  스트라센 알고리즘은 여러개의 연산행렬 M을 이용하여</font>

<p style="text-align:center;">
    <img align="center" width="600" alt="C" src="https://user-images.githubusercontent.com/63089631/79060963-f9d35680-7cc5-11ea-9e53-f75e9dde38d4.PNG">
</p>

<font size="3pt">으로 7번의 곱셈, 18번의 덧셈의 과정을 거치며 더 효율적인 연산을 진행합니다.</font>

---

