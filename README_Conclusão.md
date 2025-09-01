<p align="center">
  <img src="./_docs/assets/icon.png" alt="Mega Man Robots API" width="150"/>
</p>

<p align="center-justify">
  <h1>API REST em .NET Core para consulta de robôs da série Mega Man</h1><br/>
 </p>
 <p align="center">
  <b><sup>(MEGA-MAN-ROBOTS)</sup></b>
</p>

 <p align="center">
  </a>
  <a href="https://github.com/felipeAguiarCode/MegaApiDotnetCore/releases/latest">
    <img src="https://img.shields.io/github/v/release/felipeAguiarCode/MegaApiDotnetCore" alt="Latest Release"/>
  </a>
</p>

---

## 📌 Sobre o Projeto

O **Mega Man Robots API** é uma **API RESTful** desenvolvida em **.NET Core 3.1**, criada para documentar e disponibilizar informações sobre os chefes (robôs) da clássica franquia **Mega Man**.

### 🎯 Objetivos

- Criar uma API **robusta, escalável e bem estruturada**  
- Aplicar **boas práticas de arquitetura**: Entity Framework Core, injeção de dependências e REST  
- Servir como **exemplo de documentação e automação de projetos**  

---

## 🚀 Instalação e Execução

### ✅ Pré-requisitos
- [.NET Core SDK 3.1+](https://dotnet.microsoft.com/download/dotnet/3.1)  
- [SQL Server](https://www.microsoft.com/sql-server) ou outro banco compatível  

### ▶️ Passos

```bash
# Clonar o repositório
git clone https://github.com/felipeAguiarCode/MegaApiDotnetCore.git

# Entrar na pasta
cd MegaApiDotnetCore

# Restaurar dependências
dotnet restore

# Rodar a aplicação
dotnet run
```

### ⚙️ Configuração do Banco

Edite o arquivo **appsettings.json** com sua conexão:

```json
"ConnectionStrings": {
  "dev_ambient": "Server=localhost;Initial Catalog=dbMegamanApi;User ID=userapi;Password=SudoPass123;"
}
```

---

## 📡 Endpoints

| Método | Endpoint              | Descrição                        |
|--------|----------------------|----------------------------------|
| GET    | `/api/v1/robots`     | Lista todos os robôs             |
| GET    | `/api/v1/robots/{id}`| Retorna detalhes de um robô por ID |
| POST   | `/api/v1/robots`     | Cria um novo registro de robô    |

---

## 🛠️ Exemplos de Uso

```bash
# Listar robôs
curl http://localhost:5000/api/v1/robots

# Buscar robô por ID
curl http://localhost:5000/api/v1/robots/1

# Criar robô
curl -X POST http://localhost:5000/api/v1/robots   -H "Content-Type: application/json"   -d '{
    "name": "Cut Man",
    "game": "Mega Man",
    "weakness": "Super Arm"
  }'
```

---

## 🏗️ Arquitetura

```
src
├── 📂 Controllers      # Rotas da API
├── 📂 Models           # Modelos do banco de dados
├── 📂 Services         # Regras de negócio
├── 📂 Middlewares      # Interceptadores de requisições/respostas
├── 📂 Database
│   ├── 📂 DTOs             # Data Transfer Objects
│   ├── 📂 EntityFramework  # Configurações do ORM
│   │   ├── 📂 Context
│   │   ├── 📂 Migrations
│   ├── 📂 Repositories     # Padrão Repository
```

---

## 📦 Dependências Principais

- [Microsoft.EntityFrameworkCore (3.1.8)](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/3.1.8)  
- [Microsoft.EntityFrameworkCore.Design (3.1.8)](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/3.1.8)  
- [Microsoft.EntityFrameworkCore.SqlServer (3.1.8)](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/3.1.8)  
- [Newtonsoft.Json (12.0.2)](https://www.nuget.org/packages/Newtonsoft.Json/12.0.2)  

---

## 🤖 Automação

- **CI/CD com GitHub Actions** (badge incluso)  
- Pipeline de build e testes automáticos  
- Suporte planejado para **Swagger/OpenAPI**  

---

## 📌 Conclusão e Próximos Passos

A API foi desenvolvida com sucesso, provando a importância de **boas práticas de arquitetura**, **documentação clara** e **processos automatizados**.  

🔮 **Próximos passos**:  
- Autenticação e autorização  
- Cache e paginação  
- Mais dados da franquia Mega Man  
- Deploy em ambiente cloud  

---

## 📜 Licença

Distribuído sob a [MIT License](./LICENSE).  

---

⌨️ Desenvolvido por **Felipe Aguiar** – [GitHub](https://github.com/felipeAguiarCode)  e melhorado readme de conclusão por **Rafael Pereira** [GitHub](https://github.com/shakarpg)
