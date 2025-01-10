## 🌐 [English Version of README](README_EN.md)

# PSW 12 RETURNAL

Este repositório contém três projetos distintos: um para gerenciamento de links encurtados, um para criação de um diário digital, e um para monitoramento de dados. Cada projeto possui funcionalidades e estruturas próprias, e a documentação a seguir explica como configurar e rodar cada um deles.

---

## 🟠 Projeto 1: Encurtador de Links

Este projeto é um encurtador de links simples, desenvolvido com Django e a biblioteca NinjaAPI. Ele permite criar links encurtados, rastrear cliques únicos e gerenciar links com um tempo de expiração. O objetivo principal é facilitar a criação de links curtos que redirecionam os usuários para URLs originais, com a capacidade de limitar o número de cliques e definir um tempo de validade.

### 🔨 Funcionalidades

- Criação de links encurtados a partir de URLs fornecidas.
- Controle de expiração e limitação de cliques únicos.
- API para criação e gerenciamento de links.

### ✔️ Técnicas e Tecnologias

- **Django** para backend.
- **NinjaAPI** para criação de endpoints da API.
- **TailwindCSS** para estilização.
- **SQLite** como banco de dados.

### 📁 Estrutura do Projeto

- **core/**
    - `settings.py`, `urls.py`, `wsgi.py`, `asgi.py`
- **shortener/**
    - `models.py`, `api.py`, `schemas.py`, `views.py`, `admin.py`
    - `migrations/`: Arquivos de migração para o banco de dados.
- **manage.py**: Script de administração do Django.

### 🛠️ Rodando o Projeto

1. **Instale as dependências**:
    - Execute `pip install -r requirements.txt`.
2. **Realize as migrações**:
    - Execute `python manage.py migrate`.
3. **Inicie o servidor Django**:
    - Execute `python manage.py runserver`.

---

## 🟢 Projeto 2: Diário Digital

Este projeto é um diário digital onde você pode registrar e visualizar entradas pessoais. Ele utiliza Django para o backend e TailwindCSS para a interface. O sistema permite que o usuário registre suas entradas com informações como título, conteúdo e data.

### 🔨 Funcionalidades

- Registro de entradas de diário com título, conteúdo e data.
- Visualização das entradas registradas.
- Interface simples e intuitiva.

### ✔️ Técnicas e Tecnologias

- **Django** para backend.
- **TailwindCSS** para o design responsivo.
- **SQLite** para armazenamento das entradas.

### 📁 Estrutura do Projeto

- **core/**
    - `settings.py`, `urls.py`, `wsgi.py`, `asgi.py`
- **diary/**
    - `models.py`: Contém o modelo de dados para as entradas de diário.
    - `views.py`: Define as views para exibir o diário.
    - `templates/`: Contém o HTML para exibição das entradas.
- **manage.py**: Script de administração do Django.

### 🛠️ Rodando o Projeto

1. **Instale as dependências**:
    - Execute `pip install -r requirements.txt`.
2. **Realize as migrações**:
    - Execute `python manage.py migrate`.
3. **Inicie o servidor Django**:
    - Execute `python manage.py runserver`.

---

## 🔵 Projeto 3: Monitoramento de Dados

Este projeto é um sistema de monitoramento de dados com Flask, SQLite e gráficos utilizando Chart.js. O objetivo é coletar dados de sensores e apresentá-los em gráficos interativos em tempo real.

### 🔨 Funcionalidades

- Coleta de dados de sensores via POST.
- Visualização de gráficos em tempo real usando Chart.js.
- Exportação de dados para CSV.

### ✔️ Técnicas e Tecnologias

- **Flask** para backend.
- **Chart.js** para visualização de gráficos.
- **SQLite** para armazenamento de dados.

### 📁 Estrutura do Projeto

- **core/**
    - `app.py`: Arquivo principal que inicializa o servidor Flask e as rotas.
    - `models.py`: Define o modelo de dados para armazenar as leituras dos sensores.
    - `static/`: Contém arquivos estáticos como imagens e gráficos.
    - `templates/`: Contém os templates HTML para exibição dos dados.
- **requirements.txt**: Lista de dependências do projeto.
- **manage.py**: Script de administração para rodar o servidor Flask.

### 🛠️ Rodando o Projeto

1. **Instale as dependências**:
    - Execute `pip install -r requirements.txt`.
2. **Inicie o servidor Flask**:
    - Execute `python app.py`.
3. **Acesse o sistema**:
    - Abra o navegador e acesse `http://127.0.0.1:5000/` para ver o sistema de monitoramento em ação.

---

## 🌐 Deploy

Para fazer o deploy de qualquer um dos projetos, siga as instruções abaixo:

1. **Configuração do Banco de Dados**:
    - Para ambientes de produção, configure um banco de dados como PostgreSQL.
2. **Configuração do Servidor**:
    - Utilize um serviço de deploy como [Heroku](https://www.heroku.com/) ou [DigitalOcean](https://www.digitalocean.com/).
3. **Subir o Projeto**:
    - Para Heroku, você pode seguir a [documentação de deploy do Django](https://devcenter.heroku.com/articles/django-app-configuration) ou [Flask](https://devcenter.heroku.com/articles/getting-started-with-python).
4. **Acessar o Projeto**:
    - Após o deploy, você poderá acessar a aplicação através do domínio fornecido pela plataforma de hospedagem.
