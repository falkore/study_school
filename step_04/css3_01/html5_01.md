# 2016.04.04일차
> **학습목표**: 웹표준디자인제작  
    **학습내용**: 시각디자인 리서치<hr />
	
```
	금일 지각:  이동호, 이성령,  최유리
	금일 결석:
```
---
## html5
> html5는 이전에 쓰던 html이 버전 업된것!!
 html4, xhtml(xml + html) => html5(xhml5) : 2014년 10월 웹표준으로 제정

```
<!DOCTYPE html>
<html lang="ko-KR">
	<head>
		<meta charset="utf-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<!--[if lte IE 9]>
			
		<![endif]-->
		<title>html기초 형태</title>
		<style></style>
		<script></script>
	</head>
	<body>
		
	</body>
</html>
```
---
html문서가 table구조에서  div로 변경됨에 따라, div무덤~~ 무엇이 무엇인지 알수가 없다!!
많이 쓰고있는 영역별로 구분할수 있는 코드명을 추가!!!
1. 시멘틱 구조(각자의 임무에맞게, 정확한 의미를 가지는 코드를 작성하자!)
2. 아웃라인구조(해당하는 영역마다 순위를 매기는것!: 반드시 영역별 구분을 위해 사용!!)

>brackets플러그인 추가: document outline

### 추가된 코드(시멘틱 주요코드이해)
**header, nav, aside, section, article, footer,  hgroup**
```
<div id="header"></div><!--// #header-->
<header id="xido_head"></header>
```
1. header : 문서의 시작(웹페이지의 전체를 알리는 영역: 로고, gnb)
2. nav : 메뉴의 영역을 나타내는 코드(일반적으로 header 영역에 포함)
3. aside : 꼭있어야하는 영역보다는 보조영역의 의미를 부여, 없어도 진행/ 있으면 도움
4. section: 본문영역(재사용 불가능) - 새로운 작은 웹페이지(header, nav, article, footer)
5. article: 본문영역(재사용 가능) -내용상의 본문내용을 만들때 사용
6. footer: 문서의 하단에 위치하며, 정보를 전달하는 의미(기업의 정보, 개인의 정보: 주소, 연락처, .......)
7. hgroup : 문서를 작성하다보면, 다양한 제목을 한번에 쓰는 경우도 있다. 이를 하나의 묶음으로 처리하는 코드가 hgroup이다.


> h1이 웹문서 자체에 여러번 사용이 가능하다!
이전에 사용하던 구조범위 h1~6까지는 작은 회사처럼 꾸려졌으나.
이제는 h1~6까지의 범위내에 다시 h1~6까지 이중~삼중의 구조를 제작가능하므로 그룹회사  
	  
---
**image**
__figure, img, figcaption__
```
<figure>
	<img src="" alt="" />
	<figcaption>이미지 설명</figcaption>
</figure>
```
1. figure: 이미지가 혼자 쓰이는경우가 아닌 별도의 제목이 함께 동반되는경우
해당하는 이미지 제목을 엮기위해 감싸는 코드명
2. img...
3. figcaption: 이미지의 내용을 설명하는 코드(alt와는 다름!!)
 
**details**
__details, summary, p__
1. details: 요약된 제목과, 상세설명이 같이 있어야할 경우(ex: Q & A)
2. summary: details의 요약내용을 담는곳
3. p: details의 내부에 사용되는 p는 summary의 설명을 담는 곳
> 아직 사용하기 무리데스요~~!!(ie, firefox 에서는 작동X)

**a**
> inline 태그는 기본적으로 block 감쌀수 없다~~~(니스칠)
하지만, html5에서부터는 a는 범외로 본다. 


```
<a href="#">
	<img src="//lorempixel.com/400/400" alt="sdasdf" />
	<p>내용을 상세하게 설명한코드</p>
</a>
```













