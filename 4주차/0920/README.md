## π  perspective (μκ·Όλ²)

- ```perspective```λ μμΉ μμμ μκ·Όκ°μ μ£ΌκΈ° μν΄ νλ©΄κ³Ό μ¬μ©μ μ¬μ΄μ κ±°λ¦¬λ₯Ό κ²°μ 
- λΆλͺ¨ μμμκ² μ£Όλ©΄ μ§κ³ μμλ€μκ² μ μ©λλ€.
- κΈ°λ³Έμ μΌλ‘ μμ€μ μ΄ μ‘΄μ¬νλ©° μμ€μ μ μ μ€μμ μμΉ

<image src="https://user-images.githubusercontent.com/112460430/191278627-eed17e53-41ab-4176-9c8f-0d70da234c38.png" width="50%">

> μΊλ¦­ν°μ λ¬Όμ²΄κ° 400px κ±°λ¦¬μ μκ³  yμΆμΌλ‘ νμ νλ€. <br>
> xμΆμ λ¬Όμ²΄λ₯Ό κ°λ‘λ‘ κ΄ν΅ μν¨λ€μ νμ , yμΆμ λ¬Όμ²΄λ₯Ό μΈλ‘λ‘ κ΄ν΅ μν¨λ€μ νμ , z μΆμ λ¬Όμ²΄ μμͺ½μμ λ°μΌλ‘ κ΄ν΅ μν¨λ€μ νμ 
<br>

```
.container {
  perspective-origin: 30% 30%   // μμ μ μμΉ : Xμ’ν 30%, Y μ’ν 30% 
  perspective:400px;           //  λμ μμμ κ±°λ¦¬λ zμΆ κΈ°μ€ 400pxλ§νΌ λ¨μ΄μ Έ μμ, κ°μ΄ μ μμλ‘ λ κ°κΉμ΄ νλλμ΄ λ³΄μ
}

π‘ perspective-origin : 3D μμλ₯Ό μ΄λμ λ°λΌλ³Όμ§ λ°©ν₯ μ§μ , μκ·Ό κ±°λ¦¬μ κΈ°μ€μ  μ€μ , λμ μμΉλ₯Ό λ°κΏ μ μμΌλ©° μ΄μ λ°λΌ μμ€μ μ μμΉλ λ°λ 
```

	
```

- transform: rotateY(180deg);  // μμλ₯Ό λ€μ§μ
	
- backface-visibility: visible; // κΈ°λ³Έκ° : λ·λ©΄μ΄ λλ₯Ό ν₯ν λ λ³΄μ
- backface-visibility: hidden;

	
π‘ backface-visibility μμ±μ μμμ λ·μͺ½μμ μλ©΄μ΄ λ³΄μ΄κ² ν μ§ μ νλ μμ± 
```

	
```
transform-style : preserve-3d;

- flat : κΈ°λ³Έκ°, νννκ² λ³΄μ (2Dμ 2μ°¨μμμ λΆλͺ¨ μμμ λμΌν νλ©΄μ λ°°μΉ)

π‘ μμμμλ€μ 3D κ³΅κ°μμ λ¬μ¬νκΈ° μν΄ λΆλͺ¨ μμμ μ μ©μν€λ μμ±, μμμμλ₯Ό 3d κ³΅κ°μ²λΌ μ²λ¦¬
```
