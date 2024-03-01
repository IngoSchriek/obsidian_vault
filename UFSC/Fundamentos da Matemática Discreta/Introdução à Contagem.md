
## O que é a Análise Combinatória?
- A teoria da contagem tenta responder à pergunta "Quantos?" sem realmente enumerar quantos
- É o ramo da matemática que procura elaborar métodos nos permitam encontrar o número de possibilidades que um evento pode ocorrer, sem a obrigatoriedade de descrevermos todos os eventos possíveis.
- Essencialmente prática, teoria é apenas uma fração
- Muita criatividade e interpretação para resolver os problemas
## O básico da contagem:
#### Regra do Produto:
Suponha que uma tarefa ou processo possa ser quebrado em 2 tarefas. A primeira tarefa temos N maneiras de faze-la, a segundo M maneira. Logo, temos N.M maneiras de executar o mesmo processo;

|A1 x A2 x A3 x ... x Am| = |A1|.|A2|. ... .|Am|

Problemas para revisar:
- Contagem de subconjuntos de um conjunto finito (Rosen pág 304)
- https://www.youtube.com/watch?v=wM9T--A1gQA

#### Regra da soma:
Suponha que um processo possa ser quebrado em diferentes tarefas, neste caso, 2. Porém as duas tarefas não podem ser feitas juntas, ou é uma, ou outra. Portanto, se temos N maneiras de executar a primeira e M maneiras de executar a segunda, logo temos N + M maneiras de executar este mesmo processo.

|A1 U A2 U A3 U ... U Am| = |A1|+|A2|+ ... +|Am|


#### Observações importante:
- Muitos problemas de análise combinatória apresentam algum tipo de restrição, ou seja, uma condição prévia que deve ser satisfeita para a resolução do problema. Nos problemas em que tais restrições aparecem, devemos iniciar a resolução do problema por tal restrição e depois resolvermos o resto do problema.
- Em problemas que a restrição não tem uma posição fixa, muitas vezes é mais fácil calcular o número de combinações sem a restrição e subtrair do número de combinações que violam a restrição.
#### Problemas que envolvem a utilização das duas regras:
- Conferir exemplos da página 306 (rosen)

# Princípio de Inclusão-Exclusão:
![[Pasted image 20230922122346.png]]

![[Pasted image 20230922122410.png]]

Suponha que em um processo exista duas tarefas que possam ser executadas ao mesmo tempo:
Para sabe quantas maneiras há de executar uma das tarefas, devemos adicionar as maneiras de fazer uma e outra, e subtrair o número de fazer as duas ao mesmo tempo.

# Árvores:
Problemas de contagem podem ser resolvidos utilizando árvores, cada galho representa uma escolha possível.

## Exercícios recomendados:
- 3, 13, 15, 19, **21**, **23, 29 e 33** (pág 310 Rosen)