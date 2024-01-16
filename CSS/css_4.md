# 4 이미지와 그라데이션 효과로 배경 꾸미기

# 4.1 배경색과 배경 범위 지정하기
웹 문서의 전체 배경뿐만 아니라 텍스트, 목록 등 특정한 요소에도 배경을 지정할 수 있다. 먼저 배경색을 지정하는 방법을 알아보자

### 배경색을 지정하는 background-color
배경색을 지정하려면 배경을 넣고 싶은 요소의 스타일 규칙을 만들 때 **background-color 속성**을 지정한다. background-color는 앞에서 설명한 16진수나 rgb값 또는 색상 이름을 사용해서 지정한다. <br>
글꼴이나 글자 크기 등은 body 태그 선택자에서 지정하면 문서 전체에 상속되어 하위 요소 스타일을 수정하지 않는 한 문서 전체에 똑같이 적용되지만 background-color은 예외적으로 상속되지 않는다. 기본적으로 모든 웹 문서 요소의 배경이 투명하므로 body 스타일로 지정한 문서 배경이 그대로 비치는 것일 뿐 상속된 것은 아니다.
#### background-color 예시
```
background-color: #008000;
background-color: rgb(0,128,0);
background-color: green;
```
### 배경색의 적용 범위를 조절하는 background-clip
배경을 넣고 싶은 요소마다 속성을 입력하면 되지만 박스 모델 관점에서 배경의 적용 범위를 조절할 수 있다. 즉, 박스 모델의 가장 외곽인 border까지 적용할지, 테두리를 뺴고 padding 범위까지 적용할지, 아니면 내용 부분에만 적용할지 선택할 수 있다.
#### background-clip 속성값
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>border-box</td>
      <td>박스 모델의 가장 외곽인 border까지 적용한다. 기본값</td>
    </tr>
    <tr>
      <td>padding-box</td>
      <td>박스 모델에서 테두리를 뺀 패딩 범위까지 적용한다.</td>
    </tr>
    <tr>
      <td>content-box</td>
      <td>박스 모델에서 내용(콘텐츠) 부분에만 적용한다.</td>
    </tr>
  </tbody>
</table>

# 4.2 배경 이미지 지정하기

### 웹 요소에 배경 이미지를 넣는 background-image
웹 요소에 배경 이미지를 넣을 때 가장 기본으로 알아 둘 속성은 background-image이다. 다음 기본형과 같이 url()에 이미지 파일 경로를 넣어서 사용한다.
#### background-image 기본형
```
background-image: url('이미지 파일경로')
```
### 배경 이미지의 반복 방법을 지정하는 background-repeat 속성
background-reapeat 속성을 사용하면 배경 이미지를 가로와 세로 중에서 어떤 방향으로 반복할지 지정하거나, 반복하지 않고 한 번만 니타나게 할 수 있다.
#### background-repeat속성표

<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>reapeat</td>
      <td>브라우저 화면에 가득 찰 때까지 가로와 세로를 반복한다. 기본값</td>
    </tr>
    <tr>
      <td>repeat-x</td>
      <td>브라우저 화면 너비에 가득 찰 때까지 가로로 반복한다.</td>
    </tr>
    <tr>
      <td>repeat-y</td>
      <td>브라우저 화면 높이에 가득 찰 때까지 세로로 반복한다.</td>
    </tr>
    <tr>
      <td>no-repeat</td>
      <td>한 번만 표시하고 반복하지 않는다.</td>
  </tbody>
</table>

### 배경 이미지의 위치를 조절하는 background-position 속성
background-position 속성을 이용하면 이미지의 수평 위치 또는 수직 위치의 값을 지정할 수 있다. 속성 값을 2개로 지정할 경우, 첫 번째 값은 수평 위치이고 두 번째 값이 수직 위치가 된다. 속성값을 1개만 지정하면 지정한 값은 수평 위치이고 수직 위치는 50%나 center로 간주한다. <br>
배경 이미지 위치 지정은 **키워드(수평위치: left, center, right 수직위치: top, bottom, center), 백분율(%), 크기(px)** 로 지정할 수 있다.

### background-origin 속성을 이용한 배경 이미지 적용 범위 조절
박스 모델에 padding이나 border가 있다면 배경 이미지를 padding까지 표시하거나 border까지 포함해서 표시할 수 있다. 
#### background-origin의 속성값
<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>content-box</td>
      <td>박스 모델에서 내용 부분에만 배경이미지를 표시한다.</td>
    </tr>
    <tr>
      <td>padding-box</td>
      <td>박스 모델에서 패딩까지 배경이미지를 표시한다. 기본값</td>
    </tr>
    <tr>
      <td>border-box</td>
      <td>박스 모델에서 border까지 배경이미지를 표시한다.</td>
    </tr>
  </tbody>
</table>


























































































