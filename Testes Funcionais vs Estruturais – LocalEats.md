# PBL 4 – Testes Funcionais vs Estruturais

## 1. Escolha da funcionalidade

### Funcionalidade escolhida: Busca de restaurantes

A funcionalidade de busca de restaurantes permite que o usuário encontre restaurantes com base em filtros como nome, tipo de comida, localização ou avaliação.

O usuário espera que:
- Os resultados sejam corretos e relevantes
- A busca seja rápida
- Os filtros funcionem corretamente
- Não ocorram erros ou resultados inconsistentes

---

## 2. Testes Caixa-Preta (Visão do Usuário)

Pensando como usuário, sem acesso ao código:

### Entradas possíveis:
- Nome do restaurante (ex: "Pizzaria")
- Tipo de comida (ex: "Pizza")
- Campo vazio
- Caracteres especiais (ex: "@#$%")
- Nome inexistente

### Comportamentos esperados:
- Retornar lista de restaurantes que correspondem à busca
- Exibir mensagem quando não houver resultados
- Aplicar corretamente os filtros
- Não travar ou apresentar erro

### Situações de erro:
- Nenhum resultado encontrado
- Busca retornando resultados incorretos
- Filtros não funcionando
- Sistema lento ou travando
- Erro ao digitar caracteres inválidos

---

## 3. Testes Caixa-Branca (Visão do Sistema)

Pensando com acesso ao código:

### Possíveis estruturas lógicas:
- `if` para verificar se o campo de busca está vazio
- Validação de entrada (caracteres inválidos)
- Consulta ao banco de dados com filtros
- Ordenação dos resultados (por avaliação, distância, etc.)
- Tratamento de exceções

### Situações para testar no código:
- Condição quando o campo está vazio
- Validação de entrada inválida
- Testar retorno correto da query no banco
- Verificar se os filtros estão sendo aplicados corretamente
- Testar diferentes caminhos do código (if/else)
- Tratamento de erros no banco de dados

---

## 4. Comparação entre as abordagens

A principal diferença é:

- **Caixa-preta:** testa o sistema sem conhecer o código, focando no comportamento para o usuário
- **Caixa-branca:** testa o funcionamento interno do sistema, analisando o código

### Tipos de problemas encontrados:

- **Caixa-preta:**
  - Erros de funcionalidade
  - Problemas de usabilidade
  - Resultados incorretos

- **Caixa-branca:**
  - Erros lógicos
  - Falhas em condições específicas
  - Problemas de implementação

---

## 5. Reflexão no contexto do LocalEats

Para os problemas atuais do sistema (resultados incorretos, falhas e inconsistências):

- A **caixa-preta** ajuda a identificar problemas visíveis ao usuário
- A **caixa-branca** ajuda a encontrar a causa desses problemas no código

### Conclusão:

Nenhuma abordagem sozinha é suficiente.

O ideal é usar as duas:
- Caixa-preta para validar a experiência do usuário
- Caixa-branca para corrigir erros internos

Isso garante maior qualidade e confiabilidade no sistema.

---

## Conclusão final

A combinação das duas abordagens permite encontrar mais erros e melhorar o sistema de forma completa, garantindo que o LocalEats funcione corretamente tanto para o usuário quanto internamente.
