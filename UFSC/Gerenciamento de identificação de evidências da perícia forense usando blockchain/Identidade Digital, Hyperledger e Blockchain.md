#### Conceitos importantes:
- peer-to-peer (P2P)
	- https://www.infomoney.com.br/guias/peer-to-peer-p2p/
- DID
	- uma maneira de se identificar online, sem depender de uma organização para verificar sua identidade
	- você prova quem você é, usando um código único que está armazenado na blockchain
	- é criado pelo usuário
	- vem com um ou vários pares de chaves pública/privada
	- não contém dados pessoais ou informações da carteira
	- permite conexões privadas e seguras entre 2, e pode ser verificada a qualquer momento
	- pode-se gerar quantos DIDs quiser, para diferentes propósitos, exemplos:
		- DID 1 para jogos onlines
		- DID 2 para Diplomas
		- DID 3 para Compras onlines
	- 
- W3C
- DKMS
- Ledger
	- Ledger Public Permissioned (com permissão pública)
		- https://www.investopedia.com/news/public-private-permissioned-blockchains-compared/
- NYM transaction
	- transação utilizada para a criação de um DID conhecido pelo ledger, configuração e rotação de uma chave verificadora e definição e mudança de papéis (roles).
	- os campos mais importantes dessa transação são:
		- dest
			- (base58-encoded string)
			- DID alvo
			- destino
		- role
			- um desses valores:
				- None (common USER)
				- "0" (TRUSTEE)
				- "2" (STEWARD)
				- "101" (ENDORSER)
				- "201" (NETWORK_MONITOR)
			- para que está sendo criado
		- verkey
			- base58-encoded string, possibly starting with "~"; optional
			- chave verificadora alvo
			- permite que uma pessoa, organização ou coisa, verifique se alguém possui esse DID, já que essa pessoa, organização ou coisa, é a única que conhece a chave de assinatura correspondente e quaisquer operações relacionadas ao DID que exijam assinatura com essa chave
			- 
		- alias (opcional)
			- apelido do NYM
	- Se não há transação NYM para o DID específico ainda, então é considerado a criação de um novo DID
	- Se já tem transação NYM para o DID específico, então é considerada uma atualização desse DID.
		- nesse caso, somente os valores especificados serão mudados, o restante que não for especificado, permanece o mesmo
- SSI
- Key Rotation
	- Mudar a chave, substituindo por uma nova
	- Ocorre quando uma chave é comprometida
- Identity Records
	- São dados públicos que podem incluir chaves públicas, service endpoints, esquemas de credenciais e definições de credenciais
	- Cada Identity Record é associado com exatamente um DID que é globalmente único e solucionável (via ledger) sem necessitar da ação de qualquer autoridade centralizada
- Service endpoints
	- endereços
- Verinym
	- Tipo de DID
	- é associado com a identidade legal do indivíduo
	- DID conhecido pelo ledger
- Pseudonym
	- Tipo de DID
	- Um Identificador Cego usado para manter a privacidade no contexto de um relacionamento digital contínuo (Conexão)
	- Quando usado é uma única relação digital, é chamado de Pairwise-Unique Identifier (Identificador Único Emparelhado)
-  Trust Anchor/Endorser
	- É uma pessoa ou organização que o ledger já conhece
		- Normalmente se trata de uma entidade emissora, tais como governo e universidade, que é uma instituição autoritária
	- Necessário para adicionar transações no ledger
- STEWARDS
	- São capazes de participar do processo de validação
	- Escrevem transações no ledger
	- São os nós validadores da blockchain/ledger
- Indy Nodes (nós Indy)
	- é uma aplicação rodando em máquinas que estão em uma rede Hyperledger Indy.
- Indy-cli
	- é uma ferramenta que serve para interagir com Indy wallets e ledgers
- Indy Nodes Pool
	- É uma rede de Indy nodes conectados entre si
	- Isso geralmente se refere à rede Hyperledger Indy que você pode executar no docker, por exemplo
	- A rede de nós Indy mantém o estado do ledger, verificando as transações.
- TRUSTEES
	- Garantem diversas capacidades para o proprietário da identidade, tais como:
		- Em caso de perca dos dado
- Genesis File
	- Permite que você conecte-se a rede
	- Contém informações sobre os primeiros nós da rede (ledger)
#### O que é identidade digital?
- É quaisquer dados que levem a uma pessoa ou organização.
- No contexto de identidade digital, você é o seus dados.

4 Fases da Evolução da Identidade Digital:
1) Identidade Centralizada
2) Identidade Federada
3) Identidade Centrada no Usuário
4) Identidade Autossoberana

![[Pasted image 20231007193139.png]]

#### Identidade Autossoberana:
3 Pilares:
- Credenciais verificáveis
- Blockchain
- Identificadores Descentralizados (DIDs)

![[Pasted image 20231007193910.png]]![[Pasted image 20231007193940.png]]

Problemas com a identidade digital atual:
- Vazamento de dados
- Em sistemas federados, sistemas provedores de credenciais, como a Google, talvez use dados pessoais de usuários a fim de monetizar em cima deles

Principais vantagens da Identidade Soberana:
- Usuário possui total controle de seus dados
- Maior segurança e maior privacidade
- Usuário não depende de terceiros para armazenar e gerenciar seus dados

Principais atores da Identidade Soberana:
- Pessoa (Holder):
- Emissor (Issuer):
- Verificador (Verifier/Provedor de Serviço)

10 Princípios do SSI:
1) Existência
2) Controle
3) Acesso
4) Transparência
5) Persistência
6) Portabilidade
7) Interoperabilidade
8) Consenso
9) Minimização
10) Proteção

![[Pasted image 20231007194634.png]]

#### Blockchain:
- Pública
	- qualquer um pode acessar e participar
	- qualquer um pode ler, escrever e auditar as atividades ocorrendo na rede blockchain
	- importante para uma estrutura descentralizada
	- Desvantagens:
		- Para que funcione, é necessário que para saber qual a cadeia de blocos é a mais fidedigna ocorra um enorme trabalho computacional, que é incentivado pelo mecanismo de consenso Proof of Work, o que acaba por demandar altíssimo consumo de energia. Os participantes-validadores são recompensados por deixarem a rede utilizar seu poder computacional.
- Privado
	- Participantes podem entrar em uma rede blockchain privada somente com convite, onde sua identidade ou outra informação necessária é autentica e verificada.
	- Redes privadas de blockchain controlam quem está permitido a participar da rede
	- Se a rede é capaz de mineração, é controlado quais usuários iram executar o protocolo de consenso
	- Somente usuários selecionados devem manter o ledger compartilhado
	- O proprietário do ledger compartilhado ou operador, tem o direito de sobreescrever, editar ou deletar entradas no blockchain conforme acharem necessário ou adequado.
	- Não é descentralizado
- Permissionada
	- É uma mistura de pública e privada, que suporta diversas opções para customização (Ex: a ledger do Hyperledger Indy)
	- Permite qualquer um a entrada da rede permissionada, depois de um processo de verificação de identidade adequado
	- Alguns indivíduos/organizações podem receber permissões especiais ou designadas para executar atividades específicas na rede, tais como ler, acessar ou inserir informações na blockchain

#### Hyperledger Indy
- Hyperledger Indy é um projeto criado pela Linux Foundation que tem como ideia base o gerenciamento de identidades de maneira descentralizada. Para tanto, existem diversas ferramentas que fazem parte do Indy, como Aries Agents, Indy Node, wrappers, Indy Plenum, libindy, Ursa Python e Ursa. O projeto Ursa possui duas bibliotecas, libursa e libzmix, ambas fornecem diversos algorítmos criptográficos necessários para realização de um ecossistema descentralizado, tais como algorítmos de criptografia assimétrica, algorítmos de criptografia simétrica e além disso, possui também algorítmos necessários para Zero-Knowledge Proof. As demais tecnologias presentes no stack Indy consumem a criptografia que Ursa fornece. Para criar aplicações com identidade digital autossoberna, Indy possui uma série de ferramentas que fornecem a base necessária, inclusas no Indy SDK (Software Development Kit).
- As funcionalidades do Hyperledger Indy SDK podem ser divididas em três:
	- As que envolvem o ledger, ou seja, ser capaz de comunicar com o ledger e interfaces que são necessárias para isso
	- As que envolvem as wallets (carteiras), ou seja, ser capaz de armazenar chaves privadas de maneira protegida
	- As que envolvem as AnonCreds (AnonCred é o formato de credencial verificável mais utilizado no mundo), ou seja, ser capaz de emitir e verificar credenciais AnonCreds.
- Para executar tais funções, Indy SDK possui diversas APIs, sendo que cada uma possui uma função específica:
	- Pool API: Uma pool é grupo de nós em uma rede que recebem as transações dos clientes. A Pool API possui diversos comandos que lidam com a pool.
	- Wallet API: Esta API possui todos comandos que envolvem o gerenciamento da carteira digital, tais como criar, abrir, fechar, deletar, importar e exportar.
	- Ledger API: Contém todos os métodos necessários para assinar e enviar uma transação para uma pool. Também possui *parsers*  que agem transformando a resposta do ledger em um formato esperado por cada Indy API, e possui construtores para variadas transações, como transações Nym, gerenciamento do Pool e objetos AnonCreds.
	- DID API: Permite a criação, key rotation (necessário quando uma chave é comprometida) e armazenamento de DIDs. Possui também outras funções relacionadas, como armazenar e adquirir metadados sobre DIDs.
	- Cryto API: Contém operações criptográficas que não estão relacionadas à outras funções.
	- Non-Secrets API: Criada com a utilidade de armazenar de maneira segura valores que não são chaves privadas.
	- AnonCreds API: Métodos/Comandos para criação e interação com objetos AnonCreds, como criação de esquema de credencial e a criação, apresentação e verição do credencial.
- Indy Command Line Interface (Indy CLI)

- Indy possui um livro de registros público permissionado (public permissioned ledger), o que significa que qualquer indivíduo pode ver as transações mas somente alguns podem receber permissões especiais ou designadas para executar atividades específicas na rede, tais como editar ou inserir informações no ledger.
