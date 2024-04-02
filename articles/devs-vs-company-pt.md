# Acessibilidade: O desenvolvedor não é responsável por tudo
> mas boa parte é ele que faz

Um dos maiores equívocos de uma empresa em relação a acessibilidade, é esperar da equipe de desenvolvimento a iniciativa de tornar seu seus sites ou aplicativos acessíveis. A participação do dev é essencial, mas a organização de um projeto acessível deve envolver todos profissionais responsáveis, desde o conteudista, designer, até os profissionais  da qualidade.

Em projetos de acessibilidade não organizados é comum o desenvolver assumir praticamente toda as responsabilidades, dentre elas, contraste mínimo, espaçamentos mínimos entre conteúdos, tamanho de fonte mínimo, foco visível, mensagens não baseadas apenas em informações sensoriais (cor, som...), conteúdo compatível com diversas telas, e vários outros exemplos. Essa foi uma amostra de tarefas que seriam um problema o programador cuidar, pois por exemplo como ele faria para seguir um contraste se o designer criou um layout sem prever isso? Ou como ele resolveria um texto de difícil entendimento se este foi decidido por outros membros da empresa?

Bom, para que os devs que estão lendo, não pensem que não tem trabalho, fiz uma lista das principais tarefas de um desenvolvedor em projetos com acessibilidade.

## Elementos semânticos

Independente da interface que está sendo usada, seja Web, aplicativo ou desktop, os elementos que irão compor essas aplicações devem ser semântico, que sejam entendidos além do seu visual, como também organizados em ordem, para que possam ser entendidos. Um botão, uma lista, um título ou qualquer elemento, deve ter seu significado além do que está sendo visto em tela. [Lêda Spelta, que é deficiente visual, em um vídeo seu](https://www.youtube.com/watch?v=fha81cO2Cng&t=2977s) conta a experiência de ser instruída a pressionar um botão na tela que segundo ela semanticamente não era um botão, só tinha a aparência, e consequentemente não conseguiu encontrar.

## Sequência lógica

O desenvolvedor pode se deparar com a situação em que a versão desktop está com uma sequência de leitura correta e ao adaptar para o mobile o conteúdo perdeu a ordem que ele queria (mais um motivo para pensar no mobile primeiro), aí para corrigir isso ele aplica um estilo que ajuste a ordem do conteúdo... Errado, pois visualmente mudou alguma coisa, mas para a navegação com teclado e para leitores de tela aquele conteúdo continua na mesma sequência de leitura, o que pode ser ruim de navegar e não ter fazer sentido a leitura.

Os títulos também devem seguir uma hierarquia para que o usuário que usar um leitor de telas possa compreender e encontrar o conteúdo que ele deseja com mais facilidade, como mencionado pela [Joanna Voloski em seu artigo](https://medium.com/@jovoloski/39f13a325366), se usando teclado, ao pressionar H, pula para o próximo título. Os títulos formam uma hierarquia igual aquela utilizada em TCCs, por isso não devemos pular eles por motivo algum, por que assim como pessoas que enxergam rolam rapidamente a página para procurar a seção de conteúdo que querem ler, o mesmo deve poder ser feito por pessoas usando leitores de tela.

<p align="center">
  <img
    alt="demonstração do aninhamento dos títulos de uma página web"
    src="https://github.com/jomarcardoso/accessibility/assets/27368585/293f1e93-787e-4727-8595-bb2c5d9c603e"
  >
</p>
<p align="center">
  <small>fonte: https://www.w3.org/WAI/test-evaluate/preliminary/</small>
</p>

## Usar alternativa textual

O mais famoso trabalho do desenvolvedor em relação a acessibilidade, e o único que eu conhecia antes de estudar sobre o assunto 😅. Um texto alternativo nada mais é que um texto para explicar qualquer coisa que não seja de texto que esteja em tela e é de grande valia para quem usa leitor de tela entender o que está nela. Engana-se em pensar que isso beneficia apenas pessoas cegas, o texto alternativo é muito empregado em imagens, mas também pode ser usado em formato de legendas em vídeos e áudios, para pessoas com deficiência auditiva ou qualquer pessoa impossibilitada de escutar naquele momento, seja pela falta de caixa de som ou ambientes silenciosos, como uma TV em um saguão de recepção (tecla sap).

Mas assim como quase tudo na acessibilidade, o texto alternativo também não é apenas para pessoas com deficiência, a prova disso é quando você vê aquele ícone e não sabe o que aquilo faz e coloca o mouse sobre ele na esperança de que apareça um texto explicando o que aquele símbolo significa. Este é um bom exemplo para quem não tem uma grande limitação sensorial entender que se para ela um texto auxiliar é útil, imagina para uma pessoa que não enxerga ou alguma que te deficiência de raciocínio.

## Área de toque mínima

Elementos pequenos na tela que são clicáveis ou tocáveis podem ser desagradáveis para qualquer, mas a situação da pessoa pode piorar se ela tem alguma limitação motora como navegar com por mouse de botões, usando os pés ou até alguma doença que comprometa a precisão de seus movimentos ou de sua visão. Apesar de não ser o ideal, as vezes a área de toque pode ser maior que o elemento visual, isso é uma solução que está em poder do desenvolvedor também.

## Navegação com teclado (computador)

Nem todas as pessoas em um computador são capazes de usar mouse, seja por limitações de visão ou movimento, então é importante que o desenvolvedor tenha feito uma navegação por teclado que esteja na ordem correta de leitura e com um foco visível para aqueles que têm visão porém não navegam usando mouse.

<p align="center">
  <img
    alt="amostra do site Terra de como ele mostra o foco visível"
    src="https://github.com/jomarcardoso/accessibility/assets/27368585/5ad523c4-63aa-4556-8b99-0d165f573d13"
  >
</p>

## Saltos de conteúdos

Dar a possibilidade de saltar aquelas parte repetidas de página a página como o cabeçalho e a navegação. Inclusive ao fim do conteúdo principal disponibilizar uma forma de voltar ao início.

<p align="center">
  <img
    alt="amostra de como o Youtube mostra o salto de conteúdo"
    src="https://github.com/jomarcardoso/accessibility/assets/27368585/e6c0f9b0-3943-4143-bb60-ebef0e093233"
  >
</p>

Essa técnica é bem simples de ser aplicada, basta o desenvolvedor colocar a regra que o elemento deve ficar escondido até enquanto não estiver em foco, ou seja, o elemento não aparecerá em tela, a não se que o usuário use o teclado, com a tecla "tab" e chegue no elemento.

## Suporte a telas pequenas ou com zoom

O desenvolvedor deve ser capaz de fazer o conteúdo caber em uma de de 320px por 320px, segundo recomendações do W3C. Esse valor é derivado de uma resolução de 1280px com 400% de zoom. Com isso fica claro que o zoom não deve ser bloqueado e telas maiores do que 320px não devem ter duas rolagens (horizontal e vertical) para conseguir ver o conteúdo.

## Teclas de atalho

Sabemos que quando trabalhamos com algum software todos os dias, vamos aos poucos pegando seus atalhos e nos tornando mais produtivos. Agora, imagine o quanto além de ajudar no rendimento os atalhos podem auxiliar as pessoas que não usam mouse e ou não enxergam. Pensando no simples ato de salvar um arquivo em um editor de textos como Word, é bem intuitivo usarmos o famoso CTRL + S, porém sem esse atalho teríamos apenas formas mais trabalhosas de fazer o mesmo, com o mouse, acessando a aba arquivo e percorrer até salvar, ou com o teclado, pressionando a tecla ALT e descer até a mesma opção.

## Uso dos WAI-ARIA (web)

Para os usuários que não sabem, os atributos HTML `role` e `aria-` são da especifiação do W3C WAI chamados de WAI-ARIA que significa Aplicações de Internet Rica Acessível. A necessidade desses atributos surgiu após o AJAX, onde as páginas deixaram de serem apenas documentos de textos e imagens para terem muito mais intereções, sem que haja o recarregamento da página.

Os atributos Aria enriquecem os elementos HTML dando a eles mais significado do que originalmente eles têm. Os WAI-ARIA são "livres" da especificação do W3C, ou seja, pode evoluir muito mais rápido, e é por isso do seu uso, servem muitas vezes para complementar uma informação enquanto a especificação do W3C não fizer.

Os atributos ARIA tem 3 funções:

- dizer o papel, com o atributo `role`;
- dizer a função com um atributo `aria-`;
- dizer o estado com outro atributo `aria-`.

O role serve então para dizer alguma função que o elemento HTML não "soube dizer", por exemplo `<button type="button role="switch">`. O role deve ser evitado quando ele muda a função de um elemento HTML, por exemplo: `<div role="button>`, isso deve ser evitado, pois um elemento nativo HTML possui várias propriedades, comportamento e muito mais compatibilidade com os navegadores atuais e futuros.

O atributo ARIA de função, pode dizer o que aquele elemento faz, por exemplo `  <form aria-label="search-form">`

O atributo ARIA de estado, como o nome diz, informa como o elemento está `<button type="button" role="switch" aria-checked="true">`. Essa informação é muito importante para uma pessoa que não enxerga, para facilmente saber o estado daquele elemento.

## Escolha de bibliotecas

Primeiramente não existe uma ferramenta ou biblioteca milagrosa que tornará um site acessível, porém, se bem escolhidas, com elas o trabalho do dev pode ficar muito mais fácil para tornar acessível, ou se mal escolhido, impossível de ser acessível. Existem bibliotecas como foco na acessibilidade, por exemplo o AMP, em que vem com seus componentes acessíveis prontos para serem usados. Já existem outras que dão a possibilidade do dev tornar acessível, por exemplo o Material UI.

## Configurar ferramentas que avaliam o código

Olhando para a indústria e como ela evolui para cada vez menos seus funcionários fazerem serviços braçais, o ideal para ela é que a máquina faça tudo sozinho ou com o mínimo de esforço humano. Isso também se aplica no desenvolvimento de software, quanto mais ferramentas automatizadas usamos para nos auxiliar, melhor. A primeira ferramenta que o desenvolvedor deve colocar no projeto são os linters, àqueles voltados à acessibilidade são sutis, porém evitam erros mais comuns para novos desenvolvedores, como escutar eventos de toque em elementos que não foram desenhados para isso (no HTML a div por exemplo), não colocar o tipo de um botão, ou então não seguir uma hierarquia de elementos básica, como `<li>` filho de `<ul>`. Um segundo nível de ferramenta são aquelas que verificam a aplicação pronta, a mais conhecida delas é o Lighthouse. Ferramentas como essa podem ser usadas em uma integração contínua, e assim cumprir a primeira recomendação de testes do [eMAG](http://emag.governoeletronico.gov.br/). Os testes devem ir muito além das ferramentas, porém elas fazem o papel importante de evitar retrabalhos, uma antes mesmo da entrega da tarefa e outra antes de passar para a equipe de testes.

## Criação de componentes acessíveis

Essa parte talvez não esteja escrito em nenhum livro, mas achei muito importante colocar no [meu TCC](https://onedrive.live.com/?authkey=%21AAeLShjixe9fz84&cid=00664A182AE91239&id=664A182AE91239%2156186&parId=664A182AE91239%2155844&o=OneUp). O conceito de Componente surgiu num livro de arquitetura civil chamado Uma Linguagem de padrões e nele é explicado de que cada problema é solucionado apenas uma vez e que devemos usar aquele padrão criado para criar um padrões maiores. No desenvolvimento chamamos esses padrões de Componentes. Com ou sem uso de bibliotecas devemos ter esse componentes com todos os problemas de acessibilidade solucionados e assim replicarmos o que já está bom pelo projeto.

## Idioma

Não, as páginas e aplicativos não precisam estar traduzidas para todos os idiomas, porém é preciso especificar o idioma para que leitores de tela façam a correta leitura. Na web é identificado o idioma no elemento raiz, porém muitos não sabem que o atributo "lang" é global e pode ser usado em qualquer outro elemento HTML, isso é útil para informar se algum trecho da página muda de idioma.

```html
<html lang="pt-BR">
<p lang="ru-Cyrl-BY">
```

## O que não deve ser feito

### Recarregar página

A tarefa do dev aqui seria fazer uma implementação que não recarregue a página. Depois do Ajax não precisamos mais carregar uma página nova a cada interação, como envio de formulário ou algum clique para abrir algum elemento.

### Alternativas textuais sem utilidade

Os textos alternativos devem agregar ao conteúdo. Ter por exemplo uma alternativa textual de uma imagem dizendo o mesmo que o texto ao lado, não é útil e ainda atrasa na leitura a página. Quando a imagem é meramente decorativa ou não tem como saber o conteúdo dela, é preferível o colocar o atributo alt vazio. `<img alt="">`. Se fosse descrever a imagem de uma bota Schutz tratorada não seria o nome da bota e sim, uma bota preta, com um salto médio, quadrado, uma sola com aspecto robusto, como um pneu com garras usados em off-road, cano médio, sem cadarço...

<br>

> Material auxiliar
> ---

- [apresentação de slides](https://docs.google.com/presentation/d/1OW480D_WhBQ6QJLdVQqJPDH4ZndlRWzvjxboQHbJQZ4/edit?usp=sharing)
