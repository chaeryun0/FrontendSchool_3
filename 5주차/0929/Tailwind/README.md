# ๐ Tailwind CSS

> **CSS๋ฅผ ์ฌ์ฉํ์ง ์๊ณ  HTML ๋ฌธ์ ๋ด์์ ๋น ๋ฅด๊ฒ ์น์ ๊ตฌ์ถํ๊ฒ ํด์ฃผ๋ ํ๋ ์ ์ํฌ** <br>
> ๋ถํธ์คํธ๋ฉ ์ฒ๋ผ m-2, flex์ ๊ฐ์ด ๋ฏธ๋ฆฌ ์ธํ๋ ํด๋์ค๋ฅผ ํ์ฉํ๋ ๋ฐฉ์์ผ๋ก HTML ์ฝ๋ ๋ด์์ ์คํ์ผ๋ง์ ํ  ์ ์์ <br>
> ๋น ๋ฅด๊ณ  ํธ๋ฆฌํ ์คํ์ผ๋ง๊ณผ ์ปค์คํ์ด ๊ฐ๋ฅํ ์ฅ์ ์ด ์๋ ๋ฐ๋ฉด ๋ถํธ์คํธ๋ฉ ์ฒ๋ผ ํด๋์ค๋ช์ด ๊ธธ์ด์ง๋ ๋จ์ ์ด ์์ <br>

```
 <!-- cdn script๋ฅผ HTML ๋ฌธ์ ๋ด์ ๋ถ์ฌ ๋ฃ์ด์ ์ฌ์ฉ -->
<script src="https://cdn.tailwindcss.com"></script>
```
```
<div class="space-y-8">    // space-y-8: ์์์์๋ค์ Y์ถ์ผ๋ก 8*0.25em ์ฉ ๊ฐ๊ฒฉ์ ์ค์ 
  <div class="w-96 h-10"> // w-96 : ๋๋น 96*0.25em, h-10 : ๋์ด 10*0.25em ๋งํผ ์ค์ 
    content
  </div>
</div>
```
```
<div class="flex border-4 border-red-300 m-3">               // flex: display flex๋ก ์ง์ , m-3 : ๋ง์ง ์ํ์ข์ฐ 3*0.25em
  <div class="p-2 border-4 border-blue-500">1 hello</div>   // p-2 : padding 2*0.25em ์ง์ 
  <div class="p-2 border-4 border-blue-500">1 hello</div>  // border-4 : 4px๋งํผ ํ๋๋ฆฌ ๊ตต๊ธฐ ์ง์ 
  <div class="p-2 border-4 border-blue-500">1 hello</div> // border-blue:ํ๋๋ฆฌ์ ์ง์ 
  <div class="p-2 border-4 border-blue-500">1 hello</div>
</div>
```
```
class="flex-col"           // flex-direction์ column ๋ฐฉํฅ์ผ๋ก ์ง์ 
class="flex-wrap"         //  flex item ๋ค์ด container์ ๋์ด๋ฅผ ์ด๊ณผํ  ์ ์ค๋ฐ๊ฟ
class="gap-์ซ์"          // ์์์์์ gap๋ถ์ฌ ๋จ์๋ 0.25em
class="w-3/4"           // ํ์ฌ ์์ดํ ์์์ ๋์ด๋ฅผ ๋ถ๋ชจ์์์ 3/4๋ก ์ง์ 
class="justify-center" // justify-content: center ๋ฅผ ์ถ์ฝํด์ ์ ์ฉ
class="items-center"  // items-items : center ๋ฅผ ์ถ์ฝํด์ ์ ์ฉ

์ฃผ์ด์ง ๊ฐ ์ด์ธ์ ์ฌ์ฉํ๊ณ ์ถ์ผ๋ฉด arbitrary value[] ์ฌ์ฉ (๋จ์๋ ๊ฐ์ด) 

class="md:" // ํด์๋์ ๋ฐ๋ผ sm: ,md: ,lg: ,xl: ,2xl: ์ต์ 
<img class="w-16 md:w-32 lg:w-48" src="..."> // 768px ๋ณด๋ค ์์ผ๋ฉด w-32 ์ ์ฉ
```


## ๐ Bootstrap vs Tailwind

> **๋ ๋ค CSS ์์ด HTML ๋ฌธ์๋ด์์ ๊ฐํธํ๊ฒ ์คํ์ผ์ ์ค์ ์๋ ํ๋ ์์ํฌ**

- Tailwind์ ์ฅ์ ์ ์ ์ฐ์ฑ์ด๋ฉฐ, HTML ๋ฌธ์์ ํด๋์ค๋ฅผ ์ ์ํ๋ ๊ฒ์ผ๋ก ๋์์ธ์ ๊ตฌ์ฑํ  ์ ์์ด ์ปค์คํ์ด ์์ ๋ก์
- Bootstrap ์ ๋ฏธ๋ฆฌ ์ ํด์ง ๋์์ธ์ component๋ค์ด ์๊ณ , ๊ทธ ์ปดํฌ๋ํธ๋ค์ ๊ฐ์ ธ๋ค ์ฌ์ฉํ๋ ๋ฐฉ์์ผ๋ก ์ ํด์ง ๊ตฌ์ฑ์์์ ๊ตฌ์๋์ด ์์
