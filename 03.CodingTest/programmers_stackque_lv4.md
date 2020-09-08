# [스택/큐] 프린터

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42587



## Code

```python
def solution(priorities, location):
    answer = 1
    plist = list(reversed(list(enumerate(priorities))))
    
    while True:
        pmax = max(list(map(lambda x:x[1], plist)))
        first = plist.pop()
        
        if first[1] != pmax:
            plist[:0] = [first]
        elif first[0] == location:
            break
        else:
            answer += 1
    
    return answer
```



## enumerate

* `enumerate()` 반환값은 iterable 객체이기 때문에 list, dictionary 등으로 변환하여 넣어줄 필요가 있음



## reversed

* `reversed()` 반환값 역시 iterable 객체이기 때문에 list, dictionary 등으로 변환하여 넣어줄 필요가 있음



## pop

```python
a = [1, 2, 3, 4]
a.pop(0)  # 2 반환
```

* `pop()` 은 반환 및 제거할 값의 인덱스값을 인수로 받는다.
* 즉, 원하는 위치의 값을 pop 할 수 있음..!