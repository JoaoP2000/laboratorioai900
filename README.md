# João Pedro Figueiredo
## Tutorial Criando uma modelo de previsão no Azure ML

1. Entrar no `https://portal.azure.com/`
2. Criar Resource
    > Pesquisar Azure Machine Learning <br>
    > Caso não tenha um Resource Group, criar um.
3. Após a criação criar em `lançar studio`
4. Na página `ML automatizado`, clique em novo trabalho 
    > Neste caso, vamos pegar uma documentação pronta da Microsoft para servir de base para o nosso passo a passo `https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html`.

**Nome do trabalho:** `mslearn-bike-automl`<br>
**Novo nome do experimento:** `mslearn-bike-rental`<br>
**Descrição:** Aprendizado de máquina automatizado para previsão de aluguel de bicicletas<br>
**Tags:** nenhuma<br>

***Tipo de tarefa & data:***<br>

**Selecionar tipo de tarefa:** Regressão <br>
**Selecionar conjunto de dados:** *crie um novo conjunto de dados com as seguintes configurações:*<br>

***Tipo de dados:***<br>

**Nome:** bike-rentals<br>
**Descrição:** Dados históricos de aluguer de bicicletas<br>
**Tipo:** Tabular<br>
**Fonte de dados:** Selecionar de arquivos da Web <br>
**URL da Web:** `https://aka.ms/bike-rentals`<br>
**Ignorar validação de dados:** não selecione<br>

***Configurações:***<br>

**Formato de arquivo:** Delimitado<br>
**Delimitador:** Vírgula<br>
**Codificação:** UTF-8<br>
**Cabeçalhos de coluna:** Somente o primeiro arquivo tem cabeçalhos<br>
**Pular linhas:** Nenhum<br>
**O conjunto de dados contém dados de várias linhas:** não selecione<br>

***Esquema:***<br>

*Incluir todas as colunas diferentes de Caminho*<br>
*Revisar os tipos detectados automaticamente*<br>

5. Depois que o conjunto de dados for criado, selecione o conjunto de dados de `bike-rentals` para continuar a enviar o trabalho de ML automatizado.<br>
6. Quando o ML for criado, na guia `Visão Geral` selecionar `Nome do Algoritmo`<br>
7. Na guia `Modelo` selecione `Implantar` e ir na opção `Serviço Web`<br>
8. Novamente seguindo o modelo do documento da Microsoft:<br>

**Nome:** `predict-rentals`<br>
**Descrição:** Prever aluguéis de ciclos<br>
**Tipo de computação:** Instância de Contêiner do Azure<br>
**Habilitar autenticação:** Selecionado<br>

9. Selcionar `Implantar` e aguardar até que a implantação esteja com êxito.<br>
10. Após implantado, você poderá executar os teste na guia `Pontos de Extremidade` -> `predict-rentals`-> guia `Testes`<br>
11. Selecione o modelo .JSON que quiser. <br>
12. Clique em testar<br>

## Obrigado! 