# [스택/큐] 주식가격

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42584



## Code

```python
def solution(prices):
    answer = []
    num = len(prices)
    
    for i in range(num):
        sec = 0
        for j in range(i+1, num):
            sec += 1
            if prices[i] > prices[j]: break
        answer.append(sec)
    
    return answer
```
