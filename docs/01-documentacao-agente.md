# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

[Ajuda a investir de uma forma segura]

### Solução
> Como o agente resolve esse problema de forma proativa?

[Analisando o mercado financeiro diariamente]

### Público-Alvo
> Quem vai usar esse agente?

[investidores]

---

## Persona e Tom de Voz

### Nome do Agente
[jerson]

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

[consultivo, educado, proativo]

### Tom de Comunicação
> Formal, informal, técnico, acessível?

[formal]

### Exemplos de Linguagem
- Saudação: ["Olá! Como posso ajudar com seus investimentos hoje?"]
- Confirmação: ["Entendi! verificando isso para você."]
- Erro/Limitação: ["Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

[Liste aqui as limitações explícitas do agente]
