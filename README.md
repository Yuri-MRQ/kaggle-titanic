# kaggle-titanic

Minha primeira participação em uma competição no Kaggle, nada mais justo de ser na classica competição do Titanic.

# Notebooks

Fiz dois notebooks da seguinte forma:

Pelo notebook titanic_explore_data analise as informações dos arquivos test.csv e train.csv, optei por tratar os NaN values com a média do db.

Para o classifier usei Random Florest Classifier utilizando as seguintes colunas: Pclass,	Fare,	C,	Q,	S,	female e	male. As colunas C, Q e S correspondem a one hot enconding da coluna Embarke e as colunas female e male correspondem ao mesmo da coluna sex. 

Podemos considerar essa abordagem a mais tradicional, olhando alguns notebooks no Kaggle observamos que diversos competidores utilizaram essa forma para tratar os dados.

Obtive o public score de 0.76555, nada expressivo possuindo margem para melhorar o modelo e assim a pontuaçãp.

Já o notebook exploring_name_titanic fui por uma abordagem totalmente diferente, utilizei apenas os nomes para tentar prever se a pessoa morre ou vive ao naufrágio, algo interessante sobre os nomes é que conseguimos tirar deles o Sexo, classe Social, títulos e ate mesmo aproximar a data de nascimento (É natural ter anos em que mais pessoas são registradas com um nome, Enzo por exemplo) além é claro de dizer se há algum grau de parentesco das pessoas a bordo.

Aqui estou assumindo que nosso modelo conseguirar retirar todas essas informações, abstrair de uma forma que consiga dizer a chance de sobrevivência.

O public score desse notebook foi de 0.77511, superando o Random Florest Classifier, pouco, mais superando.

É claro que realizei essa abordagem, principalmente, para colocar em prática tudo que apendi, mas uma tentativa de ver o comportamento do modelo em um uso que não seria o mais intuitivo.

Por conta disso temos a principal barreira, quantidade de dados, o nosso banco de dados para treinamento possui apenas 891 entradas, para um modelo de DL isso representa pouquíssimo dado sendo muito fácil overfit, tentando evitar isso tive que usar dropout com uma rate bem alta (> 0,65).

Tentarei, no futuro, melhorar a arquitetura do modelo e buscar melhores resultado, mas dado a escasses das informações acho extremamente dfícil melhorar muito.
