## Notação Big-O:
![[Pasted image 20231112164629.png]]
Exemplo: f(x) = x² + 2x + 1 é O(x²)
- 2x é menor ou igual que 2x² a partir de 1
- 1 é menor que x² a partir de 1
- x² + 2x + 1 <= x² + 2x² + x² = 4x²
- C = 4, K =1, g(x) = x²
- Ou seja, f(x) é O(x²)

2 funções possuem a mesma **ordem** caso ambas sejam big-O uma da outra, como no exemplo anterior:
- x² é O(x²+2x+1), C=1, K=1

OBS.: Algumas vezes é escrito, f(x) = O(g(x)), porém o sinal de igualdade neste caso não reflete de fato uma igualdade, é o mesmo que dizer "f(x) é big-o de g(x)"

##### Como mostrar que uma função não é big-O de outra função?
- Pode ser feito por contradição, ao assumir que essa função é big-O da outra função.
- Primeiro relacione as duas funções através da desigualdade entre funções quando uma é big-O de outra. Ex: x³ <= C(7x²) para todo x > k
	- Dividindo os dois lados por x², temos: x <= 7C para todo x > k
	- Isso leva a uma contradição, pois 7C e K são constantes, enquanto que X pode ser arbitrariamente grande.
![[Pasted image 20231112171313.png]]
