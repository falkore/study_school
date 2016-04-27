# css3
## css3? 
> css3란 css2의 버전업!
css는 과거 초창기부터 존재하던기능이 아님 html에서 모두 사용되었음.(inline style)

```
<div width="300" height="500" border="1" bgcolor="blue" style="">
</div>
```
문제점: html/css의 내용이 분리되지 않아 유지보수가 힘들고, class/id개념이 거의 없어 재사용이 힘들었다~~
이에 css기능이 생성 : 개발자의 의견에의해 사용되지 못함
추후 css2를 새로 개편하여 보급화(xhml이 거의 같이 사용)
html5가 만들어지면서 css3도 함께 나타나게 됨~

> **css3의 가장크게 발전된 내용:**
- 다양한 선택자
- 동적제어기능인 js의 기능을 css3에서 일부 구동가능하게 만들었음
- illustrator, photoshop 사용에대한 비중을 줄이고, 코드로 사용할 수 있도록 제작
___

### 선택자
* 연결 선택자: +로 표기하는 선택자. 어떠한 element 동급의 바로뒤에 위치한 형제 element
	- dt + dd{} 
* 동위 선택자: ~로 표기하는 선택자. 어떠한 element 동급의 형제 태그중 하나 선택...
	- dt ~ dd{}
* :nth-child() 선택자 : 연속된 같은 레벨의 동일한 명칭의 태그들의 선택(순서에맞게 선택).....
	- :first-child(){}
	- :nth-child(){}
	- :last-child(){}
	- :nth-last-child(){}
	> 차후: 슬라이드배너 같은 효과를 사용시에는 nth-child 사용을 하면 안된다!!
	
* :nth-of-type() 선택자: 같은 레벨의 동일한 명칭의 태그선택(같은 태그끼리의 순서를 확인)...
	- :first-of-type(){}
	- :nth-of-type(){}
	- :last-of-type(){}
	- :nth-last-of-type(){}







