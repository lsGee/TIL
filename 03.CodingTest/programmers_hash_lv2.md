# [해시] 전화번호 목록

> **문제**
>
> https://programmers.co.kr/learn/courses/30/lessons/42577



## Code

```python
def solution(phone_book):
    answer = True
    
    phone_len = list(map(lambda x:len(x), phone_book))
    pmin = min(phone_len)
    dic = dict(zip(phone_book, phone_len))
    phone_min = [k for k, v in dic.items() if v == pmin]
    phone_oth = [k for k, v in dic.items() if v != pmin]
    
    for i in phone_oth:
        if i[:pmin] in phone_min:
            return False
    
    return answer
```



## map()

```python
map(함수, Iterable 객체)
```

* 해당 Iterable 객체에 지정한 함수를 적용한 Iterator를 리턴해준다.
* 리턴된 Iterator를 list() 등의 함수에 담아 다시 Iterable 객체로 만들어 사용할 수 있다.





**참고) `Iterable` 과  `Iterator`**

* `Iterable`

  멤버들을 하나씩 반환 가능한 객체(object)

  Ex. 문자열, list, tuple

* `Iterator`

  next() 메서드를 사용해 끄집어낼 수 있는 객체(object)

  iter() 메서드를 활용해 `Iterable` 을  `Iterator` 로 변환할 수 있음!

