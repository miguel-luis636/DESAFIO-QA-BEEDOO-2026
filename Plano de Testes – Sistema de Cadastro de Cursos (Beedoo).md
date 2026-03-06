# 🧪 Plano de Testes – Sistema de Cadastro de Cursos (Beedoo)

## 📌 1. Identificação

* **Projeto**: Sistema de Cadastro e Listagem de Cursos – Desafio QA Beedoo

* **Aplicação**: Módulo de Cursos

* **Ambiente de Testes**: Aplicação Web hospedada em Netlify (ambiente disponibilizado para o desafio)

* **URL da aplicação**:
  [https://creative-sherbet-a51eac.netlify.app/](https://creative-sherbet-a51eac.netlify.app/)

* **Tipos de Teste**:

  * Testes Manuais Baseados em Funcionalidade
  * Testes Exploratórios
  * Testes Negativos
  * Testes Alternativos
  * Testes de Validação de Formulário
  * Testes de Usabilidade

* **Data de Atualização**: 06/03/2026

* **Responsável**: Miguel Luis de Ataíde Ferreira

---

# 🎯 2. Objetivo

Garantir a **qualidade funcional do módulo de cadastro e listagem de cursos**, verificando se o sistema atende ao comportamento esperado, validando entradas de dados, identificando possíveis falhas e registrando defeitos encontrados durante a execução dos testes.

Os testes têm como foco principal:

* Validar o fluxo principal de cadastro de cursos
* Verificar o comportamento da listagem de cursos
* Avaliar validações de campos do formulário
* Identificar comportamentos inesperados
* Registrar defeitos e melhorias encontrados durante a execução dos testes

A execução dos testes busca simular interações reais de usuários com o sistema, garantindo que as funcionalidades apresentem comportamento consistente e confiável.

---

# 🧠 3. Abordagem de Teste

A estratégia de testes utilizada neste desafio foi baseada em **análise exploratória inicial da aplicação**, seguida pela definição de cenários de teste estruturados.

A abordagem considera os seguintes pontos:

---

### 🔹 Exploração Inicial do Sistema

Inicialmente foi realizada uma exploração da aplicação para compreender:

* Funcionalidades disponíveis
* Fluxos principais de navegação
* Estrutura do formulário de cadastro
* Comportamento da listagem de cursos

Essa etapa permitiu identificar os principais pontos do sistema que necessitam de validação.

---

### 🔹 Testes Baseados em Fluxos Principais

Os testes foram priorizados considerando os fluxos principais da aplicação:

* Cadastro de cursos
* Visualização da listagem de cursos

Esses fluxos representam o núcleo funcional do sistema e possuem maior impacto para o usuário.

---

### 🔹 Testes Negativos

Também foram criados cenários com o objetivo de validar como o sistema se comporta quando ocorre uso incorreto da aplicação, como por exemplo:

* Campos obrigatórios vazios
* Inserção de dados inválidos
* Inserção de textos muito longos
* Inserção de caracteres especiais

Esses testes ajudam a identificar possíveis falhas de validação.

---

### 🔹 Testes Exploratórios

Durante a execução dos testes também foram realizadas sessões de testes exploratórios com o objetivo de identificar comportamentos inesperados do sistema.

Esse tipo de teste permite encontrar falhas que não foram inicialmente previstas nos cenários estruturados.

---

# 🧩 4. Escopo

### ✅ Incluído no escopo

* Cadastro de novos cursos
* Validação dos campos do formulário
* Comportamento do botão de criação de curso
* Exibição dos cursos cadastrados na listagem
* Validação de entradas inválidas
* Comportamento do sistema em cenários negativos
* Verificação de possíveis falhas de usabilidade

---

### ❌ Fora do escopo

* Testes de performance e carga
* Testes de segurança avançados
* Testes de infraestrutura
* Testes de integração com serviços externos
* Testes automatizados (não aplicável neste desafio)

---

# ⚖️ 5. Ferramentas Utilizadas

Durante a execução dos testes foram utilizadas as seguintes ferramentas:

* Navegadores Web:

  * Google Chrome
  * Mozilla Firefox
  * Microsoft Edge

* Ferramentas de apoio:

  * DevTools do navegador (análise de console, network e elementos)
  * Google Sheets (documentação dos casos de teste)
  * Google Drive (armazenamento de evidências)
  * GitHub (armazenamento do repositório e documentação)
  * Ferramenta de captura de tela para registro de evidências

---

# 🧪 6. Técnicas de Teste Utilizadas

---

### Observação sobre técnicas de teste

Durante a elaboração e execução dos testes deste desafio, o foco foi seguir as instruções fornecidas na descrição da atividade, priorizando a criação de cenários e casos de teste voltados para os fluxos principais da aplicação, validações de formulário e identificação de possíveis falhas no comportamento do sistema.

Técnicas formais de projeto de testes, como **particionamento de equivalência** e **análise de valor limite**, não foram aplicadas de forma estruturada neste momento, pois o desafio não especificava a obrigatoriedade dessas abordagens.

Dessa forma, os testes realizados foram baseados principalmente em:

* Testes funcionais do fluxo principal
* Cenários positivos e negativos
* Validação de campos do formulário
* Testes exploratórios para identificação de comportamentos inesperados

Ainda assim, caso o projeto evoluísse para um ambiente de desenvolvimento contínuo, essas técnicas poderiam ser incorporadas para otimizar a cobertura de testes e melhorar a eficiência da estratégia de qualidade.

### 🔹 Testes de Fluxo Principal

Validação do fluxo principal da aplicação:

Cadastro de curso → Exibição do curso na listagem.

Esse teste garante que a funcionalidade central da aplicação esteja funcionando corretamente.

---

### 🔹 Testes Negativos

Testes realizados para verificar como o sistema se comporta quando ocorre uso incorreto da aplicação.

Exemplos:

* Tentativa de cadastro com campos vazios
* Inserção de caracteres inválidos
* Envio de dados incompletos

---

### 🔹 Testes Exploratórios

Sessões de exploração livre da aplicação com foco em:

* Identificar comportamentos inesperados
* Verificar inconsistências na interface
* Avaliar a experiência do usuário

---

# ⏱️ 7. Cronograma de Testes

| Atividade                       | Frequência                | Observação                       |
| ------------------------------- | ------------------------- | -------------------------------- |
| Exploração inicial da aplicação | Início do desafio         | Entendimento do sistema          |
| Criação dos cenários de teste   | Após análise inicial      | Baseado nos fluxos identificados |
| Execução dos testes             | Após criação dos cenários | Validação das funcionalidades    |
| Registro de defeitos            | Durante execução          | Documentação de bugs encontrados |
| Coleta de evidências            | Durante execução          | Prints e gravações               |

---

# 📋 8. Módulos e Prioridades

| Código | Módulo                            | Prioridade |
| ------ | --------------------------------- | ---------- |
| RF01   | Cadastro de cursos                | Alta       |
| RF02   | Validação de campos do formulário | Alta       |
| RF03   | Listagem de cursos                | Alta       |
| RF04   | Comportamento do formulário       | Média      |
| RF05   | Usabilidade da interface          | Média      |

---

# 🐞 9. Gestão de Defeitos

Durante a execução dos testes, os defeitos identificados são registrados contendo as seguintes informações:

* Identificador do defeito
* Título do bug
* Descrição do problema
* Passos para reprodução
* Resultado esperado
* Resultado obtido
* Severidade ou impacto
* Evidência (print ou gravação)

Os defeitos são documentados em um relatório de bugs disponível no repositório do desafio.

---

# ⚠️ 10. Análise de Risco

A priorização dos testes foi definida considerando os seguintes critérios:

* Impacto da funcionalidade no usuário final
* Importância do fluxo para o funcionamento do sistema
* Probabilidade de ocorrência de falhas
* Possíveis falhas de validação de dados

Os fluxos considerados de maior risco são:

* Cadastro de cursos
* Validação de campos obrigatórios
* Exibição correta dos cursos na listagem

Falhas nesses pontos podem comprometer diretamente a funcionalidade principal da aplicação.

---

# 📄 11. Documentação dos Testes

Toda a documentação relacionada aos testes executados neste desafio foi registrada em uma planilha estruturada no Google Sheets.

A planilha contém:

- Cenários de teste
- Casos de teste detalhados
- Resultados da execução dos testes (OK / NOK)
- Registro de evidências

📊 **Planilha de Cenários e Casos de Teste**

https://docs.google.com/spreadsheets/d/1TFpueHLFpJUTn0uwFgSRu9yisRpiB1wKSalo2ph5cRc/edit?usp=sharing

Além da planilha, parte das informações também está documentada diretamente no repositório do GitHub:

- **Resultados gerais da execução dos testes** estão descritos no README do projeto.
- **Bugs identificados durante a execução dos testes** também foram registrados no README, contendo descrição do problema, passos para reprodução, resultado esperado e impacto identificado.

Essa organização foi adotada para manter a rastreabilidade das informações e facilitar a análise do desafio durante o processo de avaliação.

---

# 🎯 Nota Final

Este plano de testes foi elaborado com o objetivo de estruturar a abordagem de qualidade aplicada ao módulo de cursos da aplicação analisada.

A estratégia prioriza a validação dos fluxos principais do sistema, bem como a identificação de possíveis falhas de validação, inconsistências na interface e comportamentos inesperados.

A documentação dos testes, evidências e defeitos encontrados está organizada no repositório do desafio, garantindo rastreabilidade e transparência durante o processo de avaliação.
