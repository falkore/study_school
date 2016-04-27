# 멀티미디어
## 멀티미디어란?
음악, 동영상등을 재생/듣거나..등등 ..
이전에는 음악/동영상 재생이 불가능했다. 별도의 플러그인 설치,
html5부터는 자체브라우저만으로도 재생이 가능하다!!

### 음악(audio)
기본:  
```
<audio src="" controls="controls" autoplay volume="" mute="" />
```
> audio태그는 파일의 허용범위는 브라우저마다 다르다.
* mp3는 거의 대다수 허용한다.(하지만, 유료다 - 게임 및 상업, 개인등 5000번이상 재생 )
	- firefox에서는 공식적으로 허용하지 않는다~
	
* ogg 파일은 무료다~~(2001년 전후 mp3가 유료라는 맹점때문에 별도로 무료로 개방하기위해 만든 파일형식)
	- ms에서 작동 되지 않는다.
	
* wav 파일은 ms에서 작동한다~
	- chrome, apple 에서 작동 x
	
```
<audio controls="controls" autoplay="autoplay">
	<source src="" type="audio/ogg" />
	<source src="" type="audio/mp3" />
	<source src="" type="audio/wav" />
	당신의 브라우저는 음악이 나올 수가 없습니다~~ 업데이트 하세욤~
</audio>
```
	
### 비디오(video)
기본:
```
<video src="" controls="" autoplay="" poster="" />
```
> video태그는 오디오와 마찬가지로 브라우저마다 지원파일이 다르다~!!!!!
* mp4 파일은 대다수 허용하지만 mp3보다는 덜하다~~~
	- 영상은 h.264 코덱만 허용, 음성은 AAC코덱만 허용  
	- 대다수 허용하고있지만, 실제로 사용이 안되는 경우도 많다.	
* webM 파일은 구글에서만들었지만 완전 무료 파일이다~
	- IE, safari에서는 사용할 수 없다.
* ogv 파일은 무료로 사용할 수 있는 파일이다.
	- 코덱은 테오라 코덱을 사용한다.
	- 인코딩(컨버팅) 은 파이어폭스 사이트에서 제공하고있다.

```
<video controls="" autoplay="" poster="">
	<source src="" type="video/webM" />
	<source src="" type="video/ogv" />
	<source src="" type="video/mp4" />
	현재브라우저 제공안해욤~
</video>
```
**음악이든, 영상이든 3초이상 재생시 
반드시 정지하거나 무음처리 할 수 있는 버튼을 만들어라**
**영상파일의 경우 1초에 3번이상 깜빡임이 재생되는 파일은 사용할 수 없다!!!**

### iframe
> 문서파일이든, 영상이든 관계없이 외부 별도의 문서를 불러와서 사용하는 방법
문서를 불러올 경우에는 src를 사용하며, frameborder는 불러오는 파일의 외곽선을
보이게하는 여부를 판단 "0 | 1"
* 외부파일을 불러오다보면 정확한 사이즈를 맞추지 못하는 경우도 있다~
이에 iframe태그에 div태그로 감싸는 것이 좋다~

```
<iframe src="" frameborder="0" ></iframe>
```

### 플래시
> 플래시파일의 경우 현재 대다수의 브라우저에서 지원이 원활하지 않다.
하지만 별도의 파일로 불러와서 인식 시킬수는 있다.
* 가급적 플래시는 사용하지 않는 것이 좋다.

```
<embed src="플래시파일.swf" />
```







