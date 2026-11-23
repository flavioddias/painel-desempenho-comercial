# Painel de desempenho comercial

Aplicação em **Streamlit** para explorar receita e volume de vendas por região, período, estado, categoria e vendedor. O objetivo é tornar indicadores comerciais acessíveis por meio de filtros e gráficos interativos.

[Código principal](Dashboard.py)

## Funcionalidades implementadas

- Consulta a uma API de produtos e conversão dos registros em um DataFrame.
- Filtros de região, ano e vendedores.
- Indicadores de receita total e quantidade de vendas.
- Mapa de receita por estado.
- Evolução mensal da receita, comparação entre anos e receita por categoria.
- Ranking de vendedores por receita e por quantidade de vendas.

O código organiza a interface nas abas Receita, Quantidade de vendas e Vendedores. A aba de quantidade apresenta indicadores; os gráficos mais detalhados estão nas outras abas.

## Tecnologias

Python, Streamlit, pandas, Plotly e Requests.

## Como executar

Na pasta do projeto, utilize um ambiente Python próprio e instale as dependências principais:

```bash
pip install streamlit pandas plotly requests
streamlit run Dashboard.py
```

É necessário acesso à internet e disponibilidade da API `https://labdados.com/produtos`, utilizada pelo código. A compatibilidade entre versões das bibliotecas ainda precisa ser registrada e validada. A pasta `venv` do repositório não deve ser usada como ambiente portátil.

## Estrutura

- `Dashboard.py`: consulta, transformação dos dados, filtros e gráficos principais.
- `pages/`: páginas adicionais da aplicação.
- `.streamlit/`: configuração do Streamlit.
- `requeriments.txt`: arquivo presente com essa grafia no repositório.

## Limitações e evolução

Esta documentação foi baseada na leitura do código; **a aplicação não foi executada nesta revisão**. Antes de uma demonstração pública, é necessário validar a execução e a construção do gráfico mensal, além de tratar falhas da API, respostas vazias e filtros sem registros.

Próximos passos: fixar dependências, adicionar timeout e tratamento de erros à consulta, usar cache quando apropriado, retirar o ambiente virtual do versionamento e publicar uma demonstração validada.

**Competências demonstradas:** dashboards, consumo de API, agregação de indicadores e visualização interativa.
