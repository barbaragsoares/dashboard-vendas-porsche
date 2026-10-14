# Dashboard de Vendas Porsche

Neste projeto do curso Santander – Excel com IA e Claude, da DIO, usei a base Porsche da aula para montar um dashboard interativo em HTML. Escolhi analisar receita por modelo, quantidade de vendas por estado e formas de pagamento.

Quis criar uma visão comercial simples, com filtros que permitissem explorar os dados sem abrir a planilha.

## Perguntas de negócio

| Pergunta | Por que escolhi | Como o painel responde |
| --- | --- | --- |
| Quais modelos geram mais receita? | Comparar a contribuição de cada modelo para o total vendido. | Barras com receita por modelo, ordenadas do maior para o menor. |
| Quais estados concentram mais vendas? | Identificar a distribuição das vendas entre os mercados da base. | Barras com quantidade de vendas por estado americano. |
| Como as vendas se distribuem entre os métodos de pagamento? | Entender a frequência de cada forma de pagamento. | Quantidade e participação percentual por método. |

Os indicadores do topo mostram quantidade de vendas, receita total e ticket médio. Os filtros de modelo, estado, ano do veículo e pagamento atualizam todas as análises e a tabela de consulta. O botão **Limpar filtros** retorna à base completa.

## Agente e habilidade utilizados

Utilizei o **agente Codex**, nesta conversa, com a habilidade personalizada **Criador de Dashboards de Vendas** (`criar-dashboard-vendas`). A habilidade reúne as instruções para conferir a base, definir análises, criar o HTML e verificar os resultados.

As regras foram discutidas por etapas antes da atualização final: função da habilidade, conferência dos dados, entregas do dashboard, visual e testes. Pedi também que a documentação identificasse o agente utilizado.

A habilidade foi salva com auxílio do **skill-creator**. Ela não apareceu na busca por `@` durante o processo. Por isso, suas instruções salvas foram lidas e aplicadas pelo Codex nesta conversa. Não utilizei Canvas nem criei um GPT separado.

## Preparação da base

A planilha original tem **100 vendas**, com identificadores distintos, e traz campos crus e sanitizados. Para o painel:

- Usei as colunas sanitizadas de modelo, ano do veículo, preço, cidade, estado, pagamento e data da venda, além do identificador.
- Preço foi convertido para número decimal e ano do veículo para número inteiro.
- A base tratada foi exportada como valores, sem fórmulas, em `base_tratada.csv`.
- As **24 datas marcadas como INVALID** passaram a ficar vazias. As vendas foram mantidas porque as três análises escolhidas não dependem da data da venda.
- Não confundi ano do veículo com ano da venda.
- Mantive os valores em **dólares americanos (USD)**, sem conversão para reais.
- Não incluí nomes de clientes e vendedores nos arquivos do projeto.
- Mantive os métodos Wire Transfer, Bank Transfer e ACH separados, conforme a sanitização da aula. Traduzi apenas os rótulos exibidos no painel.

Na base completa, a receita é **US$ 12.827.800,50** e o ticket médio é **US$ 128.278,01**. Todos os 100 preços são válidos. Receita representa a soma dos preços registrados, sem cálculo de lucro ou confirmação de recebimento.

## Prompt e ajustes

O histórico resumido está em [PROMPTS.md](PROMPTS.md). As perguntas e os filtros foram definidos na conversa antes da criação do arquivo.

O visual usa preto, branco, cinza e vermelho, com a fonte Arial e alternativas do sistema. Não há dependências externas, marca d’água ou identificação de ferramenta na tela do dashboard.

## Arquivos

- [index.html](index.html): dashboard com código e dados incorporados em um único arquivo.
- [base_tratada.csv](base_tratada.csv): dados utilizados, com separador ponto e vírgula e codificação UTF-8.
- [PROMPTS.md](PROMPTS.md): pedido consolidado a partir da conversa e decisões do projeto.
- [README.md](README.md): documentação do projeto.

## Como abrir

Acesse o [dashboard publicado no GitHub Pages](https://barbaragsoares.github.io/dashboard-vendas-porsche/).

Baixe o `index.html` e abra no navegador. Ele funciona sem instalação e sem conexão com a internet. Para testar, selecione um estado e confira os indicadores e gráficos. Depois combine com outro filtro ou clique em **Limpar filtros**.

Todos os modelos e estados estão disponíveis nos gráficos. Quando a lista for maior que a área do gráfico, use a rolagem interna para consultar as demais categorias.

## Verificação realizada

Foram conferidos os totais da fonte e os agrupamentos por modelo, estado e pagamento. A lógica foi testada em um DOM simulado, com 189 seleções individuais e combinadas, além do cenário sem resultados e do botão de limpar filtros.

Depois da publicação, abri o dashboard pelo endereço do GitHub Pages e confirmei seu funcionamento no navegador.

## Publicação

O dashboard está publicado no **GitHub Pages**.

- **Dashboard:** https://barbaragsoares.github.io/dashboard-vendas-porsche/
- **Repositório:** https://github.com/barbaragsoares/dashboard-vendas-porsche

Para a entrega na DIO, o endereço utilizado é o do repositório. O link do dashboard permite acessar diretamente o painel interativo.
