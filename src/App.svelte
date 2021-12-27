<script lang="ts">
  import Grade from "./Grade.svelte";
	export let number: number= 1
</script>

<header>
  <div class="container">
    <h1>Resultados obtidos do desafio {number}</h1>
  </div>
</header>
<main>
  <div class="container">
    <h2>Introdução</h2>
    <p>No mês de novembro de 2021, aplicamos um desafio de frontend (<a href="https://github.com/mateusavila/dev-hall-front-end-1" target="_blank" rel="noopener noreferrer">#link</a>), realizando <strong>24 avaliações</strong> até o dia de hoje. Cada pessoa avaliada recebia uma nota que ia de 0 a 10 para cada descritor avaliativo, somando 29 critérios de avaliação. Organizamos a avaliação em 3 grandes grupos de descritores, para melhor entendimento:</p>
    <h3>Descritores públicos obrigatórios</h3>
    <p>Estes descritores eram obrigatórios para todos os testes. A lista dos descritores está abaixo:</p>
    <ol>
      <li><strong>Legibilidade do Código:</strong> Mede o quão organizado e fácil de ler o código.</li>
      <li><strong>Consistência nas nomenclaturas:</strong> Se o código segue algum padrão de nomenclatura de variáveis e classes. Exemplo: se o código utilizava <i>snake_case</i> ou <i>camelCase</i>. Neste descritor medimos se os termos utilizados eram consistentes em uma língua.</li>
      <li><strong>Concisão do código:</strong> Se o desenvolvedor(a) utilizava a menor quantidade de código possível ou se importava bibliotecas desnecessárias.</li>
      <li><strong>Se é fiel à proposta estabelecida:</strong> Se ele leu o briefing proposto pelo projeto e entregou com todas as demandas solicitadas no Briefing.</li>
      <li><strong>Se é perfeitamente responsivo:</strong> Se o desenvolvedor(a) tomou cuidado com as telas de tablets e celulares.</li>
      <li><strong>Se é rápido o suficiente:</strong> Se o projeto carregava antes de 4 segundos.</li>
      <li><strong>Se os links externos das redes sociais estão apontando para uma nova aba:</strong> Se os links externos tinham <code>target="_blank"</code></li>
      <li><strong>Se o botão laranja da dobra faz o movimento de scroll para o formulário:</strong> Se havia o movimento de scroll da página a partir do click do botão.</li>
      <li><strong>Aplicou hovers:</strong> Se os botões e links haviam feedback para o usuário.</li>
      <li><strong>Se as imagens estão nas extensões corretas e recomendadas:</strong> Se as imagens de redes sociais estavam em svg, a imagem de fundo estava com jpg e a imagem do homem pensando em png.</li>
      <li><strong>Se utilizou as fontes corretas, nos tamanhos e cores recomendadas pelo designer:</strong> Se o desenvolvedor(a) conseguiu implementar as fontes como o designer definiu.</li>
    </ol>
    <h3>Descritores públicos opcionais</h3>
    <p>São descritores que agregam valor para o projeto, mas não eram obrigatórios, pois entendia que alguns desenvolvedores(as) não tinham experiência necessária para algumas tarefas. O objetivo é encorajar alguns desenvolvedores a ir além do solicitado, agregando valor à entrega. Abaixo a lsita destes descritores:</p>
    <ol>
      <li><strong>Se há animações, e se elas são agradáveis ao olhar.</strong></li>
      <li><strong>Se a máscara no input de telefone foi correta, impedindo a inclusão de letras e formatando um número</strong></li>
      <li><strong>Se a requisição para o servidor apontar para o Método Post</strong></li>
      <li><strong>Se o formulário funcionar, se o usuário terá os feedbacks necessários</strong></li>
      <li><strong>Se o HTML está semântico:</strong> se o (a) desenvolvedor(a) fez bom uso das tags do HTML 5.</li>
      <li><strong>Se a área da dobra for uma imagem e uma div por cima</strong></li>
      <li><strong>Se o hover utilizado tem transition de css</strong></li>
      <li><strong>Se as imagens possuem os atributos corretos</strong></li>
    </ol>
    <h3>Agradando o patrão</h3>
    <p>Estes descritores é que dão o diferencial de mercado para que desenvolvedores(as) consigam uma melhor colocação, pois enxergam cada projeto como uma oportunidade de mostrarem o que sabem. Os descritores abaixo não eram obrigatórios, porém oferecem um precioso extra para motivar estudos. Os descritores de "agradar o patrão" são:</p>
    <ol>
      <li><strong>Pontuação no web.dev:</strong> A nota geralmente é o valor da casa decimal de performance, exceto se as notas de SEO e de Best Practices forem menor que 90.</li>
      <li><strong>Se criou em css puro, criou variáveis internas. Se usou algum pré-processador, criou variáveis e mixins.</strong></li>
      <li><strong>Usou algum framework:</strong> Nesta tarefa aceitamos tanto pre-processadores e frameworks de JS.</li>
      <li><strong>Há feedback visual após a requisição:</strong> Aqui se o usuário conseguirá ver que a requisição deu certo, com alguma mensagem feita com qualidade.</li>
      <li><strong>Boas idéias de reutilização do código: </strong> Se ele entende de componentes.</li>
      <li><strong>Textos alternativos que respeitam pessoas de baixa visão, empoderando o usuário e não dando julgamento de valor</strong>: Se usuários de baixa visão irão ter acesso a uma imagem que os empoderem de suas ações.</li>
      <li><strong>Usou vite:</strong> Se o desenvolvedor está antenado com os hypes do momento.</li>
      <li><strong>Usou CSS-Clip para fazer a imagem de triangulo</strong>: admiti casos de divs com rotate ou a versão de triangulos usando :before e :after, mas a ideia é que o desenvolvedor utilizasse css-clip.</li>
      <li><strong>README bem escrito</strong></li>
      <li><strong>Versão em inglês</strong></li>
      <li><strong>Dark Mode</strong></li>
    </ol>
    <div class="divider"></div>
    <h2>Como calculamos a nota final?</h2>
    <p>Calculamos as notas de 0 a 10, sendo 0 que não atendeu em absoluto o descritor e 10 com atendimento total e/ou superou a expectativa do avaliador. Veja a tabela abaixo:</p>
    <table>
      <thead>
        <tr>
          <th>Tipo de descritor</th>
          <th>Total de pontos</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Descritores públicos obrigatórios (geram a nota de base)</td>
          <td>0 até 110 pontos</td>
        </tr>
        <tr>
          <td>Descritores públicos opcionais</td>
          <td>Incrementa a nota de base de 0 a 80 pontos.</td>
        </tr>
        <tr>
          <td>Agradando o patrão</td>
          <td>Incrementa a nota de base de 0 a 110 pontos.</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>Total</td>
          <th>Conceito de 0 a 300 pontos</th>
        </tr>
      </tfoot>
    </table>
    <p>A partir desta tabela, compilamos uma tabela comparativa de resultados com a expectativa de como o profissional está para assumir uma vaga de júnior:</p>
    <table>
      <thead>
        <tr>
          <th class="pontuation">Pontuação</th>
          <th>Descritivo</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>De 0 a 80</td>
          <td>Você está iniciando os estudos em front-end. Parabéns! Há um caminho longo pela frente, e te convido a continuar estudando e treinando em nossos desafios.</td>
        </tr>
        <tr>
          <td>De 81 a 110</td>
          <td>Você já tem 6 meses de estudo. Continue firme e forte. Há algum curso oferecendo formação gratuita para você? Se candidate, pode ser que você consiga uma vaga.</td>
        </tr>
        <tr>
          <td>De 111 a 180</td>
          <td>Alguma empresa grande já enxergará em você o suficiente para ser estagiário. Creio que você irá assistir muito dev programando e/ou participará de muito pair programming.</td>
        </tr>
        <tr>
          <td>De 181 a 199</td>
          <td>Você já pode ser um dev júnior numa empresa de médio porte, sem responsabilidade direta por tarefas. Falta pouco para você conseguir seu primeiro emprego.</td>
        </tr>
        <tr>
          <td>De 200 a 240</td>
          <td>Você tem condição de ser um dev júnior em qualquer empresa, com responsabilidade direta de tarefas. Já consegue flutuar por inúmeros frameworks, pois sua base é bem sólida.</td>
        </tr>
        <tr>
          <td>De 241 a 269</td>
          <td>Não sei por que você está desempregado. Eu preciso achar uma oportunidade para ti.</td>
        </tr>
        <tr>
          <td>De 270 a 290</td>
          <td>Você tem o suficiente para ser um pleno em alguma empresa pequena ou média.</td>
        </tr>
        <tr>
          <td>De 291 a 300</td>
          <td>Você pode me ajudar nestas avaliações aqui. Confio em absoluto em você. Imagino que beliscaria uma vaga de sênior em empresa pequena.</td>
        </tr>
      </tbody>
    </table>
    <p>Cada pessoa também recebeu uma avaliação da pessoa, em que estágio de desenvolvimento e maturidade está com seus códigos. Este esforço de oferecer uma avaliação mais subjetiva ajuda a confortar desenvolvedores(as) para entenderem que eles estão num processo constante de melhoramento.</p>
    <div class="divider"></div>
    <h2>Avaliação Geral Global</h2>
    <p>Nosso intuito com a avaliação global é ofertar para quem fez este teste uma visão global do que precisa melhorar, como uma guia de estudos obtidos pela análise dos códigos. Estas estatísticas que conseguimos coletar tem valor muito especial para mentores do Pessoas de Tech em entenderem como estão as pessoas estão entregando seus desafios.</p>
    <p>Para sintetizar, listamos abaixo, em termos gerais, os principais pontos positivos e negativos das entregas dos desafios.</p>
    <h3>Pontos positivos</h3>
    <ul>
      <li>Os HTMLs tem vindo semanticamente eficientes</li>
      <li>Nenhum desafio teve nota menor que 90 - mostrando que pessoas bem iniciantes tem tentado ir além do que sabem.</li>
      <li>As pessoas gostaram de ser avaliadas a fundo, sentindo falta deste padrão no mercado.</li>
      <li>O desafio fez sentido com a experimentação de técnicas novas para desenvolvedres(as) mais experientes.</li>
    </ul>
    <h3>Pontos preocupantes</h3>
    <ul>
      <li>Falta de fidelidade com o design proposto.</li>
      <li>CSS não está sendo levado a sério como poderia.</li>
      <li>Os cursos que o pessoal tem aprendido tem parado no tempo.</li>
      <li>Poucos arriscaram para além do desafio proposto. O mercado ainda avalia positivamente quem vai além.</li>
    </ul>
    <h3>Pontos negativos</h3>
    <ul>
      <li>Flagrante falta de testes em telas responsivas.</li>
      <li>Testes viciados: o desenvolvedor não valida se as coisas quebram em telas menores que a tela cheia.</li>
      <li>React com styled components não é desculpa para falta de media queries.</li>
      <li>O pessoal precisa ser heavy user de internet: as soluções de usabilidade para o formulário, quando aplicadas, foram bem abaixo do que o mercado está acostumado.</li>
    </ul>
    <div class="divider"></div>
    <h2>Avaliação Específica</h2>
    <p>Para este documento ficar completo, vamos levantar ponto-a-ponto as notas de todas as avaliações.</p>
    <h3>Legibilidade do Código:</h3>
    <p>A Legibilidade do código é referente à qualidade da leitura do código. Este critério é subjetivo, isto é, baseia-se na minha capacidade de entender o código, e se ele segue critérios sólidos de tabeamentos e se o HTML não apresenta inconsistências. Foi um critério que o povo foi muito bem obrigado.</p>
    <figure>
      <Grade width="{150}" consumed="{9.52}" total="{10}" />
      <figcaption>Uma média bem alta, mostrando que os(as) desenvolvedores (as) tomaram cuidado com a "caligrafia" do código.</figcaption>
    </figure>
    <h4>Futuro deste descritor:</h4>
    <p>Será mergido com o descritor "Consistência das nomenclaturas"</p>
    <div class="divider"></div>
    <h3>Consistência nas nomenclaturas</h3>
    <p>Este descritor mede se os(as) desenvolvedores(as) foram consistentes com a nomenclatura de classes, IDs e funções em seus códigos.</p>
    <figure>
      <Grade width="{150}" consumed="{9.3}" total="{10}" />
      <figcaption>As notas foram ótimas, sinal de que as video-aulas que o povo faz sobre arquitetura limpa surge efeito indiretamente com os júniores. É um palpite que precisa de maior confirmação.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Possivelmente será mergido com o descritor de "legibilidade do código"</p>
    <div class="divider"></div>
    <h3>Concisão do código</h3>
    <p>Verifica se o(a) desenvolvedor(a) inseriu código desnecessário para fazer o projeto.</p>
    <figure>
      <Grade width="{150}" consumed="{9.75}" total="{10}" />
      <figcaption>As notas foram ótimas, mas talvez por que o projeto é simples demais.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Não faz sentido ele ser avaliado em projetos pequenos. Em projetos enormes faz sentido a re-existência deste descritor.</p>
    <div class="divider"></div>
    <h3>Se é fiel à proposta estabelecida</h3>
    <p>Creio que é o descritor mais importante que devemos manter no futuro, visto que estar atento à complexidade das tarefas e atender as expectativas dos stackholders é o futuro do profissional.</p>
    <figure>
      <Grade width="{150}" consumed="{7.26}" total="{10}" />
      <figcaption>Esta nota é enganosa, visto que 7.26 dá a entender que a coletividade entendeu a tarefa de cabo a rabo em 72%, dando 28% de refação, que é uma taxa muito alta. Nos próximos desafios, esta nota precisa ser maior.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Ele é tão precioso que ele deve ter comportamento especial no próximo desafio.</p>
    <div class="divider"></div>
    <h3>Se é perfeitamente responsivo</h3>
    <p>Propositalmente, este projeto não foi feito com telas responsivas, pois é uma prática comum em agências de desenvolvimento e em algumas empresas.</p>
    <figure>
      <Grade width="{150}" consumed="{6.39}" total="{10}" />
      <figcaption>Fundamental o estudo de media query e de testes em telas menores para que este resultado seja coletivamente melhor.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Ele é tão precioso que ele deve ter comportamento especial no próximo desafio.</p>
    <div class="divider"></div>
    <h3>Se é rápido o suficiente</h3>
    <p>Se o(a) desenvolvedor(a) tomou cuidado em deixar o projeto bem rápido.</p>
    <figure>
      <Grade width="{150}" consumed="{8.91}" total="{10}" />
      <figcaption>Está boa a nota, mas podemos sempre melhorar.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Ele tem seu valor, mas creio que será mergido com o teste do web.dev.</p>
    <div class="divider"></div>
    <h3>Se os links externos das redes sociais estão apontando para uma nova aba</h3>
    <p>Ele não é bem um descritor, e sim uma necessidade básica do projeto. A nota 10 era dada para caso o(a) desenvolvedor(a) inseria <code>target="_blank"</code> no projeto. Na próxima versão, será exigido também <code>rel="noopener noreferrer"</code></p>
    <figure>
      <Grade width="{150}" consumed="{5.13}" total="{10}" />
      <figcaption>É assustador que a tarefa obrigatória mais simples teve uma nota tão baixa. Considero bem preocupante que detalhes preciosos demais fiquem de lado.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Imaginei de início que ele seria mergido em algum lugar, mas com uma nota tão baixa, ele será fixo.</p>
    <div class="divider"></div>
    <h3>Se o botão laranja da dobra faz o movimento de scroll para o formulário</h3>
    <p>Esta tarefa não teria o peso de um descritor de qualidade de código, porém era uma demanda do projeto que deve ter peso menor em futuros desafios.</p>
    <figure>
      <Grade width="{150}" consumed="{5.65}" total="{10}" />
      <figcaption>Esta tarefa deve ser relegada a uma tarefa opcional no futuro.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Terá peso de tarefa optativa no futuro.</p>
    <div class="divider"></div>
    <h3>Aplicou hovers</h3>
    <p>Esta tarefa é fundamental para projetos em front-end, e creio que num próximo desafio, teremos que definir a guia de estilo para ver se há maior fidelidade à propostas do designer.</p>
    <figure>
      <Grade width="{150}" consumed="{7.65}" total="{10}" />
      <figcaption>Esta nota precisa ser maior no futuro, nem que o(a) desenvolvedor(a) opte por usar versões próximas de cores e efeitos.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Será mantido onde está.</p>
    <div class="divider"></div>
    <h3>Se as imagens estão nas extensões corretas e recomendadas</h3>
    <p>Os(As) desenvolvedores(as) precisam ter maior conhecimento dos tipos de imagens. Numa próxima versão, o 10 só será aplicado caso o desenvolvedor utilize formatos novos como webp e avif usando a tag picture. Se utilizar PNG em imagens com fundo transparente e jpg em fotos, irá receber 8.</p>
    <figure>
      <Grade width="{150}" consumed="{8.13}" total="{10}" />
      <figcaption>É uma nota boa, mas que pode subir para 9 com facilidade.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Será mantido onde está.</p>
    <div class="divider"></div>
    <h3>Se utilizou as fontes corretas, nos tamanhos e cores recomendadas pelo designer</h3>
    <p>Este descritor é para capturar quem é pixel-perfect. Desenvolvedores(as) que tem bastante precisão em larguras, tamanhos de fontes, tamanhos de linha, margens, preenchimentos tem valor em agências e em equipes de marketing.</p>
    <figure>
      <Grade width="{150}" consumed="{7.87}" total="{10}" />
      <figcaption>Precisão é um diferencial importante demais para ser escanteado. Esta nota precisa subir urgente.</figcaption>
    </figure>
    <h4>Futuro do descritor:</h4>
    <p>Deve ser mergido com fidelidade ao design proposto.</p>
    <div class="divider"></div>
    <h2>Descritores opcionais e "Agradar ao patrão"</h2>
    <p>Como eram tarefas opcionais, nem todos os desenvolvedores fizeram todos os tópicos, tanto que alguns foram além ao que era sugerido pelo briefing. Para facilitar a leitura, vamos listar numa tabela todos os resultados e o futuro de cada descritor.</p>
    <table>
      <thead>
        <tr>
          <th>Descritor</th>
          <th>Quantos fizeram</th>
          <th>Média</th>
          <th>Futuro</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Se há animações, e se elas são agradáveis ao olhar.</td>
          <td>11</td>
          <td>9.55</td>
          <td>Continuará sendo um descritor opcional.</td>
        </tr>
        <tr>
          <td>Se a máscara no input de telefone foi correta, impedindo a inclusão de letras e formatando um número</td>
          <td>11</td>
          <td>8.4</td>
          <td>Continuará sendo um descritor opcional, talvez com peso de agradar o chefe.</td>
        </tr>
        <tr>
          <td>Se a requisição para o servidor apontar para o Método Post</td>
          <td>8</td>
          <td>10</td>
          <td>Ele será mergido com o descritor obrigatório de cunho amplo.</td>
        </tr>
        <tr>
          <td>Se o formulário funcionar, se o usuário terá os feedbacks necessários</td>
          <td>13</td>
          <td>7.42</td>
          <td>Continuará sendo um descritor opcional, talvez com peso de agradar o chefe.</td>
        </tr>
        <tr>
          <td>Se o HTML está semântico</td>
          <td>23</td>
          <td>8.82</td>
          <td>Será mergido com um descritor obrigatório.</td>
        </tr>
        <tr>
          <td>Se a área da dobra for uma imagem e uma div por cima</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Se o hover utilizado tem transition de css</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Se as imagens possuem os atributos corretos</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Pontuação no web.dev</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Se criou em css puro, criou variáveis internas. Se usou algum pré-processador, criou variáveis e mixins</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Usou algum framework</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Há feedback visual após a requisição</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Boas idéias de reutilização do código</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Textos alternativos que respeitam pessoas de baixa visão, empoderando o usuário e não dando julgamento de valor</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Usou vite</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Usou CSS-Clip para fazer a imagem de triangulo</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>README bem escrito</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Versão em inglês</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td>Dark Mode</td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</main>

<style lang="stylus">
  color = rgba(0,0,0,.1)
  color2 = rgba(0,0,0,.06)
  .container
    max-width 1200px
    width calc(100% - 30px)
    margin 0 auto
  header
    width 100%
    background #010101
    padding 10px
    text-align center
  h1
    color #fff
    margin 0
  table
    width 100%
    border-collapse collapse
    td, th
      border 1px solid #ccc
      padding 5px 10px
    th
      text-align left
      &.pontuation
        width 140px
  figure
    margin 30px auto
    width 100%
    margin-bottom 30px
    figcaption
      text-align center
      font-size 14px
      margin-top 20px
  h4
    margin 0
  .divider
    margin 30px 0
    height: 20px
    position: relative
    width: 100%
    background: radial-gradient(ellipse farthest-side at top center, color, transparent)
    &:before
      content: ""
      display: block
      position: absolute
      top: 0px
      right: 0
      left: 0
      height: 3px
      background: linear-gradient(left, transparent, color2, color2, transparent)
</style>