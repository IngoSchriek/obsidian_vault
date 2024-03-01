## _Finite State Machine (FSM)_
- Descreve o comportamento ao longo do tempo, a partir dos possíveis estados de um circuito
- Indica o que pode causar a transação de estados
- Indica como as saídas irão se comportar de acordo com cada estado

![[Pasted image 20231029191429.png]]

![[Pasted image 20231029191459.png]]

![[Pasted image 20231029191638.png]]

![[Pasted image 20231029191711.png]]

# Projeto de Circuitos Sequencias Síncronos (FSM)

## Procedimento:
- Especificação formal
	- Diagrama de Estados (Fluxograma)
- Projeto
	1) Codificação de Estados
		- Método One-Hot ou Método Binário (MAIS UTILIZADO)
		![[Pasted image 20231029192208.png]]
	2) Tabelas de Transição de Estados 
		- Tabelas verdade para a parte Combinacional
		![[Pasted image 20231029192313.png]]
	 3) Determinação das funções lógicas de saída e de estado seguinte
		 - Visualizar tabela e se necessário mapas de karnough para cada saída


