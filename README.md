# layout

## 아래처럼 만들기
![img](https://cloud.githubusercontent.com/assets/13831179/11373068/d64b977c-9313-11e5-8e55-ead374b8fe0a.png)

## 알아야 하는 내용
- box model
- block & inline element
- position
- float
- box-sizing
- clear


## 참고
https://drafts.csswg.org/css2/


-------------------------수업시간에 한 내용 정리한 것입니다. 참고만 해주세요^^(by 동준)----------------------------

 -우리가 만드는 CSS코드는 모든걸 ‘박스’로 다룬다고 생각해야 한다.
-보통 width는 패딩까지가 width이다(border 제외)
-한 라인에서 넘치면 그 아래로 대상이 내려가는 것을 normal flow라고 한다.

1. block과 inline의 개념차이
          -블록엘리먼트는 높이값을 지정할 수 있다.(ex)div)
          -반면에 인라인은 지정할 수 없다(ex)span)
          -블록엘리먼트는 기본적으로 오른쪽으로 붙지 않고 밑으로 떨어진다.
          -span은 너비를 갖는 텍스트를 넣으면 오른쪽으로 붙게 된다.

2. floating에 대한 이미지 이해
          -div영역에서 foating으로 떼는 순간 그 공간이 딱 비게 된다.

3. clear : both
          -clear:both는 이 시점부터 ‘나는 전체에 floating되는 개념을 막겠다는 뜻이다.'

4. 예제에서 content 아래에 margin 10px을 주는 방법

          1) <div class=“clear”></div> 가짜 div를 만들어서 clear both를 해준다.
          2) :after를 이용하여 clear:both가 실행되게 유도한다.
          3) 나의 마진은 누군가의 패딩이다. parents의 padding은 child의 margin이다.

5. CSS하다보면 생기는 문제
(내가 알고 있는게 아닌 것처럼 동작하는 경우가 많다)

     1) position

          내가 만약에 특정 엘리먼트에 2px씩 이동을 하고 싶어서 left:2px, top:2px;을 줄 수 있는데
          이 때 움직이는 조건이 있다. 기본적으로 position은 default값이 static이다. 이 상태에서는
          아무리 값을 준다해도 변함이 없다. 때문에 positioned라는 static이 아닌 값들을 지정해 주어야
          한다. 무언가의 위치를 바꾸기 위해서는 포지션이된 엘리먼트여야 하기 때문이다.

     2) floating을 하게되면

          floating을 하게 되면 엘리먼트들이 block으로 변하게 된다.
          때문에 span으로 줘도 플로팅을 하면 블록으로 움직이기 때문에 이를 인지하고 있어야 한다.

     3) 위치에 대한 우선순위

          position - float - display
          좌측으로 갈수록 우선순위가 높기 때문에 우선순위가 높은 부분에 특정 값을 지정하면
          하위에 있는 명령어들이 작동되지 않을 확률이 크다.

