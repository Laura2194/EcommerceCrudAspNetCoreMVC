# 🌿 Verde Encanto – E-commerce de Cosméticos Naturais (ASP.NET Core MVC) | 🌿 Natural Cosmetics E-commerce

# 📘 Sobre o Projeto | About the Project

**PT-BR 🇧🇷** O Verde Encanto é um projeto acadêmico de E-commerce desenvolvido com ASP.NET Core MVC e C#, voltado à comercialização de cosméticos naturais. O sistema foi desenvolvido com finalidade educacional, buscando aplicar na prática conceitos de desenvolvimento web, arquitetura MVC, persistência de dados e funcionalidades comuns em lojas virtuais. A aplicação reúne recursos de navegação pelo catálogo de produtos, carrinho de compras, finalização de pedidos, cadastro e autenticação de usuários, além de funcionalidades administrativas.

**EN 🇺🇸** Verde Encanto is an academic e-commerce project developed with ASP.NET Core MVC and C#, focused on the sale of natural cosmetics. The system was created for educational purposes, aiming to apply web development concepts, MVC architecture, data persistence, and common e-commerce functionalities. The application includes product catalog browsing, a shopping cart, order checkout, user registration and authentication, and administrative features.

# 🎯 Objetivos Educacionais | Educational Goals

**PT-BR 🇧🇷**
- Compreender o fluxo de dados em uma aplicação web.
- Aplicar o padrão MVC (Model-View-Controller).
- Desenvolver funcionalidades de catálogo e gerenciamento de produtos.
- Implementar carrinho de compras e fluxo de finalização de pedidos.
- Utilizar Entity Framework Core com abordagem Code First e Migrations.
- Trabalhar com banco de dados relacional SQL Server.
- Aplicar conceitos básicos de autenticação e gerenciamento de sessões.
- Desenvolver interfaces web com Razor, HTML, CSS e JavaScript.

**EN 🇺🇸**
- Understand data flow in a web application.
- Apply the MVC (Model-View-Controller) pattern.
- Develop product catalog and management features.
- Implement a shopping cart and order checkout workflow.
- Use Entity Framework Core with the Code First approach and Migrations.
- Work with a SQL Server relational database.
- Apply basic authentication and session management concepts.
- Develop web interfaces using Razor, HTML, CSS, and JavaScript.

# 🧱 Arquitetura | Architecture

**PT-BR 🇧🇷** O projeto segue o padrão arquitetural MVC, organizado nas seguintes áreas:

- **Models:** entidades e estruturas de dados do sistema.
- **Controllers:** controle do fluxo da aplicação e implementação das regras de negócio.
- **Views:** interfaces com o usuário utilizando Razor.
- **Data:** contexto do banco de dados e gerenciamento de Migrations.
- **Helpers:** funcionalidades auxiliares utilizadas pela aplicação.

**EN 🇺🇸** The project follows the MVC architectural pattern and is organized into the following areas:

- **Models:** system entities and data structures.
- **Controllers:** application flow control and business logic.
- **Views:** user interfaces built with Razor.
- **Data:** database context and migration management.
- **Helpers:** auxiliary application functionality.

# 🧩 Funcionalidades | Features

### 🛍️ Catálogo de Produtos | Product Catalog
- Visualização dos produtos disponíveis.
- Exibição de informações e detalhes dos produtos.
- Organização e navegação pelo catálogo.

### 🛒 Carrinho de Compras | Shopping Cart
- Adição de produtos ao carrinho.
- Visualização e gerenciamento dos itens selecionados.
- Preparação dos itens para finalização do pedido.

### 📦 Pedidos | Orders
- Fluxo de finalização de pedidos.
- Registro das informações da compra.
- Consulta ao histórico de pedidos do usuário.

### 👤 Usuários | Users
- Cadastro de usuários.
- Login e autenticação.
- Gerenciamento de informações do perfil.
- Consulta ao histórico de compras.

### ⚙️ Administração | Administration
- Funcionalidades administrativas para gerenciamento da loja.
- Controle básico de acesso às funcionalidades administrativas.

### ❤️ Favoritos e Personalização | Favorites and Customization
- Recursos de favoritos.
- Opção de personalização visual da interface.

# 🛠️ Tecnologias Utilizadas | Technologies Used

- C#
- ASP.NET Core MVC
- .NET 9
- Entity Framework Core
- SQL Server LocalDB
- Razor Views
- HTML5
- CSS3
- JavaScript
- Bootstrap
- jQuery

# 🗄️ Banco de Dados | Database

**PT-BR 🇧🇷** O projeto utiliza Entity Framework Core com a abordagem Code First, permitindo gerenciar a estrutura do banco de dados por meio de Migrations. A aplicação está configurada para utilizar o SQL Server LocalDB em ambiente de desenvolvimento. A inicialização do sistema executa as Migrations para criar ou atualizar a estrutura do banco e, em seguida, realiza a inicialização do catálogo de produtos.

**EN 🇺🇸** The project uses Entity Framework Core with the Code First approach, allowing the database schema to be managed through Migrations. The application is configured to use SQL Server LocalDB in the development environment. During startup, the application runs the Migrations to create or update the database schema and then initializes the product catalog.

# 🚀 Como Executar o Projeto | How to Run the Project

**PT-BR 🇧🇷**

1. Instale o SDK do .NET 9.
2. Instale e configure o SQL Server Express LocalDB.
3. Abra a pasta do projeto no Visual Studio ou no Visual Studio Code.
4. Confira a string de conexão `DefaultConnection` no arquivo `appsettings.json`.
5. Abra o terminal na pasta que contém o arquivo `.csproj`.
6. Execute os comandos:

```bash
dotnet restore
dotnet run
```

7. Acesse no navegador o endereço local exibido no terminal.

**EN 🇺🇸**

1. Install the .NET 9 SDK.
2. Install and configure SQL Server Express LocalDB.
3. Open the project folder in Visual Studio or Visual Studio Code.
4. Check the `DefaultConnection` connection string in `appsettings.json`.
5. Open a terminal in the folder containing the `.csproj` file.
6. Run the following commands:

```bash
dotnet restore
dotnet run
```

7. Open the local address displayed in the terminal in your browser.

**Observação | Note:** A execução depende de uma conexão funcional com o SQL Server LocalDB. Se ocorrer um erro de conexão durante a inicialização, verifique se a instância está em execução e se a configuração do banco está correta.

# 👨‍🏫 Contexto Acadêmico | Academic Context

**PT-BR 🇧🇷** O Verde Encanto foi desenvolvido como projeto acadêmico para aplicar conhecimentos de desenvolvimento de sistemas e demonstrar, na prática, a estrutura e o funcionamento de uma aplicação de E-commerce. O projeto permite estudar arquitetura MVC, persistência de dados, gerenciamento de usuários e implementação de funcionalidades comuns em uma loja virtual.

**EN 🇺🇸** Verde Encanto was developed as an academic project to apply systems development knowledge and demonstrate the structure and operation of an e-commerce application. It provides a practical opportunity to study MVC architecture, data persistence, user management, and common online store functionalities.

# 🚀 Possíveis Evoluções | Possible Improvements

**PT-BR 🇧🇷**
- Implementação do ASP.NET Core Identity.
- Criação de uma camada de serviços (Service Layer).
- Utilização de ViewModels e DTOs.
- Implementação de filtros, pesquisa e paginação.
- Integração com gateways de pagamento.
- Desenvolvimento de uma API REST.
- Implementação de testes automatizados.
- Melhorias na segurança e no controle de acesso.
- Aprimoramento da compatibilidade dos pacotes utilizados com o .NET 9.

**EN 🇺🇸**
- Implementation of ASP.NET Core Identity.
- Creation of a Service Layer.
- Use of ViewModels and DTOs.
- Implementation of filters, search, and pagination.
- Integration with payment gateways.
- Development of a REST API.
- Implementation of automated tests.
- Improvements to security and access control.
- Better compatibility between the packages used and .NET 9.

# 📄 Licença | License

**PT-BR 🇧🇷** Projeto de uso exclusivamente educacional.

**EN 🇺🇸** Project intended exclusively for educational purposes.

# 👨‍💻 Autor | Author

**Verde Encanto — Projeto Acadêmico de E-commerce**

Desenvolvido para fins educacionais, com foco em desenvolvimento web utilizando ASP.NET Core MVC e C#.
