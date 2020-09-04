# [해시] 베스트 앨범

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42579



## Code

```python
def solution(genres, plays):
    answer = []
    stotal = len(genres)
    genre_type = list(set(genres))
    dic = {}
	
    # 장르별 딕셔너리 공간 생성
    for i in genre_type:
        dic[i] = {}
    
    # 장르별 딕셔너리 공간에 고유번호(key), 재생수(value) 추가
    for i in range(stotal):
        dic[genres[i]][i] = plays[i]
        
    # 정렬
    gtotal = []
    for i in dic.keys():
        gtotal.append((i, sum(dic[i].values())))
        dic[i] = sorted(dic[i].items(), key=lambda x:x[1], reverse=True)
    
    gtotal = sorted(gtotal, key=lambda x:x[1], reverse=True)
    
    for i in gtotal:
        count = 0
        for j in dic[i[0]]:
            if count == 2: break
            answer.append(j[0])
            count += 1
    
    return answer
```



## 딕셔너리 정렬하기

**람다 함수와 sorted 함수 사용**

```python
# Key 기준 정렬
sorted(dic.items(), key=lambda x:x[0], reverse=True)

# Value 기준 정렬
sorted(dic.items(), key=lambda x:x[1], reverse=True)
```



`.items()` 메소드를 사용해 key, value 쌍을 튜플로 만들어준 후 자리값을 활용해 정렬 기준을 지정할 수 있음