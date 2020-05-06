## projeto_b3 -> Dados Históricos
 * O projeto foi desenvolvido para automatização na análise de investimentos a partir de dados históricos como: Demonstração de Resultado, Balanço Patrimonial Ativo e Balanço Patrimonial Passivo.
 * Esse programa foi construído para a matéria SIN311 - Contabilidade em Informática (UNIFEI - Sistemas da Informação)

 No momento estão disponíveis os dados das empresas:
 * MGLU3 - MAGAZINE LUIZA S.A.
 * EMBR3 - EMBRAER S.A.
 * CVCB3 - CVC BRASIL OPERADORA E AGÊNCIA DE VIAGENS S.A.
 * LREN3 - LOJAS RENNER S.A.
 * OIBR4 - OI S.A.
 * CGAS5 - CIA GAS DE SAO PAULO - COMGAS
 * VVAR3 - VIA VAREJO S.A.
 * WHRL3 - WHIRLPOOL S.A.

### Requirements
 * Python 3.x
 * requests  	-> pip install requests
 * time      	-> pip install time
 * sys			-> pip install sys

 [ParseHub](https://www.parsehub.com/) - Utilizado para crawl dos dados AJAX


### Arquivos do diretório
  * **VBA Excel** - Essa pasta contem os códigos raw para utilizção no excel
      1. BP_B3_Blazzi - Formata os arquivos de Balanço Patrimonial (BPA e BPP)
      2. DR_B3_Blazzi - Formata os arquivos de Demonstração de Resultados (DR)
  * **parsehub_projetos** - Pasta contém os projetos utilizados na aplicação do ParseHub, esses projetos precisaram ser importados para sua conta parsehub
  * **base_doc.py** - Dados utilizados para buscar os demonstrativos financeiros de cada empresa.
      1. Para adicionar um novo dado basta seguir o template no arquivos
      2. No site da b3 cada empresa em determinado ano possui uma variavel chamada NumeroSequencialDocumento que pode ser encontrada na URL do demonstrativo
  * **dados_historicos.py** - Programa principal - pode ser executado no cmd/terminal > python dados_historicos.py

### Passo a Passo
  1. Criar conta no ParseHub (fazer download da aplicação ou utilizar a versão online).
  2. Após a criação da conta no ParseHub, você possuirá uma api_key.
  3. Adicionar sua key em todas as variaveis api_key do arquivo dados_historicos.py.
  4. Importar os projetos para sua conta ParseHub - os três projetos utilizados estão na pasta parsehub_projetos.
  5. Caso necessário, substituir os tokens do projeto no arquivo dados_historicos.py.
  6. O programa é executado a com a entrada do usuário em três parâmetros (ticker, ano, demonstrativo).
  7. A execução correta do programa resultará em um arquivo csv.
  8. O arquivo csv é entitulado como ticker_ano_demonstrativo.csv (ex: MGLU3_2019_DR)
  9. O projeto acompanha o VBA do excel para uma formatação automática.
