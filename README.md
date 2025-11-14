# 🍏 Bariatric Health Care - Apresentação Web

Este repositório contém o código-fonte do site de apresentação institucional para o aplicativo Bariatric Health Care (BHC). O objetivo principal é fornecer uma landing page moderna para descrever a missão do projeto e permitir o acesso à versão web do aplicativo (desenvolvido via FlutterFlow) através de um iframe dedicado.

---

## 🛠️ Tecnologias Utilizadas

* **Framework:** React
* **Build Tool:** Vite
* **Design/Estilização:** React-Bootstrap (com classes customizadas para a paleta de cores BHC)
* **Roteamento:** React Router DOM
* **Integração:** Inclusão do App Web via `iframe` com ajuste de proporção de tela (simulação mobile).

## 🚀 Estrutura do Projeto

O projeto segue uma estrutura modular padrão para aplicações React/Vite:

bariatric-health-care/├── public/                # Arquivos estáticos (Favicon, assets para acesso público)├── src/│   ├── assets/            # Imagens e logo (importadas via JS)│   ├── components/│   │   ├── sections/      # Seções da Home Page (HomeBanner, AboutUs, Contact)│   │   ├── AppPresentation.jsx # Componente que hospeda o iframe do App│   │   └── Footer.jsx     # Rodapé do site│   ├── pages/             # Layouts de página (HomePage, AppPage)│   ├── index.css          # Estilos Globais e Sobrescrita de Cores do Bootstrap│   ├── main.jsx           # Ponto de entrada do React│   └── App.jsx            # Componente principal e Roteamento├── index.html             # Arquivo HTML principal (Configuração do Favicon e Título)└── package.json           # Dependências e Scripts
## ⚙️ Configuração e Instalação

Siga os passos abaixo para configurar e rodar o projeto localmente.

### 1. Clonar o Repositório

```bash
git clone [URL_DO_SEU_REPOSITORIO]
cd bariatric-health-care
2. Instalar DependênciasInstale todas as bibliotecas necessárias, incluindo react-router-dom e react-bootstrap:Bashnpm install
3. Configurar a URL do Aplicativo (FlutterFlow)A URL da versão web do app é configurada no componente dedicado.Abra o arquivo src/pages/AppPage.jsx.Substitua o valor da constante FLUTTERFLOW_URL pela URL correta do seu aplicativo:JavaScriptconst FLUTTERFLOW_URL = "[https://bariatric-health-care-6d8.flutterflow.app](https://bariatric-health-care-6d8.flutterflow.app)";
4. Rodar o Ambiente de DesenvolvimentoInicie o servidor de desenvolvimento do Vite. O site estará acessível em http://localhost:5173.Bashnpm run dev
🔗 Páginas e RoteamentoO site utiliza react-router-dom para navegação:RotaDescriçãoComponente/Landing Page Institucional (SPA)HomePage.jsx/appVisualização do App Web (iframe)AppPage.jsx#sobreÂncora para a seção "Sobre Nós" na HomePage-#contatoÂncora para a seção "Contato" na HomePage-🎨 Paleta de Cores (BHC Theme)As cores primárias e secundárias do Bootstrap foram sobrescritas no src/index.css para utilizar a paleta visual do projeto:Variável CSSCódigo HexUso Principal--color-bhc-dark#294134Fundo da Navbar, Footer, Títulos.--color-bhc-primary#75EBACBotões de Ação (CTA), Destaques.--color-bhc-secondary#80C09ESuporte e Borda.--color-bhc-muted#566B60Textos secundários.📦 Build para ProduçãoPara gerar os arquivos estáticos prontos para deploy (publicação em um servidor ou serviço como Vercel/Netlify):Bashnpm run build
Os arquivos finais estarão na pasta dist/.
Você pode copiar este conteúdo e salvar no arquivo `README.md` na raiz do seu projet
