# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:
O agente utilizou apenas dados mockados criados para simular diferentes cenários de gastos e rendimentos dos usuários. não foram utilizados arquivos externos da pasta 'data'.

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Os dados utilizados são fictícios (mockados) e representam diferentes cenários de gastos e rendimentos de usuários. Eles foram criados para testar as funcionalidades do agente e garantir que ele consiga fornecer recomendações financeiras realistas.

---

## Estratégia de Integração

### Como os dados são carregados?
Oagente acessa a base de conhecimento por meio de dados mockados armazenados em arquivos locais ou diretamente em variáveis no código. Ele lê essas informações para analisar padrões de gastos e gerar recomendações financeiras.

[ex: Os JSON/CSV são carregados no início da sessão e incluídos no contexto do prompt]

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados mockados são incorporados no system prompt, permitindo que o agente utilize essas informações como referência fixa para gerar respostas e recomendações financeiras.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.
 Dados do clinte: 
 Usuário: Felipe Melo
 Renda mensal: R$ 4000
 Despesas:
 - Alimentação: R$ 1200
 - Transporte: R$ 500
 - Lazer: R$ 300
 - Moradia: R$ 1500
 Objetivo: Economizar R$ 500 por mês
 
```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
