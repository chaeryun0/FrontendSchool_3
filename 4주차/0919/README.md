# ๐ Grid

> **๋ถ๋ชจ ์ปจํ์ด๋ ์์์์์ ๋ด๋ถ ์์ ์์๋ค์ ์์น๋ฅผ X์ถ๊ณผ Y์ถ ๋ฐฉํฅ ๋ชจ๋๋ฅผ ์ด์ฉํด ๋ฐฐ์นํ๋ ๋ด๋ถ๋์คํ๋ ์ดํ์์ ํ๋**

<image src="https://user-images.githubusercontent.com/112460430/192091653-49fd1155-3bcc-4292-8b70-3a7563f03a23.png" width="50%">

## ๐ง Flex์ Grid์ ์ฐจ์ด์ 
 
> Flex : ํ ๋ฐฉํฅ ๋ ์ด์์ ์์คํ (1์ฐจ์) <br>
> Grid : ๋ ๋ฐฉํฅ(๊ฐ๋ก-์ธ๋ก) ๋ ์ด์์ ์์คํ (2์ฐจ์) 
  <br>
  
## ๐ grid-container์ ์ฌ์ฉํ๋ ์์ฑ
  
```
grid-template-columns: 1fr 1fr 1fr;         /* ์ด๋ฐฉํฅ ๊ทธ๋ฆฌ๋ ํธ๋ ์ฌ์ด์ฆ ์ค์  */
grid-template-rows: repeat(3, 1fr);         /* ํ๋ฐฉํฅ ๊ทธ๋ฆฌ๋ ํธ๋ ์ฌ์ด์ฆ ์ค์  */
grid-template-columns: repeat(2, 1fr 30px); /* repeat(๋ฐ๋ณตํ์, ๋ฐ๋ณต๊ฐ) ํจ์ */

grid-template-rows: repeat(3, minmax(120px, auto));
/* ํ๋ฐฉํฅ ๊ทธ๋ฆฌ๋ ํธ๋์ ์ต์ ๋์ด๋ฅผ 120px, ์ต๋ ๋์ด๋ฅผ ๊ฐ์ฉํ  ์ ์๋ ์ต๋ ํฌ๊ธฐ ์๋์ผ๋ก */

grid-template-columns: repeat(auto-fill, minmax(50px, auto));
/* grid-template-columns: repeat(auto-fit, minmax(50px, auto)); */

gap : 10px 30px; /* (row, column), flex์์๋ ์ฌ์ฉ๊ฐ๋ฅ, ์ต์คํ๋ก๋ฌ ๋ฏธ์ง์ */
```  
  
## ๐ grid-item์ ์ฌ์ฉํ๋ ์์ฑ

> **๊ทธ๋ฆฌ๋ ์ปจํ์ด๋ ์์์ ๊ทธ๋ฆฌ๋ ์์ดํ์ด ์ฐจ์งํ๋ ์์ญ์ ๋ฒ์์ ์์น๋ฅผ ์ค์ ํ๋ ์์ฑ**

- ๋ฒ์์ ์์๊ณผ ๋ ์ค์  ๊ฐ๋ฅ
- ์ปฌ๋ผ๊ณผ ๋ก์ฐ ๋ฐฉํฅ์ ๋ํ ์ถ์ฝ ์์ฑ ์ง์
- ๋ฒ์์ ๊ธฐ์ค์ด ๋๋ ๊ฐ์ grid-line์ ๋ฒํธ

```
- grid-column : 1 / 3;
- grid-row : 1 / 3;
- grid-area : 1/1/3/3; 
- grid-area: 1 / 1 / span 2 / span 2;  -> row๋ฐฉํฅ 2์นธ / column๋ฐฉํฅ 2์นธ ์ฐจ์ง 
  
- grid-area์ ์ค์  ๊ฐ์ ์์๋๋ก ๊ฐ๊ฐ 
  grid-row-start, grid-column-start, grid-row-end, grid-column-end๋ฅผ ์๋ฏธ

- span ํค์๋๋ฅผ ์ฌ์ฉํ๋ฉด ๊ทธ๋ฆฌ๋ ๋ผ์ธ์ ๋ฒํธ๋ฅผ ์ฌ์ฉํ์ง ์์๋ ๋จ
```
### โ grid-template-areas ์์ฑ
```
.container {
  display: grid;
  grid-template-rows: repeat(4, 100px);
  grid-template-columns: repeat(3, 1fr);
  grid-template-areas:
    "header header header"
    "main . ."
    "main . aside"
    "footer footer footer";
}
header { grid-area: header; }
main   { grid-area: main;   }
aside  { grid-area: aside;  }
footer { grid-area: footer; } 
```
### โ ๊ทธ๋ฆฌ๋ ์์ดํ์ Z์ถ ์ค์ 
```
aside{
  grid-area:aside;
  background-color: lightgreen;
  transition:0.3s; /* ์์์ ๋ณํ๊ฐ ์์ ๋ ์ ์ง์ ์ผ๋ก ํํํด์ค */
  transform-origin:0 0; /* ์ด๋ค ์ขํ๋ฅผ ๊ธฐ์ค์ผ๋ก ์์์ ์์น๋ฅผ ๋ณ๊ฒฝํ ์ง */
}

/* aside ์ ๋ง์ฐ์ค๋ฅผ ํธ๋ฒํ๋ฉด 10% ํฌ๊ธฐ๋ฅผ ํค์*/
aside:hover{
  transform:scale(1.1);
}

footer{
	/* aside ์ ํฌ๊ธฐ๊ฐ ์ปค์ ธ๋ footer๋ฅผ ๊ฐ๋ฆฌ์ง ์๊ฒํจ, footer ๋ณด์ด๋๋ก */
  z-index:1;
  grid-area:footer;
  background-color: aquamarine;
}
