# dom 요소 선택
dom : 자바스크립트로 html요소들을 객체처럼 다루는 구조

## querySelector 

```document.querySelector```   
문법 ```document.querySelector(selectors);```

document.querySelector는 쉽게말해서 js가 html에 연결해 상호작용하게하는 첫번째 단계이다.   
예를 들어서 
1. 사용자의 동작을 감지할때    
버튼을 눌렀을때 무엇을 실행하려면 일단 그버튼이 뭔지 자바스크립트가 알아야 한다.
* 예:
```const btn = document.querySelector('바꿀버튼의 클래스');```
라고 선언해서 버튼을 지정하고 동작을 적는다
2. 화면의 내용을 실시간으로 바꿀때    
사용자가 버튼을 클릭하면 실시간으로 글자를 바꾸거나 숫자를 올릴때 사용한다.
* 예: 장바구니에서 +를 누르면 숫자가 올라가게하려면,버튼을 누르면 지정된 숫자영역의 수를 1올리게 변경한다.

## querySelectorAll

아까 설명한 querySelector은 일치하는것 하나만 선택되는데 이건 일치하는 모든요소를 묶어서 선택된다

querySelectorAll을 사용하는이유는 웹사이트에 있는 채크박스나 여러개의 아이템에 한꺼번에 같은 효과를 주고싶을때 사용한다

## 주의할 점

querySelector로 가져온것은 하나여서 바로 코드를 작성해도 되지만 querySelectorAll은 여러개가 담겨있기 때문에 반복문을 통해 하나씩 꺼내서 바꿔줘야한다


## dom 요소 생성

1. creatElement    
새 html요소를 생성한다    
문법: ```document.createElement("태그이름")```   
예를 들어 h1캐그를 만들고싶으면 태그이름에 h1을 넣으면 된다. 근데 중요한점은 화면에는 나타나지 않은 상태이다.

2. appendChild    
appendChild로 불러온 박스를 맨아래에 붙이라는 뜻이다.    
문법: ```document.body.appendChild(newDiv);```    
newDiv라는 박스를 body의 맨아래에 붙이라는 뜻이다.

3. innerHTML    
선택한 태그 안을 새로운 html코드로 인식하는 도구    
문법: ```box.innerHTML = '<h2>새로운 제목</h2>';```      
box라는 요소에 h2크기의 새로운 제목으로 갈아엎는다는 것이다.    
```innerHTML```의 문법은 변수에 값을 저장하듯이 = 를 사용하게 된다.+=를 쓰면 원래 내용뒤에 새로운 내용을 덧붙일 수 있다. = 없이 이름만 쓰면 그 안에 있는 html코드를 그대로 가져온다.

4. textContent   
이름대로 안에 들어있는 글자 내용만 다루는 속성이다.    
문법: ```myTitle.textContent = '안녕하세요, 반갑습니다!';```  
문법은 innerHTML과 같다 하지만 textContent는 태그를 넣어도 그것을 태그로 인식하지 않고 글자로 인식해서 그대로 화면에 출력한다.
 