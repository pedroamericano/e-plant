
# Documentação de Requisitos e Diagramas - E-Plant

## 🌱 Visão Geral do Projeto

**Nome do Produto:** E-Plant - Marketplace de Plantas e Produtos Naturais

**Objetivo:** Criar uma plataforma digital onde pequenos produtores e artesãos possam vender seus produtos naturais (mudas, terrários, kokedamas, cestas orgânicas) para consumidores finais.

**Público-Alvo:**
- Consumidores interessados em produtos sustentáveis.
- Vendedores autônomos de produtos naturais.

**Diferenciais:**
- Foco em sustentabilidade
- Apoio a pequenos produtores
- Navegação intuitiva e responsiva

**MVP (Produto Mínimo Viável):**
- Cadastro/Login de consumidores e vendedores
- Catálogo de produtos com imagem, descrição e preço
- Carrinho de compras e finalização de pedido
- Painel para vendedores gerenciarem produtos e pedidos
- Histórico de pedidos

## ✅ Requisitos Funcionais

- **RF01**: Cadastro de usuários (nome, email, senha, tipo)
- **RF02**: Login com autenticação JWT
- **RF03**: Visualização de produtos no catálogo
- **RF04**: Adição ao carrinho e checkout
- **RF05**: Histórico de pedidos do consumidor
- **RF06**: Cadastro e edição de produtos pelo vendedor
- **RF07**: Visualização de pedidos recebidos pelo vendedor

## ⚡ Requisitos Não Funcionais

- **RNF01**: Tempo de resposta < 2 segundos
- **RNF02**: Alta disponibilidade (>= 99%)
- **RNF03**: Comunicação criptografada via HTTPS
- **RNF04**: Compatibilidade com navegadores modernos

## 🔎 Modelagem e Diagramas UML

### Diagrama de Casos de Uso
```plantuml
@startuml
actor Consumidor
actor Vendedor

rectangle "E-Plant Marketplace" {
  Consumidor --> (Cadastrar)
  Consumidor --> (Login)
  Consumidor --> (Ver Produtos)
  Consumidor --> (Adicionar ao Carrinho)
  Consumidor --> (Finalizar Pedido)
  Consumidor --> (Ver Histórico de Pedidos)

  Vendedor --> (Cadastrar)
  Vendedor --> (Login)
  Vendedor --> (Cadastrar Produto)
  Vendedor --> (Editar Produto)
  Vendedor --> (Ver Pedidos Recebidos)
}
@enduml
```

### Diagrama de Classes
```plantuml
@startuml
class Usuario {
  +id: int
  +nome: string
  +email: string
  +senha: string
  +tipo: string
}

class Produto {
  +id: int
  +nome: string
  +descricao: string
  +preco: float
  +imagem: string
  +id_vendedor: int
}

class Pedido {
  +id: int
  +data: datetime
  +total: float
  +status: string
  +id_consumidor: int
}

class ItemPedido {
  +id_pedido: int
  +id_produto: int
  +quantidade: int
  +subtotal: float
}

class Carrinho {
  +id_consumidor: int
  +itens: List<ItemPedido>
}

Usuario "1" -- "0..*" Pedido
Usuario "1" -- "0..*" Produto
Pedido "1" -- "1..*" ItemPedido
Produto "1" -- "0..*" ItemPedido
Usuario "1" -- "1" Carrinho
@enduml
```

### Diagrama de Sequência (Login)
```plantuml
@startuml
actor Usuario
participant "Frontend" as FE
participant "Backend (Flask API)" as BE
database "Banco de Dados" as DB

Usuario -> FE : insere email e senha
FE -> BE : POST /login
BE -> DB : valida credenciais
DB --> BE : dados do usuário
BE -> BE : gera token JWT
BE --> FE : token JWT
FE --> Usuario : acesso concedido
@enduml
```

### Diagrama de Atividades (Venda de Produto)
```plantuml
@startuml
start
:Login do Vendedor;
:Ir para Painel de Produtos;
:Selecionar 'Novo Produto';
:Preencher Formulário;
:Enviar Produto;
:Produto Publicado;
:Receber Pedido;
:Confirmar Envio;
stop
@enduml
```

## 📄 Protótipos (Figma)

### Telas do Consumidor:
- Login / Cadastro
- Home com produtos
- Detalhes do produto
- Carrinho / Checkout
- Histórico de pedidos

### Telas do Vendedor:
- Login / Cadastro
- Painel com produtos
- Cadastro / edição de produtos
- Visualização de pedidos

**Design:**
- Paleta: Verdes, marrons e tons naturais
- Tipografia limpa (Inter ou Roboto)
- Layout responsivo com foco em usabilidade

---

> Para mais detalhes, consulte o repositório principal do projeto E-Plant.
