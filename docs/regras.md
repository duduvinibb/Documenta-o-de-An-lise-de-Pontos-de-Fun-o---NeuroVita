Onde as regras de negócio impactam a contagem:

1. Classificação do processo elementar (EE, SE ou CE)

A presença de certas lógicas de processamento define o tipo da transação:

|Lógica de processamento |	EE |	SE |	CE |
|--------|--------|--------|--------|
|Validações	|Sim	| Sim	| Sim|
|Cálculos ou fórmulas matemáticas	| Sim	| Obrigatório (ao menos uma lógica de SE) |Não|
|Conversão de valores equivalentes|	Sim	|Sim |Sim|
|Filtragem e seleção de dados	|Sim	|Sim	|Sim|
|Análise de condições para definir qual se aplica	|Sim	|Sim|	Sim|
|Atualização de ALI	|Sim|	Sim	|Não|
|Referência a ALI ou AIE	|Sim	|Sim	|Sim|
|Recuperação de dados	|Sim	|Sim	|Sim|
|Derivação de dados	|Sim	|Sim	|Não|
|Alteração do comportamento do sistema	|Sim	|Sim	|Não|
|Preparação e apresentação de informação fora da fronteira	|Sim	|Sim	|Sim|
|Aceitação de entrada de dados	|Sim	|Sim	|Sim|

Uma consulta que só recupera dados é CE; se houver cálculo, derivação ou atualização de ALI, passa a ser SE (ou EE, se a finalidade principal for manter dados).|

Complexidade

As regras de negócio influenciam indiretamente os contadores:

TD (tipos de dados): campos extras exigidos por uma regra (ex.: campo “justificativa de desconto”).
ALR/AR (arquivos referenciados): arquivos que a regra precisa consultar ou atualizar (ex.: validar contra a tabela de limites de crédito).
3. Separação ou unificação de processos elementares

Se a regra muda a lógica de processamento ou os arquivos referenciados, os processos passam a ser distintos. 
Por exemplo, “incluir pedido comum” e “incluir pedido com aprovação gerencial” podem ser dois PEs se tiverem lógica e arquivos diferentes.

O que NÃO gera ponto de função
Regras que são só detalhes de implementação (ex.: “usar índice no banco”).
Mensagens de erro e validações individuais, que fazem parte do mesmo PE.
Regras de requisitos não funcionais (ex.: “resposta em até 2 segundos”).
Dica prática na contagem

Ao analisar o requisito, procure as regras de negócio com estas perguntas:

A regra altera dados em algum ALI? (indica EE ou SE)
A regra exige cálculo ou derivação? (indica SE)
A regra consulta outro arquivo? (aumenta ALR e pode elevar a complexidade)
A regra cria um fluxo diferente com lógica própria? (pode indicar outro PE)
Erros comuns
Contar cada regra de negócio como uma função separada.
Ignorar regras de cálculo e classificar como CE uma consulta que na verdade é SE.
Esquecer de incluir campos e arquivos exigidos pelas regras na análise de TD e ALR.
