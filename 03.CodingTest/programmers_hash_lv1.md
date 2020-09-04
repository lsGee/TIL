# [해시] 완주하지 못한 선수

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42576



## Code

```python
def solution(participant, completion):
    participant.sort()
    completion.sort()
    for i in range(len(completion)):
        if participant[i]!=completion[i]:
            return participant[i]
        
    return participant[i+1]
```



## 다른 풀이

**collections 모듈을 활용한 풀이**

```python
import collections

def solution(participant, completion):
    newP = collections.Counter(participant)
    newC = collections.Counter(completion)
    print(list((newP - newC)))
    
    return list((newP - newC).keys())[0]
```

* collections 모듈의 counter 클래스를 활용하면 list 내 데이터 값을 key, 해당 데이터의 빈도를 value로 갖는 딕셔너리를 생성할 수 있음
* counter 클래스를 통해 만들어진 딕셔너리로 사칙연산도 가능해짐!