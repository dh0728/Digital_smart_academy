# 입력 양식 작성

# 3.1 폼 삽입하기
하나의 웹 사이트 안에서는 여러가지 폼을 사용한다. 아이디와 비밀번호를 입력하거나 로그인 버튼, 회원 가입 등 사용자가 웹 사이트로 정보를 보낼 수 있는 모든 요소를 폼이라고 한다. 사용자가 아이디와 비밀번호를 입력하고 로그인 버튼을 클릭하면 입력한 정보는 웹 서버로 전송된다. 그럼 서버는 자신이 가진 데이터베이스에서 입력받은 아이디와 비밀번호가 일치하는지 확인하고 그 결과를 웹 브라우저로 보낸다. 폼과 관련된 작업은 정보를 저장하거나 검색 수정하는 것이 대부분인데 모두 데이터베이스 기반으로 작동한다. 따라서 텍스트 박스나 버튼 같은 형태는 모두 태그로 만들지만, 폼에 입력한 사용자 정보는 ASP나 PHP, JSP같은 서버 프로그래밍을 이용해 처리한다.

### form태그
폼을 만드는 가장 기본적인 태그로 form태그 사이에 여러 가지 폼 요소를 넣는다. form 태그는 몇 가지 속성을 사용해서 입력 받은 자료를 어떤 방식으로 서버에 넘길 것인지 서버에서 어떤 프로그램을 이용해 처리할 것인지 지정한다. 
#### form 태그 속
  <table>
    <thead>
      <tr>
        <th>종류</th>
        <th>설명</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>method</td>
        <td>사용자가 입력한 내용을 서버 쪽 프로그램으로 어떻게 넘겨줄 것인지 지정한다. method에서 사용할 수 있는 속성 값은 get과 post이다 <br> get: 데이터를 256~4096byte까지만 서버로 넘길 수 있다. 주소 표시줄에 사용자가 입력한 내용이 그대로 드러난다는 단점이 있다. <br> post: 입력한 내용의 길이에 제한 받지 않고 사용자가 입력한 내용도 드러나지 않는다.</td>
      </tr>
      <tr>
        <td>name</td>
        <td>자바스크립트로 폼을 제어할 때 사용할 폼의 이름을 지정한다.</td>
      </tr>
      <tr>
        <td>action</td>
        <td>form 태그 안의 내용을 처리해 줄 서버 프로그램을 작성한다.</td>
      </tr>
      <tr>
        <td>target</td>
        <td>action 속성에서 지정한 스크립트  파일을 현재 창이 아닌 다른 위치에서 열도록 한다.</td>
      </tr> 
      <tr>
        <td>autocomplete</td>
        <td>폼에서 내용을 입력할 때 예전에 입력한 내용을 자동을 표시해 주는 자동완성기능이다.</td>
      </tr>
      
      
    </tbody>
  </table>

### fieldset, legend 태그
하나의 폼에 여러 구역을 나누어 표시할 때 fieldset 태그를 사용한다. legned 태그를 사용해서 fieldset로 묶인 그룹에 제목을 붙일 수 있다.

#### input
```
<form action="">
    <fieldset>
      <legend>가슴</legend>
    </fieldset>
    <fieldset>
      <legend>등</legend>
    </fieldset>
</form>
```

#### output

<form action="">
    <fieldset>
      <legend>가슴</legend>
    </fieldset>
    <fieldset>
      <legend>등</legend>
    </fieldset>
</form>

### label 태그
lable 태그는 input 태그와 같은 폼 요소에 레이블을 붙일 때 사용한다. 레이블(label)은 입력란 가까이에 아이디나 비밀번호처럼 붙여 놓은 텍스트를 말한다. label 태그를 사용하면 폼 요소와 레이블 텍스트가 서로 연결되었다는 것을 웹 브라우저가 알 수 있다. 두 가지 사용 방법이 있다.

#### 태그 안에 폼 요소를 넣는 방법
```
<label for="">아이디<input type="text"></label>
```
#### label 태그와 폼 요소를 따로 사용하고 for 속성과 폼 요소의 id 속성을 이용해 서로 연결하는 방법
```
<label for="user_id">아이디</label>
<input type="text" id="user_id">
```
# 3.2 사용자 입력을 위한 input 태그
아이디나 검색어를 입력하는 검색 상자나 로그인 버튼처럼 사용자가 입력할 부분은 주로 input태그를 이용해 넣는다.
### input 태그 속성 
input태그에서 입력 형태를 지정할 때는 type 속성을 사용한다. 

<table>
  <thead>
    <tr>
      <th>종류</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>text</td>
      <td>한 줄짜리 텍스트를 입력할 수 있는 텍스트 박스를 넣는다. </td>
    </tr>
    <tr>
      <td>passward</td>
      <td>비밀번호를 입력할 수 있는 텍스트를 넣는다.</td>
    </tr>
    <tr>
      <td>search</td>
      <td>검색할 때 입력하는 필드를 넣는다.</td>
    </tr>
    <tr>
      <td>url</td>
      <td>URL 주소를 입력하는 필드를 넣는다.</td>
    </tr>
    <tr>
      <td>email</td>
      <td>이메일 주소를 입력할 수 있는 필드를 넣는다.</td>
    </tr>
    <tr>
      <td>tel</td>
      <td>전화 번호를 입력할 수 있는 필드를 넣는다.</td>
    </tr>
    <tr>
      <td>checkbox</td>
      <td>주어진 여러 항목에서 2개 이상 선택할 수 있는 체크 박스를 넣는다.</td>
    </tr>
    <tr>
      <td>radio</td>
      <td>주어진 항목에 한 개 선택할 수 있는 라디오 버튼을 넣는다.</td>
    </tr>
    <tr>
      <td>number</td>
      <td>숫자를 조절할 수 있는 스핀 박스를 넣는다.</td>
    </tr>
    <tr>
      <td>range</td>
      <td>숫자를 조절할 수 있는 슬라이드 막대를 넣는다.</td>
    </tr>
    <tr>
      <td>date</td>
      <td>사용자 지역을 기준으로 날짜(연, 월, 일)을 넣는다.</td>
    </tr>
    <tr>
      <td>month</td>
      <td>사용자 지역을 기준으로 날짜(연, 월)를 넣는다.</td>
    </tr>
    <tr>
      <td>week</td>
      <td>사용자 지역을 기준으로 날짜(연, 주)를 넣는다.</td>
    </tr>
    <tr>
      <td>time</td>
      <td>사용자 지역을 기준으로 시간(시, 분, 초, 분할 초)을 넣는다.</td>
    </tr>
    <tr>
      <td>datetime</td>
      <td>국제표준시(UTC)로 설정도니 날짜와 시간(연,월, 일, 시, 분, 초, 분할 초)을 넣는다.</td>
    </tr>
    <tr>
      <td>datetime-local</td>
      <td>사용자가 있는 지역을 기준으로 날짜와 시간(연, 월, 시, 분, 초, 분할 초)을 넣는다.</td>
    </tr>
    <tr>
      <td>sumit</td>
      <td>전송버튼을 넣는다.</td>
    </tr>
    <tr>
      <td>reset</td>
      <td>리셋 버튼을 넣는다.</td>
    </tr>
    <tr>
      <td>image</td>
      <td>submit 버튼 대신 사용할 이미지를 넣는다.</td>
    </tr>
    <tr>
      <td>button</td>
      <td>일반 버튼을 넣는다.</td>
    </tr>
    <tr>
      <td>file</td>
      <td>파일을 첨부할 수 있는 버튼을 넣는다.</td>
    </tr>
    <tr>
      <td>hidden</td>
      <td>사용자에게는 보이지 않지만 서버로 넘겨주는 값이 있는 필드를 만든다<div class=""></div></td>
    </tr>
  </tbody>
</table>


