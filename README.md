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
- Renderização no Lado do Servidor (SSR): Melhora o SEO e o tempo de carregamento inicial.
- Gerenciamento de Rotas Automático: Facilita a criação de páginas e a navegação.
- Otimização Automática: Inclui otimização de performance e divisão de código por padrão.

#### ✅ Benefícios do Next
- Otimização de Performance: Divisão de código automática e otimização de imagens.
- Estabilidade Visual: Garantia de uma experiência de usuário consistente com renderização do lado do servidor e renderização estática.
- Carregamento Rápido de Página: Melhoria no tempo de carregamento com pré-renderização e geração de páginas estáticas.

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
```
// Button.module.css
.primary {
  background-color: blue;
  color: white;
}
```
- Importe o arquivo CSS no componente onde os estilos serão aplicados.
- Aplique os estilos usando a sintaxe `styles.nomeDaClasse`.

```
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
  
```
npm install styled-components
```

- Crie componentes estilizados diretamente usando a função `styled`.

```
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

```
// styles/globals.css
body {
  font-family: Arial, sans-serif;
}
```

```
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

```
import Image from 'next/image';

function HomePage() {
  return <Image src="/me.png" alt="Me" width={500} height={500} />;
}

export default HomePage;
```

2. Otimização de Links:

O componente `next/link` melhora a navegação pré-carregando as páginas vinculadas para que a troca entre páginas seja mais rápida.

```
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

```
import { Inter } from 'next/font/google';

const inter = Inter({ subsets: ['latin'] });

function HomePage() {
  return <div className={inter.className}>Hello World</div>;
}

export default HomePage;
```

#### Roteamento

O Next.js usa o sistema de arquivos para gerenciamento de rotas, o que simplifica a criação de páginas e navegação:

1. Rotas Simples:
Crie um arquivo com o nome da rota desejada dentro da pasta `pages/`. O nome do arquivo corresponde à URL da página.

```
// pages/about.js
export default function About() {
  return <div>About Page</div>;
}
```

2. Rotas Aninhadas:

Organize os arquivos em subpastas para criar rotas aninhadas e layouts complexos.

```
// pages/blog/index.js
export default function BlogHomePage() {
  return <div>Welcome to the Blog</div>;
}
```

```
// pages/blog/[slug].js
export default function BlogPost({ params }) {
  return <div>Post: {params.slug}</div>;
}
```
#### Busca de Dados
O Next.js oferece diferentes métodos para buscar dados dependendo da necessidade de renderização estática ou dinâmica:

1. getStaticProps:

Para páginas que não mudam frequentemente, você pode usar `getStaticProps` para gerar as páginas estaticamente durante a construção.
   
```
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

```
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

#### Busca e Paginação

Você pode implementar a busca e a paginação utilizando parâmetros de URL para filtrar e navegar entre os dados.

```
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
### Prática

1. Configuração do Projeto

Primeiro, crie um novo projeto Next.js se ainda não tiver um. Você pode fazer isso usando o comando:

```
npx create-next-app@latest github-repo-viewer
```

Navegue para o diretório do projeto:

```
cd github-repo-viewer
```

2. Criação da Página

Vamos criar uma página que mostra informações sobre um repositório do GitHub. Crie um novo arquivo chamado repo.js dentro da pasta pages/.

```
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

```
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
