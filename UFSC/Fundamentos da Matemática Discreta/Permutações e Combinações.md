# Seleção ordenada de objetos de um conjunto:
#### Permutação:
- Todos elementos do conjunto
- Arranjo ordenado de objetos distintos = n!
![[Pasted image 20230923162650.png]]
Com repetição:
- Ocorre quando nem todos os objetos são distintos
- Arranjo ordenado de objetos distintos com exceção de um repetindo p vezes = n!/p!
#### Arranjo:
- Arranjo ordenado de alguns dos objetos do conjunto
![[Pasted image 20230923162729.png]]

# Seleção não-ordenada de elementos de um conjunto:
#### Combinação:
- Uma combinação de r elementos de um conjunto é simplesmente um subconjunto com r elementos
- Combições simples de n elementos tomados k a k é representada por:
![[Pasted image 20230923162942.png]]


#### Número binomial (Combinação):
![[Pasted image 20230923163202.png]]

RESUMO:
- e = multiplicação
- ou = soma
![[Pasted image 20230923163035.png]]

## Problemas para revisar:
![[Pasted image 20230923182654.png]]
- Em problemas desse tipo, primeiramente devemos ver todas possíveis combinações e depois remover (subtrair) aquelas em que não funciona como solução.
- Ou seja, neste caso, pegamos a combinação de 10 elementos pegos de 6 em 6, já que a ordem não importa, e subtraimos uma combinação de 8 elementos (8 elementos pois estamos assumindo que já pegamos os 2 fios que fazem a bomba explodir) tomados de 4 em 4

![[Pasted image 20230923182939.png]]
- Neste problema, devemos considerar OURO como se fosse um único objeto, vamos denotá-lo por X, logo ficaríamos com DETXS, uma permutação sem repetição de 5 elementos (pois a ordem importa), então temos 5!
- Para a segunda restrição, denotamos DS como Y, ficando portanto com uma permutação de 4 elementos ETXY, 4!, porém como também pode ser SD, devemos considerar que o usuário pode escolher a permutação de 4 elementos contendo DS como Y **OU** a permutação de 4 elementos contendo SD como Y, ou seja, 4! + 4!, ou 2 x 4!
