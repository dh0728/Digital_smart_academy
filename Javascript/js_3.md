# 3 연산자와 제어문

## 3.1 연산자
**연산자(operator)** 란 프로그램에서 특정한 동작을 하도록 지시하는 기호이다. 

### 산술 연산자
수학 계산을 할 때 사용하는 연산자
  <table>
    <tr>
      <th>종류</th>
      <th>설명</th>
      <th>예시</th>
    </tr>
    <tr>
      <td>+</td>
      <td>두 연산자의 값을 더한다.</td>
      <td>c=a+b</td>
    </tr>
    <tr>
      <td>-</td>
      <td>첫 번째 피연산자 값에서 두 번째 피연산자 값을 뺀다.</td>
      <td>c= a - b</td>
    </tr>
    <tr>
      <td>*</td>
      <td>두 연산자의 값을 곱한다.</td>
      <td>c = a*b</td>
    </tr>
    <tr>
      <td>/</td>
      <td>첫 번째 피연산자 값을 두 번째 피연산자 값으로 나눈다.</td>
      <td>c=a/b</td>
    </tr>
    <tr>
      <td>%</td>
      <td>첫 번째 피연산자 값을 두 번째 피연산자 값으로 나눈 나머지를 구한다.</td>
      <td>c = a % b</td>
    </tr>
    <tr>
      <td>++</td>
      <td>피연산자를 1 증가시킨다.</td>
      <td>a++</td>
    </tr>
    <tr>
      <td>--</td>
      <td>피연산자를 1 감소시킨다.</td>
      <td>b--</td>
    </tr>
  </table>

#### 증감 연산자 (++), (--)
증감 연산자는 연산자가 어느 위치에 붙느냐에 따라 처리 방법이 달라진다. 
```
a=10
sum= a++ +5 // a=11 sum=15
a // 11
```
**a++** 연산자는 연산식을 먼저 실행한 후에 a에 1을 증가시킨다. 
<br>
```
a=10
sum= ++a +5 //a=11 sum=16
```
**++a** 연산자는 변수 a에 1을 증가시킨후 연산식을 실행한다.

### 할당 연산자 (대입 연산자)
연산자 오른쪽의 실행 결과를 왼쪽 변수에 할당하는 연산자 산술 연산자와 할당 연산자를 묶어서 표현할 수 있다. 
  <table>
    <tr>
      <th>종류</th>
      <th>설명</th>
      <th>예시</th>
    </tr>
    <tr>
      <td>=</td>
      <td>연산자 오른쪽의 값을 왼쪽 변수에 할당한다.</td>
      <td>y= x+3</td>
    </tr>
    <tr>
      <td>+=</td>
      <td>y = y+x를 의미한다.</td>
      <td>y += x</td>
    </tr>
    <tr>
      <td>-=</td>
      <td>y = y-x를 의미한다.</td>
      <td>y -= x</td>
    </tr>
    <tr>
      <td>*</td>
      <td>y = y*x를 의미한다.</td>
      <td>y *= x</td>
    </tr>
    <tr>
      <td>/</td>
      <td>y = y/x를 의미한다.</td>
      <td>y /= x</td>
    </tr>
    <tr>
      <td>%</td>
      <td>y = y % x를 의미한다.</td>
      <td>y %= x</td>
    </tr>
  </table>

### 연결 연산자
산술 연살자의 더한기(+)를 연결 연산자로 사용한다. 문자열과 문자열을 연결하는 연산자이다. **산술 연산자로 사용했는데, 연결 연산자로 인식해서 예상치 못한 결과가 나오기도 한다.**
```
document.write (birthYear + "년에 태어난 사람의 나이는" + age + "세입니다.");
```

### 비교 연산자
**비교 연산자(comparison operators)** 는 피연산자 2개의 값을 비교해서 true나 false로 결괏값을 반환한다. 주로 조건을 확인할 때 자주 사용하는 연산자이다. 

<table>
  <tr>
    <th rowspan="2">종류</th>
    <th rowspan="2">설명</th>
    <th colspan="2">예시</th>
  </tr>
  <tr>
    <th>조건식</th>
    <th>결과</th>
  </tr>
  <tr>
    <td>==</td>
    <td>피연산자가 서로 같으면 true이다.</td>
    <td>3 == "3"</td>
    <td>true</td>
  </tr>
  <tr>
    <td>===</td>
    <td>피연산자도 같고 자료형도 같으면 true이다.</td>
    <td>a === "3"</td>
    <td>false</td>
  </tr>
  <tr>
    <td>!=</td>
    <td>피연산자가 서로 같지 않으면 true이다.</td>
    <td>3 !="3"</td>
    <td> false</td>
  </tr>
  <tr>
    <td>!==</td>
    <td>피연산자가 같지 않거나 자료형이 같지 않으면 true이다.</td>
    <td>3 !=="3"</td>
    <td>true</td>
  </tr>
  <tr>
    <td> < </td>
    <td>왼쪽 피연산자가 오른쪽 피연산자보다 작으면 true이다.</td>
    <td> 3 < 4 </td>
    <td> true </td>
  </tr>
  <tr>
    <td> <= </td>
    <td>왼쪽 피연산자가 오른쪽 피연산자보다 작거나 같으면 true이다.</td>
    <td> 3 =< 4 </td>
    <td> true</td>
  </tr>
  <tr>
    <td> > </td>
    <td> 왼쪽 피연산자가 오른쪽 피연산자보다 크면 true이다.</td>
    <td> 3 > 4</td>
    <td> false</td>
  </tr>
  <tr>
    <td>>=</td>
    <td>왼쪽 피연산자가 오른쪽 피연산자보다 크거나 작으면 true이다.</td>
    <td>3 >=4</td>
    <td> false </td>
  </tr>
</table>

#### 비교연산자- 문자열비교
피연산자가 문자열이면 문자열에 있는 문자들의 아스키값(ASCII)을 비교해서 결정한다. <br>
대략적인 아스키값 순서: **제어문자 < 특수기호 < 숫자 < 영대문자 < 영소문자**
```
"A" > "B" //false("B"의 아스키값이 더크다.)
"A" < "b" //true(영소문자의 아스키값이 대문자보다 크다)
```
글자가 여러 개인 경우 문자열을 비교할 때 맨 앞의 문자부터 하나씩 비교한다.
```
Javascript < JavaScript //false( 소문자 > 대문자)
```

### 논리 연산자
**불리언(boolean)** 연산자라고도 하며 true, false를 처리하는 연산자이다. 주로 프로그램에서 조건을 처리할 때 사용하는 연산자이다.

<table>
    <tr>
      <th>종류</th>
      <th>기호</th>
      <th>설명</th>
    </tr>
    <tr>
      <td>OR연산자</td>
      <td>||</td>
      <td>피연산자 중 하나만 true여도 true가 된다.</td>
    </tr>
    <tr>
      <td>AND연산자</td>
      <td>&&</td>
      <td>피연산자 모두 true일 경우에만 true가 된다.</td>
    </tr>
    <tr>
      <td>NOT연산자</td>
      <td>!</td>
      <td>피연산자의 반댓값을 지정한다.</td>
    </tr>
  </table>

### 연산자 우선순위
**단항연산자->산술연산자->비교연산자->논리연산자->할당연산**

<table>
  <tr>
    <th></th>
    <th>1st</th>
    <th>2nd</th>
    <th>3rd</th>
    <th>4th</th>
    <th>5th</th>
    <th>6th</th>
    <th>7th</th>
  </tr>
  <tr>
    <th>단항연산자</th>
    <td>!</td>
    <td>++</td>
    <td>--</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th>산술연산자</th>
    <td>*</td>
    <td>/</td>
    <td>%</td>
    <td>+</td>
    <td>-</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th>비교연산자</th>
    <td><</td>
    <td><=</td>
    <td>></td>
    <td>>=</td>
    <td>==</td>
    <td>!=</td>
    <td>===</td>
  </tr>
  <tr>
    <th>논리연산자</th>
    <td>&&</td>
    <td>||</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th>할당연산자</th>
    <td>=</td>
    <td>+=</td>
    <td>-=</td>
    <td>*=</td>
    <td>/=</td>
    <td>%=</td>
    <td></td>
  </tr>
</table>






















