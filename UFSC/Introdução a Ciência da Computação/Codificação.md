- Necessário: [[Sistemas de Representação]] .

### Como transformar tensão alta e tensão baixa, 1 e 0, em textos, imagens e áudios?

# Textos:
### Tabela ASCII:
(código padrão americano para intercâmbio de informações)
- versão de 7 bits (128 valores)
- versão de 8 bits (256 valores)
- extensões para ASCII, suporte para múltiplas línguas (padrões ISO)

Dois problemas
- Quantiade de símbolos insuficiente
	- Documentos só podem usar um padrão (ex: misturar padrões de linguagens diferentes em um mesmo documento acarreta em problemas)

### Unicode Transformation Format (UTF):
- Codificação de tamanho varíavel
- Primeiros 128 valores iguais à tabela ASCII

UTF-8:
- mínimo de 8 bits
![[Pasted image 20230920204845.png]]

UTF-16:
- mínimo de 16 bits
UTF-32:
- mínimo de 32 bits

![[Pasted image 20230920205032.png]]

### Não confundir arquivo de texto com processadores de texto.
Arquivo de texto:
- longa sequência de símbolos codificados em ASCII ou Unicode.
- bloco de notas, gedit, etc
Processadores de texto:
- Mais elaborados
- Padrões mais específicos com informações de formatação
- ex: Word

# Imagens:
### Bitmap ou raster (mapa de bits):
- representa imagens como coleção de pontos
- esses pontos são elementos da imagem, do inglês, picture element (pixels)
- imagem: matriz de elementos da imagem
- Com pixels de 1 bit, é possível representar imagens preto e branco
- para representar cores, é utilizado o sistema RGB, q exige no mínimo 3 bits para cada pixel
- é possível pensar em 3 matrizes sobrepostas uma a outra, uma sendo R, outra G, outra B
- A quantidade de bits mais comum para representar cores em RGB são de 8 bits para cada cor (representa os mais diversos tons), ou seja, 3 bytes.

Desvantagem:
- Redimensionamento.
- Quando aumentada a imagem, perde-se a qualidade.

### Vetorial:
Figuras geométricas:
- retas, curvas
- geometria analítica
Aplicações:
- Plantas (CAD), Fontes, SVG, PDF

# Sons:
- onda de ar comprimido ou expandido
- valores de pressão variam no tempo (causa vibrações no ímã de um microfone)

Microfone:
- membrana, ímã e bobina
- ímã varia de posição, varia o campo magnético, induz corrente elétrica na bobina

Onda mecânica >>(1)>> Sinal Analógico >>(2)>> Binário >>(3)>> Corrente >>(4)>> Onda Mecânica
Corrente == Sinal Analógico == Pulsos elétricos
(1) = Microfone, que através da onda mecânica (som) gera sinais analógicos
(2) = Conversor Analógico Digital (Converte sinais analógicos em bits)
(3) = Conversos Digital Analógico (Converte bits em corrente elétrica)
(4) = Converte pulsos elétricos em onda mecânica (som)

### Como converter sinais analógicos (pulsos elétricos) em bits?
#### * Método mais comum: Amostras da amplitude dos sinais analógicos em intervalos regulares
- Naturalmente haverá distorções.
#### Dois parâmetros fundamentais:
- taxa de amostragem (relacionado ao intervalo entre leituras) (sample rate)
![[Pasted image 20230921155956.png]]

- profundidade (bit depth) (quantidade de bits)
![[Pasted image 20230921160026.png]]


Maior taxa, maior profundidade == *menor distorção, som mais fidedigno*
Problema: *Armazenamento limitado*

### Curiosidade:
frequência audível: 20Hz - 20kHz
CD: 44.1kHz (Por quê? Resposta: Teorema do Nyquist)

## Outra maneira:
### MIDI (INTERFACE DIGITAL DE INSTRUMENTO MUSICAL):
Amplamente utilizado em sintetizadores, teclados eletrônicos, sons de vídeo game etc.

Codifica 3 informações:
- instrumento, nota, tempo