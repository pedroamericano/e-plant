# 🌱 E-Plant: Marketplace de Produtos Naturais

**E-Plant** é uma aplicação web desenvolvida como MVP para um marketplace de plantas e produtos ecológicos. A plataforma conecta pequenos produtores com consumidores que valorizam sustentabilidade e produtos naturais.

## 🚀 Visão Geral

O objetivo deste projeto é criar uma plataforma funcional que permita:
- Consumidores navegarem, comprarem e acompanharem pedidos de produtos como mudas, terrários e cestas orgânicas.
- Vendedores cadastrarem seus produtos, gerenciarem pedidos e acessarem painéis com informações de vendas.

> Este projeto está em desenvolvimento como parte de um portfólio voltado para minha carreira de analista de sistemas com foco em desenvolvimento web full stack, engenharia de requisitos e qualidade de software.

---

## 🛠️ Tecnologias Utilizadas

### Front-end
- **React.js** + **Tailwind CSS**
  - Criação rápida de componentes reutilizáveis
  - Design moderno e responsivo
  - Fácil integração com bibliotecas de testes (Cypress)

### Back-end
- **Python** + **Flask**
  - Leve e rápido para MVPs
  - Excelente integração com ferramentas de testes como Robot Framework e Postman
  - Código limpo e de fácil manutenção

### Banco de Dados
- PostgreSQL ou SQLite (dependendo do ambiente)

### Testes e QA
- **Cypress** (Testes E2E no front-end)
- **Robot Framework** (Testes automatizados e BDD)
- **Postman** (Testes de API)
- **JMeter** (Testes de performance)

### CI/CD & Cloud
- **GitHub Actions** para integração contínua
- **AWS** (S3, EC2, RDS) como ambiente futuro de deploy

---

## ✨ Funcionalidades (MVP)

### 👥 Usuário Consumidor
- Cadastro/login seguro
- Visualização de catálogo de produtos
- Carrinho de compras
- Finalização de pedidos
- Histórico de pedidos

### 🛒 Usuário Vendedor
- Cadastro/login como vendedor
- Cadastro e gerenciamento de produtos
- Acompanhamento de pedidos realizados

---

## 📐 Estrutura do Projeto

```
e-plant/
├── backend/             # API Flask com banco de dados e autenticação
├── frontend/            # Interface React com Tailwind CSS
├── tests/               # Testes automatizados com Cypress e Robot Framework
├── docs/                # Documentação e diagramas UML
├── README.md
└── docker-compose.yml   # Ambientes locais com Docker
```

---

## 🔧 Como Executar Localmente

### Pré-requisitos
- Python 3.10+
- Node.js 18+
- Docker (opcional)

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/e-plant.git
   cd e-plant
   ```

2. Instale as dependências do backend:
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. Inicie o backend:
   ```bash
   flask run
   ```

4. Em outro terminal, rode o front-end:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

---

## 📅 Status Atual

- ✅ Estrutura inicial configurada
- ✅ Protótipos de baixa fidelidade definidos
- 🔄 Implementação do front-end e backend em andamento
- 🧪 Plano de testes automatizados em elaboração

---

## 📌 Objetivos QA e Requisitos

Este projeto serve como base para:
- Demonstrar habilidades práticas em análise de requisitos e testes
- Criar documentação completa (UML, casos de uso, requisitos)
- Implementar testes automatizados e pipelines CI/CD

---

## 🤝 Contribuições

Este repositório está em desenvolvimento individual. Futuramente serão bem-vindas contribuições de design, testes ou performance.

---

## 📄 Licença

Distribuído sob a licença MIT.

---

**Desenvolvido com 💚 por Pedro Americano do Brasil.**
