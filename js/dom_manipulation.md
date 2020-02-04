# DOM Manipulation

- 작성일자: 2020.02.03

## DOM (Document Object Modal)

- html 문서를 tree 형태로 구성하는 것
- JavaScript 를 통해 동적으로 변경 가능
- W3C의 공식 표준, 플랫폼/프로그래밍 언어 중립적
- HTML 문서에 대한 모델 구성 & HTML 문서 내의 각 요소에 접근 및 수정 기능 제공

## DOM tree

![](https://poiemaweb.com/img/dom-tree.png)

- 크게 4종류의 Node 로 구성
- Document Node(문서 노드)
  - tree 최상위에 존재
  - DOM tree 의 시작점(entry point)
- Element Node(요소 노드)
  - HTML 의 요소 표현
  - 문서의 구조 서술(tree 관계)
- Attribute Node(어트리뷰트 노드)
  - HTML 요소의 attribute 표현
  - class 등 수정 가능
- Text Node(텍스트 노드)
  - DOM tree 의 최종단 (자식 Node 를 가질 수 없음)
  - HTML 요소 안의 text 값

## DOM Query / Traversing (DOM 선택 및 접근)

### 하나의 Node 선택

- 특성

  - Return: Element Node 를 상속받은 Object
  - 복수개가 선택된 경우 맨 앞 1개 선택

- 종류
  - document.getElementById(id)
    - id 선택
  - document.querySelector(cssSelector)
    - css Selector 를 사용해서 node 선택
      - element, id, class 등
      - 참고: [css Selector Reference | w3schools](https://www.w3schools.com/cssref/css_selectors.asp)

### 여러 개의 Node 선택

- 종류
  - document.getElementsByClassName(class)
    - 동일한 class 이름을 가진 모든 node 선택
    - Return: HTMLCollection(live)
      - 실시간으로 값이 변하기 때문에 주의해야 함
  - document.getElementsByTagName(tagName)
    - 태그명(element) 이 같은 모든 node 선택
    - Return: HTMLCollection(live)
      - 실시간으로 값이 변하기 때문에 주의해야 함
  - document.querySelectorAll(selector)
    - css Selector 를 사용해서 모든 node 선택
    - Return: NodeList(non-live)

### DOM Traversing (탐색)

- 종류
  - parentNode
    - 선택된 node 의 부모 node 탐색
    - Return: Element Node 를 상속받은 Object
  - firstChild, lastChild, firstElementChild, lastElementChild
    - 선택된 node 의 자식 node 탐색
    - 이름에 따라 첫번째 혹은 마지막 node 선택
    - Return: Element Node 를 상속받은 Object
  - hasChildNodes()
    - 자식 node 가 있는지 확인
    - Return: Boolean
  - childNodes
    - Text node 를 포함한 모든 자식 요소 탐색
    - Return: NodeList(non-live)
  - child
