# Sistema de Gerenciamento de Biblioteca

Este projeto visa criar um sistema de gerenciamento de biblioteca usando um banco de dados SQL. O objetivo é organizar e acompanhar os livros, autores e empréstimos na biblioteca local.

## Estrutura do Banco de Dados

O banco de dados chamado **Biblioteca** é composto pelas seguintes tabelas:

### Tabela `Autores`
- **ID**: INT, Primary Key, Auto Increment
- **Nome**: VARCHAR(100)
- **Idade**: INT
- **Nacionalidade**: VARCHAR(100)

### Tabela `Livros`
- **LivroID**: INT, Primary Key, Auto Increment
- **Título**: VARCHAR(255)
- **AutorID**: INT, Foreign Key (referência ao autor)
- **AnoPublicacao**: INT
- **Gênero**: VARCHAR(100)

### Tabela `Empréstimos`
- **EmprestimoID**: INT, Primary Key, Auto Increment
- **LivroID**: INT, Foreign Key (referência ao livro)
- **DataEmprestimo**: DATE
- **DataDevolucao**: DATE (pode ser nulo)
- **NomeUsuario**: VARCHAR(100)

## Requisitos

1. **Criação do Banco de Dados**:
   - Crie um banco de dados chamado **Biblioteca**.

2. **Criação das Tabelas**:
   - Crie as tabelas `Autores`, `Livros` e `Empréstimos` conforme as descrições acima.

3. **Manipulação de Dados**:
   - **Inserir Dados**: Adicione pelo menos 5 autores, 10 livros e 5 registros de empréstimos.
   - **Consultar Dados**: 
     - Listar todos os livros junto com o nome do autor e o ano de publicação.
     - Mostrar todos os empréstimos que ainda não foram devolvidos.
   - **Atualizar Dados**: Atualize a data de devolução de um empréstimo específico.
   - **Deletar Dados**: Exclua um livro e todos os registros relacionados a ele dos empréstimos.

4. **Consultas Avançadas**:
   - Gere um relatório que mostre o número de livros emprestados por cada autor.
   - Liste os livros que foram emprestados mais de uma vez.

## Instalação e Execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
