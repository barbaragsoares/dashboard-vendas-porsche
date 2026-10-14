# Pedido e decisões do projeto

## Como o pedido foi construído

O pedido foi desenvolvido em conversa. Primeiro apresentei o enunciado da DIO. Depois pedi o caminho com agente e habilidade, pois esse conteúdo foi abordado nas aulas. A criação da habilidade foi explicada em etapas e suas regras foram aprovadas durante a conversa.

O texto abaixo é uma consolidação dessas decisões, não a transcrição de uma mensagem única nem o registro de uma execução em outro agente.

## Pedido consolidado

Usar a habilidade Criador de Dashboards de Vendas para transformar a planilha Porsche da aula em um dashboard interativo em um único arquivo index.html.

Usar os dados sanitizados e responder a três perguntas:

1. Quais modelos geram mais receita?
2. Quais estados concentram mais vendas?
3. Como as vendas se distribuem entre os métodos de pagamento?

Mostrar no topo quantidade de vendas, receita total em USD e ticket médio. Incluir filtros combinados de modelo, estado, ano do veículo e método de pagamento, além de um botão para limpar os filtros. Atualizar todos os gráficos, indicadores e a tabela de consulta com o mesmo recorte.

Usar preto, branco, cinza e vermelho, textos em português e layout adaptável a computador e celular. Não inserir marca d’água ou nome de ferramenta na interface.

Preservar a moeda original. Não inventar dados nem confundir ano do veículo com ano da venda. Manter datas inválidas como ausentes sem excluir essas vendas das análises que não dependam da data. Não publicar nomes de clientes ou vendedores.

Conferir os totais, testar os filtros e documentar os limites da verificação. Preparar README identificando o agente Codex, a habilidade personalizada utilizada, o tratamento dos dados e as decisões do projeto. Não afirmar publicação ou teste visual antes de sua realização.

## Decisões até esta versão

- Foi escolhido o caminho com Codex e habilidade personalizada, sem Canvas.
- As regras foram generalizadas para permitir reutilização com outras bases de vendas.
- O filtro de ano foi identificado como ano do veículo.
- As 24 datas inválidas não interferem nas três perguntas escolhidas.
- As análises usam USD, sem conversão para reais.
- O painel inclui os 40 modelos e todos os estados, com rolagem em listas longas.
- Os métodos sanitizados de pagamento foram preservados como categorias distintas.
- Uma tabela de consulta permite conferir os registros após aplicar filtros.

## Próxima etapa

Abrir o HTML no navegador, conferir a apresentação e solicitar ajustes se necessário. Após essa revisão, publicar no GitHub Pages, capturar as evidências e atualizar o README com o link real.
