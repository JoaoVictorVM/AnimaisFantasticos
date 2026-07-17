# Animais Fantásticos

Projeto desenvolvido durante o curso **JavaScript Completo ES6+** da [Origamid](https://www.origamid.com/). É uma landing page de uma reserva de animais fantásticos que serve de laboratório para aplicar os principais conceitos de JavaScript moderno: classes, módulos ES6, `async/await`, `fetch`, manipulação do DOM, eventos e organização de código com Webpack e Babel.

## 🐾 Demonstração

A página é composta por seções de **Animais**, **FAQ**, **Galeria**, **Números** e **Contato**, cada uma explorando uma funcionalidade construída do zero em JavaScript puro (sem bibliotecas de UI).

## ✨ Funcionalidades

Cada funcionalidade é um módulo independente em `js/modules/`, ativado a partir de `js/script.js`:

| Módulo | Descrição |
| --- | --- |
| `scroll-suave.js` | Rolagem suave até as âncoras do menu |
| `accordion.js` | Abre/fecha as respostas do FAQ |
| `tabnav.js` | Navegação por abas na seção de animais |
| `modal.js` | Abertura e fechamento do modal de login |
| `tooltip.js` | Tooltip que segue o cursor no mapa de contato |
| `dropdown-menu.js` | Menu suspenso (funciona no clique em mobile e no hover em desktop) |
| `menu-mobile.js` | Menu responsivo com botão de abrir/fechar |
| `funcionamento.js` | Indica se o estabelecimento está aberto com base no dia e horário |
| `outsideclick.js` | Utilitário que detecta cliques fora de um elemento (usado por modal e dropdown) |
| `scroll-anima.js` | Anima elementos conforme entram na tela durante o scroll |
| `anima-numeros.js` | Animação de contagem crescente dos números |
| `fetch-animais.js` | Busca os dados dos animais via `fetch` e monta a grade de números |
| `fetch-bitcoin.js` | Busca a cotação do Bitcoin em uma API externa |
| `slide.js` | Slider/carrossel de imagens com suporte a arrastar (mouse e touch) e controles de navegação |
| `debounce.js` | Utilitário de debounce para otimizar eventos como `resize` |

## 🛠️ Tecnologias

- **HTML5** e **CSS3** (organização por componentes em `css/`)
- **JavaScript ES6+** — classes, módulos, `async/await`, `fetch`, arrow functions
- **[Webpack](https://webpack.js.org/)** — empacotamento dos módulos em `main.js`
- **[Babel](https://babeljs.io/)** — transpilação para compatibilidade com navegadores mais antigos
- **[ESLint](https://eslint.org/)** — padronização do código

## 📁 Estrutura do projeto

```
animais-fantasticos/
├── css/                  # Estilos separados por componente
├── img/                  # Imagens e ícones (SVG, JPG, PNG)
├── js/
│   ├── modules/          # Módulos de cada funcionalidade
│   └── script.js         # Ponto de entrada — inicializa os módulos
├── animaisapi.json       # "API" local com o total de cada espécie
├── index.html            # Página principal
├── main.js               # Bundle gerado pelo Webpack (não editar manualmente)
├── webpack.config.js     # Configuração do Webpack + Babel
├── eslint.config.mjs     # Regras do ESLint
└── package.json
```

## 🚀 Como executar

Pré-requisitos: [Node.js](https://nodejs.org/) instalado.

1. Clone o repositório e acesse a pasta:

   ```bash
   git clone <url-do-repositorio>
   cd animais-fantasticos
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Gere o bundle. Você pode:

   - Compilar em modo de desenvolvimento e observar as alterações:

     ```bash
     npm run dev
     ```

   - Ou gerar a versão de produção:

     ```bash
     npm run build
     ```

4. Abra o `index.html` no navegador. Como o projeto usa `fetch` para carregar `animaisapi.json`, sirva os arquivos por um servidor local (por exemplo, a extensão **Live Server** do VS Code) para evitar bloqueios de CORS ao abrir o arquivo diretamente.

## 📜 Scripts disponíveis

| Comando | Ação |
| --- | --- |
| `npm run dev` | Compila em modo desenvolvimento e recompila automaticamente ao salvar (`--watch`) |
| `npm run build` | Gera o bundle otimizado para produção |

## 📚 Créditos

Projeto criado como parte do curso **JavaScript Completo ES6+** da [Origamid](https://www.origamid.com/), com fins de estudo.
