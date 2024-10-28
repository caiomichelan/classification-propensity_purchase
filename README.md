# Classificação - Propensão de Compra

## Data Science Project - Propensão de Compra

<div align='center'>

![Insurance](https://github.com/user-attachments/assets/8e4c3c32-6476-4838-8ddc-ea17c85a8237)

</div>

# 1. Problema do Negócio
<p align='justify'>Uma grande empresa do segmento de Seguros, com atuação global, identificou uma oportunidade de crescimento significativo através da implementação de estratégias de venda cruzada. A empresa possui uma base de clientes que já contratam seguros de vida e busca expandir sua oferta para esses mesmos clientes, propondo seguros automotivos.</p>
<p align='justify'>Visando aumentar a eficácia dessa estratégia, foi proposta a criação de um modelo preditivo capaz de identificar os clientes com maior propensão a contratar um seguro automotivo. Esse modelo, ao analisar as características dos clientes, é capaz de classificar a base de clientes em grupos com diferentes níveis de propensão à aquisição do serviço.</p>
<p align='justify'>Como benefícios propostos por esta solução, é esperado observar:</p>
<p align='justify'>- Otimização da Força de Vendas: Os vendedores poderão focar seus esforços nos clientes com maior probabilidade de conversão, aumentando a eficiência das ações de vendas.</p>
<p align='justify'>- Personalização da Oferta: As ofertas poderão ser personalizadas de acordo com o perfil de cada cliente, aumentando a relevância e a chance de conversão.</p>
<p align='justify'>- Melhora na Experiência do Cliente: Ao oferecer produtos relevantes, a empresa demonstra um maior cuidado com as necessidades do cliente, fortalecendo o relacionamento.</p>
<p align='justify'>- Aumento da Receita: Aumento das vendas de seguros automotivos e consequente crescimento da receita.</p>

# 2. Premissas do Negócio
<p align='justify'>Foram consideradas duas bases de dados:</p>
<p align='justify'>- Clientes já avaliados com a oferta de venda cruzada: Base com dados de aproximadamente 380 mil clientes que já responderam a pesquisa sobre interesse na aquisição do seguro automotivo.</p>
<p align='justify'>- Clientes que ainda não foram avaliados com a oferta: Base com dados de aproximadamente 125 mil clientes que ainda não responderam a pesquisa sobre interesse na aquisição do referido seguro.</p>
<p align='justify'>A primeira base de dados foi utilizada no treinamento aos algoritmos para posterior avaliação da segunda base e classificação dos clientes mais propensos à aquisição do seguro automotivo.</p>
<p align='justify'>As duas bases de dados possuem os mesmos atributos e variáveis, sendo a única diferença a segunda base não possuir a variável resposta.</p>

# 3. Estratégia da Solução
<p align='justify'>Foi utilizada a metodologia CRISP-DM no desenvolvimento do projeto, através das seguintes etapas:</p>
<p align='justify'>Business Understanding: Definição dos objetivos do projeto, entendimento das necessidades do negócio e identificação os problemas a serem solucionados e as oportunidades a serem exploradas. Nesta etapa foi avaliado que o objetivo principal do projeto se tratava de uma classificação na base de clientes da empresa, de modo a identificar os clientes mais propícios à aquisição de um produto através da venda cruzada.</p>
<p align='justify'>Data Understanding: Coleta, descrição e exploração dos dados relevantes para o projeto, bem como avaliação da qualidade, consistência e confiabilidade destes dados. Realizada análises univariada, bivariada com levantamento e validação de hipóteses e correlação entre variáveis.</p>
<p align='justify'>Data Preparation: Limpeza, transformação e formatação dos dados para a análise, bem como tratativa de dados ausentes, inconsistentes ou outliers e seleção das variáveis relevantes para o modelo de Machine Learning. Nesta etapa foi verificado que os modelos performaram melhor com a utilização de todas as variáveis constantes na base de dados.</p>
<p align='justify'>Modelling: Escolha e aplicação de técnicas de Machine Learning adequadas ao problema, juntamente com treinamento e avaliação de diferentes modelos para seleção do melhor desempenho. Realizada a definição e treinamento dos modelos de Classificação com base nos dados propostos.</p>
<p align='justify'>Evaluation: Validação dos modelos em um conjunto de dados de teste independente. Nesta etapa foram avaliados todos os modelos definidos e treinados na etapa anterior afim de adquirir conhecimento, avaliar suas performances e concluir o estudo sobre a aplicação e implementação dos mesmos nos conjuntos de dados pré definidos. Avaliado que o modelo XGBoost apresentou a melhor performance dentre os demais, sendo este considerado para classificação nos dados reais.</p>
<p align='justify'>Deployment: Implementação do modelo de Machine Learning na aplicação real, bem como monitoramento de seu desempenho em produção e realização de ajustes quando necessário. Nesta etapa, consideramos a implementação como a classificação de propensão de aquisição do seguro automotivo considerando a base de dados real, trazendo o resultado sobre a propensão de aquisição do seguro (0 - Não Propenso, 1 - Propenso) bem como uma estimativa percentual sobre a propensão.</p>
<p align='justify'>Algorimos utilizados neste projeto:</p>
<p align='justify'>- Classificação: Logistic Regression / XGBoost Classifier / K-Nearest Neighbors (KNN) Classifier / Extra Trees Classifier / Random Forest Classifier / Ensemble Method.</p>

# 4. Insights de Dados
<p align='justify'>Alguns insights obtidos através dos testes de validação dos dados de treino:</p>
<p align='justify'>- 12% dos clientes são propensos à aquisição do serviço ofertado.</p>
<p align='justify'>- Dados de gênero balanceados, sendo 54% mulheres e 46% homens.</p>
<p align='justify'>- Concentração de 32% dos dados na faixa etária de 21 a 26 anos.</p>
<p align='justify'>- Praticamente todos os clientes (99,8%) possuem habilitação.</p>
<p align='justify'>Correlação dos Dados:</p>
<p align='justify'>- Alta Correlação Positiva (Variável Resposta): Veículos já Danificados (vehicle_damage), Idade (age) e Idade do Veículo (vehicle_age).</p>
<p align='justify'>- Alta Correlação Positiva entre demais variáveis: Veículos já Danificados (vehicle_damage) x Cliente Previamente Assegurado (previusly_insured)</p>
<p align='justify'>- Alta Correlação Negativa (Variável Resposta): Cliente Previamente Assegurado (previusly_insured)</p>
<p align='justify'>- Alta Correlação Negativa entre demais variáveis: Canais de Vendas (policy_sales_channel) x Idade (age)</p>
<p align='justify'>Hipóteses validadas:</p>
<p align='justify'>- Clientes com carros já danificados tendem a contratar seguro: Verdadeira</p>
<p align='justify'>- Clientes mais velhos tendem a contratar seguro: Falsa</p>
<p align='justify'>- Clientes homens tem maior tendência a contratar seguro: Verdadeira</p>
<p align='justify'>- Clientes com carros mais novos tendem a contratar seguro: Verdadeira</p>
<p align='justify'>- Clientes já assegurados tendem a contratar seguro: Falsa</p>

# 5. Produto Final
<p align='justify'>Com base nos dados propostos, foi desenvolvido um modelo de Machine Learning capaz de identificar a propensão de adesão do novo serviço ofertado aos clientes, podendo servir como base à equipe Comercial para maior assertividade na oferta deste serviço.</p>
<p align='justify'>Os dados consistem na propensão de adesão de forma binária, bem como uma estimativa percentual desta adesão, podendo a equipe de Negócio definir a partir de qual percentual será considerada para oferta do serviço.</p>
<p align='justify'>Dentre os estudos realizados com base nos resultados, é possível segmentar a base de clientes de maneira a trabalhar apenas nos clientes mais propensos à adesão do serviço, seguindo o critério que a equipe de Negócio definir.</p>

# 6. Conclusão
<p align='justify'>O objetivo do projeto foi desenvolver um modelo de Machine Learning de Classificação capaz de identificar os clientes com maior propensão a contratar um determinado serviço ofertado.</p>
<p align='justify'>Com a implementação do modelo proposto, foi validada a classificação de clientes com maior propensão à adesão, otimizando o contato e assertividade da equipe Comercial, possibilidade de personalização de ofertas com base no perfil de cada cliente, melhora em sua experiência junto à empresa e consequente aumento de receita.</p>

# 7. Próximos Passos
<p align='justify'>Como próximos passos serão realizadas análises mais aprofundadas sobre os modelos utilizados, com aplicação de técnicas de Fine Tuning.</p>
<p align='justify'>Também serão considerados treinamento de novos modelos de Machine Learning e validação de seus resultados, buscando obter uma performance ainda melhor.</p>
<p align='justify'>Por fim será definido um cronograma para implementação do projeto em nuvem, de maneira a tornar as consultas disponíveis a qualquer momento em plataforma externa.</p>

