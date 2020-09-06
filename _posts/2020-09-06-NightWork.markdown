---
layout: post
title: 프로그래머스 야근지수
date: 2020-09-06 18:56:23 +0900
category: c# List 정렬
---

문제는 [https://programmers.co.kr/learn/courses/30/lessons/12927](https://programmers.co.kr/learn/courses/30/lessons/12927)에서 확인할 수 있습니다.

이 문제의 핵심은 정렬을 한 다음에 가장 큰 수를 찾은 후 

C#의 List를 사용하는 방법이 있습니다.


# C#에서의 리스트

>List<T> = new List<T>();
List를 선언하는 방식이다. T는 데이터 형식(타입)이 들어간다.

문제에서는 int로 주어졌으니 
>List<int> 변수명 = new List(int)();
로 선언하면 된다.

아니면 int를 List로 바꾸면 된다.
>var ListWorks = works.ToList();
이를 이용하면 List로 이용할 수 있다.

배열과 list의 큰 차이점을 배열은 선언과 동시에 공간이 고정되어 있어서 특정공간만 삭제가 불가능 하지만
list는 특정공간을 추가하거나 삭제할 수 있다.

# 내림차순 하기

방법은 2가지로 

```ruby
Array.Sort(works);
Array.Reverse(works);
```
순서대로 정렬 후 뒤집는 방법과

```ruby
works.OrderByDecending((x) => x);
```
를 이용하는 방법이 있다. 물론 위 방법 외에도 여러가지만 있지만 쉽게 사용할 수 있는 방법 2개를 골랐다.

이 방법을 이용해서 문제를 해결 하면 된다.