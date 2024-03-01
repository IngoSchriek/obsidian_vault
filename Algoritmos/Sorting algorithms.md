Para entender melhor algorítmos de ordenação, entender melhor relações de ordem (matemática discreta).

Alguns dos algorítmos de sort mais comuns:
- quick sort 
- merge sort
- selection sort
Um algorítmo de ordenação não consegue performar melhor do que O(n log n) na média.

Inversões: São pares de elementos de uma determinada sequência, que estão desordenados.
- Uma sequência ordenada é um sequência que não possui inversões

Stable Order (ordem estável): é um considerado um algorítmo de ordenação de stable order quando os elementos ao serem ordenados ficam em uma mesma ordem relativa a ordem anterior.
Ex: [“hello”, “world”, “we”, “are”, “learning, “sorting”]
![[Pasted image 20240110192953.png]]
### Comparison Based Sorts
Selection Sort:
- Um dos piores sorts
- Em todos os casos seu tempo de execução é de O(n²)
1) Verifica o menor/maior elemento da lista
2) Retira esse elemento, colocando-o em uma nova lista
3) Repete o processo até que a lista inicial tenha 0 elementos 

Quick Sort:
- O mais popular algorítmo de ordenação
- Um dos melhores casos médios, sendo seu tempo de execução de O(n)
- É feito de maneira recursiva
- Caso-base: Array com tamanho < 2 é um array já ordenado.
- Caso recursivo:
	- Retira um elemento qualquer
	- Compara todos os outros elementos com esse elemento para identificar se o elemento comparado é maior ou menor, assim criando outros dois arrays:
		- maiores
		- menores
	- Utiliza o quick sort nos outros dois arrays

Bubble Sort:
- estável, pois 2 elementos iguais nunca são trocados de lugar
- seu pior caso é de O(n²)
- Consiste em verificar os elementos do array aos pares, trocando-os de lugar quando o da esquerda for maior que o da direita.
- Repete o processo até que tudo esteja ordenado

Insertion Sort:
- pior caso de O(n²)
- é estável e a complexidade de espaço é de O(1) pois pode ser feito in-place
- A implementação oficial de Arrays.sort() em Java realiza a verificação de se o array é pequeno antes de realizar classificações teoricamente ideais. Pois Insertion Sort funciona melhor para arrays pequenos ou com poucas inversões.