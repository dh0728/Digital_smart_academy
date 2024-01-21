# 7 반응형 웹과 미디어 쿼리

## 7.1 반응형 웹 알아보기

### 반응형 웹 디자인이란 
스마트폰, 태블릿, 스마트TV 등 브라우저 환경이 빠뀜에 따라 기존 웹 사이트의 내용을 유지하면서 다양한 화면 크기에 맞게 표기 할 수 있도록 하는 것을 **반응형 웹 디자인(responsive web disign)** 이라고 한다.

### 모바일 기기를 위한 뷰포트
반응형 웹 디자인에서 기본적으로 알아야 할 것은 **뷰포트(viewport)** 이다. PC에 맞게 제작한 웹 사이트를 모바일 기기에 접속해서 모든 내용이 작게 표시된다. 그 이유는 pc 화면과 모바일 화면에서 표시되는 픽셀의 차이 때문인데, 뷰포트를 지정하면 접속한 기기의 화면에 맞추어 확대하거나 축소해서 표시할 수 있다. 이때 '뷰포트'란 스마트폰 화면에서 실제 내용이 표시되는 영역이다. 

### 뷰포트 지정하기
뷰포트는 meta 태그를 이용해 head 태그 사이에 작성한다. 

#### 뷰포트의 속성
<table>
  <tr>
    <th>종류</th>
    <th>설명</th>
    <th>사용 가능한 값</th>
    <th>기본값</th>
  </tr>
  <tr>
    <td>width</td>
    <td>뷰포트 너비</td>
    <td>device-width 또는 크기</td>
    <td>브라우저 기본값</td>
  </tr>  
  <tr>
    <td>height</td>
    <td>뷰포트 높이</td>
    <td>device-height 또는 크기</td>
    <td>브라우저 기본값</td>
  </tr>
  <tr>
    <td>user-scalable</td>
    <td>확대, 축소 가능 여부</td>
    <td>yes 또는 no <br> (yes는 1로, device-width와 <br> device-height값은 10으로 간주</td>
    <td>yes</td>
  </tr>
  <tr>
    <td>initial-scale</td>
    <td>초기 확대, 축소 값</td>
    <td>1~10</td>
    <td>1</td>
  </tr>
</table>

```
/* 기본형 */
<meta name="viewport" content="속성1=값1, 속성2=값2 .....">

/* 예시 */
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### 뷰포트 단위 
뷰포트 개념이 등장하기 전까지는 CSS에서 크기를 지정할 때 주로 px, %의 단위를 사용했지만 이제는 다음과 같이 뷰포트를 기준으로 하는 단위를 사용할 수 있다.
#### 뷰포트 단위 

<table>
  <tr>
    <th>종류</th>
    <th>설명</th>
  </tr>
  <tr>
    <td>vw(viewport width)</td>
    <td>1vw는 뷰포트 너비의 1%와 같다.</td>
  </tr>  
  <tr>
    <td>vh(viewport height)</td>
    <td>1vh는 뷰포트 높이의 1%와 같다.</td>
  </tr>
  <tr>
    <td>vmin(viewport minimum</td>
    <td>뷰포트의 너비와 높이중 작은 값의 1%와 같다.</td>
  </tr>
  <tr>
    <td>vmax(viewport maximum)</td>
    <td>뷰포트의 너비와 높이 중에서 큰 값의 1%와 같다.</td>
  </tr>
</table>

## 7.2 미디어 쿼리 알아보기

### 미디어 쿼리 
CSS 모듈인 **미디어 쿼리(media queries)** 는 사이트에 접속하는 장치에 따라 특정한 CSS 스타일을 사용하는 방법이다. 미디어 쿼리를 사용하면 접속하는 기기의 화면 크기에 따라 레이아웃이 달라진다.

### 미디어 쿼리 구문
미디어 쿼리는 **@media** 속성을 사용해 특정 미디어에서 어떤 CSS를 적용할 것인지 지정해 준다. 미디어 쿼리 구문은 stlye태그 사이에 사용하며 대소 문자를 구별하지 않는다. 기본적으로 미디어 유형을 지정해야 하고 필요한 경우 and 연산자로 조건을 적용한다. 
```
/* 기본형 */
@media [only | not] 미디어 유형 [and 조건] * [and 조건]

/*
only: 미디어 쿼리를 지원하지 않는 웹 브라우저에서는 미디어 쿼리를 무시하고 실행하지 않는다.
not: not 다음에 지정하는 미디어 유형을 제외한다. 예를 들어 not tv라고 지정하면 tv를 제외한 미디어 유형에만 적용된다.
and: 조건이 여러 개 연결해서 추가할 수있다.
*/

/* 예시 */
@media screen and (min-width: 780px) and max-width: 1439px){

}
/* 미디어 유형이 screen이면서 최소 너비가 768px이고 최대 너비는 1439px 일 경우 */
```
   










































