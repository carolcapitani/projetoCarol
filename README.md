# Blog Pessoal com Nuxt.js

Este projeto é um Blog Pessoal construído com **Nuxt.js**, **Vue.js** e **TailwindCSS**.

## Objetivo do Projeto

O objetivo deste projeto é criar uma plataforma onde eu possa compartilhar informações pessoais de forma organizada, utilizando as tecnologias Nuxt.js e Vue.js para a parte de front-end e TailwindCSS para estilização. O blog possui páginas interativas sobre:

- **Contatos**: Apresenta informações de contato, como WhatsApp, e-mail, LinkedIn e GitHub.
- **Carreira**: Detalhes sobre minha trajetória profissional.
- **Formação Acadêmica**: Informações sobre a minha formação acadêmica.
- **Vida Pessoal**: Informações sobre a minha vida pessoal.

## Tecnologias Utilizadas

- **Nuxt.js**: Framework baseado em Vue.js para a construção da interface e navegação.
- **Vue.js**: Framework JavaScript para construção de componentes.
- **TailwindCSS**: Framework CSS para estilização do layout.
- **Vue Router**: Para navegação entre as diferentes páginas do blog.
- **Vite**: Para o gerenciamento do ambiente de desenvolvimento e build do projeto.

## Como Rodar o Projeto Localmente

Para rodar o projeto localmente, siga os passos abaixo:

1. **Clone o repositório**:

   git clone https://github.com/carolcapitani/projetoCarol.git

Instale as dependências: Navegue até a pasta do projeto e execute o comando para instalar as dependências:

cd nome-do-repositorio
npm install
Ou, se preferir, use o pnpm, yarn ou bun para instalar as dependências:

pnpm install
# ou
yarn install
# ou
bun install


Rodando o servidor de desenvolvimento: Após a instalação das dependências, execute o seguinte comando para iniciar o servidor local:


npm run dev
# ou
pnpm dev
# ou
yarn dev
# ou
bun run dev

O servidor estará disponível em http://localhost:3000. Abra essa URL no seu navegador para ver o blog em funcionamento.

## Como Fazer o Build do Projeto
Para gerar a versão otimizada do seu projeto para produção, basta rodar o seguinte comando:

npm run build
# ou
pnpm build
# ou
yarn build
# ou
bun run build

Isso criará a versão de produção do seu projeto na pasta .output/

## Como Rodar em produção
Após gerar o build, você pode entregar o projeto em produção da seguinte forma:

Acesse Netlify.
Faça login e crie um novo site a partir do repositório Git.
Na configuração de build, configure o seguinte:
Build Command: npm run build (ou pnpm build, yarn build ou bun run build)
Publish Directory: .output/public (ou o diretório equivalente gerado pelo Nuxt.js).
Clique em "Deploy site" e o Netlify fará o deploy do seu projeto.

## Estrutura do Projeto
O projeto está estruturado da seguinte forma:

├── public/                 # Arquivos públicos, como imagens
│   └── images/             # Imagens do blog
├── src/                    # Arquivos de código-fonte
│   ├── assets/             # Arquivos estáticos
│   ├── components/         # Componentes Vue reutilizáveis
│   ├── pages/              # Páginas (contatos, carreira, vida pessoal, formação acadêmica)
│   ├── App.vue             # Componente principal
│   └── main.js             # Arquivo de entrada do Vue
├── nuxt.config.js          # Arquivo de configuração do Nuxt.js
├── tailwind.config.js      # Arquivo de configuração do TailwindCSS
├── package.json            # Dependências e scripts do projeto
└── README.md               # Este arquivo

