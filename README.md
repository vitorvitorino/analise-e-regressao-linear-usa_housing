# Análise e Modelo de Regressão Linear do Dataset USA Housing


Este notebook realiza uma análise exploratória de dados e a breve construção de um modelo de Regressão Linear para prever o preço de imóveis com base em características socioeconômicas e da região presentes no dataset.

No geral, o dataset contém informações sobre a renda média, idade média, número médio de salas e dormitórios dos imóveis, população, preço do imóvel e endereço.

Primeiramente realizei a remoção da coluna 'Price' que não apresenta valores númericos e em seguida, renomeei as demais colunas para facilitar a manipulação dos dados.


![image](https://github.com/user-attachments/assets/d3ee9205-4c23-45cc-ba70-2a85f8a4748a)
![image](https://github.com/user-attachments/assets/2e74478d-fbbe-4b8b-a2ff-6ec03429486c)


Pelo heatmap e pelo pairplot gerados com Seaborn, é possível observar que as variáveis com maior correlação positiva com o preço (price) são:
avg_area_number_of_rooms e avg_area_income, quão maior a quantidade de cômodos e a renda média da área, mais positiva é a inflência dessas variáveis no preço do imóvel.
enquanto as variáveis avg_number_of_bedrooms e avg_area_house_age indicam que a quantidade de quartos e a idade do imóvel tem uma relação positiva, porém menos expressiva na variável Price.


![newplot](https://github.com/user-attachments/assets/9708c0ea-04e5-4355-8d18-4b3ca5a7d3e3)

O boxplot da renda média por área indica que a maior parte dos valores está concentrada em uma faixa específica, com poucos outliers. Isso pode ser interpretado como um indicativo de que regiões com rendas médias mais altas estão associadas a preços mais altos


![image](https://github.com/user-attachments/assets/72510205-b7ce-4733-8ceb-7e3c08b1a61e)



O modelo de regressão linear foi criado com a biblioteca sklearn utilizando a função train_test_split. O dataset foi separado em duas variáveis X e Y, X incluindo as colunas do dataset (menos a coluna de endereço) e Y sendo a coluna Price. Os dados foram divididos em uma proporção de 70/30 para treino e teste e o desempenho foi avaliado com R² apresentando uma score de 0.914681849875402. 
