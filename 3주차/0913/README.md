#  ๐ CSS declarations ๐

<!-- ์ ๋์ ์ธ ๊ฒ์ ์๋๊ณ  ์ฃผ๋ก -->

### h1๊ณผ p ์ ๊ธฐ๋ณธ๋จ์

```h1์ ๊ธฐ๋ณธpx : 32px;``` <br>
```p์ ๊ธฐ๋ณธpx : 16px;```


- ๊ณ ์  ๋จ์๋ก ์ฃผ๋ฉด ์ข์ ๊ฒ : ํจ๋ฉ, ๋ง์ง, ๋ชจ๋ํฐ ํฌ๊ธฐ์ ๋ฐ๋ผ ์๊ด์์ด ๋ณด์ผ ๊ฒ๋ค,์ด๋ฏธ์ง, ๋ฐ์ํ ๊ณ ๋ คํ์ง ์์๋ ๋  ๋, ๊ธ์จ์ ๊ด๋ จ ์๋ ๊ฒ๋ค, ๊ณ์ฐํ๊ธฐ ์ฌ์์ผ ํ๋ ๊ฒ๋ค <br>
- ๊ฐ๋ณ ๋จ์๋ก ์ฃผ๋ฉด ์ข์ ๊ฒ : ํจ๋ฉ,๋ง์ง,์ด๋ฏธ์ง, ํฐํธ

### 1. ๊ณ ์  ๋จ์๋? 

์ฌ์ฉ์๊ฐ ์ ์ธํ ๊ณ ์ ๋ ํฌ๊ธฐ ๊ทธ๋๋ก๋ฅผ ํ๋ฉด์ ๊ทธ๋ฆฌ๊ธฐ ๋๋ฌธ์ ์ง๊ด์ ์ผ๋ก ์ฌ์ฉ ๊ฐ๋ฅ <br>
ex) cm, mm, px ๋ฑ์ด ์์ง๋ง cm,mm์ ๊ฑฐ์ ์ฐ์ง ์์

### 2. ์๋ ๋จ์๋?

๋ฐฐ์ ๋จ์, ๋ถ๋ชจ ์์์ ๊ธ์ํฌ๊ธฐ ๋ฑ ํน์ ํ ๋์์ ๊ธฐ์ค์ผ์ ์๋์ ์ผ๋ก font-size๊ฐ ๊ฒฐ์  ๋จ <br>
ex) em, %, rem, vw, vh ๋ฑ

### em 

em์ ์๋ ๊ธธ์ด ๋จ์๋ก ๋ฐฐ์๋ฅผ ๋ํ๋ด๋ ๋จ์์ด๋ฉฐ, ๋ถ๋ชจ์ font-size์ ๋ฐ๋ผ ๊ธฐ์ค์ ์ ์ธ์ฐ๊ณ  ๊ธฐ์ค์ ์ ๋ฐ๋ผ ํฌ๊ธฐ๊ฐ ๋ฌ๋ผ์ง <br>
ex) ๋ฒํผ(large, medium, small) ๋ฑ์ ํ์คํธ์ ๋น์จ์ ๋ฐ๋ผ ๋ฌ๋ผ์ ธ์ผ ํ  ๊ฒฝ์ฐ์ ์ฐ์
    
### rem 

rem์ html์ ํฐํธ์ฌ์ด์ฆ๋ฅผ ๊ธฐ์ค์ผ๋ก ์ ํด์ง, ๊ธฐ๋ณธ์ ์ผ๋ก em๋ณด๋ค ๋ง์ด ์ฐ์


## overflow ์์ฑ

์์์ ์ฝํ์ธ ๊ฐ ๋๋ฌด ์ปค๋ค๋ ๊ฒฝ์ฐ ์์๋ฅผ ์ด๋ป๊ฒ ์ฒ๋ฆฌํ ์ง ์ง์ 

- visible : overflow ์์ฑ์ ๊ธฐ๋ณธ ๊ฐ, ์ฝํ์ธ ๋ฅผ ์๋ฅด์ง ์์ (x์ถ์ด๋ y์ถ ๊ฐ์ ๋ฐ๋ผ ํ์ชฝ๋ง ์คํฌ๋กค ๋ฐ ์์ฑ)
- hidden : ์ฝํ์ธ ๋ฅผ ์์์ ํฌ๊ธฐ๋งํผ ๋ง์ถ๊ธฐ ์ํด ์๋ผ๋
- scroll : ์ฝํ์ธ ๋ฅผ ์์์ ํฌ๊ธฐ๋งํผ ๋ง์ถ๊ธฐ ์ํด ์๋ผ๋, ์๋ ค์ง ๋๋จธ์ง ๋ถ๋ถ์ ํ์ธ ํ  ์ ์๋๋ก ์คํฌ๋กค ๋ฐ(x์ถ, y์ถ ๋ชจ๋) ์ ๊ณต


## background-image

1) background-image : url์ ์ด์ฉํด ์ด๋ฏธ์ง์ ์ฃผ์์์ ์ด๋ฏธ์ง๋ฅผ ๋ถ๋ฌ์ด
2) background-color : ์์์ ๋ฐฐ๊ฒฝ ์ ์ง์ 
3) background-repeat : ๋ฐฐ๊ฒฝ์ด๋ฏธ์ง๋ฅผ ์ด๋ป๊ฒ ๋ฐ๋ณตํ ๊ฒ์ธ์ง ์ง์ 
    - repeat ๊ธฐ๋ณธ๊ฐ
    - no-repeat
    - repeat-x
    - repeat-y
    - round
    - space
4) background-position : ๋ฐฐ๊ฒฝ์ด๋ฏธ์ง์ ์์น๋ฅผ ์ง์ 
5) background-size


## font

text-transform : ํ์คํธ๋ฅผ ๋๋ฌธ์๋ ์๋ฌธ์๋ก ํํ
font-style : ๊ธฐ์ธ๊ธฐ ๊ธ๊ผด๋ก ํํ (normal ์ผ๋ฐ ์คํ์ผ, italic ํ๊ธฐ์ฒด, oblique ๊ธฐ์ธ์์ฒด)
text-align : ํ์คํธ์ ์ ๋ ฌ์ ํํ (justify๋ ๋ง์ง๋ง ์ค์ ์ ์ธํ๊ณ  ์์ชฝ์ผ๋ก ์ ๋ ฌ)
text-decoration : ํ์คํธ์ ์ฅ์์ ์ค์  (none์ ํจ๊ณผ์ ๊ฑฐ, underline์ ๋ฐ์ค)


## opacity

- ์์์ ํฌ๋ช๋๋ฅผ ์ง์ 
- ์ด๋ ํฌ๋ช๋๊ฐ ๋ค์ด๊ฐ ์์ ์์ ๋ด์ฉ๋ฌผ๋ ํจ๊ป ํฌ๋ช ํด์ง
- ๊ฐ์ 0.0 ๊ณผ 1 ์ฌ์ด์ ์ซ์๋ฅผ ์ง์ ํ  ์ ์์ผ๋ฉฐ ๋ง์ฝ ๊ฐ์ด 0.5๋ผ๋ฉด ํฌ๋ช๋๋ 50%

## text

![image](https://user-images.githubusercontent.com/112460430/189912069-ceb86ab8-ed6e-4eab-a8ea-e5a2a1e9fd74.png)


