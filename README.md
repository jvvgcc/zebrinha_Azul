# zebrinha_Azul

Descrição
Este projeto visa criar uma base de dados unificada a partir de duas APIs distintas: uma que fornece dados climáticos e outra que fornece dados de trânsito. Os dados coletados são inicialmente armazenados em um banco de dados MySQL. Posteriormente, são transferidos para o Google BigQuery para futura análise mais avançada. Finalmente, os dados são visualizados e analisados no Power BI.

Este projeto não só ilustra o processo de coleta, armazenamento e transferência de dados entre diferentes plataformas, mas também demonstra como esses dados podem ser analisados para obter insights valiosos sobre o impacto das condições climáticas no tráfego.

Desenvolvimento do Projeto:
Após a análise do conteúdo proposto e da consulta aos dois links solicitados, resolvi trazer o que era permitido, já que algumas API 's eram pagas. Criei duas tabelas para o primeiro link, o relacionado ao clima, e 3 para o relacionado ao trânsito através da linguagem de programação Python e suas extensões.
Na API sobre o clima, trouxe uma tabela mostrando a temperatura atual, mínima e máxima e outra tabela com a previsão dos próximos 4 dias. Salvei os resultados num .CSV (dados_climaticos.csv e  previsao_dias.csv)
Utilizei a biblioteca asyncio que permite a execução aninhada de loops; aiohttp que lê links oriundos da internet e nest_asyncio, módulo que corrige o asyncio para permitir o uso aninhado de asyncio.run e loop.run_until_complete e o pandas para leitura tabular dos dados. Nesta etapa houve processo ETL, como remoção de colunas vazias e linhas sem valor. 
Na API sobre o trânsito, trouxe uma tabela mostrando as capitais do Brasil e suas respectivas longitude e latitude; a distância entre a capital do Brasil e as demais capitais e o outra tabela mostrando o tempo até Brasília (cidades.csv, distancia_capital.csv e tempo_capital.csv). Criei uma relação não muito complexa entre os dados disponíveis.
Para essa etapa, utilizei a biblioteca do google maps para leitura de dados de muitas funções que ele pode oferecer, como: leitura de coordenadas, conversão de endereços e tempo de viagem. Módulo datetime para manipulação de datas e horas e o pandas para leitura tabular.
No Mysql, criei a modelagem lógica e seus respectivos relacionamentos; a criação da tabela física e a inserção dos valores.
Os dados foram armazenados num Data warehouse no Bigquery, o link será disponibilizado;
No Power Bi, foram feitos dois dashboards, um de clima e outro de trânsito, os dois com conceitos simples e dinâmicos.
