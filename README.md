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

- CSS Modules: Utilizando módulos de CSS, você pode garantir que o escopo dos estilos seja isolado a um componente específico. Os arquivos de estilo são nomeados com a extensão `.module.css`.

```
import styles from './Button.module.css';

function Button() {
  return <button className={styles.primary}>Click me</button>;
}
```
- Styled Components: Integração com bibliotecas como `styled-components` para definir estilos diretamente no JavaScript.
```
import styled from 'styled-components';

const Button = styled.button`
  background-color: blue;
  color: white;
`;

export default Button;
```
- Global Styles: Adicionando estilos globais com um arquivo `.css` importado no arquivo `_app.js`.
```
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />;
}

export default MyApp;
```
#### Otimização
Next.js oferece várias otimizações que ajudam a melhorar a performance da sua aplicação:

- Otimização de Imagens: O componente `next/image` oferece carregamento automático de imagens responsivas e otimizadas.
```
import Image from 'next/image';

function HomePage() {
  return <Image src="/me.png" alt="Me" width={500} height={500} />;
}

export default HomePage;
```
- Otimização de Links: O componente `next/link` permite o carregamento antecipado das páginas, melhorando a navegação.
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
- Otimização de Fontes: Utilizando o `next/font`, você pode carregar fontes de forma eficiente e otimizada.
#### Roteamento
O roteamento em Next.js é baseado no sistema de arquivos, o que facilita a criação de páginas e layouts aninhados:
- Rotas Simples: Colocando um arquivo about.js em `pages/`, você cria automaticamente uma rota `/about`.
- Rotas Aninhadas: Você pode criar layouts aninhados organizando os arquivos em subpastas.
```
// pages/blog/index.js
export default function BlogHomePage() {
  return <div>Welcome to the Blog</div>;
}

// pages/blog/[slug].js
export default function BlogPost({ params }) {
  return <div>{params.slug}</div>;
}
```
#### Busca de Dados
Next.js suporta várias formas de buscar dados:
- getStaticProps: Para renderização estática.
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
- getServerSideProps: Para renderização no lado do servidor.
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
- SWC: Integração com bancos de dados hospedados no Vercel e boas práticas para busca e streaming de dados.
#### Busca e Paginação
Você pode implementar busca e paginação utilizando parâmetros de busca na URL:
```
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
### Boas Práticas

- Organização de Componentes: Organize os componentes por funcionalidade.
- Uso de Estilos: Utilize CSS Modules para estilizar componentes de forma modular.
- Gerenciamento de Dados: Use getStaticProps e getServerSideProps para buscar dados de forma eficiente.

## Contato

Mariana Almeida - [marianaalmeidafga@gmail.com](mailto:marianaalmeidafga@gmail.com).
GitHub: [github.com/marialmeida1](https://github.com/marialmeida1)

## License

Este projeto é licenciado sob a [Nome da Licença](URL da Licença) - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

