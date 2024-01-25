# 5 DOM의 기초

## 5.1 DOM과 DOM 트리

### 문서 객체 모델(DOM)이란?
자바스크립트를 이용하여 웹 문서에 접근하고 제어할 수 있도록 객체를 사용해 웹 문서를 체계적으로 정리하는 방법이다. <br>
웹 문서를 구조화한 **DOM 트리**와 **이벤트**를 정리해 놓은 표본이다. <br>

웹에서는 자바스크립트를 사용하는 이유는 어떤 조건이 주어지거나 사용자의 동작이 있을 때 웹 문서 전체 또는 일부분이 동적으로 반응하게 하는 것이다. 이렇게 하려면 웹 문서의 모든 요소를 따로 제어할 수 있어야 한다. 

### DOM 트리
웹 문서에 있는 요소들 간의 **부모, 자식 관계**를 계층 구조로 표시한 것이다. 나무 형태로 되어 있어 **DOM 트리**라고 한다. DOM은 문서의 요소 뿐만 아니라 각 요소의 내용과 속성도 자식으로 나타낸다.<br>
**노드(node) :** DOM 트리에서 가지가 갈라져 나간 항목
**루트 노드(root node) :** DOM 트리의 시작 부분(html)

<img src="./image/domtree.png">

## 5.2 웹 요소에 접근하기


### 웹 요소에 접근하기
웹 문서에서 원하는 요소를 찾아가는 것을 **"접근한다(access)"** 라고 한다.

#### querySelector(), querSelectorAll()함수 
**선택자 :** id 이름 앞에는 해시 기호(#), class 이름 앞에는 마침표(.), 태그는 기호 없이 태그명을 사용
**반환값 :** querySelector() 메서드는 한 개의 값만 반환하고 querySelectorAll() 메서드는 반환 값이 여러 개일 때 모두 반환한다. **노드 리스트로 저장됨**

```
querySelector(선택자)

querySelectorAll(선택자)
```
### getElement~ 함수
예전부터 사용하던 방법으로 id, class, 태그명을 사용해 접근한다.

#### getElementByld()
```
document.getElementByld("id명")
```

#### getElementsByClassName()
```
document.getElementsByClassName("클래스명")
```

#### getElementsByTagName()
```
document.getElementsTagName("태그명")
```

#### getElement와 querySelector()의 차이점
id, class, 태그 이름을 사용해서 접근하는 것은 같지만 querySelector()을 사용하면 둘 이상의 선택자를 조합해서 접근할 수 있다.

### 웹 요소 내용 가져오기 및 수정하기
접귾나 요소의 텍스트 내용을 가져오거나 지정할 때는 innerText, innerHTMl, textContent 프로퍼티 사용한다. 화면에서 감춘 요소에서도 내용을 가져올 수 있고, 소스에 공백이 여러 개일 경우 그 공백도 모두 가져온다.

**innerText :** 순수 텍스트를 가져오거나, 해당 요소에 텍스트 지정 <br>
**innerHTML :** 태그와 함께 텍스트를 가져오거나, 해당 요소에 태그와 함께 텍스트 지정<br>
**textContent :** 텍스트를 가져오되, 화면에 보이는대로가 아니라 소스에 있는대로 가져온다.

```
요소.innerText 
요소.innerHTML 
요소.text.Content 

요소.innerText = "내용"
요소.innerHTML = "내용"
요소.text.Content = "내용"
```

#### 클릭으로 텍스트 내용 바꾸는 예시
```
// html
<h1 id="title">My Profile</h1>
  <div id="profile">
    <img src="images/pf.png" alt="도레미">
    <div id="desc">
      <p class="user">이름 : 도레미</p>
      <p class="user">주소 : somewhere</p>
      <p class="user">연락처 : 1234-5678</p>
    </div>
  </div>

// js파일
const title = document.querySelector("#title")

title.onclick=function() {
  title.innerText="프로필";
}

// 화살표 함수 사용시
const title =document.querySelector("#title")

title.onclick= () => title.innerText="프로필";
```

## 5.3 자바스크립트로 스타일 수정하기

### CSS 속성에 접근하기
자바스크립트를 이용하면 스타일 속성의 값을 가져오거나 원하는 값으로 수정할 수있다.
```
요소.style.속성명
```
#### 제목 클릭시 글자색과 배경색 변경 예시
```
const title = document.querySelector("#title")
title.onclick = () => {
  title.style.backgroundColor="yellow";
  title.style.color="blue";
}
```
### classList 프로퍼티
두 개 이상의 class 스타일이 적용되었을 경우 class 스타일 정보를 담아두는 프로퍼티이다. classList를 사용해서 적용 중인 class 스타일을 제거할 수도 있고 새로운  스타일을 추가할 수 있다.























