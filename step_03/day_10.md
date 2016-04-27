##


## 웹페이지 html5 형식으로 셋팅
    jQuery 파일 첨부/하위브라우저 셋팅
    >html5.shiv
    >ie9.js
    >pie.js
    >respond.js
    
## 배경이미지
### background
```
background-color: rgb(255,255,255);
background-image: url("./");
background-repeat: repeat | repeat-x | repeat-y | no-repeat ;
background-position: ; 



background
```
> **background-position**
최초의 위치는 0,0 (즉, 왼쪽 상단을 기준), 
-40px, -50px (왼쪽방향으로 40px만큼 이동하고, 위쪽방향으로 50px만큼 올라간다.) 
20px, -30px (오른쪽방향으로 20px만큼, 위쪽방향으로 30px만큼 올라간다.)
center center (가로방향 가운데, 세로방향 가운데 이미지배치 - 틀에 해당이미지 중심이 배치 ! )
기본 x축 그리고 y축 순서로 위치를 잡는다 ! ~
인디자인처럼 틀보다 이미지가 크면 넘쳐서 보이는 현상이 사라진다. (overflow: hidden 효과)

> **background**
background 속성은 image, position, repeat 모두를 한꺼번에 작성하는 기능.
```
background: url("경로") 반복여부 위치값;
background: url("파일경로/이름") repeat-x 0 -40px;
```
단 !!  IE 9버전 이하는 png 파일로 작성시 하나의 이미지만 보이는 현상이 발생하기도 함 !!
될 수 있는 한 png (투명한 영역이 있다면),
background-image: url();
background-position: ;
background-repeat: ;
모두_별도_로 사용하는 것을 권함


### IR 기법
> **IR 기법이란?**
 image replace 란 뜻으로, html 문서에 내용을 입력하고 그에 따른 글자를 이미지로 변환시켜 처리하는 것!
 ```
 <style>
     h1{background-image: url(./img/do.png); background-repeat: no-repeat;background-position: center center;
     text-indent: -9999em;
     }
     
 </style>
 <h1>웹페이지</h1>
 

 text-indent: 글씨 들여쓰기 기능으로 단위 em 값으로 (16px,12pt) -9999*16만큼 이동시킨다.-블록태그만 가능
why?? img 태그가 있는데 background-image방식으로 사용하는 이유는?
브라우저의 구현속도가 빠름, 스크린 리더가 읽어줄 수 있음
배경과 버튼 모두 설명이 가능 


___
### IS 기법
> **IS 기법이란?**
image sprites 는 하나의 아이콘 이미지가 여러 개가 모이면 복잡해지는 효과가 있다.
하나의 웹페이지 안에는 수백 개, 수천 개의 아이콘이 모여있으므로, 모든 아이콘 이미지를
관리하기는 어렵다 !!
이에 하나의 파일에 관련있는 여러 개의 아이콘 또는 이미지를 모아서 처리하는 방식을 is 기법이라고 한다.
 **IR기법에서 확장되어야만 한다 !! ** + background-position 을 활용하여 사용하는 기법
 장점: 파일관리가 용이해진다 ! 여러 개의 아주 작은 파일을 모아서 처리하므로 기본 웹 용량이 작아진다. 
         브라우저 속도가 빨라진다.
 단점:  소스파일 하나를 수정시 다른 파일을 건드릴 수도 있다 !!
         파일의 위치를 하나하나 계산하거나 ! 별도의 문서에 처리되어야 한다 !!
         팀간의 상호교류 없이 무단으로 이미지를 합치면, 혼돈을 초래할 수도 있다 !

