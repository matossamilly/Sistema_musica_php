<div align="center">

<!-- BANNER DE BOAS-VINDAS & EFEITO DE ESCRITA -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=FFB6C1&height=200&section=header&text=Sistema%20Musical%20🌸&fontSize=42&fontColor=ffffff&animation=fadeIn" width="100%" alt="Header Banner" />

# 🌸 ✨ Sistema Musical ✨ 🌸
### *Gerenciador de Artistas & Músicas*

<!-- EFEITO DE DIGITAÇÃO DINÂMICO (DIGITA E APAGA SOZINHO) -->
<a href="https://github.com">
  <img src="https://readme-typing-svg.demolab.com?font=Poppins&weight=600&size=24&pause=1000&color=F78DA7&center=true&vCenter=true&width=600&height=50&lines=%E2%9C%A8+Desenvolvido+por+Samilly+Matos+Barranova+%E2%9C%A8;%F0%9F%92%96+Clean+Girl+%26+Pink+Aesthetic+Edition+%F0%9F%92%96;%F0%9F%8E%B5+PHP%2C+MySQL+%26+Seguran%C3%A7a+Web+%F0%9F%8E%B5" alt="Typing Effect - Samilly Matos Barranova" />
</a>

<br><br>

<!-- BADGES AESTHETIC -->
<img src="https://img.shields.io/badge/PHP-8.x-ffb6c1?style=for-the-badge&logo=php&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-Database-f8c8dc?style=for-the-badge&logo=mysql&logoColor=white" />
<img src="https://img.shields.io/badge/Security-CSRF%20%26%20BCrypt-ffc0cb?style=for-the-badge" />
<img src="https://img.shields.io/badge/Style-Clean%20Girl-ff69b4?style=for-the-badge" />

---

</div>

> 🎀 *Uma aplicação web moderna, segura e minimalista criada para organizar sua biblioteca musical com máxima elegância e sofisticação.* 🎀

<br>

## 🌷 ✦ Sobre o Projeto

O **Sistema Musical** é um software completo desenvolvido em **PHP** e **MySQL** projetado para gerenciar e catalogar artistas, álbuns e faixas musicais.

O sistema conta com tratamento automático de fotos de capa através da biblioteca **GD**, validações rigorosas de segurança contra ataques **CSRF**, hash de senhas via **BCrypt** e player integrado para o **YouTube**.

<br>

## ✨ ✦ Funcionalidades Principais

| Ícone | Funcionalidade | Descrição |
| :---: | :--- | :--- |
| 🔑 | **Autenticação Segura** | Sistema de Login contra CSRF, proteção de rotas e hashes `BCrypt`. |
| 🎤 | **Gestão de Artistas** | Cadastro, edição e remoção de artistas com upload de fotos otimizadas. |
| 🎧 | **Biblioteca de Músicas** | Vinculação de faixas com suporte a letras, álbuns e capas personalizadas. |
| ▶️ | **Player YouTube** | Detecção e execução de links de vídeos diretamente da plataforma. |
| 🔍 | **Filtros Dinâmicos** | Busca em tempo real por nome de faixa, artista, álbum ou gênero musical. |
| 🖼️ | **Smart Image Resizer** | Redimensionamento automático via PHP GD para $300 \times 300\text{ px}$. |

<br>

## 💖 ✦ Tecnologias & Ferramentas

```
 🌸 PHP 8.x        ──► Lógica de Negócio, Sessões & Segurança
 🪞 MySQL          ──► Armazenamento Relacional & FK Constraints
 🩰 HTML5 & CSS3   ──► Design Clean Girl & Componentes Responsivos
 🌷 PHP GD         ──► Processamento & Crop Inteligente de Fotos
```

<br>

## 🗄️ ✦ Arquitetura do Banco de Dados

```mermaid
erDiagram
    USUARIOS {
        int id PK
        string usuario
        string senha
    }
    ARTISTAS {
        int id PK
        string nome
        string genero
        string pais
        string imagem
        timestamp criado_em
    }
    MUSICAS {
        int id PK
        int artista_id FK
        string titulo
        string album
        string genero
        string youtube_link
        text letra
        string imagem_capa
        timestamp criado_em
    }
    ARTISTAS ||--o{ MUSICAS : "possui"
```

<br>

## 🚀 ✦ Como Executar o Projeto Localmente

<details>
<summary><b>📋 Clique para expandir os passos de instalação</b></summary>

<br>

### 1️⃣ Pré-requisitos
* Servidor Web local (**XAMPP**, **WAMP**, **Laragon** ou PHP Built-in Server).
* **PHP 7.4+** com extensões `mysqli` e `gd` habilitadas.
* Servidor **MySQL** em execução.

### 2️⃣ Banco de Dados
Acesse o **phpMyAdmin** e crie a base executando o script `bd.sql`:

```sql
CREATE DATABASE IF NOT EXISTS sistema_musical_v2 
  CHARACTER SET utf8mb4 
  COLLATE utf8mb4_unicode_ci;
```

### 3️⃣ Acessar a Aplicação
> **URL:** `http://localhost/sistema_musical/login.php`  
> * **Usuário:** `admin`  
> * **Senha:** `123`  

</details>

<br>

## 📁 ✦ Estrutura do Projeto

```text
📂 sistema-musical/
 ├── 📄 bd.sql                 ── Script de banco de dados
 ├── 📄 conexao.php            ── Conexão MySQLi segura
 ├── 📄 funcoes.php            ── Helpers, GD Upload & CSRF
 ├── 📄 valida_sessao.php      ── Middleware de autenticação
 ├── 📄 login.php              ── Autenticação de usuários
 ├── 📄 logout.php             ── Encerramento de sessão
 ├── 📄 index.php              ── Dashboard Principal
 ├── 📄 cadastro_artista.php   ── Módulo de Artistas
 ├── 📄 cadastro_musica.php    ── Módulo de Músicas
 ├── 📄 listagem_musicas.php   ── Biblioteca & Filtros
 ├── 📄 geraSenha.php          ── Utilitário BCrypt
 └── 📂 img/                   ── Repositório de imagens
```

<br>

<!-- CARD DE CRÉDITOS ESPECIAL -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=F8C8DC&height=120&section=footer&text=Desenvolvido%20por%20Samilly%20Matos%20Barranova%20💖&fontSize=22&fontColor=4A4A4A" width="100%" />

### 🌸 **Samilly Matos Barranova** 🌸
*Engenharia de Software & Web Development com Estética e Precisão.*

💖 **Se este projeto te inspirou, não se esqueça de deixar uma estrela!** 🎀

</div>
