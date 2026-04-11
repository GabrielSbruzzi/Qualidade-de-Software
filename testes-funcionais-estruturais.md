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
| Gabriel Sbruzzi  | Execução dos testes              |
| Gabreil Sbruzzi  | Registro de evidências           |
| Gabreil Sbruzzi  | Análise dos resultados           |

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
Usuário: gabrielsbruzzi@gmail.com  
Senha: 123456  

**Resultado esperado:**  
O sistema deve redirecionar para a página inicial após login bem-sucedido  

---

## CT-02 – Cadastro

**Pré-condição:**  
Usuário cadastrado

**Passos:**  
1. Acessar a página de login  
2. Informar usuário válido  
3. Informar senha incorreta  
4. Clicar em "Entrar"  

**Dados de entrada:**  
Nome Completo: Gabriel Sbruzzi
Usuário: gabrielsbruzzi@gmail.com  
Senha: 123456

**Resultado esperado:**  
 sistema deve cadastrar corretamente 

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

## CT-05 – Login com senha incorreta

**Pré-condição:**  
Usuário cadastrado

**Passos:**  
1. Acessar a página de login  
2. Informar usuário válido  
3. Informar senha incorreta  
4. Clicar em "Entrar"  

**Dados de entrada:**  
Usuário: gabrielsbruzzi@gmail.com
Senha: 1234567  

**Resultado esperado:**  
O sistema deve exibir mensagem de erro informando credenciais inválidas  

# 3. Execução dos Testes

| ID     | Resultado (Passou/Falhou) | Evidência (descrição ou print) |
|--------|--------------------------|--------------------------------|
| CT-01  | Passou                   | Login realizado com sucesso     |
| CT-02  | Passou                   | Cadastro Realizado com Sucesso  |
| CT-03  | Falhou                   | Restaurantes não listados       |
| CT-04  | Passou                   | Restaurante não há Resultado    |
| CT-05  | Passou                   | Mostrou a mensagem de erro      |

---

# 4. Análise dos Resultados

- Quantidade de testes executados: 5  
- Quantidade de testes que passaram: 4 
- Quantidade de testes que falharam: 1 

## Principais problemas encontrados  
- Inconsistência no campo de Busca, pesquisando por resultados que deveriama aparecer  

---

# 5. Reflexão

- O plano de testes ajudou a organizar melhor o processo? Por quê?  
Sim, pois permitiu estruturar os testes de forma clara, facilitando a execução e identificação de problemas.

- Algum problema só foi identificado durante a execução? Explique.  
Sim, a inconsistência no campo de busca.

- O que o grupo melhoraria no processo de testes?  
Criar mais cenários de teste, incluindo casos extremos e melhorar o registro de evidências com prints.

---

## Conclusão

O comportamento das funcionalidades testadas é parcialmente aceitável, pois apesar dos fluxos principais funcionarem, ainda existem falhas importantes relacionadas à usabilidade e feedback ao usuário.

---

# 6. Conclusão Geral

- Qualidade geral do sistema testado: Média  
- Principais pontos positivos: Funcionalidades principais operacionais  
- Principais problemas identificados: Inconsistência no campo de Busca  
- Impressão geral do grupo: O sistema precisa de melhorias, mas possui boa base funcional
