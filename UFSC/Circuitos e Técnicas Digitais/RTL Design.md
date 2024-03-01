## O que é?
**Register Transfer Lever (RTL)** é uma representação de um circuito digital no nível abstrato. Existem dois elementos em circuitos digitais: Circuitos sequenciais (Flip-flop) e circuitos combinatórios (portas lógicas), com a ajuda desses dois elementos, um designer digital pode implementar qualquer circuito, por exemplo, somador, multiplicador, contador (somador + registrador), memórias e máquina de estados.

![[Pasted image 20231029193830.png]]

![[Pasted image 20231029193959.png]]

![[Pasted image 20231029194210.png]]

![[Pasted image 20231029194249.png]]

#### Operações de "Alto Nível":
- Contador Crescente (r+1)
- Atribuição (registro) de valores (r=0, r=r+1)
- Comparação de Grandezas (r<99)

![[Pasted image 20231029194552.png]]

## Elementos do Datapath
![[Pasted image 20231111181635.png]]

## Algumas informações relevantes:
- Datapath: Realiza operações com entradas/saídas de dados.
- Entradas de Dados: Dados que entram no datapath, que não passam pelo controle
- Entradas de controle: Entradas que indicaram o estado que consequentemente indicara os comandos a serem dados ao datapath.
- Comandos: São vetores que saem do controle para entrar no datapath, onde eles dirão o que será feito com os dados provenientes das entradas de dados.
- Status: Retorna informação dos dados para o bloco de controle.

## RTL Design na prática:
Passos:
1) Diagrama de estados de alto nível
![[Pasted image 20231111182817.png]]

2) Criar datapath (permite converter diag. de alto nível em FSM)
![[Pasted image 20231111182901.png]]

3) Conectar datapath ao bloco de controle
4) Projetar bloco de controle
![[Pasted image 20231111183100.png]]![[Pasted image 20231111183112.png]]
![[Pasted image 20231111183137.png]]