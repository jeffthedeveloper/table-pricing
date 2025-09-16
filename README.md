# Projeto: Tabela de Preços Responsiva com Flexbox

Este é um projeto de frontend de página única (`index.html`) que demonstra a construção de uma tabela de preços (Pricing Table) moderna e responsiva. O principal objetivo técnico do projeto é o uso de **CSS Flexbox** para organizar os planos de assinatura e garantir que o layout se adapte a diferentes tamanhos de tela.

O projeto consiste em três planos (Basic, Standard, Premium) exibidos lado a lado em telas maiores e empilhados verticalmente em dispositivos móveis.

## Tecnologias Utilizadas

  * **HTML5**
  * **CSS3** (incorporado no arquivo HTML)
  * **Google Fonts** (especificamente a fonte "Sono")

## Análise Técnica do Layout (CSS)

Todo o layout é controlado por um arquivo CSS incorporado no `<head>` do `index.html`. Os principais conceitos de CSS aplicados são:

  * **Contêiner Flexbox (`.pricing-container`)**

      * `display: flex`: Estabelece o contêiner principal como um contexto Flexbox, alinhando os planos de preço (`.pricing-plan`) horizontalmente por padrão.
      * `justify-content: center`: Centraliza os planos horizontalmente no contêiner.
      * `align-items: center`: Centraliza os planos verticalmente.
      * `height: 100vh`: Faz com que o contêiner ocupe 100% da altura da tela (viewport height), permitindo a centralização vertical completa em modo desktop.
      * `gap: 2rem`: Adiciona um espaçamento consistente entre os planos.

  * **Itens Flex (`.pricing-plan`)**

      * `flex: 1`: Permite que cada plano cresça igualmente para preencher o espaço disponível no contêiner, respeitando um `max-width: 400px` para evitar que fiquem muito largos.
      * `background-color: #f2f2f2`: Define a cor de fundo cinza claro para os cards.

  * **Design Responsivo (Media Query)**

      * Uma *media query* é usada para telas com largura máxima de 1250px (`@media (max-width: 1250px)`).
      * Dentro desta query, o `.pricing-container` tem sua direção alterada para `flex-direction: column`, o que empilha os planos verticalmente.
      * A altura (`height`) é redefinida para `100%` para permitir que o conteúdo flua naturalmente na vertical, em vez de ficar fixo à altura da tela.

## Estrutura do Projeto

```
table-pricing/
├── index.html          # Arquivo principal com HTML e CSS (versão final)
├── skeleton.html       # Versão "esqueleto" do projeto (template inicial)
├── LICENSE             # Licença MIT do projeto
└── README.md           # Este arquivo
```

*(Nota: O arquivo `skeleton.html` representa o ponto de partida do projeto, contendo apenas a estrutura HTML e um bloco de *media query* vazio, enquanto o `index.html` é a solução completa e estilizada.)*

## Como Visualizar

Este é um projeto estático. Para visualizá-lo, clone o repositório e abra o arquivo `index.html` em qualquer navegador web.

## Licença

Este projeto é distribuído sob a licença MIT.
