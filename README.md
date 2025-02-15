# Projeto Análise de Dados Zuber

## Descrição do Projeto
Este projeto envolveu a análise de dados da Zuber, uma empresa de compartilhamento de caronas que está sendo lançada em Chicago. O objetivo principal foi identificar padrões nas informações disponíveis, compreender as preferências dos passageiros e avaliar o impacto de fatores externos, como o clima, na frequência das viagens. A análise foi conduzida utilizando um banco de dados, no qual foram analisados também os dados dos concorrentes, visando uma comparação de desempenho e comportamento. Além disso, foi testada uma hipótese sobre o impacto das condições climáticas na variação da demanda pelas viagens.
A parte de SQL foi realizada na plataforma Tripleten, enquanto as demais tarefas e implementações de código foram desenvolvidas e armazenadas nos arquivos do projeto.

## As tarefas são:
- Revisar a estrutura dos dataframes
  - Inspecionar a organização e tipos de dados para garantir integridade e consistência.
- Modificar os dataframes conforme necessário
  - Tipos de dados: Garantir que as colunas possuam os tipos corretos de dados para análise (e.g., converter strings para datas, inteiros ou flutuantes quando necessário).
  - Valores ausentes: Identificar e tratar valores ausentes, substituindo-os ou removendo-os conforme apropriado.
  - Valores duplicados: Detectar e remover registros duplicados para evitar distorções nos resultados.
- Análise exploratória de dados (EDA)
  - Explorar o conjunto de dados, identificando padrões, relações e distribuições por meio de estatísticas descritivas e visualizações (como histogramas, boxplots e scatterplots).
  - Investigar a relação entre variáveis, especialmente a duração dos passeios em diferentes condições climáticas.
- Realizar testes de hipóteses
  - Hipótese: A duração dos passeios do Loop para o Aeroporto Internacional O'Hare muda nos sábados chuvosos.
  - Hipótese Nula (H0): Não há diferença significativa na duração dos passeios entre os sábados chuvosos e não chuvosos.
  - Hipótese Alternativa (H1): A duração dos passeios do Loop para o Aeroporto Internacional O'Hare é significativamente diferente nos sábados chuvosos.
  - Método de Teste: Selecionar o teste adequado (como o teste t para duas amostras independentes ou o teste de Mann-Whitney), dependendo da distribuição dos dados.
  - Nível de Significância: Definir um valor de α (geralmente 0,05) para determinar se a diferença observada é estatisticamente significativa

 ## Dicionário de dados (SQL)
 Um banco de dados com informações sobre viagens de táxi em Chicago
 - neighborhood: dados osbre os bairros da cidade
   - 'name': nome do bairro
   - 'neighborhood_id': código do bairro
- cabs: dados sobre os táxis
  - 'cab_id': código do veículo
  - 'vehicle_id': a identificação técnica do veículo
  - 'company_name': a empresa proprietária do veículo
- trips: dados sobre corridas
  - 'trip_id': código da corrida
  - 'cab_id': código do veículo que opera a corrida
  - 'start_ts': data e hora do início da corrida (tempo arrendondado para a hora)
  - 'end_ts': data e hora do final da corrida (tempo arrendondado para a hora)
  - 'duration_seconds': duração da corrida em segundos
  - 'distance_miles': distância percorrida em milhas
  - 'pickup_location_id': código do bairro de retirada
  - 'dropoff_location_id': código do bairro de entrega
- weather_records: dados sobre o clima
  - 'record_id': código de registro meteorológico
  - 'ts': grava data e hora (tempo arrendondado para a hora)
  - 'temperature': temperatura quando o registro foi feito
  - 'description': breve descrição das condições meteorológicas

## Dicionário de dados (Python)
- project_sql_result_01.csv:
  - 'company_name': nome da empresa de táxi
  - 'trips_amount': o número de corridas para cada empresa de táxi de 15 a 16 de novembro de 2017
- project_sql_result_04.csv:
  - 'dropoff_location_name': bairros de Chicago onde as corridas terminaram
  - 'avergare_trips': o número médio de viagens que terminaram em cada bairro em novembro de 2017
- project_sql_result_07.csv: dados sobre viagens do Loop para o Aeroporto Internacional O'Hare
  - 'start_ts': data e hora do começo da corrida
  - 'weather_conditions': condições meteorológicas no momento em que a corrida começou
  - 'duration_seconds': duração da viagem em segundos

## Ferramentas e Bibliotecas utilziadas
- Python: Linguagem de programação principal utilizada para análise de dados, oferecendo uma ampla gama de bibliotecas e recursos para manipulação, visualização e modelagem de dados.
- Pandas: Biblioteca essencial para manipulação e análise de dados estruturados, como DataFrames, permitindo realizar operações como filtragem, agregação e transformação de dados.
- Matplotlib: Biblioteca fundamental para a criação de gráficos e visualizações estáticas em Python, amplamente utilizada para gerar gráficos de barras, linhas, dispersão, entre outros.
- NumPy: Biblioteca poderosa para computação científica em Python, que permite trabalhar com arrays multidimensionais e realizar operações matemáticas eficientes em grandes volumes de dados.
- Math: Biblioteca que fornece funções matemáticas básicas, como operações trigonométricas, exponenciais, logaritmos e arredondamento, facilitando cálculos matemáticos precisos.
- Seaborn: Biblioteca de visualização de dados baseada em Matplotlib, projetada para criar gráficos estatísticos atraentes e informativos com menos código.
- SciPy: Biblioteca voltada para operações científicas avançadas, complementando o NumPy, com funções de otimização, integração, álgebra linear e estatísticas.
- Plotly Express: Biblioteca que permite criar visualizações interativas rápidas e eficazes com foco na facilidade de uso e na criação de gráficos dinâmicos para análise exploratória de dados.
- Datetime: Biblioteca que fornece funcionalidades robustas para manipulação de datas e horas, oferecendo suporte a cálculos e conversões de datas, além de simplificar operações temporais complexas.
- BeautifulSoup (BS4): Biblioteca indispensável para realizar Web Scraping em Python, permitindo extrair e parsear dados de páginas web de forma simples e eficiente.
- Re: Biblioteca que oferece operações para correspondência de expressões regulares, facilitando a busca e manipulação de padrões de texto em strings.

## Imagens

### Localização de destino (bairro)
<img src="https://github.com/user-attachments/assets/b4ab8d11-44e6-473b-ad5d-ac865894ee12" alt="Projeto 7" width="200"/>

### Nome da companhia
<img src="https://github.com/user-attachments/assets/9ea1e371-8bb7-470b-a4f0-6603f64176ba" alt="Projeto 7" width="200"/>

### Hipótese
<img src="https://github.com/user-attachments/assets/044e40f9-97eb-41df-b476-071f26fe4456" alt="Projeto 7" width="200"/>

## Resultados
- A empresa Flash Cab: Empresa consolidada e com alta demanda por viagens de táxi, que atende a diversos destinos em uma cidade movimentada.
- Destinos mais requisitados: Os destinos mais frequentes para corridas incluem áreas populares como River North, Streeterville, West Loop e Loop.
- Corridas com duração igual a zero: Foram identificadas corridas com duração registrada como zero, o que pode indicar que as corridas foram canceladas ou houve falhas na coleta ou extração dos dados.
- Influência da hora do dia na duração das viagens: Observou-se que a hora do dia tem um impacto significativo na duração das viagens, com variações evidentes ao longo do dia, sugerindo que fatores como tráfego e horários de pico influenciam as corridas.
- Teste da hipótese: A hipótese de que a duração média das viagens muda nos sábados chuvosos foi testada através de um t-test. O resultado foi a rejeição da hipótese nula, confirmando que a duração média das viagens é significativamente diferente nos sábados chuvosos, o que pode estar relacionado ao impacto das condições climáticas no tráfego e no comportamento dos motoristas.

## Aprendizados
- Análise de dados: Processamento e avaliação das informações disponíveis, identificando padrões e comportamentos dos dados para gerar insights úteis.
- Qualidade dos dados: Avaliação e tratamento de dados para garantir que estejam completos, precisos e consistentes. Isso inclui o tratamento de valores ausentes, duplicados e a conversão correta de tipos de dados.
- Construção e análise de gráficos: Desenvolvimento de visualizações gráficas para facilitar a interpretação dos dados, como gráficos de dispersão, histograma e boxplot, ajudando a identificar tendências, padrões e outliers.
- Análise de hipóteses: Formulação e verificação de hipóteses através de testes estatísticos, como o t-test, para confirmar ou refutar suposições sobre os dados, garantindo a validade das conclusões.
- SQL: Uso de SQL para consultar e manipular bancos de dados, extraindo e transformando dados necessários para a análise, como selecionar, filtrar, agrupar e agregar informações de diversas tabelas.
  
## Contexto real
- Empresas emergentes no setor de compartilhamento de caronas que desejam analisar os principais destinos de viagem para otimizar seus serviços e estratégias de mercado.
- Empresas consolidadas que buscam aprimorar a experiência do usuário por meio de análises de dados, visando melhorar a satisfação do cliente e a eficiência operacional.
- Profissionais de análise de dados que desejam compreender melhor os padrões operacionais de sistemas de compartilhamento de caronas e identificar oportunidades para otimização e aumento de resultados.
  
## Como executar o projeto
- Clone o repositório
- Navegue até o diretório do projeto
- Abra o projeto no seu IDE favorito
- Instale as dependências
- Execute o script principal
