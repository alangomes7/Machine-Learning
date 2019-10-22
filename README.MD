Trabalho 3 de Inteligência Artificial   Tema: Machine Learning - Classificador de Vinhos
Professora: Aline Paes Disciplina/Semestre: Inteligência Artificial/2019.1/UFF
Alunos: Alan Gomes, Eduardo Peniche e Marcelo José

1. Introdução
Neste trabalho usamos uma base de dados textual com o tema: avaliação de vinhos. Tivemos bastante discussões a respeito da escolha dos algoritmos e no final escolhemos o KNN e o BAGGING. O KNN e o BAGGING foram implementados usando os algoritmos do ​scikit-learn.

2. Base de dados
Review de vinhos (​https://www.kaggle.com/zynicide/wine-reviews#winemag-data_first150k.zzzcsv​).

2.1 Atributos utilizados:
2.1.1) designação (string): O vinhedo dentro da adega de onde são as uvas usadas no vinho;
2.1.2) pontuação (float): O número de pontos de WineEnthusiast’s que avaliaram o vinho em uma escala de 1-100;
2.1.3) preço (float): O custo da garrafa de vinho;
2.1.4) província (string): Província ou estado origem do vinho;
2.1.5) região 1 (string): Província ou estado da wine growing área vitícola;
2.1.6) variedade (string): Tipos de uvas usadas para fazer o vinho;
2.1.7) adega (string): a adega que fez o vinho.
2.1.8) Target: país (string): país de origem do vinho.

3. Pré-processamento e divisão dos dados
O tamanho dos dados é de 150 mil utilizando 10% para teste e 90% para treino.
A maioria das colunas e o target envolvem strings(província, região, variedade, vinícola, país), sendo assim foi utilizada a função ​fit_transform ​que quantifica os nomes viabilizando o aprendizado pela máquina.

4. Métodos de tratamento
Foram escolhidos os algoritmos já implementados pelo pacote: KNN e Árvore de decisão. E o algoritmo Bagging que foi implementado.
Escolhemos o KNN pois achamos que era um dos mais simples, tanto na implementação quanto no entendimento.Como o bagging, de acordo com os slides da Intel, pode ser representado como a média de um conjunto de resultados de várias árvores de decisão geradas aleatoriamente a partir de um conjunto de treino e sendo testadas individualmente com o mesmo conjunto de teste, nós escolhemos utilizar o método de Árvores de decisão para poder fazer a comparação com o bagging.

5. Resultados
Nós utilizamos várias funções de avaliação do ​sklearn , dentre elas: ​.score(), .f1_score(), precision_score(), recall_score(), zero_one_loss(). Sendo os principais deles o .score() e o zero_one_loss().

5.1 score()
In multilabel classification, this function computes subset accuracy: the set of labels predicted for a sample must exactly match the corresponding set of labels in y_true. Ou seja irá retornar a porcentagem de acertos individuais do resultado gerado pelo método.

5.2 zero_one_loss()
Foi utilizado mais como um acessório que simplesmente mostrará o número de erros reconhecido pelo algoritmo.

6. Dados de saída
Os dados de saída estão em um arquivo separado com o nome “saida_de_dados”.

7. Conclusão
Fazer a implementação dos algoritmos por mais incrível que pareça não foi a parte mais difícil do trabalho, mas sim a interpretação dos dados. No final concluímos que entre os métodos utilizados o BAGGING se mostrou o mais confiável, visto que nele foram utilizados mais de um método o que consequentemente aumentou a sua precisão nos dados.

8. Referências
8.1 KNN:
https://www.youtube.com/watch?v=gJK4fmCvcWY
https://www.youtube.com/watch?v=ddqQUz9mZaM
8.2 BAGGING:
https://www.youtube.com/watch?v=2Mg8QD0F1dQ
8.3 Slides da intel:
https://software.intel.com/en-us/ai/courses/machine-learning
