# FitMaster

O **FitMaster** é uma academia fictícia, desenvolvida com o objetivo principal de aprimorar habilidades na utilização do **Bootstrap** e aprofundar o domínio de suas classes utilitárias e componentes.

Como desafio adicional, o uso de **JavaScript foi proibido**, exigindo que toda a construção da interface, responsividade e interações visuais fossem realizadas exclusivamente com **HTML, CSS e classes do Bootstrap**.

O projeto simula o site de uma academia, reunindo páginas e seções como apresentação principal, modalidades, planos, formulário de contato, login, matrícula e dashboard administrativo.

## Tecnologias utilizadas

- HTML5 - estrutura semântica
- CSS3 - estilização
- Bootstrap - responsividade e layout (Sem JavaScript)
- Git e GitHub - versionamento
- Vercel - deploy da aplicação

## Páginas do projeto

### 1. Início

Página principal do projeto, responsável por apresentar a academia. Contém a hero section, apresentação das modalidades disponíveis, formulário de contato.

### 2. Planos

Página dedicada à apresentação dos planos oferecidos pela academia. Permite comparar benefícios, modalidades incluídas e valores de cada opção.


### 3. Nossa Unidade

Página informativa sobre a localização e horários de funcionamento da academia.


### 4. Login

Área de acesso para autenticação do usuário.

### 5. Matricule-se

Página destinada ao cadastro de novos alunos. Contém formulário para preenchimento de dados pessoais, escolha de plano e confirmação dos termos e condições para conclusão da matrícula.

### 6. Dashboard

Painel administrativo desenvolvido para simular o gerenciamento interno da academia. Apresenta informações organizadas em cards, alertas, metas, mensagens de contato e tabela com dados de alunos.

---

## Principais classes Bootstrap utilizadas

### Layout e estrutura
Classes responsáveis pela organização geral da página e distribuição dos elementos.

- `container`
- `container-fluid`
- `row`
- `col-*`
- `w-100`
- `h-100`
- `min-vh-100`

---

### Flexbox
Utilizadas para alinhamento, espaçamento e reorganização dos elementos.

- `d-flex`
- `flex-column`
- `flex-row`
- `flex-wrap`
- `justify-content-center`
- `justify-content-between`
- `align-items-center`
- `align-items-start`
- `align-self-end`
- `flex-grow-1`

---

### Responsividade
Aplicadas para adaptar o layout em diferentes tamanhos de tela.

- `col-sm-*`
- `col-md-*`
- `col-lg-*`
- `col-xl-*`
- `col-xxl-*`
- `d-none`
- `d-block`
- `d-md-none`
- `d-lg-block`
- `navbar-expand-md`
- `flex-md-row`
- `order-*`

---

### Navegação
Classes usadas na construção da navbar e menu responsivo.

- `navbar`
- `navbar-nav`
- `navbar-collapse`
- `collapse`
- `nav-link`

---

### Cores e aparência
Responsáveis pela personalização visual e estilo dos componentes.

- `text-white`
- `text-dark`
- `text-center`
- `text-uppercase`
- `text-success`
- `text-danger`
- `border`
- `border-*`
- `border-top`
- `border-bottom`
- `rounded-*`
- `rounded-pill`
- `rounded-circle`
- `overflow-hidden`
- `overflow-y-auto`

---

### Tipografia
Utilizadas para controle de tamanho e peso dos textos.

- `fw-bold`
- `fw-semibold`
- `fs-*`
- `display-*`

---

### Espaçamento
Classes utilitárias para margens e preenchimentos.

- `m-*`
- `mx-*`
- `my-*`
- `mt-*`
- `mb-*`
- `my-*`
- `p-*`
- `px-*`
- `py-*`
- `gap-*`

---

### Posicionamento
Usadas para sobreposição e posicionamento de elementos.

- `position-relative`
- `position-fixed`
- `position-absolute`
- `z-index-*`
- `top-0`
- `bottom-0`
- `start-0`
- `end-0`

---

### Componentes Bootstrap
Componentes reutilizáveis integrados ao projeto.

- `badge`
- `form-control`
- `btn`
- `input-group`
- `is-valid`
- `is-invalid`
- `form-text`

## Onde foi necessário CSS próprio e por quê

### Identidade visual personalizada

Foi necessário criar **variáveis CSS (`:root`)** para padronizar as cores e fontes utilizadas em todo o projeto.

- `--cor-fundo-primario`
- `--cor-primaria`
- `--fonte-inter`
- `--fonte-montserrat`

---

### Botões personalizados

Foi necessário criar versões próprias para manter a identidade visual, como cores, efeitos e tipografia, exclusiva do projeto.

Classes criadas:

- `.btn-primary`
- `.btn-secondary`

---

### Cores personalizadas de fundo e texto

Utilizado para a paleta de cores própria do projeto.

Classes criadas:

- `.bg-primary-color`
- `.bg-secondary-color`
- `.bg-tertiary-color`
- `.color-primary`
- `.color-secondary`

---

### Tamanho de tipografia

Utilizado para criar tamanho de fonte inexistente no Bootstrap

Classe criada:

- `.fs-7`

---

### Menu responsivo e Modal sem JavaScript

Como o uso de JavaScript foi proibido, foi necessário implementar um menu mobile utilizando a técnica checkbox hack com CSS, as classes foram utilizadas para exibir e ocultar o menu em telas menores e posicionar o menu sobre o conteúdo.

Da mesma forma, o modal de termos e condições foi desenvolvido sem JavaScript, para ele forma utilizadas classes no intuito de exibir e ocultar o modal com checkbox

Classes utilizadas:

- `.menu-mobile`
- `#menu-toggle:checked ~ .menu-mobile`
- `.modal`
- `.modal-conteudo`
- `#modal-toggle:checked ~ .modal`

---

### Imagens de fundo personalizadas

O Bootstrap não oferece controle direto para aplicação de imagens de fundo, então para isso foram criadas classes pensando em aplicar imagens de fundo, controlar o posicionamento e responsividade.

Classes criadas:

- `#hero-section`
- `.formulario`

---

### Ajustes específicos de componentes

Alguns componentes precisaram de pequenos refinamentos visuais além das opções padrão do Bootstrap.

Exemplos:

#### Formulários

Personalização de cores do texto, placeholder e focus.

Classes/seletores:

- `.form-control`
- `.form-control:focus`
- `.form-control::placeholder`

---

#### Links da navegação

Adição de efeito de transição e mudança de cor ao passar o mouse.

Classe criada:

- `.nav-link:hover`
- `.btn-whatsapp:hover`

---

#### Tabela profissional

Bootstrap não oferecia exatamente o estilo desejado para as bordas, e para personalizar as bordas laterais, impedir a quebra de linha e remoção das bordas padrão foi necessario a criação desta classe.

Classe utilizada:

- `.table td`

---

#### Cards de planos

Foi necessário limitar a largura máxima dos cards.

Classe criada:

- `.plano`

---

#### Elementos com tamanho específico

Alguns elementos precisavam de um tamanho específico, mas o Bootstrap não oferecia essa opção, por isso, foram criadas as seguintes classes:

- `.icone-metricas`
- `.icone-perfil`
- `.link-sidebar`
- `.mapa`

---

## Principais dificuldades durante o desenvolvimento

* Em projetos anteriormente desenvolvidos, eu costumava seguir o fluxo de desenvolver primeiro a versão desktop para apenas depois adaptar para dispositivos móveis, ou seja, não aplicava o Mobile First. Como o Bootstrap segue justamente esse conceito, no início do desenvolvimento acabei tendo retrabalho em algumas partes, precisando refazer trechos do código por não ter considerado esse detalhe desde o começo.

* Outro ponto que tive dificuldade foi com a legibilidade, pela falta de costume com a utilização de muitas classes do Bootstrap aplicadas juntas e também pela grande quantidade de elementos `<div>`, o que acabou deixando a estrutura mais poluída visualmente. Para facilitar a leitura e organização, adicionei espaçamentos entre os trechos do código e comentários para identificar melhor cada seção.

## Links

Repositório: [FitMaster - GitHub](https://github.com/igormartinz/fitmaster)  
Deploy: [FitMaster - Vercel](https://fitmaster-web.vercel.app/)  
Figma: [FitMaster - Figma](https://www.figma.com/design/hN1rVUEG4issEnQERjhjzX/FitMaster?node-id=1-3&p=f&t=sjJD3pa6m8lJu53m-0)