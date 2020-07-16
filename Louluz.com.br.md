<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Louluz.com.br</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h1 id="louluz.com.br"><a href="https://www.louluz.com.br/">LouLuz.com.br</a></h1>
<h3 id="questões-encontradas">Questões encontradas:</h3>
<ul>
<li>
<p>Ausência da tag <code>&lt;main&gt;</code> no corpo do site</p>
<ul>
<li>Essa tag define qual é o conteúdo principal dentro do site, ajudando os robôs de indexação a entender o tema do site.</li>
</ul>
</li>
<li>
<p>Ausência de tags <code>&lt;header&gt;</code>,<code>&lt;footer&gt;</code>,<code>&lt;nav&gt;</code></p>
<ul>
<li>Essas tags definem seções de importância pra construção de layout e navegação do usuário e ajudam com a acessibilidade do site, <a href="%5Bhttps://alistapart.com/article/accessibilityseo/%5D(https://alistapart.com/article/accessibilityseo/)">fator</a> que é importante para o posicionamento nos motores de busca.</li>
</ul>
</li>
<li>
<p>Imagens sem <code>&lt;figure&gt;</code>, <code>srcset</code> e com funções de javascript atreladas diretamente no HTML.</p>
<ul>
<li>Hoje em dia, com a web nos tantos formatos (Mobile, Tablet, Televisão, Smartwatch, além de Desktop) é importante que suas imagens tenham diversos tamanhos para que o usuário sempre veja a mais adequada à sua tela e que não gaste seus dados baixando imagens com resoluções muito maiores que seu dispositivo pode apresentar. Utilizando essas <em>tags</em> existe a possibilidade diversas imagens para as diferentes resoluções e tamanhos dos dispositivos.</li>
<li>Exceto em casos de aplicações com Frameworks modernos de Javascript (que não estão presentes no site), atrelar funções diretamente no HTML é uma má prática de programação porque fere a <a href="%5Bhttps://www.devmedia.com.br/amadurecendo-com-separation-of-concerns/18699%5D(https://www.devmedia.com.br/amadurecendo-com-separation-of-concerns/18699)">Separação De Conceitos/Preocupações</a>. Essa prática é uma base da engenharia de software que dita as melhores formas de se construir uma aplicação. A modularização de cada componente torna a manutenção e adição de funções mais fácil no futuro, além de construir produtos mais robustos e escaláveis.</li>
</ul>
</li>
<li>
<p>Separação de seções do site usando a tag <code>&lt;div&gt;</code> ao invés de <code>&lt;section&gt;</code></p>
<ul>
<li>Diminui relevância de informações importantes e mistura conteúdos que não são relacionados, diminuindo posicionamento nos motores de busca.</li>
</ul>
</li>
<li>
<p>Uso de inputs feitos com Javascript quando já existem opções em HTML que cumprem a mesma função</p>
<ul>
<li>Observado nas páginas internas, na barra lateral esquerda, onde o cliente escolhe o preço. Isso torna a operação mais custosa para o navegador, menos acessível para os usuário e faz com que os robôs não consigam entender o que aquela seção significa.</li>
</ul>
</li>
<li>
<p>Uso de <code>&lt;div&gt;</code> quando existem elementos mais semanticamente relevantes e acessíveis.</p>
<ul>
<li>Acessibilidade e SEO tem tudo à ver. Dificultar que os robôs entendam o que cada seção representa, e dificultar o trabalho dos <em>crawlers</em> faz com que o site perca posicionamento, além de perder toda uma gama de clientes com algum tipo de deficiência (visual, auditiva) que poderiam estar interessados no produto ou conteúdo.</li>
</ul>
</li>
<li>
<p>Uso de imagens para ícones ao invés de Vetores Escaláveis</p>
<ul>
<li>além da performance pior, se adequam muito mal a telas de PPI alto (como as de celulares mais modernos, principalmente iPhones)</li>
<li>Também são mais difíceis de se dar manutenção e não podem ser manipulados pelo código como um vetor pode.</li>
</ul>
</li>
<li>
<p>Ausência de Dados Estruturados / Schema</p>
<ul>
<li>Os dados estruturados são um fator de muita importância na web atual,  Com eles temos acesso aos <a href="%5Bhttps://rockcontent.com/blog/rich-snippets/">Rich Snippets</a>:</li>
</ul>
<p><img src="https://i.imgur.com/t5jCh8j.png" alt="enter image description here"></p>
</li>
<li>
<p>Arquivos de Script e Estilo separados em diversas folhas.</p>
<ul>
<li>Isso faz com que o navegador trave a renderização e aguarde o carregamento de vários arquivos de script antes de liberar o site para o usuário, segue exemplo de quantos requests estão sendo feitos de javascript no seu site:</li>
</ul>
</li>
</ul>
<p><img src="https://i.imgur.com/pJG7mei.png" alt="enter image description here"></p>
<p>Cada um desses é um recurso de script sendo baixado, isso afeta tremendamente a performance do site, já que todos esses arquivos poderiam estar sendo baixados como um grande pacote, tornando a operação menos custosa. Para referência, a mesma aba em um dos nossos clientes:</p>
<p><img src="https://i.imgur.com/RnqZdvl.png" alt="enter image description here"></p>
<p>Com a forma correta de servir os dados, você ganha prioridade nos motores de busca e oferece uma experiência melhor para usuários com redes de dado limitadas (como 4G).</p>
<h3 id="melhorias-sugeridas">Melhorias sugeridas:</h3>
<ul>
<li>
<p>Refatoração para <a href="https://gobacklog.com/blog/progressive-web-apps/">PWA</a>.</p>
<ul>
<li>Aumenta o alcance nos motores de busca</li>
<li>Possibilita funcionalidades de aplicação nativa em dispositivos mobile (adicionar o ícone para acesso direto no celular, Splash Screen, Cor de Tema, melhorias de navegação)</li>
</ul>
</li>
<li>
<p>Refatoração do <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML">HTML</a> com uso de Tags mais semânticas</p>
<ul>
<li>Faz com que os Robôs entendam o conteúdo do seu site de forma mais segmentada e possam o exibir em mais resultados de busca.</li>
<li>Aumenta a acessibilidade para uma nova gama de clientes.</li>
<li>Facilita a navegação por meios alternativos (teclado, trackpad, até controles de TV)</li>
<li>Melhora sua presença na internet de forma geral.</li>
</ul>
</li>
<li>
<p>Reestruturação dos Scripts e Estilos</p>
<ul>
<li>Remoção de código inutilizado</li>
<li>Melhora de performance (tempo de carregamento, fluidez na navegação) através da criação de pacotes mais enxutos de código, ao invés de diversos <em>requests</em> como foi demonstrado acima.</li>
<li>Facilita adição de novas funcionalidades e manutenção das existentes.</li>
</ul>
</li>
<li>
<p>Adição de <a href="https://rockcontent.com/blog/o-que-e-cta/">CTAs</a></p>
<ul>
<li>Incentivam usuários a entrarem em contato, pela disponibilidade de poderem se comunicar de diversas maneiras</li>
<li>Cria leads futuros em usuários que talvez não fariam uma compra na primeira visita.</li>
<li>Faz com que usuários retornem mais frequentemente ao site.</li>
</ul>
</li>
<li>
<p>Implementação de conceitos de <a href="https://rockcontent.com/blog/cro/">CRO</a></p>
<ul>
<li>Além de trazer clientes para o site, é também importante que a maior porcentagem possível esteja consumindo ou entrando em contato. Para isso, podemos aplicar diversas técnicas que envolvem desde layout, até os CTAs que foram mencionados acima e outros passos, fazendo com que os visitantes se tornem clientes com mais frequência.</li>
</ul>
</li>
<li>
<p>Fortalecimento da presença Institucional</p>
<ul>
<li>Ter uma marca mais forte e com mais identidade gera confiança em usuários que talvez não se tornariam clientes.</li>
<li>Ter conteúdos relevantes escritos e atrelados à sua marca faz com que seja mais fácil que pessoas interessadas no assunto geral (Jóias, pulseiras, colares, etc) cheguem ao seu site, aumentando as vendas.</li>
</ul>
</li>
<li>
<p>Modernização das técnicas de Analytics</p>
<ul>
<li>Te dá noções mais próximas da realidade de quais ações de fato estão sendo efetivas e fazendo os clientes comprarem.</li>
<li>Cria a possibilidade de ações direcionadas de Adwords para você atingir o público mais propício à converter.</li>
</ul>
</li>
<li>
<p>Adequação de Componentes Mobile</p>
<ul>
<li>Alguns dos botões, filtros e linhas de texto apresentados atualmente na versão mobile do site são pequenos e estão muito próximos, causando erros de usabilidade, o que frustra e afasta possíveis clientes, Exemplo:</li>
</ul>
<p><img src="https://i.imgur.com/VFytMfd.png" alt="enter image description here"></p>
</li>
</ul>
</div>
</body>

</html>
