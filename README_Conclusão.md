# 🤖 Mega Man Robots API

```{=html}
<p align="center">
```
`<img src="./_docs/assets/icon.png" alt="Mega Man Robots API" width="150"/>`{=html}
```{=html}
</p>
```
```{=html}
<p align="center">
```
`<b>`{=html}API REST em .NET Core para consulta de robôs da série Mega
Man`</b>`{=html}`<br/>`{=html}
`<sub>`{=html}`<sup>`{=html}(MEGA-MAN-ROBOTS)`</sup>`{=html}`</sub>`{=html}
```{=html}
</p>
```
```{=html}
<p align="center">
```
`<a href="https://github.com/felipeAguiarCode/MegaApiDotnetCore/actions/workflows/build.yml">`{=html}
`<img src="https://github.com/felipeAguiarCode/MegaApiDotnetCore/actions/workflows/build.yml/badge.svg" alt="Build Status"/>`{=html}
`</a>`{=html}
`<a href="https://github.com/felipeAguiarCode/MegaApiDotnetCore/releases/latest">`{=html}
`<img src="https://img.shields.io/github/v/release/felipeAguiarCode/MegaApiDotnetCore" alt="Latest Release"/>`{=html}
`</a>`{=html}
```{=html}
</p>
```

------------------------------------------------------------------------

## 📌 Sobre o Projeto

Este projeto é uma **API RESTful** desenvolvida em **.NET Core 3.1**,
com foco em documentar e disponibilizar informações de chefes (robôs) da
série **Mega Man**.

### 🎯 Objetivos do Desafio

-   Construir uma API robusta e escalável.\
-   Aplicar **boas práticas de arquitetura** com Entity Framework Core,
    injeção de dependências e REST.\
-   Documentar todas as etapas como parte de um **desafio de
    documentação de projetos automáticos**.

### ✅ Conclusão

A API foi implementada com sucesso, oferecendo endpoints para consulta,
criação e detalhamento de robôs.\
O desafio demonstrou a importância de **documentação clara** e
**automação de processos**, servindo como modelo para futuros projetos.

------------------------------------------------------------------------

## 🚀 Instalação e Execução

### Pré-requisitos

-   [.NET Core SDK
    3.1+](https://dotnet.microsoft.com/download/dotnet/3.1)\
-   [SQL Server](https://www.microsoft.com/sql-server) ou outro banco
    compatível

### Passos

``` bash
# Clonar o repositório
git clone https://github.com/felipeAguiarCode/MegaApiDotnetCore.git

# Entrar na pasta
cd MegaApiDotnetCore

# Restaurar dependências
dotnet restore

# Rodar a aplicação
dotnet run
```

### Configuração de Banco

Edite o arquivo **appsettings.json** conforme necessário:

``` json
"ConnectionStrings": {
  "dev_ambient": "Server=localhost;Initial Catalog=dbMegamanApi;User ID=userapi;Password=SudoPass123;"
}
```

------------------------------------------------------------------------

## 📡 Endpoints Disponíveis

  Método   Endpoint                Descrição
  -------- ----------------------- ------------------------------------
  GET      `/api/v1/robots`        Lista todos os robôs
  GET      `/api/v1/robots/{id}`   Retorna detalhes de um robô por ID
  POST     `/api/v1/robots`        Cria um novo registro de robô

------------------------------------------------------------------------

## 🛠️ Exemplos de Uso

``` bash
# Listar robôs
curl http://localhost:5000/api/v1/robots

# Buscar robô por ID
curl http://localhost:5000/api/v1/robots/1

# Criar robô
curl -X POST http://localhost:5000/api/v1/robots -H "Content-Type: application/json" -d '{
  "name": "Cut Man",
  "game": "Mega Man",
  "weakness": "Super Arm"
}'
```

------------------------------------------------------------------------

## 🏗️ Arquitetura do Projeto

    src
    ├── 📂 Controllers      [Rotas da API]
    ├── 📂 Models           [Modelos do banco de dados]
    ├── 📂 Services         [Regras de negócio]
    ├── 📂 Middlewares      [Interceptadores de requisições/respostas]
    ├── 📂 Database         [Estruturas relacionadas ao banco]
    │   ├── 📂 DTOs             [Modelos de entrada/saída (Data Transfer Objects)]
    │   ├── 📂 EntityFramework  [Configurações do ORM Entity Framework]
    │   │     ├── 📂 Context         [Configuração do contexto]
    │   │     ├── 📂 Migrations      [Migrações do banco]
    │   ├── 📂 Repositories     [Padrão de repositórios]

------------------------------------------------------------------------

## 📦 Dependências

  ------------------------------------------------------------------------------------------------------------------------------------------------------
  Pacote                                              Versão     Link
  --------------------------------------------------- ---------- ---------------------------------------------------------------------------------------
  Microsoft.EntityFrameworkCore                       3.1.8      [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/3.1.8)

  Microsoft.EntityFrameworkCore.Design                3.1.8      [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/3.1.8)

  Microsoft.EntityFrameworkCore.SqlServer             3.1.8      [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/3.1.8)

  Newtonsoft.Json                                     12.0.2     [NuGet](https://www.nuget.org/packages/Newtonsoft.Json/12.0.2)
  ------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 🤖 Automação e Documentação

-   Integração contínua via **GitHub Actions** (badge de build
    incluso).\
-   Pipeline configurado para compilar e rodar testes automaticamente.\
-   Possível integração com **Swagger/OpenAPI** para documentação
    interativa.

------------------------------------------------------------------------

## 📌 Conclusão e Próximos Passos

Este projeto reforçou a importância da **documentação em projetos
automáticos**, mostrando como boas práticas de arquitetura, clareza de
endpoints e instruções de execução tornam o sistema mais acessível.

🔮 **Próximos passos**:\
- Adicionar autenticação e autorização.\
- Implementar cache e paginação.\
- Expandir para incluir mais dados da franquia Mega Man.\
- Publicar a API em ambiente cloud para uso público.

------------------------------------------------------------------------

## 📜 Licença

Este software é licenciado sob os termos da [MIT License](./LICENSE).

------------------------------------------------------------------------

⌨️ Desenvolvido por **Felipe Aguiar** -
[Github](https://github.com/felipeAguiarCode)
