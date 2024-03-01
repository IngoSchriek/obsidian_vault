# Decimal, Binário, Octal e Hexadecimal:

Para conversão de Decimal para Binário:
- Método da divisão
De baixo para cima, da direita para esquerda.
![[Pasted image 20230916083606.png]]
- Método da subtração

![[Pasted image 20230916082803.png]]
![[Pasted image 20230916082632.png]]
# Quaternário:
base 4, agrupa de dois em dois e converte.
# Gray e BCD:
Gray: Para o sucessor ou antecedente, muda apenas um dígito. Ex: 00 (0 em decimal), 01 (1 em decimal), 11 (2 em decimal), 10 (3 em decimal).

![[Pasted image 20230916083121.png]]

O código BCD apenas vai de 0 a 9. Para conversão, agrupe de 4 em 4 e cada numble retornará um digito.


BIT = 1 
NIBBLE = 4 bits
BYTE = 8 bits ou 2 nibbles

# Sinal/Magnitude:
Basta colocar 1 na frente para indicar negativo, e 0 para positivo.

# Complemento de 1:
Basta inverter/complementar cada bit. 1 na frente indica negativo, 0 positivo.

# Complemento de 2:
Basta fazer o complemento de 1 e somar 1. Para retornar, subtrair 1 e fazer o processo inverso do complemento de 1. Faixa de representação de -2^(n-1) a +2^(n-1)-1.

![[Pasted image 20230916095941.png]]

### Quando somado N bits, com N bits, ignorar o bit de indice N

![[Pasted image 20230916100221.png]]