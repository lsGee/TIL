# [스택/큐] 기능개발

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42586#



## Code

```python
def solution(progresses, speeds):
    answer = []
    total = len(progresses)
    day = []
    
    for i in range(total):
        if speeds[i] == 0:
            day.append(1)
        elif (100 - progresses[i]) % speeds[i] > 0:
            day.append((100 - progresses[i]) // speeds[i] + 1)
        else:
            day.append((100 - progresses[i]) // speeds[i])
    
    answer.append(1)
    delay = day[0]
    for i in range(1, len(day)):
        if day[i] <= delay:
            answer[-1] += 1
        else:
            answer.append(1)
            delay = day[i]
    
    return answer
```
