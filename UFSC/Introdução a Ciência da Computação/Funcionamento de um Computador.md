# Organização e Arquitetura de Computadores:
#### Arquitetura de Von Neumman:
- Memória (ex: Registradores, Memória Cache, Memória RAM)
- Unidade Lógica Aritmética e Unidade de Controle (Juntas e mais registradores formam o processador, unidade central de processamento)
- Entradas
- Saídas

#### Processadores:
- Escrever e leem dados
- Seguem instruções 
- Operações Lógicas e Aritméticas

#### Memória:
- Armazena Dados
- Possibilita leitura e escrita
- Curiosidade: Cada variável é um apelido para um endereço de memória
![[Pasted image 20231124154707.png]]
#### Periféricos:
- Levam e trazem dados para o processador
- Apenas entrada, ou apenas saídas, ou ambos
- Grande variedade (ex: Monitor, Mouse, Display)

# Como criar soluções para problemas complexos através de instruções tão simples?
##### Ou seja, como criar programas complexos através de simples instruções?

## Resposta: Níveis de Abstração.
#### Nível -1: Transistores
![[Pasted image 20231124155317.png]]

Nivel 0: Lógico Digital
- Portas Lógicas
- AND, OR, XOR, NOT
- Hardware

Nível 1: Nível de Microarquitetura
- Registradores
- ULA (Unidade Lógica Aritmética)
- Conjunto de Portas Lógicas

Nível 2: Arquitetura

Nível 3: Sistema Operacional
- Aplicações, Kernel (núcleo), CPU, Memória, Dispositivos

Nível 4: Assembly
![[Pasted image 20231124155710.png]]

Nível 5: Linguagem orientada a problema
- Exemplos: Python, Ruby, Java, etc

#### Máquina com Múltiplos Níveis: Fundamental
- Permite dispensar detalhes complexos
- Assunto complexo se torna mais fácil de entender
- Divisão do problema e desacoplamento das soluções 
- Profissionais trabalhando em diferentes níveis sem se preocupar com os outros

Hardware: Objetos Físicos, Tangíveis
Software: São instruções detalhadas de como fazer algo (algorítmos) e suas representações em um computador que são chamados de programas.

![[Pasted image 20231124170637.png]]