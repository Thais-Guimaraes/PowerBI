# PowerBI

Descrevi abaixo, para explicar sobre o que se trata o mini projeto e também
para ajudar na retenção do conteúdo durante os estudos.

A ideia deste dashboard é demonstrar de maneira objetiva, os indicadores e métricas
para a área de Recursos Humanos, respondendo as seguintes perguntas de negócio: /n

1-Qual o total de funcionários atualmente na empresa? /n
2-Qual otempo médio de experiência dos funcionários (em anos)? /n
3-Qual o total e percentual de funcionários do gênero masculino e feminino? /n
4-Qual a média salarial mensal? /n
5-Qual o total de funcionários por função? /n
6-Qual o percentual defuncionários disponíveis para fazer hora extra? /n
7-Qual onível de envolvimento dos funcionários no trabalhoconsiderando /n
4 categorias: Ruim, Baixo, Médio e Alto? /n
8-Este item não deveestar no Dashboard,mas precisa ser calculado: /n
Qual o total e o percentual de funcionários que devem receber promoção? /n
Desde a última Promoção”com a seguinte regra: /n
Se o funcionário tiver 5 anos ou mais desde  a última  promoção, /n
deve ter  a  promoção  considerada.Caso  contrário,apromoção não deve ser /n
considerada agora. /n

Para a construção, primeiramente realizei a importação dos dados que estão em
formato CSV, depois criei uma tabela de "Medidas", em que criei 11 métricas
para auxiliar na construção do dashboard.
Ao criar estas métricas, melhoramos a performance, pois se criarmos conforme
o padrão do Power BI, o processo será feito em tempo de execução, deixando
mais "pesado".

Em se tratando de "Transformação dos dados", apenas alterei a coluna "Disponível Hora 
Extra" para "Sim" e "Não, antes estava "S" e "N". Assim, facilita o entendimento
do gráfico, para que fique bem clara a informação.

Criei uma medida na tabela original "Promover", com "IF" para responder a questão
8, ou seja, se o funcionário tiver 5 anos ou mais desde a última promoção, deverá
ser considerada a promoção, caso contrário, não.

Criei uma nova coluna com o recurso "Conditional Column", para fazer o "de-para"
da coluna "Indice Envolvimento Trabalho", porque esta coluna é numérica, e
para facilitar a leitura no gráfico, criei a coluna categórica.

Para mostrar o percentual, alterei a configuração dos campo, na seção
"propriedades" do "modelo"

Para fazer a formatação utilizei a opção "inserir", "formas"