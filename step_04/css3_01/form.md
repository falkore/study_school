form
==
xhtml기반의 form
--
> 기초
1. form태그안에는 fieldset(영역), legend(제목/영역 내)
2. input는 반드시 label과 함께(input의 id값과, label의 for값이 같아야 한다.)
3. input의 type에 따라서 모양과 기능이 달라진다.
	- text : 글자입력
	- password : 가려진 글자입력
	- radio : 선택(해제x)
	- checkbox : 선택(다중선택)
	- submit : 확인버튼
	- reset : 취소
	- image : 이미지삽입 src, alt동반
	- button : 버튼(확인/ 취소를 제외)
	- file : 첨부파일
	- hidden : 보이지 않는형태(label사용안해도 됨)
4. 서버에 전달되는 값은 value, 이름은 name
5. textarea 는 여러줄 입력 
6. select는 선택(option, optgroup)
7. button태그는 다양한기능을 한번에 처리 가능

```
<form action="#" method="get">
	<fieldset>
		<legnend>제목</legnend>
		<input type="" name="" value="" id="">
		<label for=""></label>
	</fieldset>
	<fieldset>
		<textarea name="" id="" cols="30" rows="10"></textarea>
		<select name="" id="">
			<optgroup>
				<option value=""></option>
				<option value=""></option>
				<option value=""></option>
			</optgroup>
		</select>
		<button type=""></button>
	</fieldset>
</form>
```







html5에서 추가된 내용
--
> form기능은 아주 많은 부분들을 다루기때문에 엄청난 코드가 생겨났다~(기존의 2배이상)
하지만, 아직 브라우저마다 호환성이 낮기때문에 모든기능이 작동하지는 않는다.
또한 작동되더라도 전혀 다른 성격으로 표현되기도 한다.

1. 입력(일부 선택)
	> 자바스크립트에 의존하던 검증기능들을 html5에서 사용가능하게 추가기능 생겼다.
	* required: 입력된 내용을 정확하게 검증하기위한 기능(또한, 필수 입력사항)
	* placeholder: input내용에 미리 내용을 삽입하여 접근성을 높이는 기능
	* autofocus: 자동으로 포커스가 잡혀서 바로 내용을 입력할 수 있게 하는기능
		- 단, 한번만 사용하기를 권하며, 내용이 스크롤을 움직여서 자리잡은곳에 있다면, 사용 배제
	* autocomplate: 자동 완성기능
	
	- email : <input type="email" />
	- url : <input type="url" />
	- search : <input type="search" />
	- tel : <input type="tel" /> -- 모바일로 구현시에는 숫자키패드가 나타난다
	- date : <input type="date" />
	( date, year, week 등 날짜와 관련된 내용은 브라우저마다 완전히 다른기능을 보여주거나 아직 구현이안된 것들도 많다.!)
<!--
	- year
	- week
-->
	
2. 선택
> number, range는 일정 범위, 단계를 지정해주어야한다(min, max, step)
	- number: <input type="number" />
	- range: <input type="range" />
	- color: <input	 type="color" />
	
3. 버튼(기존과 크게 달라지지 않았다!)
4. 멀티(기타)
	










