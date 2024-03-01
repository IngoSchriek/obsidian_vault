## Através da utilização de [[Lógica Booleana e Portas Lógicas]] é possível fazer com que computadores façam aritmética com números binários, como fazemos com números decimais.


![[Pasted image 20230916093248.png]]
# Meio somador:

![[Pasted image 20230916093334.png]]

# Somador completo:

![[Pasted image 20230916093427.png]]


# Somador em paralelo:

![[Pasted image 20230916094824.png]]

## Pode ser todos somadores completos também.
Em maior nível de abstração:
![[Pasted image 20230916095040.png]]

# Multiplicação:
### Basta quebrar em multiplicações por potências de dois.

![[Pasted image 20230916095136.png]]

![[Pasted image 20230916095223.png]]

# Subtração utilizando somador:

## Para tornar um número binário de n bits em complemento de 2 (olhar em [[Sistemas de Representação]], basta complementa-lo e somar 1.

## Logo, como X - Y é o mesmo que a soma X + (-Y), basta substituir o espaço (0) que resta.
## Conforme a imagem:

![[Pasted image 20230916100525.png]]![[Pasted image 20230916100747.png]]

![[Pasted image 20230916100944.png]]

## Já que no somador se utilizarmos o complemento de Y quando queremos apenas uma soma entre dois números positivos, precisamos de alguma maneira desativa a porta not para fazermos um circuito que some e subtraia, ou seja, um somador/subtrator. Fazendo a tabela verdade vemos que para isso basta substituir a porta not por uma XOR entre Cin e B.

## Obtemos portanto:

![[Pasted image 20230916101435.png]]

# Overflow:
## Ocorre quando o valor resultado da soma ou subtração está fora da faixa de complemento de 2, -2^(n-1) até 2^(n-1)-1. Ex: um número binário de 4 bits, sua faixa portanto é de -2^3 até 2^3 - 1, ou seja, -8 até 7.

## Só ocorre se os dois números somados são ambos positivos ou negativos.

## Para detectar basta uma XOR entre os dois bits de carrys mais significativos. Conforme a imagem:

![[Pasted image 20230916102050.png]]

