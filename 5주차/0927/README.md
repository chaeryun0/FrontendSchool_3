# 📚 SVG(Scalable Vector Graphics)란?

> **확장 가능한 벡터 그래픽(scalable vector graphics)으로 XML 기반의 2차원 그래픽** <br>
> → HTML 태그의 집합으로 이루어져 있어 css와 javascript로 컨트롤이 가능 


```
✓ SVG의 장점

- 아무리 확 해도 이미지가 깨지지 않음
- 이미지의 크기를 키워도 용량이 늘어나지 않음
- 검색엔진 최적화에 용이

✓ SVG의 단점

- 코드로 이루어진 이미지이기 때문에 복잡한 이미지일수록 파일 사이즈가 커짐
- 레거시 브라우저에서는 작동되지 않음
- 단순한 모양일수록 효율이 좋음
- 주로 단순한 아이콘, 로고, 도형 등을 구현할 때 많이 사용 
  → 복잡한 이미지를 굳이 SVG로 표현하고자 하면 오히려 용량이 너무 거대해져 역효과가 날 수 있음
````

### 📝 HTML에 SVG를 적용하는 여러가지 방법들

1. img 태그로 사용하기
2. css background로 사용하기
3. 인라인으로 구현하기
4. Object 태그 사용하기

> SVG가 필요하지만 이미지에 별다른 조작을 가하지 않을 것이라면 👉🏻 ```<img/>``` 또는 ```background-image``` <br>
> SVG가 필요하고 이미지에 조작을 가할 것이라면 👉🏻 ```인라인``` 또는 ```<object>```

<img svg-frog src="https://user-images.githubusercontent.com/112460430/192587732-f096791a-5024-40ee-9bc6-25eb0e3e1b3b.gif" width="25%">


# 📚 Sass(Syntactically Awesome Stylesheets)
 

> **CSS로 컴파일 되는 스타일 시트 확장 언어이며 CSS 전처리기의 하나**<br>
  
> CSS를 편리하게 작성하게 해주는 스타일 시트 확장 언어이며, CSS로 컴파일이 된다. <br>
> 브라우저가 Sass를 직접 로딩하는 것이 아니라 개발은 Sass를 기반으로 한 후, CSS로 익스포트하는 과정을 거친다.

 ### ﹅ 파일 분리 : 2가지 방법
```
- 방법1 : style.scss 파일은 컴파일러를 통해 style.css이 만들어진다.
- 방법2 : _header.scss파일명 앞에 "_"를 사용할 경우, 컴파일러를 통해 _header.css가 만들어지지 않는다. 
         레이아웃 별로 나눠 scss를 저장한 다음, style.scss 파일 안에 @import "header"; 로 가져올 수 있다. 
        (가져온 파일들을 컴파일러가 하나의 style.css로 만들어주는 것)
```
### ﹅ 중첩(Nesting)

- html의 시각적 계층 방식과 동일하게 CSS를 중첩하여 작성할 수 있다.
- 속성을 중첩 할 때는 콜론`:`을 사용
- CSS코드가 구조화 되어 가독성이 높아지며 유지 보수하기 편리

### ﹅ ampersand 앰퍼샌드

- `&`는 상위에 있는 부모선택자를 가리킴
- `&`을 이용하여 after, hover 등의 가상요소, 가상클래스, class나 id 셀렉터 등을 참조 가능
- `&`을 응용하여 공통 클래스 명을 가진 선

### ﹅ @at-root

- `@at-root`키워드를 사용하면 중첩에서 벗어날 수 있음
- 중첩에서 벗어나고 싶은 선택자 앞에 `@at-root`를 작성
- 중첩된 선택자에게만 사용 가능
```
.article {
  display: flex;
  .article-content {
    opacity: 0.7;
    @at-root i { // @at-root 중첩에서 벗어나 i 태그들의 투명도를 0.5로 설정
      opacity: 0.5;
    }
  }
}
```
