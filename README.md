[README.md](https://github.com/user-attachments/files/34107578/README.md)
# Verde Encanto — E-commerce ASP.NET Core MVC

Projeto criado a partir da base de e-commerce ASP.NET Core MVC fornecida pelo professor. A solução preserva a estrutura MVC, os modelos, os controladores, o Entity Framework Core e o SQL Server, com a identidade visual Verde Encanto baseada nas referências enviadas.

## Requisitos
- .NET 9 SDK (o projeto original usa `net9.0`)
- Visual Studio 2022 atualizado com a carga de trabalho **Desenvolvimento ASP.NET e Web**; ou Visual Studio Code com as extensões **C# Dev Kit** e **C#**
- SQL Server LocalDB (instalado normalmente junto da carga de trabalho do Visual Studio) ou outra instância SQL Server

## Abrir no Visual Studio
1. Extraia o ZIP para uma pasta normal, por exemplo `C:\Projetos\VerdeEncanto`.
2. Abra `Esse_deu_certo_MVC_Exemplo.sln`.
3. Aguarde a restauração dos pacotes NuGet.
4. Execute com `F5` ou `Ctrl+F5`.

## Abrir no Visual Studio Code
1. Extraia o ZIP e abra a pasta `EcommerceCrudAspNetCoreMVC-main` no VS Code.
2. No terminal integrado, execute:

```powershell
dotnet restore
dotnet run --project Esse_deu_certo_MVC_Exemplo.csproj
```

3. Abra a URL `http://localhost:5079` (ou a URL exibida no terminal).

## Banco de dados
O projeto usa SQL Server LocalDB por padrão, configurado em `appsettings.json`. Na primeira execução, as migrations são aplicadas e o catálogo demonstração é cadastrado. Se não tiver LocalDB, altere `ConnectionStrings:DefaultConnection` para a sua instância SQL Server.

## Primeiro acesso administrativo
Defina credenciais no terminal antes de iniciar a aplicação. Exemplo PowerShell:

```powershell
$env:Admin__Email = "admin@verdeencanto.local"
$env:Admin__Senha = "Troque-Por-Uma-Senha-Forte"
dotnet run --project Esse_deu_certo_MVC_Exemplo.csproj
```

A aplicação cria o administrador apenas se esse e-mail ainda não existir. Não há senha administrativa fixa no código.

## Funcionalidades
- Página inicial responsiva e carrossel “Nossa História” com setas, indicadores e gesto de deslizar no celular.
- Busca de produtos no cabeçalho, catálogo com busca/filtros/ordenação e páginas de detalhes.
- Favoritos salvos no navegador e alternância de tema claro/escuro.
- Carrinho: adicionar, atualizar quantidade, remover item, limpar carrinho e consultar total.
- Cadastro, login, sessão, edição de perfil e histórico de pedidos.
- Checkout demonstrativo, registro de pedido, atualização de estoque e comprovante PDF.
- Painel administrativo, gestão de produtos, categorias e usuários.
- Links de localização que abrem a busca do endereço no Google Maps.

## Observações importantes
- Os valores, descrições e estoques do catálogo são dados demonstrativos; revise antes de usar.
- As imagens SVG locais são ilustrações de demonstração, não fotografias oficiais dos produtos.
- O checkout não realiza cobrança real nem se conecta a gateway de pagamento. Pix, boleto e cartão são apenas opções demonstrativas registradas no pedido.
- E-mail de confirmação é opcional e exige configuração SMTP por variáveis de ambiente.
- Este ambiente de criação não possui SDK .NET/SQL Server instalado, então não foi possível executar `dotnet build` ou validar a conexão com o banco aqui. A estrutura e os arquivos foram revisados, mas faça a primeira execução no Visual Studio/VS Code e confira o terminal caso o LocalDB ou algum pacote não esteja disponível.

## Solução para erro de conexão com SQL Server (Named Pipes Provider, error: 40)

O projeto está configurado para usar `Server=(localdb)\\MSSQLLocalDB`, que exige o SQL Server Express LocalDB no Windows. O erro `SQL Server was not found or was not accessible` significa que essa instância não está instalada/iniciada ou que a conexão está configurada para outra instância. `EnableRetryOnFailure` ajuda em falhas transitórias, mas não instala nem substitui o SQL Server.

### Opção A — instalar LocalDB (recomendado para esta base)
1. Abra o **Visual Studio Installer**.
2. Clique em **Modificar** na sua instalação do Visual Studio.
3. Em **Componentes individuais**, procure e marque **SQL Server Express 2022 LocalDB** (ou o componente LocalDB disponível).
4. Aplique a instalação e reinicie o Visual Studio.
5. Abra o projeto e execute novamente.

Para verificar no Prompt de Comando, execute `sqllocaldb info`. Se o comando não for reconhecido, o LocalDB não está instalado ou não está no PATH. Se a instância existir, execute `sqllocaldb start MSSQLLocalDB`.

### Opção B — usar outra instância SQL Server
Edite `ConnectionStrings:DefaultConnection` em `appsettings.json` para apontar ao nome real da sua instância. Não altere para um nome de servidor fictício.

O aviso sobre `Venda.ValorTotal` também foi corrigido no modelo com precisão `18,2`. A aplicação ainda precisa de uma instância SQL Server acessível para criar/aplicar as migrations e salvar produtos, usuários e pedidos.
