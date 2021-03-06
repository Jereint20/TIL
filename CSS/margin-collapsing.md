# 마진겹침(margin-collapsing)

- 2019.04.17: 첫 작성
- 2019.04.19: 시각적 예시자료 보강

## 마진 겹침 현상

- element 간에 margin 이 겹치는 현상
  - 수직 margin (top 과 bottom)에서 발생
  - 특히, element 가 비어있는 경우에는 완벽히 겹치는 case 발생
  - margin 값이 더 큰쪽을 따라간다.
  - css framework 에서는 보통 margin bottom 만 사용함으로써 해결하는 것 같다.(정확하게 확인한 내용 아님, 경험적인 내용)

### 예시

![Margin Collapse Example](../img/collapsing-margins-in-css.png)

- _출처: [http://blog.firsthand.ca/2010/10/collapsing-margins-in-css.html](http://blog.firsthand.ca/2010/10/collapsing-margins-in-css.html)_

## 출처

- [생활코딩 css 수업: 마진겹침](https://opentutorials.org/course/2418/13464)
- [MDN: 마진 상쇄 정복](https://developer.mozilla.org/ko/docs/Web/css/css_Box_Model/Mastering_margin_collapsing)
- [BLOG - wystan's tales - css 이야기: 마진 병합(collapsing margins)](http://blog.wystan.net/2008/09/10/css-collapsing-margins)
