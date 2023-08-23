Sistema de Controle de Despesas - Descrição Detalhada

O Sistema de Controle de Despesas é uma aplicação que permite aos usuários gerenciar suas despesas e pagamentos de forma organizada. Através de uma interface textual, o usuário pode interagir com várias funcionalidades oferecidas pelo sistema para gerenciar suas finanças pessoais.

Classes:

Despesa (Classe Abstrata):

A classe abstrata Despesa é a base para todos os tipos de despesas. Ela contém atributos como descricao, valor, dataVencimento e paga. Essa classe também possui métodos como pagar (para marcar uma despesa como paga), listarDetalhes (para exibir informações da despesa) e getCategoria (um método abstrato para obter a categoria da despesa).
Alimentacao e Transporte (Subclasses de Despesa):

Alimentacao e Transporte são subclasses da classe Despesa. Elas herdam atributos e métodos da classe base e implementam o método abstrato getCategoria. Cada uma delas representa uma categoria específica de despesa (alimentação e transporte, respectivamente).
Pagavel (Interface):

A interface Pagavel define o contrato para objetos que podem ser pagos. Ela exige a implementação do método anotarPagamento, que permite registrar um pagamento para uma despesa pendente.
Usuario:

A classe Usuario representa os usuários do sistema. Cada usuário tem um login e uma senha. A classe possui métodos como verificarSenha (para comparar senhas) e um construtor para criar novos usuários.
GerenciadorDespesas:

A classe GerenciadorDespesas é responsável por gerenciar as despesas registradas no sistema. Ela mantém uma lista de despesas, permitindo adicionar novas despesas através do método adicionarDespesa e listar todas as despesas através do método listarDespesas.
TipoDespesa:

A classe TipoDespesa é utilizada para criar categorias de despesa. Ela possui um atributo nome que define o tipo de categoria. Essa classe é utilizada no gerenciamento de tipos de despesa.
Métodos e Atributos:

Construtores Sobrecarregados:

As classes Alimentacao e Transporte possuem construtores sobrecarregados que permitem criar instâncias dessas classes com diferentes detalhes, como descrição, valor e data de vencimento.
Anotar Pagamento:

A interface Pagavel define o método anotarPagamento, que é implementado na classe Transporte. Ele permite ao usuário registrar o pagamento de uma despesa pendente, marcando-a como paga.
Listagem de Despesas por Período:

O método listarDespesasPorPeriodo recebe uma lista de despesas e um intervalo de datas. Ele filtra e retorna apenas as despesas que se encaixam no período especificado.
Listagem de Despesas Pagas e em Aberto por Período:

Os métodos listarDespesasPagasNoPeriodo e listarDespesasEmAbertoNoPeriodo funcionam de maneira semelhante ao método anterior, mas apenas retornam despesas pagas ou em aberto dentro do período especificado.
Gerenciamento de Tipos de Despesa:

A classe TipoDespesa possui um atributo nome que define o tipo de despesa. Isso ajuda na organização e classificação das despesas.
Gerenciamento de Usuários:

A classe Usuario permite cadastrar, verificar senhas e autenticar usuários no sistema. Ela também simula a criptografia de senhas para manter a segurança.
Considerações Finais:

O Sistema de Controle de Despesas permite ao usuário adicionar despesas, listar, filtrar e marcar pagamentos. A implementação utiliza conceitos de herança, interfaces e polimorfismo para criar uma estrutura modular e reutilizável. Cada funcionalidade é representada por classes e métodos específicos, garantindo a organização e a eficácia do sistema. No entanto, é importante lembrar que este é apenas um exemplo básico, e um sistema real requer considerações adicionais, como segurança, usabilidade e persistência de dados.
