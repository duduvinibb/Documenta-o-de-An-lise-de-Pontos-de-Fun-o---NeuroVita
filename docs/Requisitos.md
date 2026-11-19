Na Análise de Pontos de Função, o ponto de partida são os requisitos funcionais do usuário: 
o que o software deve fazer para atender às necessidades de negócio. 
A contagem mede só isso. Os requisitos não funcionais (desempenho, segurança, usabilidade, tecnologia)
não entram diretamente nos pontos, 
embora possam influenciar o esforço.

Os requisitos funcionais são decompostos em dois grupos:

Dados: informações que o sistema precisa armazenar ou referenciar arquivos (ALI e AIE).
Transações: o que o usuário faz com essas informações (EE, SE e CE).

Processo elementar

O processo elementar (PE) é a menor unidade de atividade com significado para o usuário. Ele é a base de toda função transacional: cada EE, SE ou CE corresponde a um processo elementar.

Para ser considerado um PE, ele precisa cumprir três critérios:

- Significativo para o usuário: faz sentido do ponto de vista do negócio, não só técnico.
- Completo: é uma transação inteira, que deixa o negócio em estado consistente.
- Autocontido: termina por si só, sem depender de outra etapa para estar concluído.

 Regra de unicidade

Dois processos elementares são o mesmo (contados uma só vez) se tiverem os mesmos TDs, os mesmos arquivos referenciados e a mesma lógica de processamento. Se algum desses elementos for diferente, são PEs distintos.

Exemplo clássico: em um CRUD, incluir, alterar, excluir e consultar são quatro processos elementares distintos (três EEs e uma CE), não um só “cadastro de cliente”.

Erros comuns:
- Contar telas em vez de processos (uma tela pode conter vários PEs, ou um PE pode usar várias telas).
- Contar etapas técnicas (validação, gravação, confirmação) como PEs separados.
- Esquecer que relatórios e consultas também são PEs.
- Dividir um PE em vários só porque ele tem mensagens de erro ou confirmações (essas fazem parte do mesmo PE).

Se quiser, posso montar um exemplo prático de identificação de processos elementares a partir de um mini-requisito, como um cadastro de clientes.
