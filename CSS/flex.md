# css flex속성

## flex box에 대해서

flex는 css에 display속성중 하나로 박스 레이아웃을 작성할 때 사용되는 유용한 방법이다.   
flex는 flexible이라는 단어에서 따온대로 유연하고 균형잡힌 배치가 가능하다.

## 활용예시

```
//HTML
<body>
    <div id="parent">
        <div class="child">box1</div>
        <div class="child">box2</div>
    </div>
</body>

//CSS
* {
    box-sizing: border-box;
    margin : 10px;
    padding : 10px;
}

#parent {
    width : 300px;
    height : 100px;
    display: flex;
    flex-direction: row;
    border : 3px solid red;
}

.child {
    flex: 1 0 auto;
    border : 3px solid green;
}
```
이걸 실행하면 parent에 맞춰 child가 일정한 비율을 유지한채로 위치 되는것을 확인할수있다.   
또한 flex의 장점은 css만 맞추어 놓으면 자식 엘리먼트가 추가 되어도
비율을 유지한다는 것이다.  
parent에 box를 하나더 추가하면 똑같이 일정한 비율로 유지해서 위치된다.

* display: flex;   
-flex 레이아웃을 적용한다.
* flex-direction:row   
-내부 요소들의 정렬 방향    
-row는 가로방향 정렬   
-column은 세로방향 정렬   
-reverse는 각 방향의 반대에서 부터 정렬   

## 부가 flex 속성

1. flex-wrap:줄바꿈 설정하기

자식 요소들의 수가 많아져서 개수가 꽉차면,부모요소에   
``` flex-wrap:wrap ```을 적용하면 자동 줄바꿈을 해준다

2. justify-content:축 수평방향 정렬

* flex-start:시작점을 기준으로 정렬
* flex-and:끝점을 기준으로 정렬
* center:중앙 정렬
* space-between:양 끝에 붙혀서 정렬
* space-around:중앙점과 양 끝을 기준으로 정렬

3. align-items:축 수직 방향 정렬

* stretch:기본값으로 세로 정렬
* flex-start:수직방향의 위쪽
* flex-end:수직 방향에 아래
* center:수직방향 가운데
* baseline:글자 기준선으로 정렬

