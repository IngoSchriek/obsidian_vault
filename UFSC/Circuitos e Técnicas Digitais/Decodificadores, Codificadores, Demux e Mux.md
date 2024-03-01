Agora iremos tratar de circuitos lógicos um pouco mais complexos, o que exige amplo entendimento de [[Lógica Booleana e Portas Lógicas]] e [[Sistemas de Representação]].
## Decodificador:
Decodificador é um circuito lógico que possui uma entrada de N bits com 2^N saídas, onde em sua entrada irá receber um número, cujo será correspondente a uma de suas saídas. Ou seja, cada saída será um minitermo (confira em [[Formas Padrão Canônicas e Mapa de Karnaugh]]).

![[Pasted image 20230916113447.png]]

![[Pasted image 20230916113757.png]]

Para saídas baixas, apenas troca-se as portas and's por nand's.

![[Pasted image 20230916113842.png]]

## É possível desativar ou ativar o circuito, bastando acrescentar um pino de habilitação, chamado ENABLE

Ou seja, quando o ENABLE for igual a 0, o decodificador não funciona (independente da entrada, não há nenhuma saída). Quando ENABLE for 1, funciona normalmente.

![[Pasted image 20230916114042.png]]

## Através do pino enable, é possível associar diversos decodificadores tirando proveito do funcionamento dos bits mais significativos.

![[Pasted image 20230916114159.png]]

# Codificadores:
Codificadores são circuitos lógicos que possuem 2^N entradas e N saídas, ou seja, basicamente fazem a função oposta dos decodificadores. Também podem ser ativos altos e baixos.

![[Pasted image 20230916115133.png]]

# Demultiplexadores (DEMUX):
## Decodificadores X Demultiplexadores:
Enquanto decodificadores possuem uma entrada de um número de N bits que corresponde a uma das saídas, que são um total de 2^n, o **demultiplexador** possui uma entrada única que pode ter múltiplos bits e N entradas de seleção, as quais juntas, como um decodificador, correspondem a uma das 2^N saídas, podendo uma delas retornar o mesmo que a entrada não seletora.

![[Pasted image 20230916120013.png]]

Percebe-se que o demultiplexador utiliza diversas portas and, cada uma delas conectada a entrada principal e conectada a uma das saídas do decodificador responsável pela seleção das saídas.

# Multiplexadores:

![[Pasted image 20230916121410.png]]


![[Pasted image 20230916122400.png]]
## É possível perceber que o multiplexador é exatamente uma soma de produtos, em que cada porta lógica AND possui uma das entradas e possui um minitermo S1S0 que corresponde a entrada que será utilizada. 00, 01, 10, 11.

Duas entradas, possui apenas 1 entrada de seleção. Quatro entradas, possui duas entradas de seleção. A saída sempre é uma. Ou seja 2^N entradas possui N entradas de seleção, e uma saída. 

![[Pasted image 20230916122103.png]]

# Métodos sistemáticos de Projeto:
De maneira geral, quando se deseja projetar um circuito podemos pensar em utilizar a soma de minitermos ou produto de maxitermos para tal. Porém, tais métodos não nos permite saber de antemão:
![[Pasted image 20230916123325.png]]
Prós:
- Flexibilidade e facilidade no projeto.
Contras:
- Maior custo/desperdício e circuitos maiores

### é possível utilizar decodificadores ou multiplexadores para implementar funções lógicas genéricas de forma sistemática.

# Cada saída do decodificador, é dada por um minitermo diferente.

![[Pasted image 20230916124108.png]]
# Já no multiplexador...

![[Pasted image 20230916124040.png]]

# Look-up table:
Basicamente, grava as saídas da tabela verdade na memória e quando tais valores das entradas de seleção se repetem, seleciona exatamente a resposta desejada.

![[Pasted image 20230916124604.png]]

## Mudar os valores da memória, muda também a função!!!

![[Pasted image 20230916124639.png]]

