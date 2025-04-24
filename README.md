# Documentação do Projeto: Clínica Médica

### Estilo Arquitetural
O estilo arquitetural escolhido para este projeto é a **Arquitetura em Microserviços**, a qual permite a criação de serviços independentes e escaláveis.

### Padrões Arquitetura
O padrão arquitetural adotados serão:
- **MVC (Model-View-Controller)**, que facilita a separação de responsabilidades e mantém o acoplamento baixo.
- API Gateway para centralizar e rotear as requisições feitas aos microserviços, evitando necessidade do cliente conhecer o endereço de cada serviço.
- Utilização de token JWT como padrão para autenticação nas requisições HTTP.

---

## 🔐 BackEnd

### Requisitos de Segurança
- **OAuth2**: Utilizado para autenticação e autorização segura dos usuários.
- **HTTPS**: Protocolo de comunicação para garantir a segurança dos dados transmitidos.
- **JWT (JSON Web Tokens)**: Para gerenciar sessões de usuários de forma segura.

### Protocolo de Comunicação
- **API REST**: Utilizaremos HTTP para comunicação entre os serviços.

### Tecnologias Utilizadas
- **Java com Spring Boot (versão 21)**: Framework principal para desenvolvimento do backend.
- **JPA (Java Persistence API)**: Para comunicação com o banco de dados.
- **Lombok**: Para reduzir a verbosidade do código e agilizar o desenvolvimento.

### Diagrama Arquitetural
> ![DesignSystemImage](https://github.com/user-attachments/assets/c596c716-cdc1-4393-8d57-c095e4f413cf)

#### 🌐 API Gateway
- Ponto único de entrada para o sistema.
- Redireciona requisições para os serviços corretos.
- Pode aplicar políticas de segurança e controle de tráfego.

#### 🔐 Auth Service
- Responsável pela autenticação de usuários.
- Gera e valida tokens JWT.
- Ponto central de segurança para os demais serviços.

#### 📞 Atendente Service
- Gerencia dados e operações relacionadas a atendentes.
- Consome e valida JWT para autenticação.
- Persistência via JPA em banco de dados próprio.

#### 🩺 Doctor Service
- Gerencia informações de médicos.
- Acesso protegido por JWT.
- Comunicação JSON e persistência com JPA.

#### 👤 Client Service
- Responsável pelo cadastro e gerenciamento de clientes/pacientes.
- Integração com Auth Service para autenticação.
- Comunicação via HTTP + JSON.

#### 📅 Appointment Service
- Controla agendamentos e horários de consultas.
- Utiliza JWT para autorização.
- Armazena dados com JPA.

#### 🗂️ Medical Record Service
- Armazena e gerencia prontuários médicos.
- Acesso seguro via token JWT.
- Persistência isolada com JPA.

---

## 🎨 FrontEnd

### Padrões de Acessibilidade
- **Alt Text em Imagens**: Todas as imagens devem conter descrições alternativas.

### Jornada do Usuário
- **Médico**: Disponibiliza agenda e realiza atendimentos.
- **Paciente**: Marca horários e acessa consultas.
- **Atendente**: Acessa a agenda dos médicos, pode remover horários com autorização do paciente, e tem acesso a laudos e exames.

### Design
- **Cores**:  
  - Rosa: `#FFC0CB`  
  - Branco: `#FFFFFF`  
  - Cinza Claro: `#D3D3D3`
- **Tipografia**: Arial, Helvetica, sans-serif.
- **Ícones**: Utilização de biblioteca de ícones como Material Icons.
- **Framework CSS**: Bootstrap.

### Tecnologias Utilizadas
- **React**: Framework principal para desenvolvimento do frontend.
- **Tailwind CSS**: Para estilização e design responsivo.
- **Axios**: Para comunicação com a API.


## Dados

### 🗄️ Banco de Dados

- **SGBD Utilizado**: PostgreSQL – Banco de dados relacional escolhido para o projeto.

#### 📦 Padrão de Nomenclatura

- **Tabelas**:  
  `TB_NOME_DA_TABELA`

- **Colunas**:

| Prefixo | Significado  | Exemplo         |
|---------|--------------|-----------------|
| `NR_`   | Números      | `NR_QUANTIDADE` |
| `VL_`   | Valores      | `VL_PRECO`      |
| `NM_`   | Nomes        | `NM_NOME`       |
| `DS_`   | Descrições   | `DS_DESCRICAO`  |
| `CD_`   | Códigos      | `CD_CODIGO`     |

---

## 🎯 Motivação

Este projeto visa facilitar o gerenciamento de uma clínica médica, proporcionando uma plataforma onde médicos, pacientes e atendentes possam interagir de forma eficiente.

Através da automação de processos como agendamento de consultas e acesso a laudos e exames, a clínica pode oferecer um serviço mais ágil e organizado, melhorando a experiência dos usuários e a eficiência operacional.
