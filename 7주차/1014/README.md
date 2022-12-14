# ๐ DOM (Document Object Model)

๏น HTML ๋ฌธ์์ ๋ด์ฉ์ ํธ๋ฆฌํํ๋ก ๊ตฌ์กฐํํ์ฌ ์นํ์ด์ง์ ํ๋ก๊ทธ๋๋ฐ ์ธ์ด๋ฅผ ์ฐ๊ฒฐ์์ผ์ฃผ๋ ์ญํ   <br>

๏น ๋ธ๋ผ์ฐ์ ๋ ์๋ฒ์์ ๋ฐ์ ๋ฌธ์์ธ HTML, CSS๋ฅผ ํ์ฑํ๊ณ , ๊ทธ ๊ฒฐ๊ณผ๋ฌผ์ธ `DOM ํธ๋ฆฌ`์ `CSSOM ํธ๋ฆฌ`๋ฅผ ์ตํฉํด ์ฌ์ฉ์ ์ฅ์น์์ ๋ณผ ์ ์๋๋ก ๋ณํํ๋ค. <br>
๏น **DOM ํธ๋ฆฌ๋ HTML์, CSSOM ํธ๋ฆฌ๋ CSS ๋ฅผ ์กฐ์ํ๋ API(Application Programming Interface)**  <br>

- ๋ธ๋(node) : ๊ฐ๊ฐ์ ์์์ ์์ฑ, ์ฝํ์ธ ๋ฅผ ํํํ๋ ๋จ์  <br>
- Parsing(ํ์ฑ) : ์ผ๋ จ์ ๋ฌธ์์ด์ ์๋ฏธ์๋ token์ผ๋ก ๋ถํดํ๊ณ  ์ด๋ค๋ก ์ด๋ฃจ์ด์ง parse tree๋ฅผ ๋ง๋๋ ๊ณผ์ 

## ๐ DOM ํธ๋ฆฌ์ ์ ๊ทผํ๊ธฐ

> document ๊ฐ์ฒด๋ฅผ ํตํด HTML ๋ฌธ์์ ์ ๊ทผ์ด ๊ฐ๋ฅ <br>
> document๋ ๋ธ๋ผ์ฐ์ ๊ฐ ๋ถ๋ฌ์จ ์นํ์ด์ง๋ฅผ ๋ํ๋ด๋ฉฐ, DOM ํธ๋ฆฌ์ ์ง์์  ์ญํ ์ ์ํ

```
// ํด๋นํ๋ Id๋ฅผ ๊ฐ์ง ์์์ ์ ๊ทผํ๊ธฐ
document.getElementById()

// ํด๋นํ๋ ๋ชจ๋  ์์์ ์ ๊ทผํ๊ธฐ
document.getElementsByTagName(); 

// ํด๋นํ๋ ํด๋์ค๋ฅผ ๊ฐ์ง ๋ชจ๋  ์์์ ์ ๊ทผํ๊ธฐ
document.getElementsByClassName(); 

// css ์ ํ์๋ก ๋จ์ผ ์์์ ์ ๊ทผํ๊ธฐ (๊ฐ์ฅ ์ฒซ๋ฒ์งธ์ ์๋ ์์๋ง)
document.querySelector("selector");

// css ์ ํ์๋ก ์ฌ๋ฌ ์์์ ์ ๊ทผํ๊ธฐ
document.querySelectorAll("selector");
```

## ๐ง DOM ์ ์ด ๋ช๋ น์ด

**1. ์ด๋ฒคํธ ์ฝ์ : target.addEventListener( type, listener )**
```
<button>๋ฒํผ</button>
// ์ด๋ฒคํธ์ ํ์์๋ click, mouseover, mouseout, wheel ๋ฑ ๋ค์ํ ์ด๋ฒคํธ๋ฅผ ๊ฐ์งํจ
// listener ํจ์์ ์ธ์์๋ ์ด๋ฒคํธ์ ๋ํ ์ ๋ณด๊ฐ ๋ด๊ฒจ์์

const myBtn = document.querySelector("button");

myBtn.addEventListener('click', function(){
  console.log("hello world");
})
```
**2. ํด๋์ค ์ ์ด : DOM api๋ฅผ ํตํด ์์์ class ์์ฑ์ ์ ์ด**
```
const myBtn = document.querySelector("button");
myBtn.addEventListener('click', function(){

myBtn.classList.add("blue"); // blue ๋ผ๋ ํด๋์ค์ ์์ฑ ๊ฐ์ ์ง์  // ๋ฒํผ์ ํด๋ฆญํ๋ฉด html ํ๊ทธ์ class๊ฐ ์ถ๊ฐ๋จ
})

// myBtn.classList.remove(โblueโ);   ํด๋์ค๋ฅผ ์ ๊ฑฐ
// myBtn.classList.toggle(โblueโ);   ํด๋์ค๋ฅผ ํ ๊ธ์ ์์ผ๋ฉด ์์ฑ์ ๋ฃ์ด์ฃผ๊ณ , ์์ผ๋ฉด ์ ๊ฑฐ
// myBtn.classList.contains(โblueโ); ํด๋นํ๋ ํด๋์ค๊ฐ ์๋์ง ํ์ธ, T/F ๋ฐํ
```
**3. ์์ ์ ์ด : DOM api๋ฅผ ์ด์ฉํ๋ฉด ์์๋ฅผ ์๋กญ๊ฒ ์์ฑํ๊ณ , ์์นํ๊ณ , ์ ๊ฑฐ ๊ฐ๋ฅ**
```
document.createElement(target); target ์์๋ฅผ ์์ฑ
document.createTextNode(target); target ํ์คํธ๋ฅผ ์์ฑ

element.appendChild(target); // target ์์๋ฅผ element์ ์์์ผ๋ก ์์น (ํญ์ ๋ถ๋ชจ์ ๋ง์ง๋ง ์์์ผ๋ก ๋ฐฐ์น๋จ)
element.removeChild(target); // element์ target ์์ ์์๋ฅผ ์ ๊ฑฐ(๋ถ๋ชจ๊ฐ ์์ด์ผํจ)

parentElement.insertBefore(target, location); 
// target์์๋ฅผ ๋ถ๋ชจ ์์(parentElement)์ ์์์ธ location ์์น ์์ผ๋ก ์ด๋ํจ
```
**4. JavaScript ๋ฌธ์์ด์ ์ฌ์ฉํด element, text ๋ธ๋๋ฅผ ์์ฑํ๊ฑฐ๋ ์ถ๊ฐํ๊ธฐ**
> DOM api๋ฅผ ์ด์ฉํ๋ฉด ์์ ์์ ๊ฐ์ ์ ๊ทผํ์ฌ ๊ฐ์ ๊ฐ์ ธ์ค๊ฑฐ๋, ๋ณ๊ฒฝํ  ์ ์์
```
<p></p>
<input type="text">
<button>Write Something!</button>
```
```
const myBtn = document.querySelector("button");
const myP = document.querySelector("p");
const myInput = document.querySelector("input");

myBtn.addEventListener('click', function(){
  myP.textContent = myInput.value; 
});

// textContent๋ <p> ์์ ์๋ ํ์คํธ ๋ธ๋๋ฅผ ์๋ฏธ
// ํน์  ๊ฐ์ ๋ฃ์ผ๋ฉด <p> ์์ ์๋ ํ์คํธ ๋ธ๋ ๊ฐ์ ๋ณ๊ฒฝํ  ์ ์์

-- ์ ์๋ ์ฝ๋๋ ์ด๋ฒคํธ ํ์์ ์ฐจ์ด ('click'/'input')--

// input ์์์ 'input' ์ด๋ฒคํธ๋ฅผ ์ฐ๊ฒฐํ์ฌ ์ฌ์ฉ์ ์๋ ฅ์ ํตํด ์ค์๊ฐ์ผ๋ก ๊ฐ์ ๋ฐ์์ํฌ ์ ์์
// ์ด๋ฒคํธ๋ฅผ ์ฐ๊ฒฐํ  ๋์์ด input์ด์ด์ผ ์ฐ๊ฒฐ์ด ๊ฐ๋ฅ (๋ฒํผ X)

myInput.addEventListener('input', ()=>{
  myP.textContent = myInput.value;
});

myP.innerHTML = "<strong>I'm Strong!!</strong>"; // <p>์์ ์์ ์์๋ก <strong>์ด ๋ด์ฉ๊ณผ ํจ๊ป ์ถ๊ฐ๋จ

myP.outerHTML = "<div></div>";
```

##  ๐ง innerText ์ textContent์ ์ฐจ์ด

๏น ```innerText``` : ์์์ **๋ ๋๋ง๋** ํ์คํธ ์ฝํ์ธ ๋ฅผ ๋ํ๋ <br>
๏น ```textContent``` : ๋ธ๋์ **ํ์คํธ ์ฝํ์ธ ๋ง**์ ํํ
```
โข innerText๋ "์ฌ๋์ด ์ฝ์ ์ ์๋" ์์๋ง ์ฒ๋ฆฌ
โข ๋ฌธ์์ด ์์ ์ฒ๋ฆฌํด์ผํ  ์์ฑ๋ค์ ๋ชจ๋ ์ฒ๋ฆฌํด์ ๋ณด์ฌ์ค
โข ๋ฌธ์์ด๋ก html ๋ฌธ๋ฒ์ ์์ฑํด์ ๋ณด๋ด์ฃผ๋ฉด html ์ฝ๋๋ก ๋ง๋ค์ด์ ๋ณด์ฌ์ฃผ๋ ๊ฒ

โ ์๋ฅผ ๋ค์ด <style> ํ๊ทธ๊ฐ ์์ฑ๋์ด ์์ผ๋ฉด ์ฌ๋ผ์ ธ์ ๋ณด์ด๊ฒ ๋จ, ๊ฒฐ๊ณผ ์ถ๋ ฅ์ ํ๊ทธ๊ฐ ์ ์ฉ์ด ์๋จ 
โ ๋ฐ๋ฉด์ innerText๋ ํ๊ทธ๋ฅผ ๋ชจ๋ ์ธ์ํด์ ๋ฌธ์์ด์ ๋ณด์ฌ์ค
```
> **์๋ฐ์คํฌ๋ฆฝํธ๋ฅผ ์ข ๋ ๋น ๋ฅด๊ฒ ๋์ํ๊ฒ ํ๊ธฐ ์ํด, ์ต์ ํ์ ์์ด์๋ ! ์์ ์์ ์๋ ํ์คํธ๋ฅผ ์ฒ๋ฆฌํ  ๋ ```textContent``` ์์ฑ์ ์ฌ์ฉํ๋ ๊ฒ์ด ์ข๋ค.**


