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


