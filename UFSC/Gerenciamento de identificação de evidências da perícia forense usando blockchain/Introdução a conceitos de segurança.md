Bolsa: Gerenciamento de identificações de evidências de perícia forense, usando blockchain

Propriedades de um sistema seguro
- Confidencialidade
- Integridade
- Disponibilidade
- Autenticidade
- Irretratabilidade

### Criptografia:
- Resolve bastante dos problemas exceto disponibilidade (ex: desligar servidor da tomada).
- Comumente é utilizado chaves de 128 bits
- Em sistemas criptográficos sem vulneriabilidades demoraria milenios para desvendar o segredo

### Criptoanálise:
- O segredo deve residir totalmente na chave
- Considerar que um algoritmo é mais seguro só por que sua estrutura interna é desconhecida é **igenuidade**.
- Os melhores algorítmos atualmente são aqueles tornados públicos:
	- Atacados pelos melhores criptoanalistas do mundo por anos e, mesmo assim, não foram quebrados.

![[Pasted image 20230924194915.png]]



Segurança é um processo:
1) Riscos
2) Políticas
3) Implementação
4) Administração
5) Auditoria
6) Repete

### Blockchain:
- Blocos de informação, vinculados através de um hash

### Confidencialidade:
Prevenção do vazamento de informações

- Esteganografia: Disfarçar dados (ex: alterar bit menos significativo de pixels em imagens) (Confidencialidade)
	 - Caso Juan Carlos Abadia (2008) (hello kitty)

- Embaralhar os dados: cifras (criptografia): 
	- Exemplo: HTTP vs HTTPS (HTTP com segurança)
#### Cifras simétricas:
- Transformação matemática reversível (cifração e decifração)
- Os dois processos dependem de uma mesma informação secreta: a chave K
![[Pasted image 20230924195403.png]]
- Exemplo: Cifra de César (deslocar cada letra da mensagem K posições no alfabeto latino)
	- Sabendo K, você sabe tanto cifcrar como decifrar uma mensagem.
	- Problemas:
		- No máximo 25 chaves. 
		- Letra mais utilizada (A)
		- Letras dobradas (RR, SS, etc)
		- Palavras de no máximo 2 caracteres
		- Entre outros
#### Cifração moderna:
![[Pasted image 20230924195829.png]]
#### Difusão e Confusão:
Princípios básicos para projetar cifras seguras.
Pequenas mudanças que levam a grandes impactos, "Efeito avalanche".

Cifras seguras:
- Tamanho
- Alta difusão
- Alta confusão
- Efeito avalanche

Difusão: O princípio da difusão tem como objetivo fazer com que a relação da mensagem e da cifra seja, idealmente, oculta. Ou seja, ao mudar um caractere do texto simples, vários caracteres do texto cifrado são alterados e vice-versa. A relação entre o texto cifrado e o texto simples é mascarada pela difusão.

![[Pasted image 20230924200053.png]]

Confusão: Na confusão, se um bit do segredo for modificado, a maioria ou todos os bits do texto cifrado também serão modificados. A relação entre o texto cifrado e a chave é mascarada pela confusão.

![[Pasted image 20230924201453.png]]

### AES:
- Evita todos os problemas encontrados na Cifra de Cesar.
##### Como?
- Opera em mensagens de 128 bits 
- Rodadas: 10, 12 ou 14, para chaves de 128, 192 ou 256 bits
- 4 Operações por rodada: ByteSub, ShiftRows, MixColumns e AddRoundKey

ByteSub: Substituição de bytes com tabela fixa, independente da chave.
ShiftRows: Troca posição de alguns bytes, rotacionando linhas (deslocamento é fixo).
MixColumns: Multiplicação por matriz, coluna e coluna.
AddRoundKey: XOR de cada byte com cada byte da chave

AES (uma cifra de bloco) apenas opera sobre mensagens de tamanho fixo (128 bits)
##### Modo de operação:
- Permite cifração de mensagens com tamanho diferente do bloco
- Diversos modos de operação (pesquisar exemplos)

![[Pasted image 20230924202717.png]]


##### Definição de conceitos importantes:
- Hash: Basicamente, um resumo.
- Cálculo de hash: Unidirecional, evita alterações dos dados (integridade)
- Colisão: Dois ou mais documentos/arquivos diferentes com o mesmo hash.

Requisitos para um algorítmo de hash:
- Velocidade
- Se mudar um bit, então o hash inteiro deve ser completamente diferente (efeito avalanche)
- Evitar colisões de hash

#### Certificados digitais:
![[Pasted image 20231004101500.png]]

