# [해시] 위장

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42578



## Code

```python
def solution(clothes):
    answer = 1
    dic = {}
    
    for i in range(len(clothes)):
        try: dic[clothes[i][1]]
        except: dic[clothes[i][1]] = 0
        dic[clothes[i][1]] += 1
        
    for i in dic.keys():
        answer *= (dic[i] + 1)
    
    return answer - 1
```

* `dic` :  의상종류를 key, 해당 종류의 의상(이름) 수를 value로 갖는 딕셔너리
* 의상 조합 수는 각 의상종류별 (의상수 + 1) 값을 모두 곱한 값과 같음 (해당 종류를 아예 입지 않는 경우를 고려해 1을 더한 것!)
* 단, **스파이는 하루에 최소 한 개의 의상을 입는다**는 전제조건이 존재하므로 모두 입지 않는 경우를 제외하기 위해 리턴시 1을 빼줌