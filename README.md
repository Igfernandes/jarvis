# Tema da Accor

O tema foi criado para a empresa Accor, com modelo Hotsite, atingindo os objetivos de servir como ferramenta para a realização de um evento cultural da rede de hotéis Accor parabenizando os profissionais na área da saúde que prestaram serviços dentro da pandemia que teve início ao ano de 2020. Qualquer uso do tema além fora dos das necessidades da Accor, viola os termos de uso e exclusividade desse projeto.  


## 🔗 Grade de conteúdos:

- [Recursos](#recursos)
- [Arquitetura](#arquitetura)
- [Instruções](#instruções)


============================//================//===========

## ⚡ RECURSOS:

### [RECURSOS] - Styles
- [SASS](https://sass-lang.com/)
- [Normalize](https://github.com/necolas/normalize.css)
- [Bootstrap](https://getbootstrap.com/docs/5.0/getting-started/download/)

### [RECURSOS] - Scripts
- cnd html5shiv
- API Facebook
- API Google

### [RECURSOS] - Plugins
- Smush (Otimizar imagens)
- Yoast SEO (Aumentar desempenho SEO)
- WP Cerber Security, Anti-spam & Malware Scan (Cyber Segurança)
- WP Hide & Security Enhancer (Cyber Segurança)


## 📂 ARQUITETURA

| Directório     | 1° Setor              | 2° Setor                                 |
| ---            | ---                   | ---                                      |
| assets         | dist      | src       | css - js           | fonts - img - scss  | 
| includes       | html5Shiv | normalize | ---                | ---                 |
| language       | br        | es        | ---                | ---                 |
| plugin         | admin     | data      | br - es - settings | ---                 |
| templates      | br        | es        | ---                | ---                 | 


**Obser: A pasta "assets" está guardando todo os arquivos front-end**
**Obser¹: A pasta "includes" guarda os arquivos de ajuste e manutenção do thema.**
**Obser²: A pasta "language" guarda a tradução das páginas, além de ser uma arquitetura base do WP**
**Obser³: A pasta "plugin" guarda todo o sistema backend e arquitetura do painel adminstrativo**
**Obser¹¹: A pasta "templates" guarda todos os códigos html dos projetos.**



## 📂 INSTRUÇÕES

### [INSTRUÇÕES] - Instalação 

- Só bastas subir o projeto para o servidor, dentro do diretório "public_html/wp-content/themes/", após ativar dentro do wordpress na área da temas. Não precisa habilitar a debugação e nem precisa fazer outra config. As tabelas sql serão criadas dentro do banco de qualquer banco no momento que instalar e a área adminstrativa será criada tbm automáticamente no painel do wordpress. Caso não ocorra esses procedimentos, vasculhe o problema entre os códigos da pasta "plugin".

### [INSTRUÇÕES] - Usuários

**Main(User): internit**
**Main(Password): candle2112**

**Obser¹: O usuário principal é o da internit, permitindo ver todos os registros, no entanto, para criar o "br" e o "es", siga as instruções abaixo colocando qualquer senha, mas mantendo o usuário já determinado**

**Admin-br(User): Accor-br**
**Admin-br(User): (Crie uma senha)**

**Admin-es(User): Accor-es**
**Admin-es(User): (Crie uma senha)**



### [INSTRUÇÕES] - CSS

- A folha de estilo foi construída com SASS.

Pode usar um compilador do seu gosto. Se não tiver uma referência, para este projeto foi usado o [ruby](https://rubyinstaller.org). Baixe o instalador, faça a instalação padrão seguindo os passos e depois abra o gitbash na pasta e digite o comando "gem sass install" para em seguida fazer a compilação com os comandos "sass --watch scss:css"

Abaixo se encontra uma tabela com a indicação de cada arquivo de estilo:

| Função                     | Arquivo                                                |
| ---                        | ---                                                    |
| Índice                     | template-globals.scss                                  |
| Funções                    | tools/mixins.scss                                      |
| Fontes                     | settings/fonts.scss                                    |
| cores                      | settings/colors.scss                                   |
| bibliotecas                | libary/../bootstrap.scss  ~ libary/../owlcarousel.scss |
| layouts                    | layouts/layouts.scss                                   |
| Fonts globais              | components/measures.scss                               |
| Keyframes adicioais        | animations/animations.scss                             |        
| Keyframes Padrões          | animations/default.scss                                |
| Pagina Admin               | admin/../admin.scss                                    |
| Pagina unica Admin         | admin/../_singles-cadastro.scss                        |


**OBS¹: O container principal que engloba o layout respeita a configuração do bootstrap de "col-11" para dispositivos desktop e "col-12" para dispositivos com telas menores do que 1444px.**

Na função criada de responsividade, existem as seguintes medidas:

| Dispositivo                 | Largura    |
| Extra Extra largo (desktop) | 2000px     |
| Extra largo (desktop)       | 1540px     |
| largo (notebook)            | 1200px     |
| médio (laptop)              | 1024px     |
| pequeno (tablet)            | 768px      |
| extra pequeno (mobile)      | 425px      |

**Para fazer o responsivo no SASS, basta chamar a função ``` @include mq()``` com dois parâmetros. O primeiro é a medida:**

- xs
- sm
- md
- lg
- xl

**O segundo parâmetro determina se são valores menores que alcançam até essa medida ou valores que iniciam após essa medida**

@include mq('sm'){
    -- tudo aqui irá ocorrer da resolução 769px pra acima --
}
@include mq('sm', max){
    -- tudo aqui irá ocorrer até a resolução 768px --
}

### [INSTRUÇÕES] - Páginas

A configuração padrão do wordpress pede a criação das páginas na home, mas o escopo html se encontra dentro da página "templates".

### [INSTRUÇÕES] - Functions.php

Foram pré-definidos:

- carregamento de css e js de acordo com a página carregada;

- configuração da chamada Js do arquivo "templates-globals.js" para "type=module"

- carregamento de cdn's em uma área específica;

- chamada para o arquivo que guarda as configs do banco de dados.

- configurações do navbar e sidebar

- chamada para criação da pagina do admin


### [INSTRUÇÕES] - Layout admin

- Busque dentro do diretório plugin/admin/br ~ es para encontrar os códigos htmls referentes aos layouts existentes.


