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

