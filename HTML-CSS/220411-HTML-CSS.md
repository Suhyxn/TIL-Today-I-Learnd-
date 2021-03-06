# 2주차 4/2 ~ 4/8 

<hr/>

### 웹사이트는 크게 3종류로 나뉜다
## HTML / CSS / JavaScript
  
![](https://imagedelivery.net/v7-TZByhOiJbNM9RaUdzSA/966ea84e-a4d1-4508-2997-7497071a0c00/public)
  
#### 웹사이트 생성을 캐릭터 얼굴 생성과 비유한다면
HTML를 통해 눈, 코, 입 (뼈대) 를 만들고 CSS를 통해 배치하고 (꾸미고) JS를 통해 움직임(기능)을 추가한다.

#### HTML : HyperText Markyp Language
#### CSS : Cascading Style Sheets
#### JS : JavaScript

<br/>
<br/>

### 크로스브라우징(Cross Browsing)이란? 
<li>조금은 다르게 구동되는 여러 브라우저에서, 동일한 사용자 경험(같은 화면, 같은 동작 등)을 줄 수 있도록 제작하는 기술, 방법.</li>

<br/>
<br/>

<hr/>

<br/>

## 부모와 자식 요소

```
<div class="1">
	<div class="2">
    	<div class="3"> 기준 </div>
    </div>
</div>

div 태그들을 숫자로 표기한다면
3을 기준 1번은 상위(조상) 요소이다.
3을 기준 2번은 부모 요소이다.
1을 기준 3번은 하위(후손) 요소이다.
1을 기준 2번은 자식 요소이다.

```
<br/>
<br/>

### 컨테이너 태그란? (ex.div, span)
<li> 콘텐츠나 레이아웃에 아무런 영향도 주지 않고, 단지 다른 요소 여럿을 묶어 관리하기 편하게 만드는 역할을 하는 태그를 '컨테이너'라고 한다. </li>

<br/>
<br/>

## Block 요소와 Inline 요소

### Block 요소 : 상자 (레이아웃)를 만들기 위한 요소들 (ex.div)
<ul>
<li>요소가 수직으로 쌓인다 </li>
<li>가로는 부모 요소의 크기 만큼 늘어나며 세로는 콘텐츠 크기 만큼 줄어든다. </li>
<li>가로는 + 늘어나려는 습성 세로는 - 줄어드려는 습성을 갖고 있다. </li>
<li>가로/세로 너비와 내/외부 여백 지정이 가능하다. </li>
<li>인라인 요소와 블럭 요소 상관없이 모두 자식 요소로 가질 수 있다. </li>
</ul>


### Inline 요소 : 글자를 만들기 위한 요소들 (ex.span)

<ul>
<li> 요소가 수평으로 쌓인다. </li>
<li> 콘텐츠의 크기 만큼 자동으로 줄어든다. </li>
<li> 가로와 세로 모두 - 줄어드려는 습성을 갖고 있다. </li>
<li> 가로/세로 너비를 지정할 수 없으며 내/외부 여백은 좌우만 가능하다. </li>
<li> 블럭 요소를 자식으로 가질 수 없다. </li>
</ul>

### Inline-block 요소 : inline 특성과 block 특성을 섞은 요소 (ex.input)

<ul>
<li> 요소가 수평으로 쌓인다. </li>
<li> 여백과 너비를 지정 가능하다. </li>
</ul>

<br/>
<br/>

## 전역 속성(Global attributes)이란?
모든 HTML 태그에서 공통으로 사용할 수 있는 속성이다.

속성이란 태그의 부가적인 기능을 정의하는 것으로, 선택사항이다.
속성은 시작태그의 내부에 정의한다. 속성의 개수에는 특별한 제한이 없다.


```
<태그명 속성명="속성값" 속성명="속성값">콘텐츠</태그명>
대포적인 전역 속성들

id : 요소에 고유한 이름을 부여하는 식별자 역할 속성.
class : 요소를 그룹 별로 묶을 수 있는 식별자 역할 속성.
style : 요소에 적용할 css 스타일을 선언하는 속성.
title : 요소의 추가 정보를 제공하는 텍스트 속성.(툴팁)
```

<br/>
<br/>

### 상속(Inherit)
<ul>
<li> CSS 속성들은 부모요소들이 자동으로 자식요소에게 상속되도록 한다. </li>
<li> 상속 기능들 대부분은 글자/문자와 관련이 있다! <br/>
  (inherit 을 통한 강제 속성 방법이 있으나 모든 속성이 가능하지는 않다.) </li>
</ul>

<br/>
<br/>

## CSS 선택자
```
선택자 { }

< 기본 선택자 >

* {} 				/* 기본 전체 선택자 */
ABC {} 				/* 태그 선택자 */
.ABC {}				/* 클래스 선택자 */
#ABC {}				/* 아이디 선택자 */

< 복합 선택자 >

ABCXYZ {}			/*일치 선택자 */
ABC>XYZ {}			/*자식 선텍자 */
ABC XYZ {}			/*하위(후손) 선택자 */
ABC+XYZ {}			/*인접한 형제 선택자 (한가지만 선택) */
ABC ~ XYZ {}		/*일반 형제 선택자 (모두 선택) */

< 가상 클래스 선택자 >

ABC:hover {}		/* 마우스 커서가 올라가 있는 동안 선택 */
ABC:active {}		/* 마우스를 클릭하고 있는 동안 선택 */
ABC:focus {}		/* 포커스 되면 선택 */
ABC:first-child {}	/* 형제 요소 중 1번째라면 선택 */
ABC:last-child {}	/* 형제 요소 중 막내라면 선택 */
ABC:nth-child(n) {}	/* 형제 요소 중 n번째라면 선택 */
ABC:not(XYZ) {}		/* XYZ 요소가 아닌 ABC 요소 선택 */

< 가상 요소 선택자 >

ABC::before {}		/* 요소의 내부 앞에 내용을 삽입 */
ABC::after {}		/* 요소의 내부 뒤에 내용을 삽입 */

< 속성 선택자 >

[ABC] {}			/* 속성 ABC를 포함한 요소 선택 */
[ABC="XYZ"] {}		/* 속성 ABC를 포함하고 값이 XYZ인 요소 선택 */
```

<br/>
<br/>

## 선택자 우선순위

<ul>
<li> 같은 요소가 여러 선언의 대상이 된 경우, 어떤 선언의 css 속성을 우선 적용할지 결정하는 방법 </li>
<li> 점수가 높으면 선언이 우선한다. </li>
<li> 만약 같다면, 가장 마지막에 해석된 선언이 우선한다. </li>
</ul>

```
1.!important : 무한대
2.인라인 방식 스타일 명시 : 1000점
3.ID 선택자(#) : 100점
4.Class 선택자(.) : 10점
5.태그 선택자(div) : 1점
6.전체 선택자 (*) : 0점

🎯  인라인 방식과 important 방식은 가급적 사용하지 않는 것을 권장한다.
```
<br/>
<br/>

## Position

```
 static 
  
기본값으로 위치를 지정하지 않았을 때와 같다.
위치를 임의로 설정해 줄 수 없다

relative 
요소 자신을 기준으로 상대 위치를 조절한다.
상대 위치가 지정된 relative 요소는 절대 위치 요소에 대한 컨테이너 블럭으로 사용될 수 있다. ( 자식요소의 positiono:absolute 의 위치 기준이 됨 )

absolute
가장 가까운 상위 요소 (부모 태그)를 기준으로 위치가 결정된다.
부모 중 포지션이 relative, absolute, fixed 인 태그가 없다면 최상위 태그 body가 기준이 된다.
원래 위치와 상관 없이 위치 지정이 가능하다.

fixed
뷰포트(브라우저)를 기준으로 위치를 조절한다.
상위 요소에 영향을 받지 않고 화면이 바뀌더라도 고정된 위치를 설정할 수 있다.

sticky
스크롤 영역을 기준으로 위치를 조절한다.
부모 요소 중 어느 하나라도 overflow : hidden 값일 경우 동작하지 않는다.

inherit
부모 태그의 속성값을 상속받는다. 
```

</br>
</br>

## Display: Flex

Flex container의 화면 출력(보여짐) 특성
flex : 블럭 요소와 같이 flex container 정의
inline-flex : 인라인 요소와 같이 flex container 정의

![](https://velog.velcdn.com/images/momentomori/post/c2aadd16-1dfd-41f1-ad4d-b9d3e87e11f8/image.png)

Flex 내에서 Container는 Items를 감싸는 부모 요소이며, 각 Item을 정렬하기 위해선 Container가 필수이다.
Container에는 display, flex-flow, justify-content 등의 속성을 사용할 수 있으며,
Items에는 order, flex, align-self 등의 속성을 사용할 수 있다.

<blockquote>

```
Flex Container

display	: Flex Container를 정의
flex-flow : flex-direction와 flex-wrap의 단축 속성 
flex-direction : Flex Items의 주 축(main-axis)을 설정 
flex-wrap : Flex Items의 여러 줄 묶음(줄 바꿈) 설정 
justify-content : 주 축(main-axis)의 정렬 방법을 설정 
align-content : 교차 축(cross-axis)의 정렬 방법을 설정(2줄 이상) 
align-items : 교차 축(cross-axis)에서 Items의 정렬 방법을 설정


Flex itmes


order : Flex Item의 순서를 설정 
flex : flex-grow, flex-shrink, flex-basis의 단축 속성 
flex-grow : Flex Item의 증가 너비 비율을 설정 
flex-shrink : Flex Item의 감소 너비 비율을 설정
flex-basis : Flex Item의 (공간 배분 전) 기본 너비 설정
align-self : 교차 축(cross-axis)에서 Item의 정렬 방법을 설정 

```
</blockquote>


