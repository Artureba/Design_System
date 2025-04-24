# Documentação do Projeto: Clínica Médica

## 🧩 Desenho Arquitetural

### Estilo Arquitetural
O estilo arquitetural escolhido para este projeto é o **Microservices Architecture**, que permite a criação de serviços independentes e escaláveis.

### Padrão Arquitetural
O padrão arquitetural adotado será o **MVC (Model-View-Controller)**, que facilita a separação de responsabilidades e mantém o acoplamento baixo.

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

---

## 🗃️ Dados

### Banco de Dados
- **PostgreSQL**: Banco de dados relacional escolhido para o projeto.

### Diagrama de Dados
> ![DesignSystemImage](https://github.com/user-attachments/assets/c596c716-cdc1-4393-8d57-c095e4f413cf)


---

## 🎯 Motivação

Este projeto visa facilitar o gerenciamento de uma clínica médica, proporcionando uma plataforma onde médicos, pacientes e atendentes possam interagir de forma eficiente.

Através da automação de processos como agendamento de consultas e acesso a laudos e exames, a clínica pode oferecer um serviço mais ágil e organizado, melhorando a experiência dos usuários e a eficiência operacional.
