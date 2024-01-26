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

```
document.querySelector("#desc p").classList 
```

### 클래스 스타일 추가 및 삭제하기
새로운 클래스 스타일을 추가하거나(이 경우, 클래스 스타일이 만들어져 있어야 함) 기존에 적용 중인 클래스 스타일을 제거할 수 있다.
```
요소.classList.add(클래스명) 
요소.classList.remove(클래스명) 
```

#### add() 클래스 스타일 추가 예시
```
//css
h1 {
  font-size:2rem; 
  margin-bottom:20px ;
}
.clicked {
  background-color:yellow;
}

// js
const title = document.querySelector("#title");

title.onclick = () => {
  title.classList.add("clicked");
}
```

### contain()-특정 클래스 스타일이 있는지
특정 클래스 스타일이 있는지 체크해주는 함수이다. 이 함수를 사용해 클래스 추가 및 삭제를 연속적으로 실행할 수 있다.
```
요소.classList.contains(클래스명) 
```
#### contain() 예시
```
const title = document.querySelector("#title");

title.onclick = () => {
  if(!title.classList.contains("clicked")){
    title.classList.add("clicked");              // .clicked가 없으면 추가
  } else {
    title.classList.remove("clicked");           // .clicked가 있으면 삭
  }
}
```

### toggle() - 특정 스타일 토글
특정 클래스를 추가하거나 삭제하기를 반복할 경우에는 classList의 toggle() 함수가 더 편하다.

```
요소.classList.toggle(클래스명)
```

```
//toggle() 사용x
const title = document.querySelector("#title");

title.onclick = () => {
  if(!title.classList.contains("clicked")){
    title.classList.add("clicked");
  } else {
    title.classList.remove("clicked");
  }
}

//toggle() 사용o
const title = document.quenySelector("#title")

title.onclick = () => {
  title.classList.toggle("clicked");
}
```

## 5.4 DOM에서 폼 다루기

### 문서에 접근하기
**id**를 사용해 접근
```
document.querySelector("#order-name")
```
**텍스트 필드에 입력한 내용 가져오기**
```
document.querySelector("#order-name").value
```

```
//html 
<fieldset>
  <legend>주문 정보</legend>
  <ul>
    <li>
      <label class="field" for="order-name">이름 : </label>
      <input type="text" class="input-box" id="order-name" name="order-name">
    </li>
    ……
  </ul>
</fieldset>
```

**name 속성 값을 사용해 접근하기**
만약 name 속성이 있다면 name속성으로도 폼요소에 접근할 수 있다. <br>
form 태그에도 name속성이 있어야 하고, form 태그 안의 폼 요소에도 name 속성이 있어야한다.
```
document.order.product.value //order: form의 name값, product: 상품 필드의 name값
```

```
//html
<form name="order">
  <fieldset>
  <legend>상품 정보</legend>
    <ul>
      <li>
        <label class="field" for="product">상품 : </label>
        <input type="text" class="input-box" id="product" name="product">
    </li>
    ……
  </ul>
</fieldset>
……
```

### 폼 배열을 사용해 접근하기
폼 요소에 id나 class 속성뿐만 아니라 name 속성도 없을 시 사용한다. DOM에서는 웹 문서 안에 있는 모든 요소를 배열 형태로 저장한다. <br>
폼 배열을 써서 주문자 이름을 입력하는 필드에 접근하려면 id, class, name 속성 모두 없다고 가정한다.**나중에 확인 해보기**

**문서 안에 있는 form태그는 모두 forms라는 프로퍼티에 저장되어 있다.**
```
document.forms
```
**폼 안에 있는 요소들이 elements 속성에 역시 배열 형태로 저장된다.**
```
document.forms[0].elements
```

### 선택 목록과 항목에 접근하기
```
<select name="major" id="major">
  <option>---- 학과 선택 ----</option>
  <option value="archi">건축공학과</option>
  <option value="mechanic">기계공학과</option>
  <option value="indust">산업공학과</option>
  <option value="elec">전기전자공학과</option>
  <option value="computer">컴퓨터공학과</option>
  <option value="chemical">화학공학과</option>
</select>
```
**선택 목록에 접근하기**
```
document.querySelector("#major")
```
**선택 목록에 있는 항목에 접근하기**
```
document.querySeclector("#major").options
```
#### selectedIndex
**selectedIndex 값**은 선택 목록에서 선택한 항목의 인덱스 값을 나타낸다.
```
//selectedIndex 값 확인방법
document.querySelector("#major").options.selectedIndex
document.querySelector("#major").selectedIndex
```
#### selectedIndex 값(선택한 황목) 화면에 표시하기
```
const selectMenu =document.querySelector("#major");

function displaySelect() {
  let selectedText = selectMenu.options[selectMenu.selectedIndex].innerText;
  alert(`[${selectedText}]를 선택했다.`);
}
selectMenu.onchange = displaySelect;


//화살표 함수

const selcetMenu = document.querySelector("major")

selectMenu.onchange = () => {
  let selectedText = selectMenu.options[selectMenu.selectedIndex].innerText;
  alert('[${selectedText}]를 선택했다.');
}
```

### 라디오 버튼과 체크 박스에 접근하기
1.라디오 버튼이나 체크 박스는 name을 사용해 버튼을 그룹으로 묶는다.(라디오 버튼이나 체크 박스는 하나의 그룹 안에서 항목을 선택하기 때문) <br>
2.라디오 버튼과 체크박스는 name 값을 사용해 접근한다. <br>
3.같은 name을 가진 항목이 많기 때문에 RadioNodeList라는 노드 리스트 형태로 저장된다.(배열과 비슷한 형태)<br>
4.어떤 항목을 선택했는지 알려면 checked 속성이 있는지 체크한다.(checked 속성은 HTML에서 라디오 버튼과 체크 박스에서 사용할 수 있는 속성)

#### 라디오 버튼에 접근하기
```
// HTML
<fieldset>
  <legend>신청 과목</legend>
  <p>이 달에 신청할 과목을 선택하세요.</p>
  <label><input type="radio" name="subject" value="speaking">회화</label>
  <label><input type="radio" name="subject" value="grammar">문법</label>
  <label><input type="radio" name="subject" value="writing">작문</label> 
</fieldset>

//radio

const radioMenu= document.testForm.subject
console.log(radioMenu[0].value)

const radioMenu1 =document.querySelector("input[name='subject']:checked")
console.log(radioMenu1)

//mailing (체크박스 2개 이상 선택 가능하므로 querySelectorAll() 사용)

const checkMenu=document.testForm.mailing
console.log(checkMenu[0].value)

const checkMenu1 =document.querySelectorAll("input[name='mailing']:checked")
console.log(checkMenu1)

```


























