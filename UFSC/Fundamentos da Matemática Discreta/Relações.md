- Ligações entre elementos de conjuntos

Exemplos de aplicações:
- Pares de cidades ligadas por linhas aéreas em uma rede.
- Elaboração de um modo útil de armazenar informação em um banco de dados computacionais.

Tupla ordenada: lista de objetos em que a ordem importa.
![[Pasted image 20231007150048.png]]
## Domínio, Imagem e R-relativos:
##### Domínio de R
- denota-se Dom(R)
- o domínio do conjunto da relação R, é um subconjunto do conjunto de partida
- é igual aos elementos do conjunto de partida que estão relacionados com os do conjunto de chegada

##### Imagem de R
- denota-se Im(R)
- a imagem do conjunto da relação R, é um subconjunto do conjunto de chegada
- são todos elementos do conjunto de chegada, que tem algum elemento relacionado do conjunto de partida

##### R-relativos de x:
- denota-se R(x), para algum elemento x do conjunto de partida
- são todos elementos do conjunto de chegada que estão relacionados com x
- R(B), sendo B um subconjunto do conjunto de partida, é igual a todos elementos que tem relação com algum dos elementos do subconjunto B
Operações:
Teorema 1: Seja R uma relação de A em B e sejam A1 e A2 subconjuntos de A, então:
![[Pasted image 20231012153624.png]]
Teorema 2: Sejam R e S relações de A em B. Se R(a) = S(a) para todo a E A, então R = S

## Representação
##### Para representar relações entre conjuntos finitos, é possível:
- Matrizes de 0's e 1's
- Grafos direcionados (digrafos)

##### Matrizes de relações
Se A = {a1, a2, ..., an} e B {b1, b2, ..., bn} são conjuntos finitos e R é uma relação de A em B, então R pode ser representada pela matriz mxn Mr = |mi|, definida como mij que será 1 se (ai,bj) E R e
será 0, se (ai,bj) (não pertence) R
Mr é denominada de matriz de R.
Exemplo:
![[Pasted image 20231012155813.png]]

##### Manipulação de relações:
![[Pasted image 20231012160119.png]]
Como obter R complementado através da matriz de R?
- Basta trocar todos 0's por 1's e todos 1's por 0's
- Complementar cada mij
Como obter a inversa de R através da matriz de R?
- Basta fazer a transposta da matriz
	- Primeira coluna vira primeira linha, primeira linha vira primeira coluna
![[Pasted image 20231012160407.png]]

Teorema: Suponha que R e S são relações de A em B
1) Se R está contido em S, 
	1) então a inversa de R está contido na inversa de S
	2) então o complemento de S está contido no complemento de R
2) a inversa da intersecção entre R e S é igual a inversa de R intersecção com a inversa de S
3) a inversa da união entre R e S é igual a inversa de R união com a inversa de S
4) o complemento da intersecção entre R e S é igual ao complemento de R união com o complemento de S
5) o complemento da união entre R e S é igual ao complemento de R união com o complemento de S

Obs.: Lembre-se, relações não deixam de ser conjuntos, portanto todas propriedades de conjuntos também valem para relações

##### Composição de Relações:
- Sejam A, B e C conjuntos, R uma relação de A em B e S uma relação de B em C, então
	- a relação de composição de R e S, escrita como S o R, é definida como:
		- Se a E A e c E C, então (a,c) E S o R, se e somente se existir algum b E B tal que (a,b) E R e (b,c) E S
		- "S em seguida de R" (R primeiro, depois S)
	- Msor = Mr (X) Ms, além disto, se |A| = m, |B| = n e |C| = p:
		- Mr tem ordem mxn
		- Ms tem ordem nxp
		- Msor tem ordem mxp
	- Considere mais um terceiro conjunto D, e T uma relação de C em D, então:
		- T o S o R = T o (S o R) = (T o S) o R (ASSOCIATIVIDADE)
	- a inversa de (S o R) é igual a inversa de R em composição com a inversa de S

##### Relações Sobre um Conjunto ( A = B ):
- É possível representar utilizando **dígrafos**
	- cada elemento é um vértice
	- cada aresta ou arco é uma relação
- Caminhos em relações e dígrafos:
	- Seja R uma relação sobre o conjunto A. Um **um caminho de comprimento n** em R de A para B é uma sequência finita &=a,X1,X2,...,Xn-1,b tal que:
		- a R X1, X1 R X2, ..., Xn-1 R b
	- um caminho de comprimento n envolve n+1 elementos, não necessariamente distintos
	- um caminho que começa e termina no mesmo elemento é chamado cíclico
![[Pasted image 20231012162809.png]]
Significa que há um caminho de comprimento n de x até y, R^n é a relação de caminho n de A em B.
![[Pasted image 20231012162921.png]]
Significa que há algum caminho em R de x até y.
![[Pasted image 20231012163009.png]]
é chamada de relação de conectividade para R

Como encontrar R^n?
- Solução mais simples: Através de multiplicação de matrizes
![[Pasted image 20231012163157.png]]

LEMBRE-SE: |A x B| = |A|.|B|

## Propriedades das relações:

- REFLEXIVA
-![[Pasted image 20231014100513.png]]
- NÃO-REFLEXIVA
![[Pasted image 20231014100603.png]]
- IRREFLEXIVA
![[Pasted image 20231014100638.png]]
- NÃO-IRREFLEXIVA
![[Pasted image 20231014100706.png]]
- MATRIZES E DÍGRAFOS DE REFLEXIVA E DE IRREFLEXIVA
	- REFLEXIVA
		![[Pasted image 20231014100831.png]]
	- IRREFLEXIVA
	![[Pasted image 20231014100928.png]]
- SIMÉTRICA
  ![[Pasted image 20231014101018.png]]
- NÃO-SIMÉTRICA
  ![[Pasted image 20231014101037.png]]
- ASSIMÉTRICA
  ![[Pasted image 20231014101059.png]]
- NÃO-ASSIMÉTRICA
  ![[Pasted image 20231014101112.png]]
- ANTISSIMÉTRICA
  ![[Pasted image 20231014101200.png]]
- NÃO-ANTISSIMÉTRICA
  ![[Pasted image 20231014101221.png]]
  - TRANSITIVA
![[Pasted image 20231014101421.png]]
  - NÃO-TRANSITIVA
  ![[Pasted image 20231014101406.png]]
RECONHECER TRANSITIVIDADE PELA MATRIZ:
![[Pasted image 20231014120354.png]]
R² deve estar contido em R.

RECONHECER SIMETRIA PELA MATRIZ:
![[Pasted image 20231014120707.png]]
Simétrica em relação a diagonal principal, ou seja, como se a diagonal principal fosse um espelho.

OBS.: PARA VERIFICAR SE A RELAÇÃO É TRANSITIVA, VERIFICAR SE A RELAÇÃO DE CAMINHO 2 ESTÁ CONTIDA NA DE CAMINHO 1
