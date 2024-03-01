#### Memória:
O elemento de memória mais importante é o flip-flop, composto por conjunto de portas lógicas. Embora uma porta lógica, por si só, não tenha capacidade de armazenamento, algumas podem ser conectadas entre si de modo a permitir o armazenamento de informação.
Um elemento de memória pode ser criado aplicando-se o conceito de realimentação. Esta é conseguida conectando-se determinadas saídas de porta de volta às entradas de porta apropriadas.
A realimentação é um conceito de engenharia extremamente importante, que tem muitas aplicações na eletrônica. Algumas formas diferentes de arranjo de portas são usadas para produzir flip-flops (FFs)

![[Pasted image 20230927201836.png]]


#### Sequencial x Combinacional
Circuitos Combinacionais:
- a saída depende apenas do estado atual das entradas
- não possui memória
Circuitos Sequenciais:
- a saída depende do atual estado das entradas e do estado anterior

#### Flip-flops x Latches
A principal diferença de um flip-flop para um latch é em que momento é gravada a saída na memória. Em flip-flops esse momento pode ocorrer ou na borda de subida ou na borda de descida do clock, ou seja, na transição de 0 para 1 ou de 1 para 0. Já nos Latches, ocorre enquanto o clock está em 1 ou pode ocorrer quando o clock está em 0, quando o latch é sensível a entrada baixa do clock.

##### FF-D
Como um exemplo de Flip-Flop D (FF-D), temos a figura abaixo:
![[Pasted image 20231006190304.png]]
- 1D, representa a entrada D que é síncrona ao clock
- O triângulo representado na entrada do clock sem nenhum círculo significa que o ff é sensível à borda de subida
- Caso houver um círculo representando entrada baixa, antes do triângulo, significa que é sensível à borda de descida
- Flip-flops grava em sua memória o instante imediatamente anterior a borda
Tabela Verdade do Flip-Flop D:
![[Pasted image 20231006191458.png]]
#### Set x Reset
Set é uma entrada com prioridade que obriga o circuito, quando set for 1, a retornar 1.
Reset é uma entrada que "reseta" o circuito para 0.
Podem ser síncronos ou assíncronos, o reset quase sempre é assíncrono.

##### FF-T
- Semelhante ao anterior, exceto por:
- Quando T está em nível alto, o próximo estado será oposto ao anterior 
![[Pasted image 20231006191817.png]]
#### FF-SR
- Flip flop com entradas set-reset
Um exemplo:
![[Pasted image 20231006192305.png]]
#### FF-JK
- Mesmo do anterior, porém no caso proíbido do FF-SR, ou seja, quando S=1 e R=1, o próximo estado será o complemento do estado anterior.
- Lembre-se que é SÍNCRONO com o clock.

#### Outras possíveis formas de circuito sequencial:
- Com o que se tem acima, podemos criar diversos circuitos diferentes, como:
	- Um latch-d sensível ao nível baixo do clock com entrada set e reset
	- Um flip-flop SR com uma entrada D síncrona ao clock e set síncrono também
	- e outros...

##### FF-D a partir de um FF-JK
- Observe a tabela do FF-JK
![[Pasted image 20231006193010.png]]
##### FF-T a partir de um FF-JK
- Observe a tabela do FF-JK
![[Pasted image 20231006193347.png]]