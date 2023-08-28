## Projeto de Autenticação usando .NET Core e JWT

Projeto de autenticação utilizando .NET Core, JWT (JSON Web Tokens), C#, Entity Framework e seguindo a arquitetura Clean Architecture.

### Proposta

1. Introdução:

O objetivo deste projeto é desenvolver um serviço de autenticação seguro e eficiente utilizando .NET Core, JWT (JSON Web Tokens), C#, Entity Framework e seguindo os princípios da arquitetura Clean Architecture. O serviço permitirá que os usuários se registrem, façam login, gerenciem suas contas e acessem recursos protegidos com autenticação.

2. Escopo e Funcionalidades:

Implementação de um sistema de registro de usuário com validações adequadas para garantir a integridade dos dados.
Desenvolvimento de um sistema de autenticação com geração de tokens JWT.
Proteção de rotas sensíveis, permitindo o acesso apenas para usuários autenticados.
Perfil do usuário, permitindo que os usuários visualizem e atualizem suas informações de conta.
Implementação de medidas de segurança para garantir a validade e integridade dos tokens JWT.
Criação de testes unitários e de integração para garantir a qualidade e a segurança do sistema.
Implementação da arquitetura Clean Architecture para manter a separação de preocupações e facilitar a manutenção.

3. Benefícios:

Segurança Avançada: A utilização de JWT e medidas de segurança apropriadas garantirá a autenticação segura dos usuários.
Experiência do Usuário Aprimorada: Os usuários terão uma experiência positiva ao se registrar e acessar os recursos do sistema de maneira segura.
Manutenção Facilitada: A arquitetura Clean Architecture facilitará a manutenção contínua do sistema, permitindo que as atualizações sejam feitas com segurança.
Testabilidade Garantida: Os testes unitários e de integração garantirão a qualidade e a robustez do sistema.
Escalabilidade: A arquitetura modular permitirá que o sistema seja facilmente escalável conforme as demandas cresçam.

4. Tecnologias Utilizadas:

.NET Core
C#
Entity Framework Core
Identity
JWT (JSON Web Tokens)
Clean Architecture
Testes Unitários e de Integração


### Arquitetura

O projeto seguirá a arquitetura Clean Architecture para promover uma estrutura organizada, manutenção facilitada e escalabilidade. A arquitetura é composta pelas seguintes camadas:

1. **Domain Layer**: Contém as entidades de negócios e a lógica central do sistema.
2. **Application Layer**: Orquestra o fluxo de dados e regras de negócios, conectando a camada de domínio com as interfaces de entrada/saída.
3. **Infrastructure Layer**: Lida com detalhes de implementação e tecnologia, como bancos de dados e APIs externas.
4. **Presentation/Interface Layer**: Lida com a interação do usuário e apresentação de dados.

### Estrutura de Pastas

```
Web Service de Autenticação usando .NET Core
├── API
│   ├── Controllers
│   │   ├── AuthController.cs
│   │   └── ...
│   ├── Models
│   │   ├── AuthenticationRequest.cs
│   │   ├── AuthenticationResponse.cs
│   │   └── ...
│   ├── Services
│   │   ├── IAuthService.cs
│   │   ├── AuthService.cs
│   │   └── ...
│   └── Startup.cs
├── Application
│   ├── DTOs
│   │   ├── UserDTO.cs
│   │   └── ...
│   ├── Interfaces
│   │   ├── IUserService.cs
│   │   └── ...
│   ├── Services
│   │   ├── UserService.cs
│   │   └── ...
│   └── ...
├── Domain
│   ├── Entities
│   │   ├── User.cs
│   │   └── ...
│   ├── Repositories
│   │   ├── IUserRepository.cs
│   │   └── ...
│   └── ...
├── Infrastructure
│   ├── Data
│   │   ├── ApplicationDbContext.cs
│   │   └── ...
│   ├── Repositories
│   │   ├── UserRepository.cs
│   │   └── ...
│   └── ...
├── Common
│   ├── Constants
│   │   ├── JwtSettings.cs
│   │   └── ...
│   ├── Extensions
│   │   ├── JwtExtensions.cs
│   │   └── ...
│   └── ...
└── ...
```

### Tecnologias e Padrões Utilizados
----
```
- .NET Core
- C#
- Entity Framework Core
- Identity
- JWT (JSON Web Tokens)
- Clean Architecture
- Dependency Injection
- Repository Pattern
- DTOs (Data Transfer Objects)
- Service Pattern
- Separation of Concerns
```
 
```
- AuthController.cs: Controller que lida com as requisições de autenticação, como login e registro.
- AuthenticationRequest.cs: Modelo para as requisições de autenticação.
- AuthenticationResponse.cs: Modelo para as respostas de autenticação, contendo o token JWT.
- IAuthService.cs: Interface para o serviço de autenticação.
- AuthService.cs: Implementação do serviço de autenticação.
- Startup.cs: Configuração inicial do aplicativo, incluindo configurações de autenticação e injeção de dependência.
- UserDTO.cs: Objeto de transferência de dados para a entidade de usuário.
- IUserService.cs: Interface para o serviço de usuário.
- UserService.cs: Implementação do serviço de usuário.
- User.cs: Entidade de usuário no domínio.
- IUserRepository.cs: Interface para o repositório de usuário.
- UserRepository.cs: Implementação do repositório de usuário utilizando Entity Framework.
- ApplicationDbContext.cs: Contexto do banco de dados usando Entity Framework.
- JwtSettings.cs: Configurações para o JWT.
- JwtExtensions.cs: Extensões úteis para trabalhar com JWT.
```
Este projeto oferece uma estrutura robusta para implementar um sistema de autenticação seguro utilizando .NET Core e outras tecnologias relevantes, seguindo as melhores práticas de desenvolvimento. A arquitetura Clean Architecture garante uma organização eficiente do código, enquanto as tecnologias e padrões utilizados garantem a segurança, escalabilidade e manutenção do sistema.
