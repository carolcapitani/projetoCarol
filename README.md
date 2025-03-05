# Blog Pessoal com Nuxt.js

Este projeto é um **Blog Pessoal** construído com **Nuxt.js**, **Vue.js** e **TailwindCSS**.

## Objetivo do Projeto

O objetivo deste projeto é criar uma plataforma onde eu possa compartilhar informações pessoais de forma organizada, utilizando as tecnologias **Nuxt.js** e **Vue.js** para a parte de front-end e **TailwindCSS** para estilização.

O blog possui páginas interativas sobre:

- **Contatos**: Apresenta informações de contato, como WhatsApp, e-mail, LinkedIn e GitHub.
- **Carreira**: Detalhes sobre minha trajetória profissional.
- **Formação Acadêmica**: Informações sobre a minha formação acadêmica.
- **Vida Pessoal**: Informações sobre a minha vida pessoal.

---

## Tecnologias Utilizadas

- **Nuxt.js**: Framework baseado em Vue.js para a construção da interface e navegação.
- **Vue.js**: Framework JavaScript para construção de componentes.
- **TailwindCSS**: Framework CSS para estilização do layout.
- **Vue Router**: Para navegação entre as diferentes páginas do blog.
- **Vite**: Para o gerenciamento do ambiente de desenvolvimento e build do projeto.

---

## Como Rodar o Projeto Localmente

Para rodar o projeto localmente, siga os passos abaixo:

### 1. Clone o repositório:

```sh
git clone https://github.com/carolcapitani/projetoCarol.git
```

### 2. Instale as dependências:

Navegue até a pasta do projeto e execute o comando para instalar as dependências:

```sh
cd projetoCarol
npm install
```

Ou, se preferir, use **pnpm**, **yarn** ou **bun**:

```sh
pnpm install
# ou
yarn install
# ou
bun install
```

### 3. Rode o servidor de desenvolvimento:

```sh
npm run dev
# ou
pnpm dev
# ou
yarn dev
# ou
bun run dev
```

O servidor estará disponível em **http://localhost:3000**. Abra essa URL no seu navegador para ver o blog em funcionamento.

---

## Como Fazer o Build do Projeto

Para gerar a versão otimizada do seu projeto para produção, execute o seguinte comando:

```sh
npm run generate
```

Isso criará a versão de produção do projeto na pasta **.output/public**.

---

## Como Rodar em Produção

Após gerar o build, você pode entregar o projeto em produção utilizando **Netlify**:

1. Acesse [Netlify](https://www.netlify.com/), faça login e crie um novo site a partir do repositório Git.
2. Na configuração de build, configure:
   - **Build Command**: `npm run build` (ou `pnpm build`, `yarn build` ou `bun run build`)
   - **Publish Directory**: `.output/public` (ou o diretório equivalente gerado pelo Nuxt.js).
3. Clique em **"Deploy site"** e o Netlify fará o deploy do seu projeto.

---

## Estrutura do Projeto

```sh
PROJETOCAROL/              # Diretório raiz do projeto
├── .nuxt/                 # Diretório gerado pelo Nuxt.js para build e cache
├── .output/               # Saída da compilação do projeto
├── assets/                # Arquivos estáticos como estilos e imagens
│   └── index.css          # Arquivo de estilos CSS
├── components/            # Componentes Vue reutilizáveis
│   ├── Carousel.vue       # Componente de carrossel
│   ├── Footer.vue         # Componente de rodapé
│   └── Navigation.vue     # Componente de navegação
├── node_modules/          # Pacotes e dependências do Node.js
├── pages/                 # Páginas do projeto
│   ├── academic.vue       # Página sobre formação acadêmica
│   ├── career.vue         # Página sobre carreira
│   ├── contacts.vue       # Página de contatos
│   ├── home.vue           # Página inicial
│   ├── index.vue          # Página principal do projeto
│   └── personal.vue       # Página sobre vida pessoal
├── public/                # Arquivos públicos acessíveis diretamente
│   ├── images/            # Diretório para armazenar imagens
│   ├── favicon.ico        # Ícone do site
│   ├── index.html         # Arquivo HTML principal
│   └── robots.txt         # Arquivo para configurar rastreamento por mecanismos de busca
├── server/                # Diretório para arquivos do servidor
├── .gitignore             # Arquivo para ignorar arquivos no Git
├── App.vue                # Componente raiz do Vue.js
├── nuxt.config.ts         # Configuração do Nuxt.js em TypeScript
├── package-lock.json      # Arquivo de bloqueio de versões das dependências do npm
├── package.json           # Gerenciador de dependências e scripts do projeto
├── README.md              # Documentação do projeto
├── tailwind.config.js     # Configuração do Tailwind CSS
└── tsconfig.json          # Configuração do TypeScript
```

---

## Autor

**Carolina Capitani**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin)](https://www.linkedin.com/in/carolcapitani)
[![GitHub](https://img.shields.io/badge/GitHub-black?logo=github)](https://github.com/carolcapitani)


