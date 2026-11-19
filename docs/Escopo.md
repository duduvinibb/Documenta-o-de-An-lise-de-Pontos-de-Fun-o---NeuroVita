O escopo da contagem define quais funcionalidades serão incluídas na medição. 
Ele responde à pergunta: “o que exatamente estou contando?”. 
Um escopo mal definido gera contagens inconsistentes e difíceis de auditar.

#Tipo de contagem

O primeiro passo é definir o tipo de contagem, que determina o escopo:

#Tipos e O que mede:

Projeto de desenvolvimento: Todas as funções entregues na primeira versão do software

Projeto de melhoria: Funções incluídas, alteradas ou excluídas em uma aplicação existente, mais as funções de conversão de dados

Aplicação: Todas as funções que a aplicação oferece hoje (o “tamanho instalado”)

Fronteira da aplicação

A fronteira é a linha conceitual que separa o software medido do usuário e de outras aplicações.

O que está dentro da fronteira: dados mantidos pela aplicação (ALI) e processos que ela executa.
O que está fora: o usuário e os sistemas externos. Dados mantidos por esses sistemas, mas lidos pela sua aplicação, são AIE.

A fronteira é definida pela visão do usuário e pelo negócio, não pela tecnologia, plataforma ou arquitetura física (servidores, camadas, módulos de código).

Exemplo: um sistema de vendas que consulta o cadastro de clientes mantido pelo sistema de CRM. O cadastro de clientes está fora da fronteira de vendas e é contado como AIE.

Escopo x fronteira
Escopo: o conjunto de funções que serão medidas nesta contagem (pode ser só um módulo, uma sprint ou um projeto).
Fronteira: a divisão entre sistemas, que existe independentemente de qual parte você decidiu contar.

Em uma melhoria, por exemplo, o escopo é só o que mudou, mas a fronteira continua sendo a da aplicação inteira.

O que registrar na definição do escopo:

Propósito da contagem: estimativa, medição de contrato, benchmark, etc.
Tipo de contagem (desenvolvimento, melhoria ou aplicação).
Fronteira da aplicação e sistemas vizinhos.
Funcionalidades incluídas e excluídas.
Documentação base: requisitos, protótipos, modelo de dados, versão.
Método e versão do manual: IFPUG CPM, NESMA, Roteiro SISP.
Premissas e restrições assumidas

Erros comuns: 

Definir a fronteira por módulos técnicos ou equipes, e não pela visão do negócio.
Misturar tipos de contagem (ex.: contar funções existentes dentro de um projeto de melhoria sem mudança).
Não documentar o que ficou de fora do escopo.
Incluir requisitos não funcionais ou atividades como testes, treinamento e gerência de projeto, que não geram pontos de função.
