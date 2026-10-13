Algumas anotações da monitoria do dia 4 de setembro de 2025, (04/09/2025):

O arquivo apresentado na monitoria foi o ExemploSympy.ipynb. Os demais arquivos tem outras demonstrações ainda não oficializadas. 



Outros links interessantes:

Animação Simplex (INGLÊS)
https://www.youtube.com/watch?v=E72DWgKP_1Y

Lista Pedro Munari (PORTUGUÊS)
https://www.youtube.com/watch?v=TX2Ffzx_rDE&list=PLjK8TkmwOe0qQiJwSB_uxGsUNf54HPeS8



Questões que ficaram da última monitoria:

Questão 1 (Xiana): "Existem outros tipos de funções de perda disponíveis para aprendizado supervisionado além da entropia cruzada binária?"

Tipos de loss na execução de model.compile:
model.compile( 
	loss = 'binary_crossentropy', 
	optimizer = 'nadam', 
	metrics = [ 'accuracy' ] 
)

Algumas outras funções disponíveis em:
https://keras.io/api/losses/



Questão 2 (Xiana): "Qual a elevância da variável max_length no notebook de aprendizado supervisionado (Aula 7) e o que deve ser levado em conta na hora de escolhê-lo?"

O max_length é o número máximo de palavras/tokens que cada "frase" de entrada do modelo terá. Se o tamanho da frase for > max_length, ela será truncada. Se for menor, ela será preenchida com "0"s.

Quanto maior o max_length, menos perda de contexto ocorre (por conta dos cortes que ocorrem no truncamento), mas mais pesado fica o treino. Para encontrar o max_length "ótimo" é necessário fazer uma análise de trade-off se for possível, medindo a acurácia x desempenho computacional...
