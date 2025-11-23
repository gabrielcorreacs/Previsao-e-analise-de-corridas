#Funcionalidades

Previsão de preço de corrida com base em distância, hora do dia e dia da semana.

Classificação dinâmica das corridas usando um limiar adaptativo.

Cálculo de distância entre bairros usando a fórmula Haversine ou Google Maps API.

Geração de explicações concisas usando Gemma 3-4B-IT.

Suporte para simulações offline sem dependência da API do Google Maps.

Visualização de dados, análise de erros e importância das features.
------------------------------------------------------------------------------------------------------------------------------
#Tecnologias Utilizadas

Python 3.10+

Pandas, NumPy, Scikit-Learn, XGBoost

Matplotlib, Seaborn (visualização)

SpaCy (processamento de linguagem natural)

Transformers / Gemma 3-4B-IT (LLM para explicações)

Joblib (salvamento de modelos)

Google Maps API (opcional, para cálculo de rotas)
------------------------------------------------------------------------------------------------------------------------------
#Estrutura do Projeto

/data: datasets originais e processados

/artifacts: modelos treinados e scaler

Células do Notebook:

Configurações iniciais e importações

Criação de coordenadas dos bairros

Função Haversine e cálculo de distâncias

Pré-processamento do dataset

Treinamento do modelo XGBoost com features aprimoradas

Avaliação e limiar dinâmico

Integração com Google Maps API

Função de predição de corridas

Processamento de linguagem natural (NLP)

LLM Gemma 3-4B-IT

Funções de interação para motorista

Simulação de corridas offline
------------------------------------------------------------------------------------------------------------------------------
#Instalação

Clone o repositório:

git clone <URL_DO_REPO>
cd <NOME_DO_REPO>


Instale as dependências:

pip install -r requirements.txt


(Opcional) Configure a Google Maps API:

Adicione sua chave em uma variável de ambiente GMAPS_KEY.

baixe o modelos do Hugging Face (Gemma 3-4B-IT) 

Como Usar

0. Adicione a base de dados de fortaleza em /content /data

1. Interação Manual

Execute o notebook ou script principal.

Digite o pedido da corrida, ex:

de Aldeota para Meireles

Informe a tarifa recebida pelo app.

O sistema retorna:

Distância e duração da corrida

Preço previsto pelo modelo

Lucro estimado

Diferença percentual vs preço esperado

Decisão do modelo: ACEITAR / DEPENDE / RECUSAR

Explicação gerada pelo LLM
------------------------------------------------------------------------------------------------------------------------------
2. Simulação Offline

Gera corridas aleatórias entre bairros de Fortaleza.

Permite testar o modelo sem dependência do Google Maps.

Explicações geradas pelo LLM se tiver api ou por texto padrão.

Contribuições

Sugestões de melhoria para features, explicações LLM ou simulação de corridas são bem-vindas.

O projeto é open-source, focado em aprendizado e pesquisa.
