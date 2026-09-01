# NIAS-IA
## Treinamento 2026-1

### Formas de iteração com o repositório:
1. Clone o repositório em sua máquina. 
2. Edite e salve o notebook que você vai apresentar na entrevista do Processo Seletivo.
3. Faça uma seção neste README.md como o exemplo abaixo.
4. Não retire as instruções do README.md

#### Rodolpho Neves
- Problema escolhido: Titanic - Machine Learning from Disaster
- O que precisa ser resolvido: Predizer se uma determinada pessoa sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 75% de acurácia
- Técnicas utilizadas para resolver o problema: 
    1. Descarte das colunas 'sibsp', 'parch', 'ticket' e 'cabin'
    2. Imputação de dados de média na coluna 'Age'
    3. Padronização da coluna 'fare'
    4. Transformação dos dados da coluna 'embarked' em valores numéricos ordinais
- Créditos: @rodolpho-neves

#### João Victor de Freitas Lucas
 - Problema escolhido: Titanic - Machine Learning from Disaster
 - O que precisa ser resolvido: Predizer se uma determinada pessoa sobrevive ou não ao acidente do Titanic
 - Melhor resultado obtido na submissão: 77,75% de acurácia
 - Técnicas utilizadas para resolver o problema:
     1. Comparação de diversos métodos e modelos
     2. Aplicação da estratégia ordinal encoder nas features catégoricas
     3. Imputação de dados nas colunas numéricas utilizando a estratégia most_frequent
- Créditos: @joaovictorfl18

#### Leonardo Celeste
  - Problema escolhido: Titanic - Machine Learning from Disaster (Capítulo 9 - Feature Engineering)
  - O que precisa ser resolvido: Transformar e enriquecer as variáveis brutas do dataset para que capturem melhor os padrões relacionados à sobrevivência dos passageiros, antes da etapa de modelagem
  - Melhor resultado obtido na submissão: *
  - Técnicas utilizadas para resolver o problema:
     1. Feature Selection com Mutual Information Score (mutual_info_classif) para medir a relevância de cada variável em relação a 'Survived'
     2. Feature Construction: extração do título social ('Title') a partir do campo 'Name', criação de 'FamilySize' (soma de 'SibSp' + 'Parch') e 'IsAlone'
     3. Feature Extraction com K-means (6 clusters em 'Age'/'Fare', com remoção de outliers) para gerar uma nova variável de agrupamento
     4. Feature Extraction com PCA (após normalização com MinMaxScaler) reduzindo 'Age' e 'Fare' a um componente principal
     5. Target Encoding da feature 'Title' com MEstimateEncoder, suavizando a média por categoria para evitar vazamento de dados
 - Créditos: @leoscelestee-coder

#### Victor Ferreira
- Problema escolhido: Titanic - Machine Learing from disaster
- O que precisa ser resolvido: Predizer se um determinado passageiro sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 76,5% de acurácia
- Técnicas utilizadas para resolver o problema:
    1. Descarte das colunas 'Cabin', 'Ticket' e 'Name' (excesso de nulos ou sem uso direto)
    2. Imputação de valores ausentes em 'Age', 'Fare' e 'Embarked' via pipelines, testando estratégias de média, mediana, zero e moda
    3. Encoding das variáveis categóricas 'Sex' e 'Embarked' com OneHotEncoder e LabelEncoder, comparando one-hot vs ordinal
    4. Criação de variáveis derivadas com pd.cut (AgeGroup) e pd.qcut (FareGroup)
    5. Validação cruzada para comparar Random Forest e Gradient Boosting e escolher o modelo final
- Créditos: @victortdsferreira

#### Igor Cabral
- Problema escolhido: Titanic - Machine Learning from Disaster (Capítulo 7 Data Cleaning)
- O que precisa ser resolvido: preparação dos dados para melhor desempenho do treinamento.
- Técnicas utilizadas para resolver problema:
    1. Seguir os passos dados na apostila!
        a. realizar a remoção das colunas "Cabin" e "Ticket"
        b. preencher as lacunas de NaNs com dados estatísticos razoáveis (no caso, mediana e moda)
        c. realizar um cut para agrupar "Age" e "Fare".
    2. Responder as perguntas.
-Créditos @igorye1010

#### Mauro Victor Carogio Manhaes de Araujo
- Problema escolhido: Covid Dataset (Capítulo 5 - Data Visualization)
- O que precisa ser resolvido: Analisar dados sobre a pandemia e tornar a analise de dados facil para o publico leigo por meio de graficos,
  que informem os diferentes efeitos da pandemia nos paises 
- Técnicas utilizadas para resolver o problema:
    1. Filtragem de dados
    2. Agrupamento de informacoes pertinentes
    3. Montagem de graficos 
- Créditos: @maurovicotcma

#### Gustavo Silva Pereira
- Problema escolhido: Análise Exploratória Global de Dados da COVID-19
- O que precisa ser resolvido: Analisar a evolução temporal de mortes por regiões da OMS, calcular taxas proporcionais de mortalidade e verificar a correlação entre o tamanho da população e o impacto da doença.
- Principais resultados obtidos: Constatação de que as Américas lideraram o acumulado de mortes no período e comprovação estatística (via matriz de correlação) de que a população total de um país não afeta a sua taxa de mortes por milhão.
- Técnicas utilizadas para resolver o problema:
	1. Conversão da coluna de datas de string para o formato datetime
	2. Agrupamento de dados (groupby) para sumarizar as informações por região da OMS
	3. Cruzamento de tabelas (merge) para unificar o dataset da doença com os dados de população mundial
	4. Construção de gráficos de linhas, dispersão e mapa de calor para correlação de Pearson
Créditos: @elgusta

#### Lavínia Name
- Problema escolhido: Titanic - Machine Learning from Disaster
- O que precisa ser resolvido: Predizer se uma determinada pessoa sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 67% de acurácia
- Técnicas utilizadas para resolver o problema: 
    1. Descarte das colunas 'Cabin' e 'Ticket', devido a falta de valores;
    2. Imputação de valores nas colunas que possuíam valores ausentes (Age, Fare...), utilizando diferentes estratégias;
    3. Criação de grupos (AgeGroup e Fare Group) para facilitar o tratamento dos dados;
    4. Uso do OneHotEncoder para fazer o encoding das variáveis 'Sex' e 'Embarked', que são categóricas, para evitar a perda de informação;
    5. Cross Validation para analisar qual modelo obteve maior acurácia (Random Forest ou Gradient Boosting).
- Créditos: @lavinianame04

#### Luiz Octávio Garcia Teixeira
- Problema escolhido: Titanic - Machine Learning from Disaster(capítulo 8)
- O que precisa ser resolvido: Aprimorar o modelo inicialmente produzido no capítulo 6 aplicando as técnicas dos capítulos 7 e 8
- Melhor resultado obtido na submissão: 85.47%
- Técnicas utilizadas para resolver o problema: 
    1. Uso do o SimpleImputer para preencher os dados ausentes, com média, mediana ou moda;
    2. Aplicação do One Hot Encoder e Ordinal Encoder para as colunas de variáveis categóricas;
    3. Utilização do ColumnTransformer e de Pipelines para aninhar as etapas 1 e 2, facilitando o entendimento do código e a reprodução posteriormente;
    4. Criação dos modelos utilizando Random Forest e Gradient Boosting;
    5. Utilização do Cross-Validation para obter uma avaliação menos enviesada dos dois modelos, utilizando accuracy como métrica;
    6. Por fim, comparação dos dois modelos com base nos resultados.
- Créditos: @Luiz-032

