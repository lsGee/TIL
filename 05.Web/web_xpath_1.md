# XPath 기본 표현식

* `/` :  **루트 노트**부터 순서대로 탐색해나감(**절대 경로** 탐색)

* `//` :  **지정된 노드**에서부터 순서대로 탐색해나감(**상대 경로** 탐색)

  * `//` 하나만 쓰면, 루트 노드의 하위 노드를 모두 선택하게 됨

* `.` :  현재 노드 선택

  * `.//` :  현재 노드의 하위 노드 모두 선택

* `..` :  현재 노드의 부모노드 선택

* `@` :  속성 노드를 선택

* `::` :  왼쪽은 검색 방향, 오른쪽은 검색할 노드

  * `child::language` :  현재 노드의 자식 노드 중 `<language>`요소를 모두 선택함.

  * `attribute::version` :   현재 노드의 version 속성 노드를 선택함.

  * `descendant::*` :  현재 노드의 자손 노드를 모두 선택함.

  * `descendant::text()` :  현재 노드의 자손 노드 중 텍스트 노드를 모두 선택함.

  * `ancestor::language` :  현재 노드의 조상 노드 중 `<language>`요소를 모두 선택함.

  * `ancestor-or-self::language` :  현재 노드와 현재 노드의 조상 노드 중 `<language>`요소를 모두 선택함.

  * `child::*/child::category` :  현재 노드의 자식 노드의 자식 노드 중 `<category>`요소를 모두 선택함.



**참고사이트**

[XPath 표현식 - 위치경로](http://tcpschool.com/xml/xml_xpath_pathExpression)

