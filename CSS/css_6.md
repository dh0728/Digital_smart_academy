# 트랜지션과 애니메이션

## 6.1 변형 알아보기

### transform과 변형 함수
css에서 변형을 적용하려면 transform 속성과 변형 함수 이름을 함께 작성해야 한다.
```
기본형
trnasfrom: 함수

예시
.photo { transform: translate(50px, 100px);}
```

2차원 변형과 3차원 변형
**2차원 변형은 웹 요소를 평면으로 번형**한다. 수평 방향으로 이동하거나 수직 방향으로 왜곡한다. 2차원 좌표를 사용하는데 x축은 오른쪽으로 갈수록 커지고 y축은 아래로 내려갈수록 값이 커진다. <br>
**3차원 변형** 은 x축과 y축에 원근감을 주는 z축을 추가해서 변형한다. 3차원 변형에서 z축은 앞뒤로 이동하며, 보는 사람 쪽으로 다가올수록 값이 커지고 뒤로갈수록 값이 작아진다.


#### 2차원 변형함수
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>:translate(tx, ty)</td>
    <td>지정한 크기만큼 x축, y축으로 이동한다.</td>  
  </tr>
  <tr>
    <td>translateX(tx)</td>
    <td>지정한 크기만큼 x축으로 이동한다.</td> 
  </tr>
  <tr>
    <td>translateY(ty)</td>
    <td>지정한 크기만큼 y축으로 이동한다.</td>
  </tr>
  <tr>
    <td>scale(sx,sy)</td>
    <td>지정한 크기만큼 x축과 y축으로 확대, 축소한다.</td>
  </tr>
  <tr>
    <td>scaleX(sx)</td>
    <td>지정한 크기만큼 x축으로 확대, 축소한다.</td>
  </tr>
  <tr>
    <td>scaleY(sy)</td>
    <td>지정한 크기만큼 y축으로 확대, 축소한다.</td> 
  </tr>
  <tr>
    <td>rotate(각도)</td>
    <td>지정한 각도만큼 회전한다.</td>
  </tr>
  <tr>
    <td>skew(ax, ay)</td>
    <td>지정한 각도만큼 x축과 y축으로 왜곡한다.</td>
  </tr>
  <tr>
    <td>skewX(ax)</td>
    <td>지정한 각도 만큼 x축으로 왜곡한다.</td>
  </tr>
  <tr>
    <td>skewY(ay)</td>
    <td>지정한 각도 만큼 y축으로 왜곡한다.</td>
  </tr> 
</table>

#### 3차원 변형 함수
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>:translate(tx, ty tz)</td>
    <td>지정한 크기만큼 x축, y축, z축으로 이동한다.</td>  
  </tr>
  <tr>
    <td>translateZ(tZ)</td>
    <td>지정한 크기만큼 z축으로 이동한다.</td> 
  </tr>
  <tr>
    <td>scale3s(sx,sy, sz)</td>
    <td>지정한 크기만큼 x축, y축, z축으로 확대, 축소한다.</td>
  </tr>
  <tr>
    <td>scaleZ(sz)</td>
    <td>지정한 크기만큼 z축으로 확대, 축소한다.</td>
  </tr>
  <tr>
    <td>rotate(rx, ry, 각도)</td>
    <td>지정한 각도만큼 회전한다.</td>
  </tr>
  <tr>
    <td>rotate3d(rx, ry, rz, 각도)</td>
    <td>지정한 각도만큼 회전한다.</td>
  </tr>
  <tr>
    <td>rotateX(각도)</td>
    <td>지정한 각도만큼 x축으로 회전한다.</td>
  </tr>
  <tr>
    <td>rotateY(각도)</td>
    <td>지정한 각도만큼 y축으로 회전한다.</td>
  </tr>
  <tr>
    <td>rotateZ(각도)</td>
    <td>지정한 각도만큼 z축으로 회전한다.</td>
  </tr>
  <tr>
    <td>perspective(길이)</td>
    <td>입체적으로 보일 수 있도록 깊잇값을 지정한.</td>
  </tr> 
</table>


# 6.2 트랜지션 알아보기

## 트랜지션이란
**트랜지션(transition)**은 웹 요소의 배경색을 바꾸거나 도형의 테두리를 사각형에서 원형으로 바꾸는 것처럼 스타일 속성을 바뀌는 것을 말한다. 트랜지션에서는 스타일이 바뀌는 시간을 조절하여 자바스크립트를 사용하지 않고도 애니메이션 효과를 낼 수 있다. 
#### 트랜지션의 속성
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>transition-property</td>
    <td>트랜지션 대상을 지정한다.</td>  
  </tr>
  <tr>
    <td>transition-duration</td>
    <td>트랜지션을 실행할 시간을 지정한다.</td> 
  </tr>
  <tr>
    <td>transition-timing-function</td>
    <td>트랜지션의 실행 형태를 지정한다.</td>
  </tr>
  <tr>
    <td>transition-delay</td>
    <td>트랜지션의 지연 시간을 조정한다.</td>
  </tr>
  <tr>
    <td>transition</td>
    <td>transition-property, transition-duration, transition-timing-function, transition-delay 속성을 한꺼번에 정의한다.</td>
  </tr>
  <tr>
    <td>cubic-bezuer(n,n,n,n)</td>
    <td>베지에 함수를 정의해서 사용한다. 이떄 n값은 0~1사이만 사용할 수 있다.</td>
  </tr>
</table>



### transition-property 속성
트랜지션을 만들려면 맨 먼저 transition-property 속성을 사용하여 어떤 속성에 트랜지션을 적용할 것인지 대상을 지정해야 한다.

#### transition-property 기본형
```
/* 기본형 */
transition-property : all | none | <속성이름>

/* 예시 */
transition-property : all;                 /* 해당 요소의 모든 속성에 트렌지션 적용
transition-property : background-color;    /* 해당 요소의 배경색에 트렌지션 적용
transition-property : width, height;       /* 해당 요소의 너비와 높이에 트렌지션 적용
```

### transition-duration 속성
transition-property로 트랜지션 대상을 지정했다면 다음으로 진행 시간을 지정해야 속성이 자연스럽게 바뀌는 애니메이션 효과를 만들 수 있다. 진행 시간은 **transition-duration 속성**으로 지정할 수 있다. 지정할 수 있는 시간 단위는 초 또는 밀리초 이다. 트랜지션의 대상 속성일 여러 개라면 진행 시간도 쉽표(,)로 구분해서 여러 개를 지정할 수 있다.
```
/* 기본형 */
transition-duration: <시간>

/* 예시 */
transition-property: width, height;
transition-duration: 2s, 1s;
```

### transition-timing-function 속성
transition-timing-function 속성을 사용하면 트랜지션 효과의 시작, 중간, 끝에서 속도를 지정해 전체 속도 곡선을 만들 수 있다. 속도 곡선은 미리 정해진 키워드나 베지에 곡선을 이용해 표현 한다.
```
/* 기본형 */
transition-timing-function: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(n, n, n, n)
```
#### transition-timing-function 속성값

<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>ease</td>
    <td>처음에는 천천히 시작하고 점점 빨라지다가 마지막엔 천천히 끝낸다. 기본값</td>  
  </tr>
  <tr>
    <td>linear</td>
    <td>시작부터 끝까지 똑같은 속도로 진행한다.</td> 
  </tr>
  <tr>
    <td>ease-in</td>
    <td>느리게 시작한다.</td>
  </tr>
  <tr>
    <td>ease-out</td>
    <td>느리게 끝낸다.</td>
  </tr>
  <tr>
    <td>ease-in-out</td>
    <td>느리게 시작하고 느리게 끝난다.</td>
  </tr>
  <tr>
    <td>cubic-bezuer(n,n,n,n)</td>
    <td>베지에 함수를 정의해서 사용한다. 이떄 n값은 0~1사이만 사용할 수 있다.</td>
  </tr>
</table>

### transition-delay 속성
transition-delay 속성은 트랜지션 효과를 언제부터 시작할 것인지 설정한다. 사용할 수 있는 값은 초나 밀리초이고 기본값은 0이다.
```
/*기본형*/
transiton-delay: <시간>
```

### transition 속성
트랜지션 적용 대상이 전체이고 각각의 진행시간이 같다면 transition 속성으로 한꺼번에 할 수 있다.
```
/* 기본형 */
transition : <transition-property값> | <transition-duration값> | <transition-timing-function값> | <transition-delay값>

/* 예시 */

transition: 2s ease-in

/*
transition-property: 기본값 all
transition-duration: 2s
transition-timing-function: ease-in
transition-delay: 기본값 0   
 */
```

# 6.3 애니메이션 알아보기

### CSS 애니메이션에서 사용하는 속성
CSS3의 animation 속성을 사용하면 자바스크립트를 사용하지 않고도 웹 요소에 애니메이션을 추가할 수 있다. animation 속성은 특정 지점에서 스타일을 바꾸면서 애니메이션을 만드는데, 이렇게 애니메이션 중간에 스타일이 바뀌는 지점을 **키프레임(keyframe)** 이라고 한다. 키프레임은 **@keyframes**속성으로 정의하고, animation속성과 그 하위 속성을 이용해서 애니메이션의 실행 시간이나 반복 여부 등을 지정한다. 

#### 애니메이션 속성
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>@keyframes</td>
    <td>애니메이션이 바뀌는 지점을 지정한다.</td>  
  </tr>
  <tr>
    <td>animation-delay</td>
    <td>애니메이션의 시작 시간을 지정한다.</td> 
  </tr>
  <tr>
    <td>animation-direction</td>
    <td>에니메이션을 종료한 뒤 처음부터 시작할지, 역방향으로 진행할지 지정한다.</td>
  </tr>
  <tr>
    <td>animation-duration</td>
    <td>애니메이션의 실행 시간을 지정한다.</td>
  </tr>
  <tr>
    <td>animation-iteration-count</td>
    <td>애니메이션의 반복 횟수를 지정한다.</td>
  </tr>
  <tr>
    <td>animation-name</td>
    <td>@keyframes로 설정해 놓은 중간 상태를 지정한다.</td>
  </tr>
  <tr>
    <td>animation-timng-function</td>
    <td>키프레임의 전환 형태를 지정한다.</td>
  </tr>
  <tr>
    <td>animation</td>
    <td>animation 속성을 한꺼번에 묶어서 지정한다.</td>
  </tr>  
</table>

### @keyframes 속성, animation-name속성
애니메이션의 시작과 끝을 비롯하여 상태가 바뀌는 부분이 있으면 **@keyframes 속성을 이용해 바뀌는 지점을 설정**한다. 또한 웹 문서에서는 애니메이션을 여러 개 정의할 수 있으므로 **이름**을 이용해 애니메이션을 구별해야 한다. 이떄 **animation-name 속성으로 어떤 애니메이션을 사용할지 이름으로 구분**한다. <br>
**@keyframes**속성에서 사용하는 선택자는 스타일 속성값이 바뀌는 지점을 가르킨다. 예를 들어 애니메이션의 중간 지점을 추가하려면 시작 위치를 0%, 끝 위치를 100%로 놓고 50%위치에 키프레임을 추가하면 된다. 시작과 끝 위치만 사용하려면 0%, 100%와 같은 값 대신 from과 to라는 키워드를 사용해도 된다.
```
/*기본형*/
@keyframes <이름> {
  <선택자> { <스타일> }
}

animation-name: <키프레임 이름> | none
```
### animation-duration 속성
animation-duration 속성은 **애니메이션을 얼마 동안 재생할 것인지 설정**한다. 사용할 수 있는 속성값은 초와 밀리초 같은 시간 단위이다. 기본값은 0이므로 속성값을 지정하지 않으면 애니메이션은 실행되지 않는다. 
```
/*기본형*/
animation-duration: <시간>
```

#### 애니메이션의 지점, 이름, 실행시간 지정 예시
```
#box1 {
  background-color: #4cff00;
  border: 1px solid transparent;
  animation-name: shape;         /*애니메이션 지정*/ 
  animation-duration: 3s;        /*애니메이션 실행시간*/ 
}
#box2 {
  background-color: #000f00;
  border: 1px solid transparent;
  animation-name: rotate;        /*애니메이션 지정*/                  
  animation-duration: 2s;        /*애니메이션 실행시간*/
}
@keyframes shape {
  from { border: 1px solid transparent; }  /* 1px 투명 테두리에서 */
  to {
    border: 1px solid #000;                /* 검은색 테두리로 변경 */
    border-radius: 50%;                    /* 테두리를 둥글게 변경 */
  }
}
@keyframes rotate {
  from { transform: rotate(0deg); }        /* 0도에서 시작해서 */
  to { transform: rotate(45deg);]          /* 45도까지 회전하기 */
}
```

### animation-direction 속성
애니메이션은 기본적으로 keyframes에서 정의한 from에서 to 순서로 진행하는데 animation-direction속성을 사용해서 진행 방향을 바꿀 수 있다.
```
/*기본형*/
animation-direction: normal | reverse | alternate | alternate-reverse
```

#### animation-direction 속성값
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>normal</td>
    <td>애니메이션을 from에서 to로 진행한다. 기본값</td>  
  </tr>
  <tr>
    <td>reverse</td>
    <td>애니메이션을 to에서 from으로, 원래 방향과는 반대로 진행한다.</td> 
  </tr>
  <tr>
    <td>alternate</td>
    <td>홀수 번째는 normal로, 짝수 번쨰는 reverse로 진행한다.</td>
  </tr>
  <tr>
    <td>alternate-reverse</td>
    <td>홀수 번째는 reverse로, 짝수 번째는 normal로 진행한다.</td>
  </tr>
</table>

### animation-iteration-count 속성
애니메이션을 반복해서 보여 줘야 할 때 사용해 반복 횟수를 정한다.
```
/*기본형*/
animation-iteration-count: <숫자> | infinite
```
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tr>
    <td>숫자</td>
    <td>애니메이션 반복 횟수를 정한다</td>  
  </tr>
  <tr>
    <td>infinite</td>
    <td>애니메이션을 무한 반복한다.</td> 
  </tr>
</table>


























































