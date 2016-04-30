
jQuery
===
> javascript library

```
<script>
    $(document).ready(function(){
    //jQuery 코드 작성
    // javascript 코드도 쓸 수 있음
    });
</script>
```

## jQuery 선택자!
0. 종류가 다양하여 상황에 맞는 쓰임에 맞는 선택자를  찾아서 사용할 수 있다.
1. $() 로 시작하여 () 내부에 작성하도록 한다.
2. 변수가 아닌이상 css 선택자와 동일하게 작성할 수 있다.
3. 자식선택자의 경우! >        
    :  $("ul>li") => $("ul").children("li") 로 표기 할 수 있다.
4. 자손선택자의 경우! 빈칸 
    :  $("ul a") => $("ul").find("a") 로 표기 할 수 있다.
5. nth 선택자의 경우! :nth-child()   --->.eq()
    :  $("ul>li:nth-child(2)") => $("ul>li:eq(1)")  
                              => $("ul>li").eq(1)
                              => $("ul").children("li").eq(1)
    로 표기 할 수 있다.
6. nth 중 first/last 선택자   ---> .first() / .last()
    : first-child / : last-child
    => $("ul>li:first-child")
    => $("ul>li:first")
    => $("ul>li").first()
    => $("ul").children("li").first()
    
    => $("ul>li:last-child")
    => $("ul>li:last")
    => $("ul>li").last()
    => $("ul").children("li").last()
    
7. 형제선택자  '+' (바로 뒤 형제), '~' (형제 관계)
    :  $("dl>dt:first + dd") => $("dl>dt:first").next("dd")
       $("dl>dt:first ~ dd") => $("dl>dt:first").siblings("dd")
    
    (jQuery에는 이외에도 몇 가지가 더 있다.)
    :  $("dl>dt:last").prev("dd")   // 바로 앞(이전) 선택
    :  $("dl>dt").eq(1).not()       // dt 중 두번째 dt가 아닌 모든 것을 선택
    :  $("dt").parent()             // 부모(상위) 선택
    
8. 홀수/짝수 선택자(.odd / .even)
    :  $("ul>li:odd") => $("ul>li").odd()     // 홀수
    :  $("ul>li:even") => $("ul>li").even()   // 짝수
    (실제 순서는 반대로 보임 : 0부터 시작해서)
    
9. 자신 선택자
    :  $(this) 선택한 자신
    
    ex) 
    ```
       $("ul>li").on("click", function(){
          $(this).css({"background-color" : "pink"});
       });
    ```

10. 각각  '.each()' : 사용하면 메모리 축적이 덜 되기 때문에 좀 더
                    간결하고 오류가 덜 발생하게 만듦...?
                    또는 각 각 지정하고자 할 때...
                    
---
## 속성 변경하기
1. .css()   '두 가지 이상의 속성을 변경할 경우 각각의 속성사이에 ','(쉼표)로 구분해 준 뒤, 같은 방식
            으로 css의 속성명과 속성값을 추가할 수 있다.
    :  .css("color", "#faa").css("background-color", "#adf").css("font-size", 8 + "rem");
       .css({"color": "#faa", "background-color": "#adf", "font-size": 8 + "rem"});
       .css({color: "#faa", backgroundColor: "#adf", fontSize: 8 + "rem"});
       
2. .attr()  '속성을 의미.  html의 속성을 변경할 때 사용함'
    :  $("img").attr("src", "./test2.jpg").attr("alt", "테스트 이미지로 변경");
    :  $("img").attr({"src": "./test2.jpg", "alt": "테스트 이미지로 변경"});
    
3. .val()   'value를 의미.  form 태그 사용시 들어가는 값'
    :  $("input").val("값을 변경");
    
4. .html()  'html "코드"를 삽입'
    :  $("p").html("<a href=\"#\">link</a>");
    
5. .text()  '글씨를 삽입하거나 변경'

ex)
   $(this).find("a").text("따옴표를 조심하자 특히, 시작과 끝부분~")
                   .attr("href", "http://naver.com")
     
---
## 이벤트
> 사용자가 웹상에서 특정한 행동을 취하는 것!

ex) click, dblclick, drag, keydown, keyup, scroll,
    mouseover, mouseout, mouseenter, mouseleave,
    resize

    $(window).on("resize", function(){
        $("body").css("background-color", "#afd");
    });
<<<<<<< HEAD
    
    
---
## 문법

### for

> javascript 내 ' for 문 ' 개념
```
  for 문은 여러개의 반복효과를 가질 때 사용하는 기능
```
  for ( 최초의 변수명 = 최초값 ; 변수명 >= 최종 값 ; 연산값 ){
        console.log(변수명);
  };
```javascript
  var sum = 0;
  for(var i = 0 ; i <= 100 ; i = i+1) {
    console.log(i);
    sum += i;       // sum 의 변수에 0~100 까지의 값을 더한 수를 저장.
  };

```
  
  // ' i=i+1; '  ==  ' i +=1 '   우측이 ( '+=', '-=' ) 속도가 더 빠릅니다.
  // ' i=i-1; '  ==  ' i -=1 '
  // ' i++ '  먼저 i값을 도출시키고 1을 더하는 값은 가지고 있음(예: 1(+1)) 
              =>다음 결과는 +1이 된 값이 대입됨.
  // ' ++i '  1+i 값
  
  
  
```
*.append   :  메소드는 각 요소의 마지막 자식으로 지정된 내용을 삽입합니다
*.prepend  :  메소드는 각 요소의 첫 번째 자식으로 지정된 콘텐츠를 삽입합니다
```
(function($){})(this.jQuery);  // 다른 javascript library 와의 충돌을 방지하기 위해
                                  끝에 this(전역변수).jQuery 를 써줌..
                                  $ 가 jQuery 임을 명시해 주는 것임
                                  
                                  
```
슬라이드 메뉴 활용 --- jquery_05.html
```
마우스오버(mouseover)와 마우스엔터(mouseenter)
    : 마우스엔터는 자기자신에게 포인터가 와야 반응함(메모리소요가 상대적으로 적음)
마우스리브(mouseleave)와 마우스아웃(mouseout)


### if
 조건문
=======
>>>>>>> 2717f307e75aa3305521ccd64743c2d0fd399128

    

    
    
    
    