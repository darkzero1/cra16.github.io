---
layout: post
title: 3주차 C 언어 과제
tags: C
---

# 스무고개

## Level 1

> 컴퓨터가 0 - 99 사이의 숫자를 결정한다. 사람이 답을 입력할 때, 컴퓨터는 '정답보다 크다, 작다, 일치' 3가지 대답을 할 수 있다. 사람이 맞출 수 있는 기회는 20번이다.

### 이걸 어떻게 짤까?

- 0 - 99 임의의 숫자 결정: ```x = rand() % 100;``` (구글 검색!)

- 컴퓨터의 대답: 정답과 입력 값을 비교(if, case 등)

- 20번의 기회: 반복문 사용(for, while, do while 등)

### Flowchart

![](/images/assignment-3-1-flowchart.png)

## Level 2

> 사람이 문제를 내고, 컴퓨터가 맞춰라!

* 컴퓨터는 이진탐색(Binary search) 알고리즘을 사용해서 문제를 맞출 수 있다.

### 이진탐색 알고리즘

	initially, left = 0, right = n - 1 // (n은 총 길이)
	middle = (left + right) / 2
	compare middle with x

	case1: x < middle, set right = middle - 1
	case2: x == middle, return middle
	case3: x > middle, set left = middle + 1

> 자세한 내용은 구글 검색!

# 가위 바위 보

> 사용자가 가위, 바위, 보 중에 하나를 입력한다. 컴퓨터가 가위, 바위, 보 중에 하나를 결정한다. 두 값을 비교한 후 결과를 출력한다(승, 무, 패). 사용자가 5번 이기면 사용자의 전적을 출력 후 종료한다.

## Statechart

![](/images/assignment-3-2-statechart.png)

# 구구단을 외자 (3, 6, 9 게임)

## Level 1

> 게임에 참여하는 사람 수를 입력 받는다. 사용자의 차례는 사람들 중 맨 마지막 번째이다. 사용자는 숫자, 또는 박수(0으로 표시)을 입력할 수 있다. 입력 대기 시간은 2초, 초과시 패배하게 된다.

### 어떻게...?!

- 1의 자리수가 3, 6, 9일 때 박수, 그렇다면 1의 자리수만 따로 떼어서 비교하려면?

```n % 10 == 3, 6, 9``` 이면 박수

- 입력 대기 시간을 구하는 방법?

```<ctime.h>``` 레퍼런스를 구글에서 찾아보자.

- 일단 원리만 간단히 말하자면

	A = 현재 시간;
	scanf("%d", &user);
	B = 현재 시간;
	if(B - A > 2)
		시간 초과!!

### Flowchart










