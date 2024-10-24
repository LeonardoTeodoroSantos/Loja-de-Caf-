# Loja de Cafés

<p>
Neste projeto eu aprendi sobre algumas coisas (vou descrever em mais detalhes abaixo). Projeto inspirado neste <a href='https://www.youtube.com/watch?v=zQR_LD_gJs8'>video do YouTube</a>.
</p>

## Descrição
Este projeto é sobre um site de loja de cafés brasileiros (simulação). O site tem um scroll page animado, image-background, alguns botões como "carrinho", "adicionar ao carrinho", links de midias sociais, opiniões de clientes etc.
<!-- colocar aqui um gif do site -->

## Tecnicas e Tecnologias Utilizadas
![Static Badge](https://img.shields.io/badge/HTML-yellow?style=for-the-badge&logo=html5&logoColor=%23E34F26&logoSize=auto&labelColor=black&color=%23E34F26) ![Static Badge](https://img.shields.io/badge/CSS3-%231572B6?style=for-the-badge&logo=css3&logoColor=%231572B6&logoSize=auto&labelColor=black&color=%231572B6)
 ![Static Badge](https://img.shields.io/badge/javascript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E&logoSize=auto&labelColor=black&color=%23F7DF1E) 

- `HTML`: O arquivo **HTML** é basico, tem somente uma página. Ele é responsável por imagens, links, botões etc. Este projeto me ajudou a treinar mais sobre os comandos emmet.

- `CSS`: Este arquivo **CSS** também é básico, aqui eu aprendi sobre "transform: translateX and translateX"; "display: grid" e mais. Relacionado a **@media querrys** eu aprendi sobre **grid-template-columns** que ajuda em uma melhor visualização para celulares e tablets, mas o mais importante para mim, foi treinar o aninhamento no **CSS**, na minha opinião ajuda a entender melhor onde o CSS está sendo utilizado.

- `JavaScript`: JavaScript é responsável por três principais funções: _**Menu Responsivo:**_ Um menu que pode ser aberto e fechado, mudando seu icon. _**Slide dos Clientes:**_ Um slider que permite a navegação entre diferentes slides, usando bullets para facilitar a interação. _**Interseção do Observador:**_ Monitora elementos que entram na viewport, adicionando um efeito na visualização desses elementos. Esta função melhora a interatividade e a experiencia do usuário com a página.

    ### 1. **Menu Responsivo**

    <img src="https://github.com/user-attachments/assets/9f6928e3-36d8-4a0f-acf4-3234c1ea9196" width="60%" border="1">

    #### DESCRIÇÃO:

    - **Seletores:** A função seleciona elementos da página usando `document.getElementById` e `document.querySelector`.

    - `menuBtn`: É o botão que abre ou fecha o menu.

    - `navLinks`: Contém o link de navegação do menu.

    - `menuBTNicon`: É o ícone do botão que muda entre menu e fechar.

    #### FUNCIONAMENTO:

    - Ao clicar no ícone, o evento `click` é acionado.

    - `navLinks.classList.toggle("open")`: alterna a classe **"open"** no lemento `navLinks`. Se a classe já estiver presente, ela é removida; caso contrário, é adicionada.

    - O ícone também muda de classe entre `ri-close-line` e `ri-menu-line` dependendo do estado do menu.

    <!-- gif do funcionamento do menu abrindo e fechando -->
    <video muted loop preload="auto" autoPlay playsInline src="https://github.com/user-attachments/assets/80181b22-a4bb-4305-b04c-00b4fe5945a9" width="80%"></video>

    ### 2. **Fechar o Menu ao Clicar em um Link**

    <img src="https://github.com/user-attachments/assets/475022a0-6fc6-4801-ae29-8e2483884bf5" width="60%" border="1">

    #### DESCRIÇÃO:

    - Este bloco adiciona um evento ao `navLinks`, que fecha o menu ao clicar em qualquer um dos links.

    - `nabLinks.classList.remove("open")`: Remove a classe "open" para fechar o menu.

    - O ícone do botão é redefinido para `ri-menu-line`.

    <!-- gif do funcionamento de clicar em um dos links e fechar o menu -->
    <video muted loop preload="auto" autoPlay playsInline src="https://github.com/user-attachments/assets/e88dec4a-de0f-428f-be1f-34203857948a" width="80%"></video>

    ### 3. **Slides dos Clientes**

    <img src="https://github.com/user-attachments/assets/710bea11-3d86-4c31-8751-36438ba4dbfb" width="60%" border="1">

    #### DESCRIÇÃO:

    - O evento `DOMContentLoaded` assegura que o código só execute após todo o HTML ter sido carregado.

    - **Seletores:** `slides` e `bullets`. São pontos selecionáveis que "traz" opiniões dos clientes "escondidas" no eixo x.

    - `currentSlide`: Variável que mantém o índice do slide atual.

    #### FUNCIONAMENTO:

    - `showSlide(index)`: Esta função altera a posição dos slides usando `translateX` para mostrar o slide correspondente ao índice. Também atualiza os indicadores (`bullets`).

    - Um evento `click` é adicionado a cada bullet, que ao ser clicado, muda o slide atual.

    <!-- gif do funcionamento dos bullets de slides -->
    <video muted loop preload="auto" autoPlay playsInline src="https://github.com/user-attachments/assets/3b04c4e5-bf8c-46d6-a388-5628f9f8483f" width="80%"></video>

    ### 4. **Efeitos de Interseção**

    <img src="https://github.com/user-attachments/assets/abe2ae90-bd4c-4974-966a-29b3197d9ab6" width="60%" border="1">

    #### DESCRIÇÃO:

    - `IntersectionObserver`: Uma **API** que permite observar a visibilidade de elementos dentro do viewport (área visível da página).

    - O código cria um observador que adiciona a classe "show" a elementos quando eles entram na área visível e remove a classe quando eles saem.

    #### FUNCIONAMENTO:

    - Os elementos com a classe "hidden" são observados. Assim que se tornam visíveis, recebem a classe "show", que pode ser estilizada para criar animações ou efeitos.

    <!-- gif do funcionamento do efeito de interseção -->
    <video muted loop preload="auto" autoPlay playsInline src="https://github.com/user-attachments/assets/c58dfea1-1da8-4b13-b90c-c83fb6120dc5" width="80%"></video>

    #### RESUMO
    O arquivo Javascript implementa um **menu responsivo**, **bullets de slides** e **efeitos de interseção** para elementos da página. Cada parte do código tem um propósito específico para melhorar a interação do usuário e a estética da página.