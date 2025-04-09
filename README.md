<h1 style="font-weight: bold;">AWS QuickSight 💻</h1>

<h2>Descrição do Projeto</h2>
Nesse projeto irei usar o Amazon QuickSight para analisar dados e gerar a visualização deles. Esse projeto servirá de base para o aprendizado de serviços de nuvem e análise de dados (os dados analisados aqui são referentes a uma plataforma de streaming).

<h3>Considerações Iniciais</h3>

- É importante que desmarcar o checkbox de 'Add Paginated Reports' para evitar uma cobrança financeira imediata.
- O "manifest.json" é um arquivo que conta para o QuickSight o caminho e a estrutura o data set.
- O Amazon S3 será usado para armazenar o data e o manifest.json.

<h3>Armazenando o conjunto de dados no Amazon S3</h3>

- É criado um bucket s3.
- Fazemos o upload do data set para esse bucket.
- Devemos fazer as devidas alterações no manifest.json (indicando o nome do bucket que está sendo usado no momento) e depois realizar seu upload também para o bucket.

<h3>Criando uma conta no Amazon QuickSight</h3>

- Aqui é importante criar uma conta associada a sua conta da aws para que se possa acessar os serviços do quicksight.
- O detalha nessa parte ainda consite em desmaracar a opção que vem marcada por padrão de 'Ass Paginated Reports'.
  

<h3>Conectando ao bucket S3</h3>

- Criamos um novo conjunto de dados dentro do QuickSight.
- Conectamos o QuickSight ao nosso bucket usando o manifest.json.

<h3>Criando Gráficos</h3>

- Para criarmos quadros de visualização simplesmente precisamos clicar em "ferramentas" e o QuickSight vai automaticamente gerar um gráfico que melhor comporta os tipos de dados no nosso dataset.
- Aqui podemos criar os próximos gráficos escolhendo quais campos serão analisados e qual será o eixo y, bem como as formas de visualização (barras, tabela, linha etc) e se desejamos aplicar filtros.
- É importante que saibamos escolher o formato de visualização que mais facilita a geração de insights para o nosso conjunto de dados que estamos analisando.

<h3>Atualizando dados</h3>

- Há uma boa quantidade de células vazias no campo "country" de nosso data set.
- Assim que baixarmos a nova versão do conjunto de dados (com todas as células preenchidas), nós temos que atualizar os arquivos no bucket S3 que estamos usando.
- o manifest.json deve ser alterado também indicando o novo arquivo de nosso conjunto de dados.
- Após isso, devemos dar um refresh na página do AWS QuickSight e ele mostrará os gráficos com as novas alterações.

<h4>Finalizando</h4>

- Apóa essas configurações poderemos ver todos os gráficos que geramos e podemos dar nomes a eles também para facilitar a leitura de terceiros.
