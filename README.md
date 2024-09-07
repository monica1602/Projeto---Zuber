# Projeto Análise de Dados Zuber

## Descrição do Projeto
Nesse projeto foi analizado a empresa Zuber, uma empresa de compartilhamento de caronas que está sendo lançado em Chicago. Os Objetivos são encontrar padrões nas informações disponíveis, entender as preferências dos passageiros e o impacto de fatores externos sobre as caronas. Foi trabalhado em um banco de dados, analisando os dados dos concorrentes e testado uma hipótese sobre o impacto do clima na frequência das viagens.
Obs: a parte do SQL foi feita dentro da plataforma Tripleten, mas as demais tarefas e os códigos estão nos arquivos

## As tarefas são:
- Revisar a estrutura dos dataframes
- Modificar os dataframes conforme necessário: tipos de dados, valores ausentes, valores duplicados
- Análise exploratória de dados
- Realizar testes de hipóteses:
  - Hipótese: a duração dos passeios do Loop para o Aeroporto Internacional O'Hare muda nos sábados chuvosos

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
- Pyhton: Linguagem principal utilizada para análise
- Pandas: Biblioteca para manipulação e análise de dados
- Matplotlib: Biblioteca para gerar gráficos
- Numpy: Biblioteca que permite trabalhar com objetos multidimensionais, como matrizes e sequências
- Math: Biblioteca que permite usar funções matemáticas
- Seaborn: Biblioteca de visualização de dados
- Scipy: Bbilioteca que fornece uma manipulação conveniente e rápida de um array N-dimensional
- Ploty.express: Bbilioteca que permite criar visualizações rápidas e eficientes
- Datetime: Biblioteca que oferece uma ampla gama de recursos que simplificam a comunicação com a internet
- BS4: Bbilioteca essencial para realizar Web Scraping com Pyhton
- Re: Biblioteca que fornece operações de correpsondência de expressões regulares

## Resultados
- A empresa Flash Cab é uma empresa consolidada com uma alta demanda or viagens
- Os destinos mais requisitados são River North, Streeterville, West Loop e Loop
- Foram encontrados algumas corridas com duração igual a zero. O que quer dizer que ou elas foram canceladas ou tiveram problemas na extração de dados
- Foi possível verificar que a hora do dia tem uma influência significativa na duração da viagem
- A hipótese foi testada através de um t-test e ela foi rejeitada, confirmando que a duração média das viagens realmente varia nos sabádos chuvosos

## Aprendizados
- Análise de dados
- Qualidade dos dados
- Construção e análise de gráficos
- Análise de hipóteses
- SQL

## Como executar o projeto
- Clone o repositório
- Navegue até o diretório do projeto
- Abra o projeto no seu IDE favorito
- Instale as dependências
- Execute o script principal
