<script lang="ts">
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
          <td>Descritores públicos obrigatórios</td>
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
    <p>Com estas avaliações acima, as pessoas tendem a achar que o 10 é praticamente impossível, entretanto, a minha expectativa é que se algum dev atingir 255, ele tira nota 10.</p>
  </div>
</main>

<style lang="stylus">
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
</style>