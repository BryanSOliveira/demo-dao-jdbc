# Data Access Object (DAO)

O padrão Data Access Object (DAO) é um conceito de design amplamente utilizado na programação para promover uma separação clara entre a lógica de negócios e o acesso aos dados em uma aplicação. O principal objetivo do padrão DAO é fornecer uma camada de abstração que isola o código de acesso a dados, permitindo que a lógica do programa interaja com os dados de maneira eficiente e desacoplada.

## Vantagens do Padrão DAO

- **Separação de Responsabilidades:** O DAO divide a lógica de acesso a dados da lógica de negócios, melhorando a organização do código e a manutenibilidade.
- **Reutilização de Código:** Com as operações de acesso a dados encapsuladas em classes DAO, é mais fácil reutilizar esse código em diferentes partes do sistema.
- **Facilita Mudanças:** Se houver alterações na camada de dados (por exemplo, mudança de banco de dados), apenas a implementação do DAO precisa ser modificada, sem afetar o restante do código.

## Componentes Principais do Padrão DAO

1. **Interface DAO:** Define um conjunto de métodos abstratos que representam as operações de acesso a dados relacionadas a uma entidade específica (por exemplo, Cliente, Pedido, Produto).
2. **Classe DAO de Implementação:** Fornece a implementação real dos métodos definidos na interface DAO. Essa classe é responsável por interagir com a fonte de dados (como um banco de dados) para realizar as operações CRUD (Criar, Ler, Atualizar, Excluir) necessárias.
3. **Entidades:** Representam os objetos de dados que estão sendo armazenados. As classes de entidade contêm os atributos e métodos relacionados aos dados em si.
4. **Lógica de Negócios:** Esta camada interage com os DAOs para executar operações de acesso a dados sem a necessidade de conhecer os detalhes de implementação do banco de dados.

## Exemplo de Uso

Suponha que temos uma aplicação de gerenciamento de livros. Usando o padrão DAO, teríamos:
- **`LivroDAO`:** Interface que define os métodos como `buscarPorId(int id)`, `buscarTodos()`, `inserir(Livro livro)`, `atualizar(Livro livro)`, `excluir(int id)`.
- **`LivroDAOImpl`:** Classe que implementa os métodos da interface `LivroDAO` e lida com o acesso aos dados reais do livro (por exemplo, armazenados em um banco de dados).

## Conclusão

O padrão DAO é uma abordagem valiosa para separar as preocupações de acesso a dados e lógica de negócios. Ele promove uma estrutura organizada, facilita a manutenção do código e permite a reutilização eficiente do código de acesso a dados em várias partes da aplicação. A utilização do padrão DAO é particularmente vantajosa em aplicativos complexos ou que possam evoluir com o tempo.
