### 1. Relacionamento e Associação de Objetos
Analisando a chave estrangeira `FK_Tarefa_Funcionario`, onde a tabela `Tarefa` possui a coluna `FuncionarioId` apontando para a tabela `Funcionario`, como essa relação de **1 para N (1:N)** é representada em C# nas classes de modelo?

- [ ] **A)** A classe `Funcionario` possui uma propriedade `public Tarefa Tarefa { get; set; }` e a classe `Tarefa` possui uma propriedade `public List<Funcionario> Funcionarios { get; set; }`.
- [ ] **B)** A classe `Funcionario` possui uma propriedade de navegação `public virtual ICollection<Tarefa> Tarefas { get; set; }` e a classe `Tarefa` possui a propriedade de navegação `public virtual Funcionario Funcionario { get; set; }`.
- [ ] **C)** Ambas as classes precisam apenas de propriedades do tipo `int` representando os IDs, sem utilizar propriedades de navegação de objetos.
- [ ] **D)** O Entity Framework Core cria automaticamente uma terceira classe chamada `FuncionarioTarefa` para gerenciar a associação.

---

### 2. Encapsulamento e Propriedades
No código C# gerado pelo EF Core Power Tools, as colunas das tabelas do SQL Server são mapeadas utilizando o conceito de **Propriedades (Getters e Setters)**. Qual é a principal finalidade do **Encapsulamento** ao utilizar propriedades em C# em vez de atributos/campos públicos (`public string Nome;`)?

- [ ] **A)** Permitir controlar o acesso e a validação dos dados de um objeto, podendo aplicar regras de negócio na leitura ou escrita sem expor os campos privados diretamente.
- [ ] **B)** Impedir que o banco de dados armazene valores do tipo texto (`string` ou `VARCHAR`).
- [ ] **C)** Garantir que todas as propriedades sejam obrigatoriamente estáticas (`static`).
- [ ] **D)** Aumentar a velocidade de execução do banco de dados SQL Server.

---

### 3. Abstração e Tipos Nulos (Nullable Types)
No script SQL fornecido, as colunas `DataIniciada`, `DataFinalizada` e `DataCancelada` da tabela `Tarefa` foram criadas como `DATETIME NULL`. Como o C# representa essa abstração do banco de dados para permitir que uma data seja opcional (ou nula) no objeto?

- [ ] **A)** Utilizando o tipo `DateTime` padrão, pois ele aceita valores nulos por padrão em C#.
- [ ] **B)** Utilizando o tipo `string`, convertendo a data para texto quando ela for nula.
- [ ] **C)** Utilizando o tipo de dado anotado com *Nullable*: `DateTime?` ou `Nullable<DateTime>`.
- [ ] **D)** O C# lança uma exceção de compilação caso tente mapear colunas do tipo `NULL`.

---

### 4. O Papel do DbContext (Abstração e Herança)
A classe `dbTasksContext` herda da classe base `DbContext` do Entity Framework Core. Nesse contexto de POO, qual é o papel principal da classe `dbTasksContext`?

- [ ] **A)** Ela representa a interface gráfica (HTML/Razor) onde o usuário interage na aplicação.
- [ ] **B)** Ela funciona como uma representação (abstração) da sessão com o banco de dados, exposta através de propriedades `DbSet<T>` que permitem realizar operações de CRUD em coleções de objetos.
- [ ] **C)** Ela é responsável por compilar o código em linguagem de máquina para o servidor.
- [ ] **D)** Ela substitui a necessidade de criar a camada de *Controllers* no padrão MVC.

---
