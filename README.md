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

<center> Figura 1 - Estrutura em Madeira MDF </center>


### **PI System**
<img src="images/LOGOOSI.png" height="90px"> 

O PI System™ é uma infraestrutura empresarial aberta que conecta dados baseados em sensores, sistemas e pessoas. O resultado é: informações acionáveis e em tempo real que capacitam as empresas a otimizar e transformar seus negócios.

## __Guia de Implementação__

### **PI Data Archive**

Foram criados 30 *points* para armazenar as informações de cada atributo no *Data Archive*.

*Points* criados para armazenar informações dos sensores Sigtemp.

![](images/points.PNG)

### **Sigtemp Template**
Foi criado um template para organizar os elementos. Foram adicionadas todas as tags com um caminho genérico **\\%Server%\%..\..\Element%.%..\Element%.%Element%.%Attribute%**, que por sua vez busca o *point* de acordo com o diretório gerado pelos nomes dos elementos.

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
