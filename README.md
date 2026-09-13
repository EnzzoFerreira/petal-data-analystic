# petal-data-analystic

Projeto de Machine Learning

Entendendo o processamento de dados e o processo de construção de uma arvore de decisao

O projeto consiste de duas partes a parte de interpretar os dados, e outa de usar os dados analizados

Temos um projeto base criado conjuntamente com o professor na sala de aula respeitando o modelo KNC.

Utilizaremos desse projeto inicial como base para construir a arvore de decisoes

# Arvore de Decisão

A estrutura da árvore de decisão pode ser analisada para obter uma compreensão mais profunda da relação entre as características e o alvo da previsão.

Para começar a construção da Árvore de Decisão, iremos classifica-la com a profundidade máxima dela ( max-depth ) e o ccontrole de aleatoriedade que ela vai ter ( random_state ) para que nenhum test ou treinamento sai fora dos padrões.

# mas-depth
A profundidade da árvore de decisão se defini pelo parâmetro max-depth,
se a profundidade for alta, o detalhamento e o refinamento na árvore yambém será alta, mas 
tem um porém pois ter um alto refinamento dos dados acaba que ela aprende com os ruídos, o que acaba 
gerando sobreajuste. 

# random_state
A aleatoriedade do modelo ou da divisão dos dados será feito por esse método, evitar a geração de resultados diferentes, com ele
você consegue repetir o testes e os treinamentos e comparar os resultados com segurança.

##  se colocarmos 3 no max-depth ocorre um OVERFITTING a arvore decora o padrão e ficou na acurácia: 1.0, por isso na profundidade colocarmos 2 pra forçar a arvore a aprender mais regras.

Após isso iremos fazer o treinamento da árvore com (x_train) contendo caracteristicas das pétalas e (y_train) contendo a resposta de cada pétala (setosa, versicolor, virginica)

Na Ácuracia da Arvore iremos o quanto que a árvore aprendeu com os dados, observação importante quando p resultado é 1.0 exato isso significa algo ruim pois pode ser que ou a árvore de Decisão teve um vazamento de dados ( quando o modelo de teste teve informação sobre os dados do treinamento ) ou Overfitting aonde o modelon da Arvore de Decisão decorou os padrões especificos dos dados de treino inclusive os ruídos.

Agora para determinarmos a area, tamnho e como será o gráfico usamos o método ( figure() ) para criar a area do gráfico, ( figsize= 14, 8 ) definir o tamanho da area, 14 sendo a largura e o 8 a altura.

E por final desenharemos a Arvore, pegaremos a arvore e definiremos nomes das características usadas para tomar as decisões ( feature_names=x.columns ). Os nomes das classes que a árvore está tentando prever ( class_names=dataset.target_names ) class = setosa, class = versicolor, class = virginica. preenche os nós da árvore com cores para facilitar a visualização ( filled=True ) praticamente para dar cor aos nodos ou nós.

Laranja -> setosa
Verde -> versicolor
Roxo -> virginica