#### Tangentes, velocidades e outras taxas de variação:
Sinonimos para a equação:
![[Pasted image 20230928164334.png]]
- Inclinação da curva no ponto
- Inclinação da reta tangente
- Taxa
- Taxa média de variação de y em relação a x
- Taxa (instantânea) de variação de y em relação a x
- Inclinação
- Coeficiente angular
- etc
Outras alternativas:
![[Pasted image 20230928165052.png]]
![[Pasted image 20230928164737.png]]
## Derivadas:
![[Pasted image 20230928164932.png]]
##### Interpretação da Derivada Como a Inclinação da Reta Tangente:
- A reta tangente a y = f(x) em (a, f(a)) é a reta que passa em (a, f(a)), cuja inclinação é igual a f'(a), a derivada de f em a.
![[Pasted image 20230928165434.png]]
- Exemplo: Encontre uma equação da reta tangente à parábola y = x² - 8x + 9 no ponto (3,-6)
![[Pasted image 20230928173615.png]]
**PERCEBA:** 
- Em l(x) a derivada é igual a 0, pois a inclinação é igual a 0. L(x) é constante.
- Em g(x) a derivada é igual a 8, pois é evidente da equação ax + b, que 8 é a inclinação e a inclinação é constante.
- Em h(x) a derivada é igual a 2x, por conta da inclinação variar (calculando derivadas de funções da forma x^n, tem-se que a derivada é igual a nx^(n-1).

##### Interpretação da Derivada Como uma Taxa de Variação:
A derivada f'(a) é a taxa de variação instantânea de y = f(x) em relação a x quando x = a.

Exercícios para refazer:
- Seção 2.7 (equação da reta tangente) (pág 154):
	 - 8 e 9
- Seção 2.8 (Cálculo de derivadas s/ tabela) (pág 162):
	- 13 ao 18 (muita dificuldade tive)
##### A derivada como uma função:
Outras notações:
![[Pasted image 20230929200305.png]]
Exemplo de f(x) e f'(x):
f(x):
![[Pasted image 20230929200452.png]]
f'(x):
![[Pasted image 20230929200923.png]]
#### Deriviabilidade (diferenciabilidade) e Continuidade:
![[Pasted image 20231007150542.png]]
Definição 1: Uma função é **diferenciável** em a, se f'(a) existe.
Definição 1.1: Uma função é diferenciável em um **intervalo aberto** (a,b) se for diferenciável em cada ponto do intervalo. 

Diferenciável == Derivável

Exemplo de função diferenciável em todo o seu domínio: f(x) = x²
Exemplo de função não diferenciável em todo o domínio: f(x) = |x|

###### Teorema 1: Se f for diferenciável em a, então f é contínua em a.
###### Teorema 1.1 (Contrapositiva): Se f não é contínua em a, então f não é diferenciável em a.
OBS.: HÁ FUNÇÕES CONTÍNUAS EM a QUE NÃO SÃO DIFERENCIAVEIS EM a. Ex.: Função modular.

![[Pasted image 20230929202418.png]]
Zoom nos casos (a), (b), (c) e (d):
- Note a diferença.
	![[Pasted image 20230929202648.png]]

### FAZER EXERCICIOS DE REVISÃO PARA PROVA, página 174

# Regras de diferenciação (derivação):

##### Função constante: f(x) = k
- f'(x) = 0

##### Função potência: f(x) = x^n
- f'(x) = nx^(n-1)
- exemplo: f(x) = x
	- f'(x) = 1x^(1-1) = 1

OBS.: Fazer prova da Regra de potência, página 182.

##### Regra do Múltiplo Constante:
"A derivada de uma constante vezes uma função é a constante vezes a derivada da função."
![[Pasted image 20230930150602.png]]
Ou, pela notação linha: (c.f(x))' = c.f'(x)
OBS.: Fazer prova, partindo de g(x) = c.f(x)

##### Regra da Soma:
![[Pasted image 20230930151028.png]]
OBS.: Fazer prova, dica: semelhante ao anterior.

Regra da Soma + Regra do Multiplo Constante = Regra da Diferença
##### Regra da diferença: O mesmo da anterior, porém subtração.

##### Funções exponenciais:
Se a função exponencial f(x) = a^x for diferenciável em 0, então é diferenciável em toda parte e,
f'(x) = f'(0) . a^x
Essa equação diz que a taxa de variação de qualquer função exponencial é proporcional a sua função. (A inclinação é proporcional à altura)

![[Pasted image 20230930152151.png]]
OBS.: e é um número tal que a dada proporção seja igual a 1.


- Exercícios a refazer:
	- 48 (pg 190) http://www.soensino.com.br/foruns/viewtopic.php?f=6&t=71842
	- a fazer: 53, 55, 56, 60

#### Regra do produto: 
![[Pasted image 20231003063037.png]]
- Em outras palavras, a Regra do produto diz que __a derivada de um produto de duas funções é a primeira função vezes a derivada da segunda mais a segunda função vezes a derivada da primeira.__
- Verificar prova na página 190.

#### Regra do Quociente:
![[Pasted image 20231003063517.png]]
- Em outras palavras, __a derivada de um quociente é o denominador vezes a derivada do numerador menos o numerador vezes a derivada do denominador, todos divididos pelo quadrado do denominador.__
- Ver prova na página 193.

- EXERCÍCIOS:
	- ímpares até o 9 (fiz) página 195

#### Derivadas de Funções trigonométricas:
Derivadas:
![[Pasted image 20231003170821.png]]
EXERCÍCIOS:
- ímpares até o 21 página 213 (seção 3.4)
- Seção 3.5 (Regra da Cadeia) (opcional)
	- fiz até a 6
- Seção 3.6 (Trigonométricas Inversas) (fazer)
	- fiz os ímpares até 10
	- ler material
- Seção 3.8 (Derivadas de funções logarítmas)
	- ler material
	- fiz os ímpares até 20

OBS.: REVISAR MODULO (VALOR ABSOLUTO)