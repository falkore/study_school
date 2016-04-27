# css3
___
### text추가
1. word-break: 띄어쓰기 없이 문서를 작성할경우! 정해진 크기의 상자에서 텍스트가 줄바꿈이 자동으로 되지않고 넘치는경우
	- break-all;  자동으로 크기에 맞춰 자동 줄바꿈
	- keep-all;  무존건 넘치게 처리하는 것(기본상태)
	- normal;
1. text-overflow: 정해진 상자의 크기에서 텍스트가 넘쳐날 경우 
	- clip; 넘치는 글씨 관계없이 과감하게 컷팅!! (overflow:hidden; 과유사!!)
		* overflow | overflow-x | overflow-y: hidden | scroll | auto | normal
	- ellipsis; 보이는 글자의 말미를 말줄임표로 바꿀수 있다.
1. white-space: 박스에서 텍스트의 줄바꿈처리시 사용자가 직접 관여를 하느냐 마느냐
	- inherit;	 말그대로 상속 받는 것
	- normal;	 일반적인 것, default
	- nowrap;	 줄바꿈을 하지 않는다
	- pre;	 pre 태그와 같은 기능, 마크업에서 앤터로 줄바꿈 한것만 적용이 되고 
				넘어가는 것에는 줄바꿈 하지 않는다
	- pre-line;	 마크업에서 줄바꿈 한 것이 적용 되면서 width를 넘어가는 텍스트도 
						자동으로 줄바꿈이 된다
	- pre-wrap;	 pre-line 과 비슷
	
___
### 배경
> css2에서는 하나의 색상, 하나의 이미지, 고정사이즈 등으로만 설정이 가능했다.
css3로 버전이 향상되면서 여러개의 색상(그라데이션), 여러장의 이미지(멀티 이미지)
이미지의 크기값(retina구현이 추가로 생겼다) 등을 변경이 가능하게 되었다
1. background-color :
	- ``` #fac ```
	- rgba(255, 100, 0, 0.5) ; 빨강(0~255), 녹색(0~255), 파랑(0~255), 투명도(0~1)
	- hsla(360, 100%, 50%, 0);  색상(0~360), 채도(0~100%),명도(0~100%), 투명도(0~1)
	- transparent; 공간은 존재하지만 색상은 투명
		* background-color가 아닌 opacity:0;은 자신을 포함한 내부 element모두 투명 효과
1. background-image : 
	- url("test.jpg") ,url("test2.png");  이미지담기 " "로 구분 중간에 ,로 표기 사용시 여러장의 이미지 삽입가능(background-position으로 위치 설정)
	- linear-gradient(45deg, #faa 50%, #fa0 100%); 직선형 그라데이션 색상만들기
		linear(방향성을가진), deg(degree_각도), 색 위치(그라데이션 색 포인트위치)
	- radial-gradient(#faa 50%, #fa0 100%); 회전형 그라데이션 색상만들기
1. background-position :
	- left top, right bottom;  두장의 배경이미지를 사용했을경우 ,로 구분하여 위치를 설정
	
1. background-repeat : 반복여부
	- repeat
	- repeat-x
	- repeat-y
	- no-repeat
1. background-attatchment : 스크롤시 위치 고정여부
	- scroll
	- fixed
1. background-size : 주어진 element 크기에 어떻게 맞출것인가를 판단하는 속성
	- 100%; 가로기준해서 100%크기(상대)값을 가짐
	- 100% 50%; 가로100%, 세로 50% 크기(상대)값을 가짐
	- cover ; 화면에 이미지를 꽉채우겠다
	- contain ; 이미지 전체를 다 보이게 하겠다


### display: inline, block, inline-block

### 단위값(반응형에따른)_vh, vw

___
## 도형 모양

### box-sizing

### border-radius

### box-shadow / text-shadow

___
## animation

### transition

### animation / @keyframes

___
## responsive web design(RWD)

### mediaquery(@media screen)

### jQuery에서 RWD작업시 설정사항

### 단위값 다시한번 확인!!!

### retina display







