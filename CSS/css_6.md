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































