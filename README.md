<div align = "justify">

# **FarmFIT**

## __Introdução ao FarmFit__

 O Brasil é referência para o mundo inteiro no quesito do agronegócio, reconhecido mundialmente pela qualidade de seus solos, recursos naturais e produtividade rural. Mas, o que as pessoas não percebem é que neste mercado quem predomina são os pequenos e médios agricultores com baixo poder aquisitivo e que realizam trabalhos manuais, isto é, normalmente trata-se de tarefas sem nenhum tipo de tecnologia em todos os processos. Segundo dados do Governo Federal em 2022, cerca de 25% de toda a produção agrária nacional vem da agricultura familiar.

 A partir deste fato, o mercado focou-se no desenvolvimento de soluções tecnológicas para as grandes fazendas e agricultores. Este público possui grande investimento e capacidade para investir em softwares designados para grandes controles de processos. O cenário atual  é de que normalmente são vendidos ERP 's e softwares complexos para o gerenciamento de grandes fazendas, não justificando a compra de um software robusto para o pequeno produtor, além disso, a agricultura é responsável por 70% do desperdício de água tratada no Brasil,  o uso irresponsável dos recursos naturais é um dos maiores problemas da sociedade.

 Visando remediar esse problema, o projeto tem como objetivo o melhor planejamento do uso dos recursos hídricos de pequenos e médios agricultores, por meio da captação de águas pluviais e seu uso em sistemas de irrigação, sendo um produto low-cost e que possibilite a utilização do mesmo para todos os tipos de clientes. 


## __Objetivos Específicos__

Com o objetivo de melhorar a administração dos recursos hídricos de pequenos e médios produtores, propõe-se a captação de águas pluviais na região de suas propriedades. Isso ocorre por meio de canos conectados às calhas de casas, barracões ou outras construções do local. Em seguida vem o armazenamento e o direcionamento para um sistema de irrigação. O tanque que estoca o líquido também pode ser preenchido manualmente ou ligado com a rede pública de abastecimento de água, de modo a não depender exclusivamente das chuvas e não comprometer a aguagem em períodos de estiagem. A rega é feita de modo a otimizar a utilização do líquido e evitar seu desperdício. Optou-se pela criação de um protótipo em escala que representa a iniciativa descrita instalada em uma quinta.

Ademais, dados a respeito do índice pluviométrico do local e da umidade do solo são coletados via sensores, os quais são disponibilizados em um aplicativo. Com tais informações, os agricultores têm os meios para tomada de decisões mais conscientes que melhorem a produtividade e a gestão de seus negócios de modo sustentável.

## __JUSTIFICATIVA__ 

Diversas notícias são publicadas cotidianamente a respeito da escassez hídrica e as dificuldades trazidas por ela. Estes problemas advêm da utilização exacerbada e incorreta da água e pelo descompromisso com a sustentabilidade. Desta forma, o projeto é desenvolvido com a finalidade de auxiliar na economia, no uso deste recurso e na consequente diminuição das despesas de maneira geral. 

Para o alcance de tal objetivo, pretende-se construir um esquema de captação da água da chuva, a qual é utilizada em sistemas de irrigação, automatizado por um ESP-32 (placa de prototipagem semelhante a um Arduino). Com o desenvolvimento desta proposta, é possível o reaproveitamento da água, por meio das precipitações. Como consequência, pretende-se alcançar uma melhor administração dos recursos hídricos, redução dos gastos a longo prazo e a ampliação dos lucros.

A ideia para a elaboração de tal plano surgiu através da preocupação com a insuficiência de água em inúmeros âmbitos, e consequentemente, com a intenção de auxiliar a resolver este problema. Sendo assim, o uso sustentável deste recurso se mostrou como uma necessidade. 

Depois de muito planejamento e pesquisa, foi decidido que o diferencial do projeto está relacionado a criação de um aplicativo que tornará possível a exposição dos dados relacionados a captação da água da chuva para o usuário. Com esse feedback, o planejamento e a organização poderão ser efetuados da melhor maneira possível, permitindo reduções de gastos e consequentemente o aumento dos lucros do agricultor.


## __MATERIAIS E MÉTODOS__

<br>

O protótipo desenvolvido consiste em uma casa de 30 cm por 30cm e 22 cm de altura apoiada sobre uma base retangular de 80 cm por 50 cm, ambas feitas de madeira MDF e banhadas em membrana acrílica, um impermeabilizante também conhecido como manta acrílica líquida. Esta estrutura é mostrada em Figura 1 e o desenho das peças que a compõem em Figura 2. Dois potes feitos do mesmo material contendo uma pequena horta de mini alfaces estão apoiados sobre o suporte, representando as plantações existentes nas propriedades rurais. 

<div style="display:inline_block" align="center">

 <p>Figura 1 - Estrutura em Madeira MDF </p>

 <img src="assets/estruturaemmdf.png" height="250px">

 Fonte – Elaboração Própria
 
</div>
<br>
<div style="display:inline_block" align="center">

 <p> Figura 2 – Desenho das peças usadas </p>
 
 <img src="assets/pecasusadas.png" height="300px">

 Fonte – Elaboração Própria
 
</div>
<br> 
Ademais, cabos flexíveis estão conectados ao telhado da residência para, juntamente com um sensor de fluxo de água, representar o sistema de captação de águas pluviais. Eles são ligados a um aquário acrílico, usado como tanque de estocagem do recurso, e o conectam ao sistema de irrigação do pequeno canteiro, composto por um sensor de umidade do solo e uma mini válvula solenoide. Ambos os sensores citados estão conectados a um ESP-32, o qual é mantido em uma caixa de passagem. 
<br>
O website, cuja página inicial pode ser vista em Figura 3, por sua vez, traz ao usuário um acesso fácil e rápido às informações coletadas pelos sensores. Ele foi estruturado usando o padrão proposto pelo framework Web do Python chamado Django. Esta ferramenta lida com o back-end (termo amplo que abrange operações no banco de dados, roteamento, autenticação, etc.), sendo responsável por atualizar dinamicamente os gráficos de umidade e fluxo d'água, visíveis nas Figuras 4 e 5, de acordo com novas entradas no banco de dados. O software XAMPP foi empregado a fim de hospedar um servidor local Apache, que permanece ativo para receber as requisições do ESP-32 contendo as leituras dos sensores, bem como um banco de dados MySQL, o qual é atualizado em seguida. Ademais, o Django oferece uma ORM nativa (camada entre o banco de dados e a linguagem em si) para facilitar a gestão do banco de dados. ChartJS, um API do JavaScript, foi utilizado no contexto de gerar gráficos com maior facilidade e nível de abstração, além de providenciar numerosas opções de estilização. Por fim, linguagens como HTML, CSS e JavaScript foram utilizadas no front-end, ou seja, aquilo que o usuário vê, de fato, ao acessar o site.

## __Orçamento__

O planejamento é uma etapa fundamental para o sucesso de um projeto. Nesse contexto, a pesquisa de valores dos itens e a realização do orçamento são mecanismos de controle imprescindíveis. É com isso que as informações sobre o desempenho financeiro da proposta em questão são extraídas.

Empregou-se a metodologia “bottom up”, uma estratégia cujo nome significa de baixo para cima, para o cálculo do orçamento. Nela são analisados, primeiramente, os aspectos financeiros e, posteriormente, a economia da empresa como um todo. Este método possui uma análise fundamentalista, sendo uma maneira de detalhar e verificar profundamente os dados de uma companhia (Jehniffer,2021).

Em razão do “bottom up”, três buscas diferentes para o preço de cada objeto foram feitas e, com a média dos valores encontrados, calculou-se o orçamento, como demonstrado na Figura 6. A estimativa final foi de R$ 198,81. Os links dos sites consultados estão no apêndice.

<div style="display:inline_block" align="center">
  <p> Figura 3 – Orçamento do Projeto </p>

  <img src="assets/orcamento.png" height="150px">

  Fonte – Elaboração Própria
 
</div>

## __Retorno Esperado__

Como consequência de um planejamento bem estruturado e organizado do projeto de maneira geral, espera-se um retorno considerando aspectos econômicos e sociais.
<br>

 Em relação a perspectiva tangível, pode-se destacar:
 <ul>
     <li> Otimização sustentável da utilização da água </li>
     <li> Redução do consumo de água devido ao processo de captação </li>
     <li> Redução de custos em consequência a economia de água </li>
     <li> Melhor aproveitamento das águas pluviais </li>
 </ul>
 <br>
 
 Em relação a perspectiva intangível, pode-se destacar:
 <ul>
     <li> Melhoria da administração dos recursos hídricos de pequenos e médios produtores </li>
     <li> Melhoria da produtividade de maneira geral </li>
     <li> Desenvolvimento de uma gestão de negócios mais sustentável </li>
     <li> Possibilidade de obtenção de feedback sobre o processo, contribuindo para tomada de decisões mais conscientes </li>
 </ul>

![](images/template.png)  

O template também contém análises para indicar se os dados estão atualizados.

Análise do status dos dados

![](images/analise.PNG)  

### **Enumeration Sets**
Foram utilizados *enumeration sets* para transformar os números inteiros vindo das análises em frases para a melhor clareza das informações.
![](images/enumeration_sets.PNG)

### **Elements**
A árvore de elementos foi criada de forma a trabalhar em conjunto com o template formando o caminho das *tags*.

![](images/elements.PNG)

### **Servidor**

Ubuntu#######  LTS com o IP: ```###.##.###.#```

## __Visualização criada no projeto__

![](images/dashboard.PNG) 

## __Resultados Esperados__
O projeto deve receber um call back da Sigfox e inserir os dados no Data Archive através de uma Web API da OSISoft.

## __Pontos de Atenção__
 
Credenciais da <a href="https://dashboard.####### .com.br/####### 
">Plataforma da Sigmais</a>   
Login: #######    
Senha: ####### 

## __Referências__
**Sites**:

[Sigfox](https://www.sigfox.com/en "Sigfox")   
[tudosobreiot](https://tudosobreiot.com.br/agora-ficou-facil-chegou-a-conectividade-sigfox-plug-play/ "Sigmeter")  
[Sigmais](https://sigmais.io/br "Sigmais")  
[Zdnet](https://www.zdnet.com/article/what-is-the-internet-of-things-everything-you-need-to-know-about-the-iot-right-now/ "IoT")  
[Sebrae](https://www.sebrae.com.br/sites/PortalSebrae/artigos/o-que-e-uma-startup,6979b2a178c83410VgnVCM1000003b74010aRCRD "Startup")  
[Thalesgroup](https://www.thalesgroup.com/en/markets/digital-identity-and-security/iot/resources/innovation-technology/low-power-wide-area-technology "LPWAN")  
[Totvs](https://www.totvs.com/blog/developers/back-end/ "Backend")  
[Vertigo](https://blog.vertigo.com.br/o-que-e-api-entenda-de-uma-maneira-simples/ "API")  
[PHP](https://www.php.net/manual/pt_BR/intro-whatis.php "PHP")


 


</div>
