## Configuração do Espaço de Trabalho do Azure Machine Learning

- Faça login no portal do Azure.
- Crie um recurso do Azure Machine Learning com configurações específicas, como nome, região e grupo de recursos.
- Após isso, acesse o [Azure Machine Learning studio](https://ml.azure.com/) e bora por as mãos na massa.

## Treinamento do Modelo com Aprendizado de Máquina Automatizado

- Acesse a página Automated ML no Azure Machine Learning studio.
- Configure um novo job Automated ML com configurações detalhadas, incluindo nome, experimento, tipo de tarefa, dataset, métricas, modelos permitidos, limites e configurações de computação.
- Submeta o trabalho de treinamento e aguarde os resultados.

## Revisão do Melhor Modelo

- Assim que o job de Automated ML for concluído, analise o resumo do melhor modelo na guia de Visão Geral.
- Selecione o nome do algoritmo para visualizar detalhes adicionais.
- Analise métricas de desempenho e gráficos, como o de resíduos e previsto_verdadeiro.

## Deploy e Teste do Modelo

- Na guia do modelo, selecione "Deploy" e escolha as configurações para o serviço da web, incluindo nome, descrição, tipo de computação e autenticação.
- Aguarde até que o _deploy_ esteja com o status de "success".
- Acesse o _endpoint_ implantado e teste usando o código abaixo:

    {
        "Inputs": {
            "data": [
            {
            "day": 1,
            "mnth": 1,
            "year": 2022,
            "season": 2,
            "holiday": 0,
            "weekday": 1,
            "workingday": 1,
            "weathersit": 2,
            "temp": 0.3,
            "atemp": 0.3,
            "hum": 0.3,
            "windspeed": 0.3
            }
            ]
        },
        "GlobalParameters": 1.0
    }

Depois clique em \Testar\

E observe o resultado retornado, deve estar parecido com o abaixo:

{
  "Results": [
    352.4596561115442
  ]
}
_este foi o meu resultado_

## Deletar tudo para evitar cobranças

- Agora é só excluir o endpoint para evitar cobranças na sua fatura.
- E se quiser é só retornar na tela principal da azure e deletar o seu workspace.

