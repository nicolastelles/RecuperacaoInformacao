# RecuperacaoInformacao
Repositório criado para contemplar as aulas de recuperação da informação


# Trabalho1 
  ## Questão 1
A função process_data disponibilizada no arquivo trabalho1_base.R faz um processamento básico dos arquivos,
similar ao exemplo visto em sala. O resultado é um data.frame com duas colunas: identificador do documento
e termo. Use o data.frame gerado por essa função para processar a coleção de documentos e as consultas. Em
seguida, crie uma matriz Termo-Documento com a coleção e calcule as estatísticas tf-idf e bm25. As estatísticas
deverão ser convertidas para data.frame. Esses valores serão usados para computar os rankings. Lembre-se de
configurar os parâmetros b e k, usados para o cálculo do bm25.

## Questão 2

Nesta questão, iremos fazer consultas na coleção de documentos e analisar os rankings gerados por essas consultas.
  (a) Implementações: No arquivo inf0611_trabalho1.R, temos um esboço detalhado de uma função que irá gerar
um ranking e apresentará informações sobre esse ranking, para serem analisadas em seguida. A assinatura
da função já é fornecida no arquivo, bem como uma lista de parâmetros e suas funcionalidades. A seguir,
listamos as tarefas que essa função deve cumprir.
    (i) Gerar um ranking usando a função get_ranking_by_stats. Essa função computa o ranking de uma
consulta baseado nos valores de tf-idf ou bm25. Ela recebe como parâmetros o nome da estatística, um
data.frame com as estatísticas e uma lista simples de tokens de uma consulta.
   (ii) Calcular a precisão para o ranking gerado, considerando os k = 20 elementos do topo do ranking.
  (iii) Calcular a revocação para o ranking gerado, considerando os k = 20 elementos do topo do ranking.
  (iv) Apresentar um gráfico com a Precisão e a Revocação no eixo y, e os valores de 1 à k no eixo x, representando o topo do ranking.
(b) Análise: Após a implementação especificada acima, escolha duas consultas do arquivo queries.txt. Para
cada consulta, crie um ranking usando a estatística tf-idf e outro com a estatística bm25. Compare os
rankings de cada consulta e responda:
  (i) Qual dos modelos teve o melhor resultado para as consultas escolhidas? Justifique sua resposta. Nesta
questão você pode usar qualquer uma das medidas de avaliação de ranking vistas na Aula 1.

## Questão 3

Nesta questão, iremos analisar o impacto das técnicas de processamento de texto.
(a) Implementações: Repita os passos da Questão 1 modificando a chamada da função process_data para
incluir a remoção de stopwords. Em seguida, aplique a função da Questão 2 gerando novos rankings com as
duas consultas escolhidas e as estatísticas tf-idf e bm25. Analise os novos rankings gerados e responda:
  (i) Qual o impacto da remoção de stopwords na precisão tanto de tf-idf quanto de bm25? E na Revocação?
