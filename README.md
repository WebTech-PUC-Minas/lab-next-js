<!-- Exemplo de uso do template: https://github.com/kspencerl/lab-springboot-basic-api -->

# Lab Next.js

Construção de uma Página utilizando Next.js.

## Tecnologias utilizadas

Linguagens, Frameworks e Bibliotecas utilizadas na construção do projeto.

<!-- Link com os badges para inserir abaixo https://devicon.dev/ -->
<div style="display: flex; gap: 10px;">
  <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg">
  <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg">
  <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/npm/npm-original-wordmark.svg">
  <img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg" />    
</div>

## Onde Aplicar

Este projeto pode ser aplicado em diversas situações:

- Desenvolvimento de sites e aplicações web.
- Desenvolvimento de componentes reutilizáveis.
- Integrações com back-end.
- Construções de dashboards.

# Sumário

- [História do Next](#história-do-next)
  - [O início](#-o-início)
  - [A Solução: Next](#-a-solução-next)
  - [Benefícios do Next](#-benefícios-do-next)
  - [O que é Next?](#o-que-é-next)
    - [Objetivo do Next](#-objetivo-do-next)
- [Roadmap](#roadmap)
  - [Estilização](#estilização)
    - [Hora de Praticar 01](#-hora-de-praticar-01)
  - [Roteamento](#roteamento)
    - [Hora de Praticar 02](#-hora-de-praticar-02)
  - [Otimização](#otimização)
    - [Hora de Praticar 03](#-hora-de-praticar-03)
  - [Busca de Dados](#busca-de-dados)
    - [Hora de Praticar 04](#-hora-de-praticar-04)
- [Boas Práticas](#boas-práticas)

## Instalações

Siga com precisão as orientações de configuração do ambiente para assegurar eficácia consistente no desenvolvimento do projeto.

### Recursos adicionais

<!-- Aqui você pode inserir sites ou ferramentas online que não serão necessárias instalar, mas serão necessárias para realizar o projeto-->

- **[Nome](site para download aqui)**

## História do Next

O desenvolvimento front-end evoluiu com o tempo, e uma das grandes inovações recentes é o Next.js. Ele é um framework para React que facilita a criação de aplicações web completas e otimizadas.

### 🌐 O início

Antes do Next.js, a construção de aplicações React envolvia configurar manualmente o roteamento, o gerenciamento de estado e a Otimização de Motor de Busca (SEO). Isso resultava em:

- Configuração Manual: Necessidade de configurar roteamento e otimizações manualmente.
- Desafios com SEO: Aplicações React geralmente enfrentam dificuldades com SEO, pois o conteúdo é carregado no cliente.

### 🚀 A Solução: Next

Next.js resolve esses problemas oferecendo uma solução pronta para construir aplicações React com recursos avançados, como:

- **Renderização no servidor (SSR)**: Renderiza as páginas no servidor antes de enviá-las para o cliente.
- **Geração de páginas estáticas (SSG)**: Gera páginas estáticas otimizadas para melhor performance.
- **Roteamento automático**: As rotas são baseadas na estrutura de pastas do projeto.

### ✅ Benefícios do Next

- **Otimização de Performance:** Divisão de código automática e otimização de imagens.
- **Estabilidade Visual:** Garantia de uma experiência de usuário consistente com renderização do lado do servidor e renderização estática.
- **Carregamento Rápido de Página:** Melhoria no tempo de carregamento com pré-renderização e geração de páginas estáticas.

### O que é Next?

Next.js é um framework para React que permite criar aplicações web com funcionalidades avançadas de forma simples e eficiente. Desenvolvido pela Vercel, ele é ideal para construir sites rápidos, escaláveis e otimizados para SEO.

#### 🎯 Objetivo do Next

O Next.js visa facilitar a criação de aplicações web otimizadas, permitindo:

- Renderização no Lado do Servidor: Gera páginas no servidor para melhorar o SEO e a performance.
- Gerenciamento de Rotas: Automatiza a criação de rotas com base na estrutura de arquivos.
- Otimização de Performance: Oferece suporte a recursos como pré-carregamento de páginas e otimização de imagens.

## Roadmap

### 🎨 Estilização

No Next.js, você pode estilizar sua aplicação de diversas maneiras. As principais opções incluem:

1. CSS Modules:
   CSS Modules permitem que você escreva CSS que é escopado para um componente específico, evitando conflitos de nomes e garantindo que os estilos sejam aplicados apenas ao componente desejado.

- Crie um arquivo CSS com o sufixo .module. Por exemplo, `Button.module.css`.

```css
/* Button.module.css */
.primary {
  background-color: blue;
  color: white;
}
```

- Importe o arquivo CSS no componente onde os estilos serão aplicados.
- Aplique os estilos usando a sintaxe `styles.nomeDaClasse`.

```jsx
// Button.js
import styles from "./Button.module.css";

function Button() {
  return <button className={styles.primary}>Click me</button>;
}

export default Button;
```

2. Styled Components:

styled-components é uma biblioteca que permite definir estilos diretamente no código JavaScript, criando componentes estilizados com sintaxe similar ao CSS.

- Instale a biblioteca

```bash
npm install styled-components
```

- Crie componentes estilizados diretamente usando a função `styled`.

```jsx
// Button.js
import styled from "styled-components";

const Button = styled.button`
  background-color: blue;
  color: white;
`;

export default Button;
```

```jsx
// page.js
import Button from "./components/Button.js";

export default function Home() {
  return <Button>Clique aqui</Button>;
}
```

3. Global Styles:

Para aplicar estilos globais, você pode criar um arquivo CSS e importá-lo no arquivo `layout.js`. Isso garante que os estilos sejam aplicados a toda a aplicação.

```css
/* globals.css */
body {
  font-family: Arial, sans-serif;
}
```

```jsx
// layout.js
import "./globals.css";

export default function RootLayout({ children }) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

#### 👨‍🏫 Hora de Praticar 01

Agora que você aprendeu as diferentes maneiras de estilizar sua aplicação Next.js, é hora de colocar esse conhecimento em prática. Complete os exercícios abaixo para consolidar seu aprendizado.

1. CSS Modules:

- Crie um componente chamado `Card.js` que exiba informações sobre um produto.
- Crie um arquivo de estilos `Card.module.css` com a classe `.card` que define um fundo cinza claro, borda arredondada e um padding de 20px.
- Importe o `Card.module.css` no seu componente `Card.js` e aplique os estilos usando `className`.

```css
// Card.module.css
.card {
  background-color: #f0f0f0;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
```

```jsx
// Card.js
import styles from "./Card.module.css";

function Card() {
  return (
    <div className={styles.card}>
      <h2>Produto 1</h2>
      <p>Descrição do produto.</p>
    </div>
  );
}

export default Card;
```

2. Styled Components:

- Crie um componente `Button.js` utilizando styled-components para definir um botão com fundo verde e texto branco.

```jsx
// Button.js
import styled from "styled-components";

const Button = styled.button`
  background-color: green;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;

  &:hover {
    background-color: darkgreen;
  }
`;

export default Button;
```

> Não se esqueca de instalar a biblioteca `styled-components`.

3. Global Styles:

- O arquivo `globals.css` já é criado automaticamente na pasta `app/`. Insira nele os estilos globais para o corpo da página e os títulos.

```css
/* globals.css */
body {
  margin: 0;
  padding: 0;
  font-family: "Arial", sans-serif;
  background-color: #f9f9f9;
}

h1, h2, h3, h4, h5, h6 {
  color: #333;
}
```

- O `globals.css` também já e importado por padrão dentro do arquivo `layout.js`.

```jsx
// layout.js
import "./globals.css";

export default function RootLayout({ children }) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

### 🗺️ Roteamento

No Next.js, o sistema de roteamento é baseado na estrutura de arquivos e pastas. Cada página do Next.js deve ser representada por um arquivo JavaScript ou TypeScript dentro da pasta `pages/`. O nome da pasta ou do arquivo determinará o caminho da rota correspondente. A seguir, estão os exemplos de roteamento com explicações sobre rotas simples, aninhadas e dinâmicas:

1. Rotas Simples:

Para criar uma rota simples, basta adicionar um arquivo JavaScript dentro da pasta `pages/`, onde o nome da pasta será o nome da rota.

```jsx
// pages/about/page.js
export default function About() {
  return <div>About Page</div>;
}
```

- O arquivo `page.js` dentro da pasta `about\` define a rota `/about`.
- A função exportada será o componente exibido quando o usuário acessar esta rota.

2. Rotas Aninhadas:

Para criar rotas aninhadas, você pode organizar arquivos em subpastas. Isso permite estruturar layouts mais complexos ou criar seções específicas do site.

```jsx
// pages/blog/page.js
export default function BlogHomePage() {
  return <div>Bem-vindo ao Blog</div>;
}
```

- Aqui, o arquivo `index.js` dentro da pasta `blog\` cria a rota `/blog`, que serve como a página inicial do blog.

```jsx
// pages/blog/[slug].js
export default function BlogPost({ params }) {
  return <div>Post: {params.slug}</div>;
}
```

- Este arquivo define uma rota dinâmica `[slug]`, onde `slug` é um parâmetro de rota variável.
- Por exemplo, ao acessar `/blog/my-first-post`, o valor de slug será "my-first-post".

3. Rotas Dinâmicas:

As rotas dinâmicas permitem que você crie rotas que mudam com base em valores variáveis. Para isso, use colchetes `[]` no nome do arquivo para indicar uma rota dinâmica. No exemplo acima `[slug].js`, o valor de `slug` é passado como parâmetro e pode ser usado dentro do componente.

```jsx
// pages/products/[id].js
export default function ProductPage({ params }) {
  return <div>Product ID: {params.id}</div>;
}
```

- Aqui, `id` é o parâmetro dinâmico, que será substituído por qualquer valor fornecido na URL. Se a rota acessada for `/products/123`, o componente exibirá Product ID: 123.

#### 👨‍🏫 Hora de Praticar 02

Nesta seção, você vai praticar o roteamento básico do Next.js, explorando rotas simples, rotas aninhadas e rotas dinâmicas. Siga os exercícios abaixo para entender como o Next.js gerencia rotas usando o sistema de arquivos e estruturar suas páginas corretamente.

1. **Rotas Simples:**

- No diretório `pages/`, crie uma pasta chamada `contact` e dentro dela uma arquivo com o nome `page.js`.
- Adicione um componente simples que exiba uma mensagem de contato.

```jsx
// pages/contact/page.js
export default function Contact() {
  return <div>Página de Contato</div>;
}
```

- Teste sua aplicação acessando a rota `/contact` no navegador para verificar se a página foi criada corretamente.

> Veja o resultado em: [/contatos](http://localhost:3000/pages/contact)

1. **Rotas Aninhadas:**
   - Crie uma subpasta chamada `products` dentro da pasta `pages/`.
   - Adicione um arquivo `page.js` dentro da pasta `products/` para a página inicial de produtos.

```jsx
// pages/products/page.js
export default function ProductsHomePage() {
  return <div>Bem-vindo à página de produto</div>;
}
```

> Veja o resultado em: [/products](http://localhost:3000/pages/products)

- Dentro da pasta `products/`, crie uma subpasta chamada `electronics/`.
- Adicione um arquivo `page.js` dentro de `electronics/` para a página de produtos eletrônicos.

```jsx
// pages/products/electronics/page.js
export default function ElectronicsPage() {
  return <div>Bem-vindo à seção de Eletrônicos</div>;
}
```

> Veja o resultado em: [/electronics](http://localhost:3000/pages/products/electronics)

- Dentro da pasta `products/`, crie uma subpasta chamada `clothing/`.
- Adicione um arquivo `page.js` dentro de `clothing/` para a página de roupas.

```jsx
// pages/products/clothing/page.js
export default function ClothingPage() {
  return <div>Bem-vindo à seção de Roupas</div>;
}
```

> Veja o resultado em: [/clothing](http://localhost:3000/pages/products/clothing)

3. Rotas Dinâmicas:

- Dentro de `products/`, crie um arquivo `[id]` para representar a página de detalhes de um produto.
- Adicione um arquivo `page.js` dentro de `[id]/` para a página do produto.

```jsx
// pages/products/[id].js
export default function Product() {
  return <h1>Bem-vindo à página do produto</h1>;
}
```

> Veja o resultado em: [/123](http://localhost:3000/pages/products/123)

### ↗️ Otimização

Next.js oferece várias otimizações que ajudam a melhorar a performance da sua aplicação:

1. Otimização de Imagens:

O componente `next/image` é otimizado para fornecer imagens responsivas e carregadas de forma eficiente. Ele garante que as imagens sejam carregadas apenas quando necessário e são redimensionadas automaticamente para diferentes tamanhos de tela.

```jsx
import Image from "next/image";

function HomePage() {
  return <Image src="/me.png" alt="Me" width={500} height={500} />;
}

export default HomePage;
```

Quando você deseja utilizar imagens de domínios externos com o componente next/image, é necessário configurar o arquivo next.config.js. Isso é importante para que o Next.js saiba que essas imagens são seguras e estão autorizadas a serem carregadas.

```jsx
import Image from "next/image";

function Gallery() {
  return (
    <div>
      <h1>Galeria de Imagens</h1>
      <Image
        src="https://images.pexels.com/photos/4665189/pexels-photo-4665189.jpeg?cs=srgb&dl=papel-de-parede-4k-wallpaper-4k-praia-litoral-4665189.jpg&fm=jpg"
        alt="Imagem 1"
        width={300}
        height={200}
      />
      <Image
        src="https://images.pexels.com/photos/1991621/pexels-photo-1991621.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260"
        alt="Imagem 2"
        width={300}
        height={200}
      />
    </div>
  );
}

export default Gallery;
```

```mjs
/** @type {import('next').NextConfig} */
const nextConfig = {
  images: {
    domains: [
      // exemplo de domínios de imagens:
      "images.unsplash.com", // Unsplash, uma fonte popular de imagens
      "images.pexels.com", // Pexels, outra fonte popular de imagens
      "picsum.photos", // Lorem Picsum, para imagens de espaço reservado
      "static.wikia.nocookie.net", // Wikia, para imagens de wikis
      "external-content.duckduckgo.com", // DuckDuckGo
      "tse4.mm.bing.net", // Bing
    ],
  },
};

export default nextConfig;
```

2. Otimização de Links:

O componente `next/link` melhora a navegação pré-carregando as páginas vinculadas para que a troca entre páginas seja mais rápida.

```jsx
import Link from "next/link";

function HomePage() {
  return <Link href="/about">Go to About</Link>;
}

export default HomePage;
```

3. Otimização de Fontes:

No `next/font`, utilizado para otimizar o carregamento de fontes no Next.js, há vários parâmetros que você pode utilizar para customizar o comportamento das fontes, garantindo que elas sejam carregadas de maneira eficiente. Abaixo estão alguns dos parâmetros principais disponíveis:

1. **subsets:** Define quais subconjuntos da fonte serão carregados. Subconjuntos são grupos de caracteres específicos de uma língua ou conjunto de línguas. Exemplos comuns incluem 'latin', 'latin-ext', 'cyrillic', e outros. Isso garante que apenas os caracteres necessários sejam baixados, reduzindo o tamanho do carregamento.

   - Exemplo: subsets: ['latin', 'latin-ext'].

2. **weight:** Especifica o peso da fonte a ser utilizado. Diferentes pesos controlam a espessura das letras (como normal, negrito, etc.). Isso permite que apenas os pesos necessários sejam baixados, evitando o carregamento desnecessário de variações que não serão usadas.

   - Exemplo: weight: ['400', '700'].

3. **style:** Define o estilo da fonte, como 'normal' ou 'italic'. Similar ao peso, esse parâmetro ajuda a garantir que apenas os estilos necessários sejam baixados.

   - Exemplo: style: ['normal', 'italic'].

4. **display:** Controla como a fonte é exibida durante o carregamento. Valores comuns incluem:
   - **'auto':** O comportamento padrão do navegador.
   - **'block':** A fonte só será exibida quando for totalmente carregada, evitando o "flash of unstyled text" (FOUT).
   - **'swap':** O texto será exibido com uma fonte fallback enquanto a fonte personalizada carrega, evitando o atraso na exibição do conteúdo.
   - **'fallback':** Similar ao 'swap', mas permite uma transição mais suave.
   - **'optional':** Exibe a fonte fallback imediatamente, e a fonte personalizada será carregada opcionalmente (não bloqueia a renderização).
5. **preload:** Um parâmetro booleano que define se a fonte deve ser pré-carregada (true) ou não (false). O pré-carregamento faz com que a fonte seja baixada assim que possível, evitando atrasos no seu uso. Isso é útil quando você sabe que uma fonte específica será necessária imediatamente.
   - Exemplo: preload: true.

```css
/* globals.css */
body {
  margin: 0;
  padding: 0;
  font-family: "Inter", sans-serif; /* Use a fonte Inter como padrão */
  background-color: #f9f9f9;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  color: #333;
}
```

```jsx
// layout.js
import { Inter } from "next/font/google";
import "./globals.css";

const inter = Inter({ subsets: ["latin"] });

export default function Layout({ children }) {
  return <main className={inter.className}>{children}</main>;
}
```

O `next/font` possui alguns parâmetros para

#### 👨‍🏫 Hora de Praticar 03

Nesta seção, você vai praticar algumas das principais otimizações oferecidas pelo Next.js, incluindo a otimização de imagens, links e fontes. Siga os exercícios para aprender como aplicar essas técnicas na sua aplicação.

1. Otimização de Imagens:
   - Crie uma página chamada `page.js` no diretório `pages/Gallery/`.
   - Utilize o componente `next/image` para exibir duas imagens de sua escolha. Para testar, você pode usar imagens locais na pasta `public/` ou imagens externas.
   - Configure as imagens para serem responsivas utilizando as propriedades `layout="responsive"` e ajuste o `width` e `height` conforme necessário.

```jsx
// pages/Gallery.js
import Image from "next/image";

function Gallery() {
  return (
    <div>
      <h1>Galeria de Imagens</h1>
      <Image
        src="https://avatars.githubusercontent.com/u/138007302?s=280&v=4"
        alt="Imagem 1"
        width={800}
        height={600}
        layout="responsive"
      />
      <Image
        src="https://avatars.githubusercontent.com/u/138007302?s=280&v=4"
        alt="Imagem 2"
        width={800}
        height={600}
        layout="responsive"
      />
    </div>
  );
}

export default Gallery;
```

1. Otimização de Links:
   - Adicione um link de navegação para a página Gallery na página principal (`page.js`).
   - Utilize o componente `next/link` para garantir que a página de destino seja pré-carregada.

```jsx
// pages/index.js
import Link from "next/link";

function HomePage() {
  return (
    <div>
      <h1>Página Principal</h1>
      <Link href="/Gallery">Ir para Galeria</Link>
    </div>
  );
}

export default HomePage;
```

1. Otimização de Fontes:

- Escolha uma fonte do [Google Fonts](https://fonts.google.com/), como Roboto, e configure-a para ser carregada de forma otimizada em seu projeto.
- Aplique a fonte no componente principal da página `Gallery.js`.

```jsx
// pages/Gallery.js
import Image from "next/image";
import { Roboto } from "next/font/google";

const roboto = Roboto({ subsets: ["latin"], weight: "400" });

function Gallery() {
  return (
    <div className={roboto.className}>
      <h1>Galeria de Imagens com Fonte Roboto</h1>
      <Image
        src="/image1.jpg"
        alt="Imagem 1"
        width={800}
        height={600}
        layout="responsive"
      />
      <Image
        src="/image2.jpg"
        alt="Imagem 2"
        width={800}
        height={600}
        layout="responsive"
      />
    </div>
  );
}

export default Gallery;
```

### 🔎 Busca de Dados

No Next.js, você pode buscar dados em componentes de página utilizando getStaticProps para geração estática e getServerSideProps para renderização no servidor. No entanto, se estiver usando a nova estrutura do Next.js, você pode simplesmente utilizar a função de busca diretamente dentro do componente.

1. Busca com getStaticProps:

A função `getStaticProps` é usada para gerar páginas estáticas com dados durante o build. Abaixo está um exemplo de como implementar isso na nova estrutura.

```jsx
// app/products/page.js
export default async function Products() {
  const res = await fetch("https://fakestoreapi.com/products");
  const products = await res.json();

  return (
    <div>
      <h1>Lista de Produtos</h1>
      <ul>
        {products.map((product) => (
          <li key={product.id}>
            {product.title} - ${product.price}
          </li>
        ))}
      </ul>
    </div>
  );
}
```

2. Busca com getServerSideProps

A função `getServerSideProps` é utilizada quando você precisa buscar dados no servidor a cada requisição, o que é útil quando os dados mudam com frequência ou precisam ser baseados em informações da requisição.

```jsx
// app/comments/page.js
export default async function Comments() {
  const res = await fetch("https://jsonplaceholder.typicode.com/comments");
  const comments = await res.json();

  return (
    <div>
      <h1>Lista de Comentários</h1>
      <ul>
        {comments.map((comment) => (
          <li key={comment.id}>
            {comment.name}: {comment.body}
          </li>
        ))}
      </ul>
    </div>
  );
}
```

#### 👨‍🏫 Hora de Praticar 04

Nesta seção, você vai praticar a busca de dados no Next.js, explorando as funções `getStaticProps` e `getServerSideProps`. Siga os exercícios abaixo para aplicar esses conceitos em situações práticas.

1. Busca de Dados Estáticos:
   - Crie uma página chamada `products.js`.
   - Utilize a função de busca diretamente no componente para buscar produtos de uma API pública e exibi-los em uma lista.

```jsx
// app/products/page.js
export default async function Products() {
  const res = await fetch("https://fakestoreapi.com/products");
  const products = await res.json();

  return (
    <div>
      <h1>Lista de Produtos</h1>
      <ul>
        {products.map((product) => (
          <li key={product.id}>
            {product.title} - ${product.price}
          </li>
        ))}
      </ul>
    </div>
  );
}
```

> Teste a aplicação acessando a rota `/products` no navegador para verificar se os posts foram carregados corretamente.

2. Busca de Dados no Servidor:

- Crie uma página chamada `comments.js`.
- Utilize a função de busca diretamente no componente para buscar comentários de uma API pública e exibi-los em uma lista.

```jsx
// app/comments/page.js
export default async function Comments() {
  const res = await fetch("https://jsonplaceholder.typicode.com/comments");
  const comments = await res.json();

  return (
    <div>
      <h1>Lista de Comentários</h1>
      <ul>
        {comments.map((comment) => (
          <li key={comment.id}>
            {comment.name}: {comment.body}
          </li>
        ))}
      </ul>
    </div>
  );
}
```

- Teste a aplicação acessando a rota `/comments` no navegador para verificar se os comentarios foram carregados corretamente.

## Prática

1. Configuração do Projeto

Primeiro, crie um novo projeto Next.js se ainda não tiver um. Você pode fazer isso usando o comando:

```bash
npx create-next-app@latest github-repo-viewer
```

Navegue para o diretório do projeto:

```bash
cd github-repo-viewer
```

2. Criação da Página

Vamos criar uma página que mostra informações sobre um repositório do GitHub. Crie um novo arquivo chamado repo.js dentro da pasta pages/.

```jsx
import { useState } from "react";

// Função para buscar dados do repositório do GitHub
async function fetchRepoData(owner, repo) {
  const res = await fetch(`https://api.github.com/repos/${owner}/${repo}`);
  if (!res.ok) {
    throw new Error("Failed to fetch repository data");
  }
  return res.json();
}

// Componente da página
export default function Repo({ repo }) {
  const [data, setData] = useState(repo);

  return (
    <div>
      <h1>{data.name}</h1>
      <p>
        <strong>Description:</strong> {data.description}
      </p>
      <p>
        <strong>Stars:</strong> {data.stargazers_count}
      </p>
      <p>
        <strong>Forks:</strong> {data.forks_count}
      </p>
      <p>
        <strong>Language:</strong> {data.language}
      </p>
      <a href={data.html_url} target="_blank" rel="noopener noreferrer">
        View on GitHub
      </a>
    </div>
  );
}

// Função para obter dados do repositório no lado do servidor
export async function getServerSideProps(context) {
  const { owner = "vercel", repo = "next.js" } = context.query;

  try {
    const repoData = await fetchRepoData(owner, repo);
    return { props: { repo: repoData } };
  } catch (error) {
    return { props: { repo: null } };
  }
}
```

3. Testando a Página

Para testar a página, execute o projeto com:

```bash
npm run dev
```

Abra o navegador e vá para http://localhost:3000/ Você deve ver informações sobre o repositório do Next.js.

### Boas Práticas

- Organização de Componentes: Organize os componentes por funcionalidade.
- Uso de Estilos: Utilize CSS Modules para estilizar componentes de forma modular.
- Gerenciamento de Dados: Use getStaticProps e getServerSideProps para buscar dados de forma eficiente.

## Contato

Mariana Almeida - [marianaalmeidafga@gmail.com](mailto:marianaalmeidafga@gmail.com).
GitHub: [github.com/marialmeida1](https://github.com/marialmeida1)

Nilson Deon Cordeiro Filho - [nilsondeon01@gmail.com](mailto:nilsondeon01@gmail.com@gmail.com).
GitHub: [github.com/NilsonDeon](https://github.com/NilsonDeon)

## License

Este projeto é licenciado sob a [Nome da Licença](URL da Licença) - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.
