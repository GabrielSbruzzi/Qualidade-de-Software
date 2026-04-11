# Aula 6 – Planejamento e Execução de Testes

> Disciplina: Qualidade de Software  
> Projeto: LocalEats  
> Integrantes do grupo:  
> - Gabriel Sbruzzi  

---

# 1. Plano de Testes

## 1.1 Objetivo

Validar as principais funcionalidades do sistema LocalEats, garantindo que apresentem comportamento correto, consistente e que atendam às expectativas do usuário final.

---

## 1.2 Escopo

### O que será testado
- Login de usuário  
- Busca de restaurantes  
- Avaliação de restaurantes  

### O que NÃO será testado
- Integração com sistemas externos  
- Testes de performance em larga escala  
- Segurança avançada  

---

## 1.3 Funcionalidades selecionadas

- Login/Cadastro  
- Busca de restaurantes  
- Avaliação  

---

## 1.4 Estratégia de Testes

Os testes serão realizados de forma manual, baseados em cenários reais de uso do sistema.

- Tipos de teste:
  - (X) Funcional  
  - ( ) Usabilidade  
  - ( ) Outros: Testes exploratórios  

- Abordagem:
  Testes manuais baseados em cenários previamente definidos, utilizando comportamento do usuário (BDD).

---

## 1.5 Responsáveis

| Nome              | Responsabilidade                  |
|------------------|----------------------------------|
| Gabriel Sbruzzi  | Criação dos casos de teste       |
| Nome 2           | Execução dos testes              |
| Nome 3           | Registro de evidências           |
| Nome 4           | Análise dos resultados           |

---

# 2. Casos de Teste

---

## CT-01 – Login com sucesso

**Pré-condição:**  
Usuário já cadastrado no sistema

**Passos:**  
1. Acessar a página de login  
2. Informar usuário válido  
3. Informar senha válida  
4. Clicar em "Entrar"  

**Dados de entrada:**  
Usuário: usuario_teste  
Senha: 123456  

**Resultado esperado:**  
O sistema deve redirecionar para a página inicial após login bem-sucedido  

---

## CT-02 – Login com senha incorreta

**Pré-condição:**  
Usuário cadastrado

**Passos:**  
1. Acessar a página de login  
2. Informar usuário válido  
3. Informar senha incorreta  
4. Clicar em "Entrar"  

**Dados de entrada:**  
Usuário: usuario_teste  
Senha: 1234567  

**Resultado esperado:**  
O sistema deve exibir mensagem de erro informando credenciais inválidas  

---

## CT-03 – Busca de restaurante com resultado

**Pré-condição:**  
Usuário na página inicial

**Passos:**  
1. Digitar "Pizza" no campo de busca  
2. Clicar em buscar  

**Dados de entrada:**  
Texto: Pizza  

**Resultado esperado:**  
O sistema deve exibir uma lista de restaurantes relacionados à busca  

---

## CT-04 – Busca de restaurante sem resultado

**Pré-condição:**  
Usuário na página inicial

**Passos:**  
1. Digitar "asdfghjkl" no campo de busca  
2. Clicar em buscar  

**Dados de entrada:**  
Texto: asdfghjkl  

**Resultado esperado:**  
O sistema deve exibir mensagem informando que não há resultados  

---

## CT-05 – Avaliação de restaurante

**Pré-condição:**  
Usuário logado e acessando um restaurante

**Passos:**  
1. Selecionar 5 estrelas  
2. Confirmar avaliação  

**Dados de entrada:**  
Avaliação: 5 estrelas  

**Resultado esperado:**  
O sistema deve registrar a avaliação corretamente  

---

# 3. Execução dos Testes

| ID     | Resultado (Passou/Falhou) | Evidência (descrição ou print) |
|--------|--------------------------|--------------------------------|
| CT-01  | Passou                   | Login realizado com sucesso     |
| CT-02  | Falhou                   | Não exibiu mensagem clara       |
| CT-03  | Passou                   | Restaurantes listados           |
| CT-04  | Falhou                   | Não mostrou mensagem de erro    |
| CT-05  | Passou                   | Avaliação registrada            |

---

# 4. Análise dos Resultados

- Quantidade de testes executados: 5  
- Quantidade de testes que passaram: 3  
- Quantidade de testes que falharam: 2  

## Principais problemas encontrados
- Falta de mensagens de erro claras  
- Inconsistência na busca sem resultados  
- Feedback insuficiente ao usuário  

---

# 5. Reflexão

- O plano de testes ajudou a organizar melhor o processo? Por quê?  
Sim, pois permitiu estruturar os testes de forma clara, facilitando a execução e identificação de problemas.

- Algum problema só foi identificado durante a execução? Explique.  
Sim, a ausência de mensagens de erro só foi percebida durante a execução prática dos testes.

- O que o grupo melhoraria no processo de testes?  
Criar mais cenários de teste, incluindo casos extremos e melhorar o registro de evidências com prints.

---

## Conclusão

O comportamento das funcionalidades testadas é parcialmente aceitável, pois apesar dos fluxos principais funcionarem, ainda existem falhas importantes relacionadas à usabilidade e feedback ao usuário.

---

# 6. Conclusão Geral

- Qualidade geral do sistema testado: Média  
- Principais pontos positivos: Funcionalidades principais operacionais  
- Principais problemas identificados: Falta de feedback e inconsistências  
- Impressão geral do grupo: O sistema precisa de melhorias, mas possui boa base funcional
