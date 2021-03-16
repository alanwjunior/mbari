<h1>ARQUITETURA DE INTEGRAÇÕES - IGTI</h1>

<h4>Fazer uma análise crítica sobre a aplicação monolítica, destacando o entendimento sobre o seu funcionamento, quais seriam os benefícios e/ou problemas dessa aplicação em uma arquitetura de integração com clientes.</h4>

<p>A aplicação monolítica pode ser uma boa opção para o início do projeto, tendo em vista que as fronteiras dos domínios serão amadurecidas conforme o tempo. Além do mais, pode ser difícil dimensionar o uso da aplicação em um primeiro instante. Entre as principais vantagens da arquitetura atual, podemos levantar:
- a simplicidade inicial da arquitetura permite uma entrega e manutenção do produto mais rápido (achar bugs e debugar a solução é mais fácil);
- a arquitetura monolítica, para um primeiro momento que não requer uma escalabilidade, irá requerer um custo mais baixo de infraestrutura.</p>

<p>Porém no longo prazo essa arquitetura pode trazer problemas de integração, pois:
- como os domínios não estão separados, as informações estão centralizadas em um único banco de dados. Uma sobrecarga no banco de dados poderia ocasionar uma queda completa da aplicação;
- caso surja a necessidade de trazer dados que não são retornados hoje, vai ser necessário criar novos endpoints para serem consumidos.
</p>

<p>Portanto, em um momento posterior pode ser interessante adotar uma arquitetura de microserviços e até mesmo utilizar o GraphQL para criar um padrão de consulta mais sofisticado para os consumidores da API. Porém essa decisão trás consigo os seguintes pontos:
- aumento de complexidade: debugar é mais difícil, requer maior domínio e conhecimento de cada parte;
- aumento no custo de infraestrutura: cada microserviço precisa possuir o seu próprio banco de dados e deve ser publicado e configurado para escalar de forma individual;
</p>

<p>Por outro lado, teremos vantagens como:
- possibilidade de escalar cada microserviço conforme necessidade;
- aumento da resiliência da solução: se um microserviço estiver fora do ar, ainda assim os outros microserviços estarão disponíveis.
</p>
