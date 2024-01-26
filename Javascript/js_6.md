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







