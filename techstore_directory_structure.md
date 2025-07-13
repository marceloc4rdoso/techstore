# Estrutura de Diretórios - Sistema TechStore

```
techstore/
├── manage.py
├── requirements.txt
├── .env                              # Variáveis de ambiente
├── .gitignore
├── README.md
├── db.sqlite3                        # Banco de dados SQLite
│
├── core/                        # Configurações principais do projeto
│   ├── __init__.pytechstore/
├── .venv/
├── core/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── dashboard/
├── products/
├── sales/
├── users/
├── .env
└── manage.py
```

## Principais Diretórios e Arquivos

### 📁 **Apps Principais**
- **`users/`** - Gerenciamento de usuários e autenticação
- **`products/`** - Produtos, categorias, marcas, estoque
- **`sales/`** - Vendas e itens de venda
- **`dashboard/`** - Dashboard e relatórios com KPIs

### 📁 **Estrutura de Templates**
- **`templates/`** - Templates globais compartilhados
- **`templates/base.html`** - Template base com navbar e sidebar
- Cada app tem sua pasta de templates específica

### 📁 **Arquivos Estáticos e Mídia**
- **`static/`** - CSS, JavaScript, imagens estáticas
- **`media/`** - Uploads de usuários (fotos de produtos, logos)

### 📁 **Configurações e Utilitários**
- **`techstore/settings.py`** - Configurações principais
- **`requirements.txt`** - Dependências do projeto
- **`.env`** - Variáveis de ambiente

### 📁 **API REST**
- Cada app tem seus próprios serializers e URLs da API
- **`api/`** - Configurações centralizadas da API

### 📁 **Testes e Documentação**
- **`tests/`** - Testes automatizados
- **`docs/`** - Documentação do projeto
- **`scripts/`** - Scripts utilitários

## Mais alguns detalhes da Estrutura

```bash

## Níveis de Acesso por Diretório

### 👑 **Admin** - Acesso Total
- Todos os diretórios e funcionalidades
- Dashboard completo
- Gerenciamento de usuários

### 🛒 **Vendedor** - Acesso Limitado
- `sales/` - Criar e gerenciar vendas
- `products/` - Apenas visualização do catálogo
- `dashboard/` - KPIs de vendas

### 📦 **Estoquista** - Acesso Específico
- `products/` - CRUD completo de produtos
- `dashboard/` - KPIs de estoque
- Movimentações de estoque

### 👤 **Convidado** - Acesso Público
- `products/catalog/` - Apenas catálogo público
- Visualização de produtos e avaliações

Esta estrutura garante organização, escalabilidade e separação clara de responsabilidades entre os diferentes módulos do sistema.
#### << Volta https://github.com/marceloc4rdoso/techstore/blob/main/README.md
