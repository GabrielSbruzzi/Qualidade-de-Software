# Estratégia Inicial de Testes – LocalEats

## 1. Funcionalidades principais

As principais funcionalidades do sistema LocalEats são:

- Busca de restaurantes (por culinária, localização e preço)  
- Visualização de cardápios, fotos e avaliações  
- Salvamento de restaurantes favoritos  
- Sistema de recomendações personalizadas  
- Compartilhamento de experiências (avaliações dos usuários)  

---

## 2. Níveis de teste

### 2.1 Busca de restaurantes

- **Teste unitário:** validação dos filtros (culinária, localização, preço) e regras de busca  
- **Teste de integração:** comunicação entre front-end e API de busca + banco de dados  
- **Teste de sistema:** usuário realiza busca e recebe lista correta de restaurantes  
- **Teste de aceitação:** usuário consegue encontrar restaurantes relevantes facilmente  

---

### 2.2 Visualização de cardápios, fotos e avaliações

- **Teste unitário:** carregamento de dados individuais (imagens, textos, avaliações)  
- **Teste de integração:** integração entre API e serviço de armazenamento de mídia  
- **Teste de sistema:** usuário acessa um restaurante e visualiza todas as informações corretamente  
- **Teste de aceitação:** usuário consegue entender o restaurante e decidir se deseja ir  

---

### 2.3 Salvamento de favoritos

- **Teste unitário:** lógica de salvar/remover favorito  
- **Teste de integração:** comunicação entre usuário autenticado e banco de dados  
- **Teste de sistema:** usuário adiciona e visualiza lista de favoritos  
- **Teste de aceitação:** usuário consegue salvar restaurantes para acessar depois  

---

### 2.4 Recomendações personalizadas

- **Teste unitário:** algoritmo de recomendação baseado em preferências  
- **Teste de integração:** integração entre histórico do usuário e motor de recomendação  
- **Teste de sistema:** usuário recebe sugestões personalizadas na plataforma  
- **Teste de aceitação:** recomendações fazem sentido para o usuário  

---

### 2.5 Avaliações e compartilhamento de experiências

- **Teste unitário:** criação, edição e exclusão de avaliações  
- **Teste de integração:** envio e recuperação de avaliações no banco  
- **Teste de sistema:** usuário publica avaliação e ela aparece corretamente  
- **Teste de aceitação:** usuário consegue compartilhar sua experiência sem perder dados  

---

## 3. Prioridades e riscos

As funcionalidades mais críticas são:

### Busca de restaurantes
- Impacto direto na usabilidade do sistema  
- Problemas já relatados: resultados incorretos  
- Se falhar, o sistema perde sua principal função  

### Avaliações
- Problema real: avaliações desaparecendo  
- Afeta confiança dos usuários e reputação da plataforma  

### Performance (sistema como um todo)
- Lentidão em horários de pico  
- Pode causar abandono do app  

### Recomendações
- Impacto médio (experiência do usuário)  
- Não impede uso do sistema, mas reduz valor  

### Favoritos
- Impacto menor, mas importante para retenção  

 **Justificativa:**  
Prioridade foi definida com base no impacto no usuário e nos problemas já identificados no sistema. Funcionalidades essenciais (busca e avaliações) têm maior risco e devem ser testadas primeiro.

---

## 4. Pirâmide de testes

A estratégia ideal segue a pirâmide de testes:

### Base (maior quantidade): Testes unitários
- Mais rápidos e baratos  
- Garantem funcionamento da lógica básica  
- Devem cobrir filtros, regras e validações  

### Meio: Testes de integração
- Validam comunicação entre serviços  
- Importantes para APIs, banco e autenticação  

### Topo (menor quantidade): Testes de sistema e aceitação
- Mais caros e lentos  
- Focados em fluxos críticos (ex: buscar restaurante, avaliar)  

 **Justificativa:**  
Testes unitários são mais eficientes e baratos, permitindo detectar erros cedo. Testes de sistema devem ser usados com moderação, focando apenas nos fluxos mais importantes.

---

## 5. Testes em produção

Sim, o sistema deve utilizar testes em produção, com cuidado.

### Situações recomendadas:

- **Feature flags:** liberar funcionalidades para poucos usuários  
- **Testes A/B:** validar melhorias de interface e recomendações  
- **Monitoramento contínuo:** identificar lentidão e falhas em tempo real  
- **Logs e métricas:** detectar erros que não aparecem em ambiente de teste  

**Justificativa:**  
Como o sistema já apresenta problemas em produção (lentidão, falhas em dispositivos), testes controlados em produção ajudam a identificar comportamentos reais dos usuários.
