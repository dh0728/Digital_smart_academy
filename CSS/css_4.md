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

# 4.2 배경 이미지 지정하

