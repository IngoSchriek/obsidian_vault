## FSM com estados de bloqueio (lock-out)
- no caso de não serem utilizados todos os estados disponíveis, pode ocorrer a situação do contador se encontrar num estado não desejado (fora da sequência de contagem) devido a ruído no circuito ou à não imposição de estado inicial.
- Nessa situação ou o contador entra na sequência de contagem pretendida ou fica indefinidamente no exterior (Lock-Out).

Soluções:
- Solução mais prática: impor a transição de qualquer estado externo para um estado da sequência de contagem
- Outra solução: considerar uma entrada extra, de inicialização, que coloque o sistema num dos estados de contagem pretendido.

OBS.: LEMBRE-SE QUE AO ALTERAR A LÓGICA PARA SOLUCIONAR O LOCK-OUT, PODE ACABAR ALTERANDO A SEQUÊNCIA ORIGINAL DO CIRCUITO.

## Engenharia Reversa:
##### Dado um circuito sequencial para chegar no diagrama de estados você deve:
1) Obter funções lógicas
2) Obter tabela de transição de estados
3) Decodificar estados
4) Obter diagrama de estados

![[Pasted image 20231029193407.png]]
