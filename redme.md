# Planejamento do projeto 

## 1- Resumo do Projeto

- __Nome:__ _Setsuna Sekai_
- __Descrição:__ Um site onde o usuário pode cadastrar, listar e organizar os animes que já assistiu, está assistindo ou pretende assistir.
- __Objetivo:__ Ajudar fãs de anime a manterem o controle de suas séries, episódios e progresso de forma simples e rápida.


## 2- Público-Alvo

- Fãs de anime de todas as idades, especialmente os que assistem muitos títulos e querem organizar isso online.

## 3- Funcionalidades


**MVP**
- Cadastro e login de usuários
- Adicionar animes manualmente ou atraves do Banco de dados
- Editar e excluir animes
- Cards personalizados 
- Marcar status: _Assistido, Concluido, Pausado, Dropado, Assistir mais tarde_
- Navegação por filtragem de: _Gênero, Score, Marca de status, Ano de lançamento, temporada..._
- Acompanhar número de episódios assistidos

**Futuras Funcionalidades**

- Integração com API externa: ([myAnimeList](https://myanimelist.net/), [anilist](https://anilist.co/) e [Jikan](https://jikan.moe/) )
- Dark mode
- Compartilhamento de listas públicas
- Chat geral
- sistema de notas e resenhas
- sistema para listagem de mangá e manhwa
- Ranking de mais assitidos


## 4- Telas / Interface

- Pagina de login/cadastro
- Dashbord com a lista de animes do usúario
- Pagina para adicionar/editar anime
- Pagina de detalhes do anime
- Barra de pesquisa
- Filtro por status
- Tela de configurações


## 5- Arquitetura Tècnica

- **Front-end**: Next.js + TypeScript + Tailwind CSS
- **Back-end**: Node.js + Express
- **Banco de dados**: MangoDB, podendo sofrer alteração para (Firebase Firestone ou POstgreSQL)

### 6- Organização de pastas: 

```bash

Setsuna-Sekai/
├── src/
│   ├── app/                        # Páginas e rotas do Next.js
│   │   ├── layout.tsx              # Layout principal do site (navbar, footer, etc.)
│   │   ├── page.tsx                # Página inicial
│   │   ├── login/                  # Página de login e cadastro
│   │   │   ├── page.tsx            # Página de login
│   │   │   └── register.tsx        # Página de cadastro
│   │   ├── dashboard/              # Dashboard do usuário com lista de animes
│   │   │   └── page.tsx            # Página do dashboard
│   │   ├── anime/                  # Rota para adicionar e editar animes
│   │   │   ├── [id]/               # Página de detalhes do anime
│   │   │   │   └── page.tsx        # Página de detalhes
│   │   │   ├── novo/               # Página para adicionar novo anime
│   │   │   │   └── page.tsx        # Página para adicionar anime
│   │   │   └── editar/             # Página para editar anime
│   │   │       └── page.tsx        # Página para editar anime
│   │   ├── filtros/                # Filtros de busca (status, gênero, etc.)
│   │   │   └── page.tsx            # Página de filtros
│   │   └── configurações/          # Tela de configurações do usuário
│   │       └── page.tsx            # Página de configurações
│   ├── components/                 # Componentes reutilizáveis
│   │   ├── Header.tsx              # Cabeçalho (Navbar)
│   │   ├── Footer.tsx              # Rodapé
│   │   ├── AnimeCard.tsx           # Cartão de anime
│   │   ├── FilterBar.tsx           # Barra de filtros (status, gênero, etc.)
│   │   ├── SearchBar.tsx           # Barra de pesquisa
│   │   └── StatusBadge.tsx         # Indicador de status do anime (Assistido, Pausado, etc.)
│   ├── lib/                        # Funções auxiliares e utilitários
│   │   ├── db.ts                   # Conexão com o banco de dados (MongoDB ou outro)
│   │   ├── auth.ts                 # Funções relacionadas à autenticação
│   │   └── api.ts                  # Funções para integração com APIs externas (myAnimeList, anilist, etc.)
│   ├── services/                   # Lógica de acesso à API ou ao banco de dados
│   │   ├── userService.ts          # Lógica de gerenciamento de usuários
│   │   ├── animeService.ts         # Lógica de gerenciamento de animes
│   │   └── reviewService.ts        # Lógica para resenhas e avaliações de animes (futuro)
│   ├── models/                     # Modelos de dados (tipos e esquemas)
│   │   ├── user.ts                 # Modelo de dados do usuário
│   │   ├── anime.ts                # Modelo de dados de anime
│   │   └── review.ts               # Modelo de resenhas e avaliações (futuro)
│   ├── styles/                     # Estilos globais e temas
│   │   ├── globals.css             # Estilos globais (reset CSS, etc.)
│   │   └── tailwind.config.js      # Configuração do Tailwind CSS
├── public/                         # Imagens e arquivos públicos
│   ├── logo.png                    # Logo do site
│   └── background.jpg              # Imagem de fundo
├── middleware.ts                   # Middleware para autenticação de rotas protegidas
├── .env.local                      # Variáveis de ambiente (segredos)
├── next.config.js                  # Configurações do Next.js
├── package.json                    # Dependências e scripts do projeto
└── tsconfig.json                   # Configuração do TypeScript
```

## 7- Fluxo de Usuário

1. Usuàrio acessa o site
2. Faz login ou se cadastra
3. Adiciona um anime á sua lista
4. Marca o status do anime e atualiza os epsódios assistidos
5. Vizualiza e organiza sua lista com filtros e buscas 

## 8- Banco de Dados (exemplos básicos)
**Usuario**
- id
- nome
- email
- senha (criptografada)

**anime**

- id
- titulo
- status
- temporadas 
- episodios assistidos
- total de episodios
- nota
- comentario
- user_id (relacionado ao dono)

## 9- Diferencias 

- Interface simples, rapida e leve
- Pode ser usada offiline (PWA no futuro/app)
- Permite progressão por episódio
- Foco em experência pessoal

## 10- Notas e Inspirações

- [myAnimeList](https://myanimelist.net/)
- [anilist](https://anilist.co/)
- [Jikan](https://jikan.moe/)

## Contribuicôes e Parcerias

Estamos sempre em busca de novas parcerias e colaboradores para o ***Setsuna Sekai***!. Se você está interessado em contribuir para o projeto, seja com ideias, desenvolvimento, design ou ou outras formas de colaboração, entre em contato.

## Como se tornar parceiro?

Envie uma mensagem para [setsunasekaii@gmail.com](setsunasekaii@gmail.com) ou entre em contato através do nosso whatsapp clicando aqui => [SETSUNA](https://Wa.me/+5571996538037), para discutir possíveis colaborações.

## Benefícios para Parceiros:

- Participação no desenvolvimento e evolução do projeto.
- Divulgação e visibilidade no site e em outras plataformas.
- Possibilidade de trabalhar em um projeto inovador na comunidade de fãs de anime.







