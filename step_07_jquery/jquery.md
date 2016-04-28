
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

    

    
    
    
    