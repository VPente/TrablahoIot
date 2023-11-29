<div align="center">
<h1>Máquina de vendas automática portátil</h1>
</div>
<h2>O Problema</h2>

A falta de pontos fixos de venda em eventos que ocorrem em cidades distantes.
Máquinas de vendas convencionais são grandes e pesadas o que dificulta o transporte fazendo com que oportunidades de vendas em eventos  sejam perdidas para isso a nossa solução propõem um projeto de máquina de vendas automática portátil onde que é facilmente carregada de evento em evento trazendo assim uma maior eficiência e maiores oportunidades, abaixo será documentado as etapas e processos para o desenvolvimento do MVP desta solução
<div>
<h2>Diagrama de Arquitetura</h2>
<img src="./imgs/DiagramArq.png">
</div>

<h2> Listas de Componentes utilizados </h2>
<p>- 3 ESP32</p>
<p>- 2 Motores de Passo 28byj-48</p>
<p>- 2 Controladores de Motor de passo Driver Uln2003 Arduino Robótica/nf</p>
<p>- 2 Sensores Ultrassonicos Hc-Sr04</p>
<p>- 1 Fonte 5V </p>


<h1>Estrutura</h1>

<div align="center">
<h2>Back-End</h2>
</div>
<div>
    <h3>Tecnologias Utilizadas:</h3>
    <div> <h4>Node.js, JavaScript e TypeScrip</h4>
    O projeto utiliza o ambiente de execução Node.js, que permite a execução de código JavaScript do lado do servidor. O código é desenvolvido principalmente em JavaScript, com o uso opcional de TypeScript para fornecer tipagem estática e outras funcionalidades avançadas.</div>
    <div>
    <h4>Prisma</h4>
    O Prisma é o principal ORM (Object-Relational Mapping) escolhido para a interação com o banco de dados. Ele simplifica a manipulação de dados, oferecendo uma abstração intuitiva para consultas ao banco de dados MongoDB.</div>
    <div><h4>MongoDB</h4>
    O banco de dados escolhido para armazenar os dados do projeto é o MongoDB. Sua natureza de banco de dados NoSQL oferece flexibilidade e escalabilidade, adequando-se bem às necessidades do projeto.</div>

</div>
<div>
<h3>Arquitetura</h3>
O projeto adota uma arquitetura limpa, que visa separar as responsabilidades em diferentes camadas para facilitar a manutenção e escalabilidade do sistema. A orientação a objetos é utilizada para promover um design modular e coeso.
</div>
<div>
<h3>Camadas da Arquitetura</h3>
<div><h4>Entidades</h4>
Nesta camada, são definidas as entidades de negócio do sistema. Cada módulo do projeto possui suas próprias entidades, como máquinas de venda, esteiras, produtos, histórico de vendas e filas de venda.
</div>
<div><h4>Casos de Uso</h4>
Os casos de uso representam as principais funcionalidades do sistema. Cada módulo possui seus próprios casos de uso, que interagem com as entidades para realizar operações específicas.
</div>
<div><h4>Controladores</h4>
Os controladores atuam como interfaces entre as rotas da aplicação e os casos de uso correspondentes. Eles recebem as requisições, manipulam os dados necessários e chamam os casos de uso apropriados.
</div>
<div><h4>Gateways</h4>
Os gateways são responsáveis pela comunicação com fontes externas, como o banco de dados MongoDB. O Prisma é utilizado como gateway para manipular os dados no banco de dados.
</div>
Módulos
1. vendingMachines
Este módulo é responsável por gerenciar as máquinas de venda. As entidades associadas incluem informações sobre as máquinas e funcionalidades relacionadas à venda de produtos.

2. vendingMachinesConveyors
O módulo vendingMachinesConveyors concentra-se no gerenciamento das esteiras das máquinas de venda.

3. products
O módulo products gerencia as informações sobre os produtos disponíveis para venda. Isso inclui detalhes como nome, preço e descrição.

4. productSalesHistory
Este módulo armazena o histórico de vendas dos produtos. Ele registra informações relevantes sobre cada transação realizada.

5. shoppings
O módulo shoppings é responsável por armazenar a fila de vendas. Ele gerencia a ordem em que as transações são processadas, garantindo uma experiência de compra eficiente.
</div>
