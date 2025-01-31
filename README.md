# Atividade do Módulo 14 do Curso Cientista de Dados

Nessa ativida foi feito o pré-processamento dos dados de uma base de telecomunicação. O objetivo dessa análise no futuro será criar modelos para prever quais clientes são propensos a abandonar. Com isso a coluna Churn tem vital importância em nosso pré-processamento.

Antes de iniciar o pré-processamento abri a base de dados no excel para a verificação dos dados.

Passos realizados na atividade:
- Carregamento e verificação dos tipos de dados para possível transformação desses tipos:
  - As colunas 'Casado', 'Dependents' e 'Churn' estão com o tipo object( Yes e No).
  - Coloquei os campos em caixa baixa e depois substitui 'yes' por 1 e 'no' por 0.

* Verificação dos dados faltantes e ausentes e trazendo essas informações em forma de porcentagem:
  * As colunas Genero, PhoneService, Pagamento_Mensal e Churn apresentaram, respectivamente, as seguintes porcentagens: 0.48, 59.28, 13 e 0.20.
  * Verifiquei que a coluna Genero possui uma distruição homegênea dos dados entre os sexos. Dessa forma foi possível excluir as 12 linhas ausentes sem prejuízo à análise.
  * A coluna Pagamento_Mensal é relevante, por isso fiz o cálculo da média e mediana para verificar qual seria a melhor opção para substituir os dados ausentes. Utilizei os gráficos boxplot e histograma para análise. Como não havia uma assimetria significativa nos gráficos, os valores ausentes foram substituídos pela média.
  * Na coluna PhoneService tem uma grande porcentagem de valores ausentes ( 59% ). Fiz uma contagem dos valores e pude verificar que 91% dos campos foram preenchidos com 'Yes'. Substitui os valores ausentes po 'Yes'.
  * Ao retirar as 12 linhas de Genero, também foram retiradas as 4 linhas de Churn, contudo isso não afetará a análise.
  * Após todas as substituições e exclusões fiz a conversão dos valores das coluna Casado, Dependents e Churn de object para inteiro.

* Verificação e correção de valores digitados incorretamente, ou com letras maiusculas ou minusculas:
  * A coluna Genero possuia valores digitados de forma diferente. Fiz a substituição dos valores 'F' e 'f' para Female e os valor 'M' para Male.
  * Na coluna Servico_Internet havia valores em maiúsculos e minúsculos. Foi feita a substituição para todos os valores em minúsculo.
 
Por fim foram renomeadas as colunas Dependents, PhoneService e PaymentMethod para o português, ficando: Dependentes, Servico_Telefonico e Metodo_Pagamento.


