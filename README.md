# Eleicoes_Municipios_Paraenses

## Análise exploratória dos dados dos candidatos a vereador do estado do Pará e modelos de Machine Learning pra prever se o candidato será eleito ou não

### Linguagem Python

## Intenção:
  * Explorar os dados afim de encontrar padrões que possa identificar quando um candidato é eleito;
  * Prever se o candidato a eleição será eleito ou não de acordo com algumas características, como idade, valor declarado na campanha, gênero, local de nascimento, entre outras.

## Aplicabilidades:
 * Identificar qual o perfil de um candidato eleito
 * Identificar quais características contribuem mais para a eleição de um candidato;
 * Possibilita um candidato se preparar melhor para a eleição;
 * Expõe quais grupos tem mais chance de serem eleitos

## Obtenção dos dados:
#### Conjunto de Dados
  Conjunto de Dados com informações dos candidatos a vereador dos municípios do Pará nas eleições de 2020

#### Fonte: https://www.tse.jus.br/

#### Os dados foram extraídos de 3 arquivos csv diferentes. Foi feito as transformações necessárias na ferramenta Pentaho Data Integration. Lá foi feito merges, mudança de tipo, limpesa de dados etc. Foram selecionados somente os candidatos a vereador.

## Análise Exploratória:

#### Foram feitas algumas análises e identificamos alguns padrões:
* Candidatos casados tem maior probabilidade de serem eleitos;
* 93% dos candidatos eleitos declararam bens;
* O perfil do candidato eleito é: Homem, pardo, casado entre 37 e 51 anos que possui ensino médio completo

## Modelos de Machine Learning:
* Foram usados 4 algoritmos diferentes (RandomForest, ExtraTrees, DecisionTrees e KNN) e diferentes hiperparâmetros;
* Inicialmente usamos todas as variáveis e o modelo que apresentou as melhores métricas de acurácia, precisão, recall e F1 foi o modelo de Floresta Aleatória com Critério de Entropia;
* Posteriormente foram testados os mesmos modelos com diferentes variáveis, mas nenhum obteve resultados melhores;
* O modelo de Floresta Aleatória com Critério de Entropia foi selecionado e com 95% de confiança tem precisão entre  83.67 % e  85.01 %
