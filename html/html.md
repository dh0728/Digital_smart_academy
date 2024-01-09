# 1.1 HTML이란

HTML은 HyperText Markup Language의 약자로 **웹사이트의 모습을 기술하기 위한 마크업 언어**이다. Hypertext란 문서를 서로 연결해주는 링크를 의미하고 markup은 '표시한다'라는 뜻을 가진다. 따라서 HTML은 웹 문서를 서로 연결해주고 웹 브라우저에 내용을 보여 주는 텍스트, 이미지, 영상 등의 위치를 표시하는 것을 의미한다. 

# 1.2 HTML 구조 파악하기
  
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html>

<!DOCTYPE html>로 시작해 <html>, <head>, <body> 3개의 영역으로 구성된다.
```

HTML 문서는 일반 문서와 달리 정해진 형식에 맞추어 내용을 입력해야 한다. 요즘은 세상이 좋아져서 html파일을 만들고 vs code 같은 웹편집기에서 shift+!를 누르면 저절로 기본 구조가 작성된다.

**!DOCTYPE html** : 현재 문서가 HTML5로 작성한 웹 문서라는 뜻이다
**html ~ /html** : 웹 문서의 시작과 끝을 나타내는 태그이다. 웹 브라우저가 html태그를 만나 /html까지 소스를 읽어 화면에 표시한다.
**head ~ /head** : 웹 브라우저가 웹 문서를 해석하는데 필요한 정보를 입력하는 부분이다.
**body ~ /body** : 실제로 웹 브라우저 화면에 나타나는 내용이다. 



  
