Aplicações:
- Criptografia (devido a dificultade de fatorar dois primos muito grandes)

Observações importantes:
-  Inteiro divisível por outro (noção central na TI)
- d|a se e somente se -d|a
- os divisores triviais de a são 1 e a
- divisores não-triviais = fatores
- d|a, se a = kd
- todo inteiro divide 0
- se a > 0 e d|a, então |d| <= |a|
- se d|a, a é um múltiplo de d e d é um divisor de a
- o 1 é chamado de unidade, pois não é nem primo e nem composto
## Primos:
- inteiro maior que 1 cujo únicos divisores são os triviais
- são os blocos de construção dos números
# Teorema 1: Existem infinitos números primos

## Teorema da Divisão:
![[Pasted image 20230924155422.png]]
Dado um inteiro n, o conjunto dos números inteiros (Z) pode ser particionado em:
- múltiplos de n
- não-múltiplos de n
Obs.: Boa parte da teoria dos números é baseada em um refinamento desta partição
- classificar os não-multiplos de n de acordo com seus restos quando dividos por n

# Teorema 2:
### Para todo inteiro a e todo inteiro positivo n, existem inteiros únicos q e r tais que:
## 0 <= r < n             e             a = qn + r

_a: dividendo
q: quociente
n: divisor
r: resto_

_q = floor(a/n)
r = a mod n_
_a mod n = a - floor(a/n).n_
###### obs. 1: n|a se e somente se a mod n = 0
###### obs. 2: o resto sempre é um número não negativo! 

###### exemplos:
-37/5
-37 = 5.(-7) + (-2) (resto negativo!!!! incorreto!)
-37 = 5.(-8) + 3 (correto!)

-11/4
-11 = 4.(-2) + (-2) (incorreto!)
-11 = 4.(-3) + 1 (correto!!)

###### é possível verificar que,
11/4
11 = 4.2 + 3
-11 mod 4 é diferente de 11 mod 4

###### observe que,
1/4
1 = 4.0 + 1
-3/4
-3 = 4.(-1) + 1
###### portanto 1 é congruente a -3 (mod 4), pois diferem um múltiplo de 4 entre si (4.1) logo -7, -11 e 5, também são congruentes a 1 e -3
-7 = 4.(-2) + 1
-11 = 4.(-3) + 1
5 = 4.1 + 1
(todos tem resto 1)

## Módulo Congruente:
a mod n = b mod n <---> n | a-b <---> a é congruente a b (mod n)
## Divisores comuns:
Se d é um divisor de a e de b, então d é um divisor comum de a e b.

Propriedades importantes:
- Se d|a e d|b, então d|(a+b)
- Se d|a e d|b, então d|(ax + by) (combinação linear
- Se a|b, então |a| <= |b| ou b = 0
- Se a|b e b|a, a = +-b

## Máximo Divisor Comum:
mdc(a,b): maior dos divisores comuns entre a e b

Propriedades importantes:
- Se a e b forem não-nulos, 1 <= mdc(a,b) <= min(a,b)
- mdc(a,b) = mdc(b,a)
- mdc(a,b) = mdc(-a,b)
- mdc(a,b) = mdc(|a|,|b|)
- mdc(a, 0) = |a|
- mdc(a, ak) = |a|

a pode ser escrito como produto de números primos elevados a potencias aj em que 0 <= j <= k
![[Pasted image 20230924164343.png]]

![[Pasted image 20230924165159.png]]

Ou seja, outras propriedades importantes:
- min(a,b) + max(a,b) = a + b
- mmc(a,b) . mdc(a,b) = a . b

# Teorema 3:
## Se a e b são inteiros quaisquer (não nulos), então:
## mdc(a,b) é o menor inteiro positivo do conjunto {ax + by: x,y E Z}

Em resumo:
Se mdc(a,b) = s, s = ax + by (para alguns inteiros x e y)

##### Corolário 1:
- Se d|a e d|b, então d|mdc(a,b)

##### Corolário 2:
- mdc(n.a, n.b) = n.mdc(a, b)

##### Corolário 3:
- Se n|a.b e mdc(a,n) = 1, então n|b

# Primos entre si (coprimos):
2 inteiros a e b são primos entre si, se o único divisor comum é 1, ou seja, mdc(a,b
) = 1

# Teorema 4:
Para todo inteiro a, b e p:
- Se mdc(a,p) = 1 e mdc(b,p) = 1,
- então mdc(ab,p) = 1

# Teorema 5:
Se p|ab, então p|a ou p|b (ou ambos)

# Teorema 6:
Todo número inteiro pode ser fatorado de maneira única em primos.

# Quantidade de divisores:
![[Pasted image 20230924180248.png]]

# Algorítmo de Euclides:
## Sejam a, b E Z+, e c = a mod b, então o mdc(a,b) = mdc(b,c) e mdc(n,0)=n
Ou seja mdc(a,b)=mdc(b,a mod b)
# Complexidade, tempo (checar em vídeo)
t >= log b (base 2)

# Aritmética Modular:
Zn = {0, 1, 2, ..., n-1} (todos restos possíveis da divisão por n)
onde n E Z+
Universo dos inteiros mod n.

##### Operações:
- As mesmas propriedades que valem para o conjunto dos inteiros, vale também para o conjunto dos inteiros mod n (Zn). Ex.: Comutatividade, associatividade, distributividade, etc...
![[Pasted image 20230926201121.png]]
- Adição mod n
- Subtração mod n
- Multiplicação mod n
- Divisão mod n

1) ADIÇÃO MODULAR:
   ![[Pasted image 20230926201425.png]]
2) MULTIPLICAÇÃO MODULAR:
   ![[Pasted image 20230926201441.png]]
3) SUBTRAÇÃO MODULAR:
   ![[Pasted image 20230926201653.png]]
4) DIVISÃO MODULAR:
   Primeiro passo:
   - Dá para dividir? B e N são relativamente primos?
     Segundo passo:
     - Encontrar o inverso multiplicativo de B e multiplicar por A (mod n) 
   ![[Pasted image 20230926201958.png]]
#### OBS.: UM NÚMERO B SÓ É INVERSÍVEL SE FOR COPRIMO DE N

# Inverso Aditivio x Inverso Multiplicativo
Inverso Aditivo:
- No conjunto dos números inteiros, nós temos que o inverso aditivo do número A é igual a -A, ou seja, A + (-A) = 0, portanto, o inverso aditivo é número que somado a este resulta em 0.
- No conjunto dos números inteiros mod n, temos de maneira semelhante que o inverso aditivo é o número que somado a este resulta em 0.
- Exemplo: 
![[Pasted image 20230926204602.png]]

Inverso Multiplicativo:
- únicos elementos inversíveis em Zn são aqueles coprimos de n
- para encontrar o inverso de a no universo de discurso dos inteiros mod n, considerando a coprimo de n, precisamos encontrar b que é um número que, (a x b) mod n = 1 ou a x b congruente a 1, mod n.
Qual é o inverso multiplicativo de 7, quando n = 3?
![[Pasted image 20230926213624.png]]
Qual é o inverso multiplicativo de 7, quando n = 10?
![[Pasted image 20230926213923.png]]
Qual é o inverso multiplicativo de a no universo n?
https://www.youtube.com/watch?v=hvSCBruPrIo&ab_channel=DhiegoLoioladearaujo
- _a mod n = a - q.n_
- ou seja, ab mod n = ab - q.n
- de 0 a n-1 (sem a restrição, no exemplo anterior o inverso de 7 também poderia ser 13)
![[Pasted image 20230926214749.png]]

# Sistema de equações de congruências:

Teorema 3: 



![[Pasted image 20230926220039.png]]
- Revisar