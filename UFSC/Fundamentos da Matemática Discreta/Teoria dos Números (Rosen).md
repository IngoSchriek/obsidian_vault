##### Divisão
Definição 1:
- Se a e b são inteiros com a diferente de 0, dizemos que a divide b se existe um inteiro c tal que b = ac, ou de maneira equivalente, b/a é um inteiro.
- Quando a divide b, dizemos que a é fator ou divisor de b, e b é múltiplo de a.

Exemplos:
- Quantos inteiros positivos até 50 são divisíveis por 3? R: 16
- Quantos inteiros positivos até 20 são divisíveis por 7? R: 2
![[Pasted image 20231001153038.png]]

Teorema 1:
- Se a, b e c são inteiros, em que a é diferente de 0. Então:
1) se a|b e a|c, então a|(b+c)
2) se a|b, então a|bc, para todos inteiros c
3) se a|b e b|c, então a|c

- Corolário 1:
	- Se a|b e a|c, então a|(mb+nc) (a combinação linear de b e c)

##### Algorítmo da Divisão:
Teorema 2:
- Seja a um inteiro e d um inteiro positivo. Então existem os inteiros únicos q e r, em que 0 <= r < d, de tal modo que a = d.q + r
![[Pasted image 20231001153945.png]]

Definição 2:
- Na expressão dada, o algorítmo da divisão, a é chamado de dividendo, d de divisor, q de quociente e r de resto.
- r = a mod d = a - d.q
- q = a div d = floor(a/d)
![[Pasted image 20231001154428.png]]

##### Aritmética Modular:
Definição 3:
- Se a e b são inteiros e m um inteiro positivo, então dizemos que a é congruente a b módulo m, se m divide a-b.
- Usamos a notação a ≡ b (mod m), que é uma congruência e que m é seu módulo.

Teorema 3:
- Seja a e b inteiros e m um inteiro positivo, então a ≡ b (mod m) é equivalente a a mod m = b mod m.

Teorema 4:
- Seja m um inteiro positivo. Os inteiros a e b são congruentes se e somente se houver um inteiro k tal que a = b + mk
- Exemplo:
	- x ≡ 2 (mod 3)
	- logo x = 2 + 3k
Prova do teorema:

![[Pasted image 20231001160054.png]]
Teorema 5: 
- Seja m um inteiro positivo. Se a ≡ b (mod m) e c ≡ d (mod m), então:
	- a + c ≡ b + d (mod m)
	- ac ≡ bd (mod m)
Prova do teorema (soma) (a multiplicação é feita de maneira semelhante):
![[Pasted image 20231001160458.png]]


Colorário 2:
- Seja m um inteiro positivo e seja a e b inteiros. Então:
	- (a + b) mod m = ((a mod m) + (b mod m)) mod m
	- ab mod m = ((a mod m)(b mod m)) mod m.

EXERCÍCIOS
- página 244, respostas 973
	 - 13 e 14 (a ao f) (fáceis) (equações de congruência)
	 - 15 e 16 (prova de teorema) (fácil)
	 - 17 (prova) (não consegui) (função floor e função ceiling)
	 - 19 (encontrar fórmula) (congruência)
	 - 21 ao 33 (fácil) (congruência) (praticar)
	 - 34 ao 44 (provas de congruência) (faceis, medias e talvez difíceis)

##### Primos, mdc, algorítmo de euclides...
- Algorítmo de Euclides ( mdc(a,b) = mdc(b, a mod b) )
- Teorema de Bezout ( mdc(a,b) = ax + by )

Teorema 7:
- Seja m um inteiro positivo e a, b e c inteiros. Se ac ≡ bc (mod m) e mdc(c,m)=1, então a ≡ b (mod m)

EXERCÍCIOS
- página 273, respostas 975
	- 1 ao 40 (exercícios de mdc)
	- 41 ao 44 (exercícios de algoritmo de euclides extendido) (fáceis)

#### Resolvendo congruências:
Congruências lineares:
- ax ≡ b (mod m)
- Para resolver, precisamos encontrar o inverso de a, ou seja a', tal que a.a' = 1 (mod m).

Teorema 1:
- Se a e m são primos entre si e m >1, então o inverso de a modulo m existe.
- Além disso, esse inverso módulo m é único. (menor que m)

Como encontrar o inverso de a modulo m?
1) Verificar se a é coprimo de m, ou seja, mdc(a, m) = 1
2) Através do teorema de Bezout, expor o mdc(a, m) como uma combinação linear de a e m.
3) Pegar o número que multiplica a. Entenda:
	- mdc(a, m) = 1, pode ser escrito como:
	- 1 = ax + my
	- Colocando sob modulo m, temos que:
	- 1 ≡ ax + my (mod m)
	- 1 mod m = (ax mod m + my mod m) mod m
	- Já que my é um múltiplo de m, o resto é 0. Portanto:
	- 1 ≡ ax (mod m)
	- e portanto x é o inverso de a modulo m.
Exemplo 1:
![[Pasted image 20231001174905.png]]

Exemplo 2:
![[Pasted image 20231001180255.png]]


EXERCICIOS:
- Refazer prova ex 41 seção 4.2 rosen7
- Refazer ex 6 seção 4.3 rosen7
- 
##### Teorema Chinês do Resto:
- Revisar

##### Teorema de Fermat:
- Revisar

![[Pasted image 20231012191803.png]]