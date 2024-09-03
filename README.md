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

* [Instalações](#instalações)
* [Roadmap](#roadmap)
  * [História do Next.js](#história-do-next)
  * [O que é Next.js?](#o-que-é-next)
  * [Usando o Next](#usando-o-next)
* [Contato](#contato)
* [License](#license)


## Instalações

Siga com precisão as orientações de configuração do ambiente para assegurar eficácia consistente no desenvolvimento do projeto.

### Recursos adicionais
<!-- Aqui você pode inserir sites ou ferramentas online que não serão necessárias instalar, mas serão necessárias para realizar o projeto-->
- **[Nome](site para download aqui)**

## Roadmap
### História do Next

O desenvolvimento front-end evoluiu com o tempo, e uma das grandes inovações recentes é o Next.js. Ele é um framework para React que facilita a criação de aplicações web completas e otimizadas.

#### 🌐 O início

Antes do Next.js, a construção de aplicações React envolvia configurar manualmente o roteamento, o gerenciamento de estado e a Otimização de Motor de Busca (SEO). Isso resultava em:
- Configuração Manual: Necessidade de configurar roteamento e otimizações manualmente.
- Desafios com SEO: Aplicações React geralmente enfrentam dificuldades com SEO, pois o conteúdo é carregado no cliente.

#### 🚀 A Solução: Next

Next.js resolve esses problemas oferecendo uma solução pronta para construir aplicações React com recursos avançados, como:
- **Renderização no servidor (SSR)**: Renderiza as páginas no servidor antes de enviá-las para o cliente.
- **Geração de páginas estáticas (SSG)**: Gera páginas estáticas otimizadas para melhor performance.
- **Roteamento automático**: As rotas são baseadas na estrutura de pastas do projeto.

#### ✅ Benefícios do Next
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

### Usando o Next


#### Estilização

No Next.js, você pode estilizar sua aplicação de diversas maneiras. As principais opções incluem:

1. CSS Modules:
CSS Modules permitem que você escreva CSS que é escopado para um componente específico, evitando conflitos de nomes e garantindo que os estilos sejam aplicados apenas ao componente desejado.

- Crie um arquivo CSS com o sufixo .module.css. Por exemplo, `Button.module.css`.
``` jsx
// Button.module.css
.primary {
  background-color: blue;
  color: white;
}
```
- Importe o arquivo CSS no componente onde os estilos serão aplicados.
- Aplique os estilos usando a sintaxe `styles.nomeDaClasse`.

``` jsx
// Button.js
import styles from './Button.module.css';

function Button() {
  return <button className={styles.primary}>Click me</button>;
}

export default Button;
```

2. Styled Components:
   
styled-components é uma biblioteca que permite definir estilos diretamente no código JavaScript, criando componentes estilizados com sintaxe similar ao CSS.

- Instale a biblioteca
  
``` bash
npm install styled-components
```

- Crie componentes estilizados diretamente usando a função `styled`.

``` jsx
// Button.js
import styled from 'styled-components';

const Button = styled.button`
  background-color: blue;
  color: white;
`;

export default Button;
```

3. Global Styles: 

Para aplicar estilos globais, você pode criar um arquivo CSS e importá-lo no arquivo `_app.js`. Isso garante que os estilos sejam aplicados a toda a aplicação.

``` jsx
// styles/globals.css
body {
  font-family: Arial, sans-serif;
}
```

``` jsx
// _app.js
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />;
}

export default MyApp;
```

##### 👨‍🏫 Hora de Praticar 01

Agora que você aprendeu as diferentes maneiras de estilizar sua aplicação Next.js, é hora de colocar esse conhecimento em prática. Complete os exercícios abaixo para consolidar seu aprendizado.

1. CSS Modules:
- Crie um componente chamado `Card.js` que exiba informações sobre um produto.
- Crie um arquivo de estilos `Card.module.css` com a classe `.card` que define um fundo cinza claro, borda arredondada e um padding de 20px.
- Importe o `Card.module.css` no seu componente `Card.js` e aplique os estilos usando `className`.

```jsx
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
import styles from './Card.module.css';

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
import styled from 'styled-components';

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
> Não se esqueca de instalar o biblioteca `styled-components`.

3. Global Styles:

- Crie um arquivo `globals.css` na pasta `styles/` e defina estilos básicos para a sua aplicação, como o estilo do corpo da página, fontes, e margens padrões.
  
```jsx
/* styles/globals.css */
body {
  margin: 0;
  padding: 0;
  font-family: 'Arial', sans-serif;
  background-color: #f9f9f9;
}

h1, h2, h3, h4, h5, h6 {
  color: #333;
}
```

- Implemente os estilos globais na aplicação importando o `globals.css` dentro do arquivo `_app.js`.

```jsx
// _app.js
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />;
}

export default MyApp;

```

#### Otimização
Next.js oferece várias otimizações que ajudam a melhorar a performance da sua aplicação:

1. Otimização de Imagens:

O componente `next/image` é otimizado para fornecer imagens responsivas e carregadas de forma eficiente. Ele garante que as imagens sejam carregadas apenas quando necessário e são redimensionadas automaticamente para diferentes tamanhos de tela.

``` jsx
import Image from 'next/image';

function HomePage() {
  return <Image src="/me.png" alt="Me" width={500} height={500} />;
}

export default HomePage;
```

2. Otimização de Links:

O componente `next/link` melhora a navegação pré-carregando as páginas vinculadas para que a troca entre páginas seja mais rápida.

``` jsx
import Link from 'next/link';

function HomePage() {
  return (
    <Link href="/about">
      <a>Go to About</a>
    </Link>
  );
}

export default HomePage;
```

3. Otimização de Fontes:

Utilize o `next/font` para carregar fontes de forma eficiente, garantindo que elas sejam otimizadas e carregadas apenas quando necessário.

``` jsx
import { Inter } from 'next/font/google';

const inter = Inter({ subsets: ['latin'] });

function HomePage() {
  return <div className={inter.className}>Hello World</div>;
}

export default HomePage;
```
##### 👨‍🏫 Hora de Praticar 02

Nesta seção, você vai praticar algumas das principais otimizações oferecidas pelo Next.js, incluindo a otimização de imagens, links e fontes. Siga os exercícios para aprender como aplicar essas técnicas na sua aplicação.

1. Otimização de Imagens:
   - Crie uma nova página chamada `Gallery.js` no diretório `pages/`.
   - Utilize o componente `next/image` para exibir duas imagens de sua escolha. Para testar, você pode usar imagens locais na pasta `public/` ou imagens externas.
   - Configure as imagens para serem responsivas utilizando as propriedades `layout="responsive"` e ajuste o `width` e `height` conforme necessário.


   ```jsx
   // pages/Gallery.js
   import Image from 'next/image';

   function Gallery() {
     return (
       <div>
         <h1>Galeria de Imagens</h1>
         <Image src="/image1.jpg" alt="Imagem 1" width={800} height={600} layout="responsive" />
         <Image src="/image2.jpg" alt="Imagem 2" width={800} height={600} layout="responsive" />
       </div>
     );
   }

   export default Gallery;
```

1. Otimização de Links:
   - Adicione um link de navegação para a página Gallery na página principal (index.js).
   - Utilize o componente next/link para garantir que a página de destino seja pré-carregada.

```jsx
// pages/index.js
import Link from 'next/link';

function HomePage() {
  return (
    <div>
      <h1>Página Principal</h1>
      <Link href="/gallery">
        <a>Ir para Galeria</a>
      </Link>
    </div>
  );
}

export default HomePage;
```

3. Otimização de Fontes:
- Escolha uma fonte do [Google Fonts](https://fonts.google.com/), como Roboto, e configure-a para ser carregada de forma otimizada em seu projeto.
- Aplique a fonte no componente principal da página `Gallery.js`.

```jsx
// pages/Gallery.js
import Image from 'next/image';
import { Roboto } from 'next/font/google';

const roboto = Roboto({ subsets: ['latin'], weight: '400' });

function Gallery() {
  return (
    <div className={roboto.className}>
      <h1>Galeria de Imagens com Fonte Roboto</h1>
      <Image src="/image1.jpg" alt="Imagem 1" width={800} height={600} layout="responsive" />
      <Image src="/image2.jpg" alt="Imagem 2" width={800} height={600} layout="responsive" />
    </div>
  );
}

export default Gallery;
```

#### Roteamento

O Next.js usa o sistema de arquivos para gerenciamento de rotas, o que simplifica a criação de páginas e navegação:

1. Rotas Simples:
Crie um arquivo com o nome da rota desejada dentro da pasta `pages/`. O nome do arquivo corresponde à URL da página.

``` jsx
// pages/about.js
export default function About() {
  return <div>About Page</div>;
}
```

2. Rotas Aninhadas:

Organize os arquivos em subpastas para criar rotas aninhadas e layouts complexos.

```jsx
// pages/blog/index.js
export default function BlogHomePage() {
  return <div>Welcome to the Blog</div>;
}
```

``` jsx
// pages/blog/[slug].js
export default function BlogPost({ params }) {
  return <div>Post: {params.slug}</div>;
}
```
##### 👨‍🏫 Hora de Praticar 03

Nesta seção, você vai praticar o roteamento básico do Next.js, explorando rotas simples, rotas aninhadas e rotas dinâmicas. Siga os exercícios abaixo para entender como o Next.js gerencia rotas usando o sistema de arquivos.

1. **Rotas Simples:**
   - No diretório `pages/`, crie um arquivo chamado `contact.js`.
   - Adicione um componente simples que exiba uma mensagem de contato.

```jsx
   // pages/contact.js
   export default function Contact() {
     return <div>Página de Contato</div>;
   }
```
  - Teste sua aplicação acessando a rota `/contact` no navegador para verificar se a página foi criada corretamente.

2. **Rotas Aninhadas:**
   - Crie uma subpasta chamada blog dentro da pasta `pages/`.
   - Adicione um arquivo `index.js` dentro da pasta `blog/` para a página inicial do blog. 

```jsx
// pages/blog/index.js
export default function BlogHomePage() {
  return <div>Bem-vindo ao Blog</div>;
}
```

- Na pasta blog, crie um arquivo [slug].js para capturar URLs dinâmicas.

```jsx
// pages/blog/[slug].js
import { useRouter } from 'next/router';

export default function BlogPost() {
  const router = useRouter();
  const { slug } = router.query;

  return <div>Post: {slug}</div>;
}
```

- Teste a rota aninhada acessando `/blog` e a rota dinâmica acessando `/blog/primeiro-post`.

#### Busca de Dados
O Next.js oferece diferentes métodos para buscar dados dependendo da necessidade de renderização estática ou dinâmica:

1. getStaticProps:

Para páginas que não mudam frequentemente, você pode usar `getStaticProps` para gerar as páginas estaticamente durante a construção.
   
``` jsx
export async function getStaticProps() {
  const res = await fetch('https://api.github.com/repos/vercel/next.js');
  const repo = await res.json();

  return {
    props: { repo },
  };
}

export default function Repo({ repo }) {
  return <div>{repo.name}</div>;
}
```

2. getServerSideProps: 

Para páginas que precisam de dados atualizados a cada requisição, use `getServerSideProps` para renderizar a página no lado do servidor.

``` jsx
export async function getServerSideProps() {
  const res = await fetch('https://api.github.com/repos/vercel/next.js');
  const repo = await res.json();

  return {
    props: { repo },
  };
}

export default function Repo({ repo }) {
  return <div>{repo.name}</div>;
}
```

##### 👨‍🏫 Hora de Praticar 04

Nesta seção, você vai praticar a busca de dados no Next.js, explorando as funções `getStaticProps` e `getServerSideProps`. Siga os exercícios abaixo para aplicar esses conceitos em situações práticas.

1. **Usando `GetStaticProps`:**
   - No diretório `pages/`, crie um arquivo chamado `github-user.js`.
   - Utilize `getStaticProps` para buscar dados de um usuário do GitHub usando a API do GitHub.
  
  ```jsx
   // pages/github-user.js
   export async function getStaticProps() {
     const res = await fetch('https://api.github.com/users/octocat');
     const user = await res.json();

     return {
       props: { user },
     };
   }

   export default function GithubUser({ user }) {
     return (
       <div>
         <h1>{user.name}</h1>
         <p>{user.bio}</p>
         <img src={user.avatar_url} alt={user.name} width={100} />
       </div>
     );
   }
  ```

2. **Usando `GetServerSideProps`:**
  - Crie um arquivo weather.js dentro da pasta pages.
   - Utilize getServerSideProps para buscar dados do clima de uma API (por exemplo, OpenWeather) com base na cidade especificada.

```jsx
// pages/weather.js
export async function getServerSideProps() {
  const res = await fetch('https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=London');
  const weather = await res.json();

  return {
    props: { weather },
  };
}

export default function Weather({ weather }) {
  return (
    <div>
      <h1>Clima em {weather.location.name}</h1>
      <p>Temperatura: {weather.current.temp_c}°C</p>
      <p>Condição: {weather.current.condition.text}</p>
    </div>
  );
}
```
> **Nota:** Lembre-se de substituir YOUR_API_KEY pela sua chave de API do [OpenWeather](https://openweathermap.org/).


#### Busca e Paginação

Você pode implementar a busca e a paginação utilizando parâmetros de URL para filtrar e navegar entre os dados.

``` jsx
// pages/search.js
import { useState, useEffect } from 'react';

export default function SearchPage({ searchTerm, page }) {
  const [data, setData] = useState([]);

  useEffect(() => {
    async function fetchData() {
      const res = await fetch(`/api/search?q=${searchTerm}&page=${page}`);
      const result = await res.json();
      setData(result);
    }

    fetchData();
  }, [searchTerm, page]);

  return <div>{data.map(item => <p key={item.id}>{item.name}</p>)}</div>;
}

SearchPage.getInitialProps = ({ query }) => {
  return {
    searchTerm: query.q || '',
    page: query.page || 1,
  };
};

```

##### 👨‍🏫 Hora de Praticar 05

Nesta prática, você vai implementar busca e paginação utilizando parâmetros de URL para filtrar e navegar pelos dados na sua aplicação Next.js.

1. Implementando busca e paginação
   - No diretório `pages/`, crie um arquivo chamado `search.js`.
   - Utilize o código abaixo para começar a implementação.

```jsx
   // pages/search.js
   import { useState, useEffect } from 'react';

   export default function SearchPage({ searchTerm, page }) {
     const [data, setData] = useState([]);

     useEffect(() => {
       async function fetchData() {
         const res = await fetch(`/api/search?q=${searchTerm}&page=${page}`);
         const result = await res.json();
         setData(result);
       }

       fetchData();
     }, [searchTerm, page]);

     return (
       <div>
         <h1>Resultados da Busca</h1>
         {data.map((item) => (
           <p key={item.id}>{item.name}</p>
         ))}
         <Pagination searchTerm={searchTerm} page={parseInt(page)} />
       </div>
     );
   }

   SearchPage.getInitialProps = ({ query }) => {
     return {
       searchTerm: query.q || '',
       page: query.page || 1,
     };
   };

   function Pagination({ searchTerm, page }) {
     return (
       <div>
         {page > 1 && (
           <a href={`/search?q=${searchTerm}&page=${page - 1}`}>Anterior</a>
         )}
         <span> Página {page} </span>
         <a href={`/search?q=${searchTerm}&page=${page + 1}`}>Próxima</a>
       </div>
     );
   }
```
- Teste a aplicação acessando `/search?q=example&page=1`.
  - Modifique o termo de busca e os números de página na URL para testar a navegação entre os resultados.

### Prática

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
import { useState } from 'react';

// Função para buscar dados do repositório do GitHub
async function fetchRepoData(owner, repo) {
  const res = await fetch(`https://api.github.com/repos/${owner}/${repo}`);
  if (!res.ok) {
    throw new Error('Failed to fetch repository data');
  }
  return res.json();
}

// Componente da página
export default function Repo({ repo }) {
  const [data, setData] = useState(repo);

  return (
    <div>
      <h1>{data.name}</h1>
      <p><strong>Description:</strong> {data.description}</p>
      <p><strong>Stars:</strong> {data.stargazers_count}</p>
      <p><strong>Forks:</strong> {data.forks_count}</p>
      <p><strong>Language:</strong> {data.language}</p>
      <a href={data.html_url} target="_blank" rel="noopener noreferrer">View on GitHub</a>
    </div>
  );
}

// Função para obter dados do repositório no lado do servidor
export async function getServerSideProps(context) {
  const { owner = 'vercel', repo = 'next.js' } = context.query;

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
