##javascript    

###script 작성위치
1. head영역 내부에 작성(inline script)
2. body영역에 작성
 - html 코드내부에 작성
 - body 말미에 작성
3. 외부에서 불러오는 방법(src)

###javascript
```
<script src=""></script> 
// 외부 문서 불러오기, script 내부에 작성할 수 없음
<script type="text/javascript"></script>
// script 기본형태

```

### 간단한 이해해야하는 내용
1. 주석
 - // 한줄주석(간단한 설명)
 - /* */ 여러줄 주석(지시, 가이드)
2. 문자일 경우 "", '' 표기 짝은 맞출 것~!!
3. 내용이 끝났을 경우 ;
4. 사용자가 이해할 수 있게 코드를 이쁘게 가독성있게
  정리할 것 ~!!!
5. 속도, 작업자의 원활한 (쾌적한) 환경을 위해서 변수
  VAR(variable) 를 사용하시오 ~!!!
6. 변수 선언시 var가 없어도 변수는 선언되지만 !!
  사용하지 않을 것~!!!
  (전역변수: 추후 변경도 되지 않으며 웹을 무겁게 만드는 요인이 됨. 좋지 않은 방법)
7. 결과물을 확인하는 방법
  - document.writeln(); 
  // 실제 어떠한 표현시에만 사용, 테스트용 아님.
  // 브라우저에서 보이기
  - alert();
  // 메세지창
  - console.log();
  // 주로 작업 과정 / 결과 확인시(개발자모드에서 확인)
8. 결과물 처리하는 방법***
  -  return : 결과물이 보이지 않는다. 중간처리값
              결과값(도출값)을 임시로 저장 !!
              
              
### 선택자 !!!
1. tagName : document.getElementsByTagName();
2. class : document.getElementsByClassName();
3. id : document.getElementById();
4. ECMA 5 추가된 선택자 : document.querySelector(); // id, class, tagname 모두 가능합니다.

* 항상 변수를 생활화 하자 ~!!!
* 변수로 선언 후 class 선택시....
* 사용할 때 변수[]로 표기(배열 !!)

### 입력 또는 생성
1. 코드 생성하기 :  document.createElement();
2. 내부에 작성  :  .innerHTML = "";

### javascript 형식
1. number  : 숫자
2. string  : 문자
3. boolean : true/false
4. 배열     : Array [a, b, c, d];
5. 객체     : Object {a:1, b: 2, c: 3};
            var box = {};
                box = {a:1, b: 2, c: 3};
                box.b = 77;
                box = {a:1, b: 77, c: 3};
6. 함수     : function(){}; // 함수 끝나고 다시 이름(); 으로 결과값 도출 시켜야 함
            function box(){};
            var box2 = function(){};
            (function(){})(); // ()안의 결과값이 즉시 도출됨. 즉시 실행 함수
            
            재귀함수는 함수 안에서 자신을 호출하는 형식
            자기호출함수는 해석과 동시에 실행되는 코드블럭
7. null/undefined  :
  var box= null,    //null
      box2;         //undefined

