# 6 이벤트와 이벤트 처리기

## 6.1 이벤트 알아보기
**이벤트(event) :** 웹 브라우저나 사용자가 실행하는 어떤 동작을 말한다. 사용자가 웹 문서 영역을 벗어나서 클릭하는 행위는 이벤트가 아니다.

### 문서 로딩과 관련된 이벤트

  <table>
    <tr>
      <th>이벤트</th>
      <th>기능</th>
    </tr>
    <tr>
      <td>abort</td>
      <td>웹 문서가 완전히 로딩되기 전에 불러오기를 멈추었을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>error</td>
      <td>문서가 정확히 로딩되지 않았을 때, 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>load</td>
      <td>문서 로딩이 끝나면 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>resize</td>
      <td>문서 화면 크기가 바뀌었을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>scroll</td>
      <td>문서 화면이 스크롤 되었을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>unload</td>
      <td>문서를 벗어날 때 이벤트가 발생한다.</td>
    </tr>
  </table>

### 마우스와 관련된 이벤트
마우스 버튼이나 휠 버튼을 조작할 때 발생하는 이벤트
  
  <table>
    <tr>
      <th>이벤트</th>
      <th>기능</th>
    </tr>
    <tr>
      <td>click</td>
      <td>사용자가 HTML 요소를 클릭했을 떄 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>dbclick</td>
      <td>사용자가 HTML 요소를 더블 클릭했을 떄 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>mousedown</td>
      <td>사용자가 요소에서 마우스 버튼을 눌렀을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>mousemove</td>
      <td>사용자가 요소에서 마우스 포인터를 움직일 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>mouseover</td>
      <td>마우스 포인터를 요소 위로 옮길 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>mouseout</td>
      <td>마우스 다.</td>
    </tr>
  </table>

### 폼과 관련된 이벤트

  <table>
    <tr>
      <th>이벤트</th>
      <th>기능</th>
    </tr>
    <tr>
      <td>blur</td>
      <td>폼 요소에 포커스를 잃었을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>change</td>
      <td>목록이나 체크 상태 등이 변경되었을 때 이벤트가 발생한다.(input, select, textarea 태그에서 사용.)</td>
    </tr>
    <tr>
      <td>focus</td>
      <td>폼 요소에 포커스를 놓았을 때 이벤트가 발생한다.(label, select, textarea, botton 태그에서 사용)</td>
    </tr>
    <tr>
      <td>reset</td>
      <td>폼이 리셋되었을 때 이벤트가 발생한다.</td>
    </tr>
    <tr>
      <td>submit</td>
      <td>submit 버튼을 클릭했을 때 이벤트가 발생한다.</td>
    </tr>
  </table>

## 6.2 이벤트 처리하기

### 이벤트 처리하기
이벤트가 발생하면 그에 따른 연결 동작이 있어야 한다. 이렇게 이벤트를 처리하는 것을 **이벤트 처리기** 또는 **이벤트 핸들러(event handler)** 라고 한다. 

### HTML 태그에 연결하기
이벤트가 발생한 HTML 태그에 직접 함수를 연결한다.
```
<태그on이벤트명="함수명">

//예시
<button onclick = "alert('클릭!')">Click</button>
```

### 웹 요소에 직접 함수 연결하기
스크립트 소스를 변경해도 HTML 마크업에는 영향을 주지 않게 하려면 이벤트 처리기도 스크립트 소스에서 처리하는 것이 좋다.
```
요소.on이벤트명=함수

//예시
const button = document.querySelector("button");

button.onclick= function () {
  document.body.style.backgroundColor = "green"
}

// 함수를 미리 만들고 그함수를 지정해도 된다. 이때 실행할 함수 이름 뒤에 중괄호(())사용하지 않는다. 
function changeBackground() {
  document.body.style.backgroundColor = "green";
}
const button = document.querySelector("button");
button.onclick = changeBackground;
```
### addEventListener() 사용하기
이벤트 리스너는 어떤 DOM 요소에서도 사용할 수 있다. <br>
```
요소.addEventListener(이벤트,함수,캡처 여부);
```
**요소:** 요소가 발생한 요소 <br>
**이벤트:** 이벤트 유형. 단, 여기에서는 이벤트 이름 앞에 on을 붙이지 않고 click이나 keypress처럼 이벤트 이름을 그대로 사용한다. <br>
**함수:** 이벤트가 발생했을 때 실행할 함수. 기존에 있는 함수를 사용해도 되고 직접 익명 함수를 작성해도 된다. 익명 함수로 실행할 때는 event 객체를 사용해서 다양한 것들을 처리할 수 있다. <br>
**캡처 여부:** 이벤트를 캡처링하는지의 여부. true면 캡처링을, false면 버블링을 한다는 의미, 선택 사항이며 기본값은 false <br>

#### addEventListener() 사용하기
```
// 웹 요소에서 직접 함수 연결
 
function changeBackground() {
  document.body.style.backgroundColor = "green";
}
const button = document.querySelector("button");
button.onclick = changeBackground;


//addEventListener() 사용

function changeBackground() {
  document.body.style.backgroundColor = "green";
}
const button = document.querSelector("button");
button.addEventListener(click,changeBackground);

// 익명함수 사용
button.addEventListener("click",function() {
  document.body.style.backgroundColor="green";
});

//화살표 함수 사용
button.addEventListener("click",()=>{
  document.body.style.backgroundColor = "green"
});
```

#### 텍스트 필드에 입력한 글자 수 체크하기
```
// HTML
<div id="contents">
  <input type="text" id="word">
  <button id="bttn">글자 수 확인</button>
</div>

<div id="result"></div>
```
```
const botton =document.querySelector(#bttn");

button.addEventListener("click",() => {
  const word = document.querySelcetor("#word).value; //텍스트 상자의 내용 
  const result = document.querySelector("#result");  //결과값 표시
  let count = word.length; //문자열의 길이

  result.innerText = `${count};
});
```

### 모달 박스 만들기
**모달 박스(modal box):** 화면에 내용이 팝업되면서 기타 내용은 블러 처리되어 팝업된 내용에만 집중할 수 있게 해 주는 창이다.(라이트 박스라고 한다) <br>

모달 박스에 표시되는 내용은 웹 문서 안에 미리 만들어져 있어야 한다. <br>
css와 자바스크립트를 사용해서, 처음에는 모달 박스 부분을 화면에 감춰 두었다가 버튼을 클릭하거나 특정 이벤트가 발생했을 때 모달 박스를 표시한다.

```
//HTML 
<body>
  <button id="open">프로필 보기</button>

  <div id="modal-box">
    <div id="modal-contents">
      <button id="close">&times;</button>
      <h1 id="title">My Profile</h1>
      <div id="profile">
        <img src="images/pf.png" alt="도레미">
        <div id="desc">
          <p class="user">이름 : 도레미</p>
          <p class="user">주소 : somewhere</p>
          <p class="user">연락처 : 1234-5678</p>
        </div>
      </div>
    </div>
  </div>

  <script src="js/modal-result.js"></script>
</body>
```

```
//css 파이
button { …… }
#modal-box{
  position:fixed;
  top:0;
  left:0;
  bottom:0;
  right:0;
  background-color: rgba(0,0,0,0.6);
  display: none;
  justify-content: center;
  align-items: center;
}

#modal-box.active {
  display: flex;
}
```

```
//js파
const open = document.querySelector("#open")
const modalBox = document.querySelector("#modal-box")
const close = document.querySelector("#close")

open.addEventListener("click", () => {
  modalBox.classList.add("active");
});
close.addEventListerner("click", () =>
  modalBox.classList.remove("active")
})
```

## 6.3 event 객체
이벤트가 발생하면 자동으로 만들어지는 객체<br>

### event 객체의 메서드
<table>
    <tr>
      <th>메서드</th>
      <th>기능</th>
    </tr>
    <tr>
      <td>preventDefault</td>
      <td>(취소할 수 있는 경우) 기본 동작을 취소한다.</td>
    </tr>
  </table>

### event 객체의 프로퍼티
  <table>
    <tr>
      <th>프로퍼티</th>
      <th>기능</th>
    </tr>
    <tr>
      <td>altKey</td>
      <td>이벤트가 발생했을 때 alt를 누르고 있었는지 여부를 확인하고 Boolean값을 반환한다.</td>
    </tr>
    <tr>
      <td>botton</td>
      <td>마우스 키를 반환한다.</td>
    </tr>
    <tr>
      <td>charCode</td>
      <td>keypress 이벤트가 발생했을 때 어떤 키가 눌렸는지 유니코드 값으로 반환한다.</td>
    </tr>
    <tr>
      <td>clientX</td>
      <td>이벤트가 발생한 가로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>clientY</td>
      <td>이벤트가 발생한 세로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>ctrlKey</td>
      <td>이벤트가 발생했을 때 ctrl을 누르고 있었는지의 여부를 확인하고 boolean 값을 반환한다.</td>
    </tr>
    <tr>
      <td>pageX</td>
      <td>현재 문서를 기준으로 이벤트가 발생한 가로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>pageY</td>
      <td>현재 문서를 기준으로 이벤트가 발생한 세로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>screenX</td>
      <td>현재 화면를 기준으로 이벤트가 발생한 가로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>screenY</td>
      <td>현재 화면를 기준으로 이벤트가 발생한 세로 위치를 반환한다.</td>
    </tr>
    <tr>
      <td>shiftKey</td>
      <td>이벤트가 발생했을 때 shift를 누르고 있었는지 여부를 확인하고 Boolean 값응ㄹ 반환한다.</td>
    </tr>
    <tr>
      <td>target</td>
      <td>이벤트가 발생한 대상을 반환한다.</td>
    </tr>
    <tr>
      <td>timeStamp</td>
      <td>이벤트가 발생한 시간을 밀리초 단위로 반환한다.</td>
    </tr>
    <tr>
      <td>type</td>
      <td>발생한 이벤트 이름을 반환한다.</td>
    </tr>
    <tr>
      <td>which</td>
      <td>키보드와 관련된 이벤트가 발생했을 때 키의 유니코드 값을 반환한다.</td>
    </tr>
  </table>

























