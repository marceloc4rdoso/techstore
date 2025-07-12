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
│   ├── __init__.py
│   ├── settings.py                   # Configurações principais
│   ├── urls.py                       # URLs principais
│   ├── wsgi.py
│   └── asgi.py
│
├── static/                           # Arquivos estáticos
│   ├── css/
│   │   ├── dashboard.css
│   │   ├── products.css
│   │   └── custom.css
│   ├── js/
│   │   ├── dashboard.js
│   │   ├── products.js
│   │   └── sales.js
│   └── img/
│       ├── logo.png
│       └── default-product.png
│
├── media/                            # Arquivos de mídia (uploads)
│   ├── products/                     # Imagens de produtos
│   ├── brands/                       # Logos de marcas
│   └── users/                        # Fotos de usuários
│
├── templates/                        # Templates globais
│   ├── base.html                     # Template base
│   ├── navbar.html                   # Barra de navegação
│   ├── sidebar.html                  # Barra lateral
│   ├── messages.html                 # Mensagens do sistema
│   └── pagination.html               # Paginação
│
├── accounts/                         # App de usuários e autenticação
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py                     # Modelo de usuário customizado
│   ├── views.py                      # Views de login/logout/registro
│   ├── forms.py                      # Formulários de usuário
│   ├── urls.py                       # URLs do app accounts
│   ├── permissions.py                # Permissões customizadas
│   ├── migrations/
│   │   ├── __init__.py
│   │   └── 0001_initial.py
│   └── templates/
│       └── accounts/
│           ├── login.html
│           ├── register.html
│           ├── profile.html
│           └── user_list.html
│
├── products/                         # App de produtos
│   ├── __init__.py
│   ├── admin.py                      # Configuração do admin
│   ├── apps.py
│   ├── models.py                     # Modelos de produtos, categorias, etc.
│   ├── views.py                      # Views dos produtos
│   ├── forms.py                      # Formulários de produtos
│   ├── urls.py                       # URLs do app products
│   ├── api_urls.py                   # URLs da API REST
│   ├── serializers.py                # Serializers para API
│   ├── filters.py                    # Filtros para produtos
│   ├── utils.py                      # Utilitários e helpers
│   ├── migrations/
│   │   ├── __init__.py
│   │   ├── 0001_initial.py
│   │   └── 0002_add_product_fields.py
│   └── templates/
│       └── products/
│           ├── catalog.html          # Catálogo público
│           ├── detail.html           # Detalhes do produto
│           ├── list.html             # Lista para estoquistas
│           ├── form.html             # Formulário criar/editar
│           ├── stock_form.html       # Formulário de estoque
│           └── partials/
│               ├── product_card.html
│               ├── product_filters.html
│               └── stock_alert.html
│
├── sales/                            # App de vendas
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py                     # Modelos de vendas
│   ├── views.py                      # Views de vendas
│   ├── forms.py                      # Formulários de vendas
│   ├── urls.py                       # URLs do app sales
│   ├── serializers.py                # Serializers para API
│   ├── utils.py                      # Utilitários de vendas
│   ├── migrations/
│   │   ├── __init__.py
│   │   └── 0001_initial.py
│   └── templates/
│       └── sales/
│           ├── list.html             # Lista de vendas
│           ├── detail.html           # Detalhes da venda
│           ├── form.html             # Formulário de venda
│           ├── invoice.html          # Fatura/recibo
│           └── partials/
│               ├── sale_items.html
│               └── sale_status.html
│
├── dashboard/                        # App de dashboard e relatórios
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py                     # Modelos de relatórios (se necessário)
│   ├── views.py                      # Views do dashboard
│   ├── urls.py                       # URLs do dashboard
│   ├── utils.py                      # Utilitários para KPIs
│   ├── charts.py                     # Geração de gráficos
│   ├── migrations/
│   │   └── __init__.py
│   └── templates/
│       └── dashboard/
│           ├── index.html            # Dashboard principal
│           ├── products_report.html  # Relatório de produtos
│           ├── sales_report.html     # Relatório de vendas
│           ├── stock_report.html     # Relatório de estoque
│           └── partials/
│               ├── kpi_cards.html
│               ├── charts.html
│               └── recent_activities.html
│
├── api/                              # App dedicado à API (opcional)
│   ├── __init__.py
│   ├── urls.py                       # URLs centralizadas da API
│   ├── permissions.py                # Permissões da API
│   ├── authentication.py             # Autenticação personalizada
│   ├── throttling.py                 # Rate limiting
│   └── views.py                      # Views gerais da API
│
├── core_utils/                       # App para funcionalidades centrais
│   ├── __init__.py
│   ├── apps.py
│   ├── models.py                     # Modelos base/abstratos
│   ├── utils.py                      # Utilitários globais
│   ├── validators.py                 # Validadores customizados
│   ├── mixins.py                     # Mixins para views
│   ├── decorators.py                 # Decoradores personalizados
│   └── exceptions.py                 # Exceções personalizadas
│
│
├── scripts/                          # Scripts utilitários
│   ├── __init__.py
│   ├── populate_db.py               # Popular banco com dados de teste
│   ├── backup_db.py                 # Backup do banco
│   ├── import_products.py           # Importar produtos via CSV
│   └── generate_reports.py          # Gerar relatórios
│
├── tests/                            # Testes do projeto
│   ├── __init__.py
│   ├── test_models.py               # Testes de modelos
│   ├── test_views.py                # Testes de views
│   ├── test_forms.py                # Testes de formulários
│   ├── test_api.py                  # Testes da API
│   └── factories.py                 # Factories para testes
│
├── docs/                             # Documentação
│   ├── README.md
│   ├── API.md                       # Documentação da API
│   ├── DEPLOYMENT.md                # Guia de implantação
│   ├── CONTRIBUTING.md              # Guia de contribuição
│   └── CHANGELOG.md                 # Histórico de mudanças
│
├── config/                           # Configurações de ambiente
│   ├── development.py               # Configurações de desenvolvimento
│   ├── production.py                # Configurações de produção
│   ├── testing.py                   # Configurações de teste
│   └── docker/
│       ├── Dockerfile
│       ├── docker-compose.yml
│       └── nginx.conf
│
└── logs/                             # Logs da aplicação
    ├── django.log
    ├── error.log
    └── access.log
```

## Principais Diretórios e Arquivos

### 📁 **Apps Principais**
- **`accounts/`** - Gerenciamento de usuários e autenticação
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
- **`fixtures/`** - Dados iniciais para desenvolvimento

### 📁 **API REST**
- Cada app tem seus próprios serializers e URLs da API
- **`api/`** - Configurações centralizadas da API

### 📁 **Testes e Documentação**
- **`tests/`** - Testes automatizados
- **`docs/`** - Documentação do projeto
- **`scripts/`** - Scripts utilitários

## Comandos para Criar a Estrutura

```bash
# Criar projeto Django
django-admin startproject techstore
cd techstore

# Criar apps
python manage.py startapp accounts
python manage.py startapp products
python manage.py startapp sales
python manage.py startapp dashboard
python manage.py startapp core_utils
python manage.py startapp api

# Criar diretórios
mkdir -p static/{css,js,img}
mkdir -p media/{products,brands,users}
mkdir -p templates/{accounts,products,sales,dashboard}
```

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
