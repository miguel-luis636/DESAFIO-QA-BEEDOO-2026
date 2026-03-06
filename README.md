# Desafio QA – Beedoo 2026

## 1. Análise inicial da aplicação

### Objetivo da aplicação

A aplicação analisada tem como objetivo permitir o **cadastro e a visualização de cursos** por meio de uma interface simples. O sistema disponibiliza um formulário para criação de novos cursos e uma página de listagem onde os cursos cadastrados podem ser visualizados.

Esse tipo de aplicação representa um módulo básico de gerenciamento de informações, no qual usuários podem inserir dados em um formulário e posteriormente consultar esses dados em uma listagem.

A partir da exploração inicial da aplicação, é possível entender que o foco principal do sistema é permitir que o usuário:

* Cadastre novos cursos através de um formulário.
* Visualize os cursos cadastrados em uma listagem.
* Verifique as informações inseridas após o cadastro.

Embora seja uma aplicação simples, esse tipo de funcionalidade é bastante comum em sistemas reais, como plataformas educacionais, sistemas de gestão de treinamentos ou sistemas administrativos.

---

# 2. Principais fluxos da aplicação

Durante a exploração da aplicação foram identificados os seguintes fluxos principais:

### 2.1 Fluxo de cadastro de cursos

Esse é o fluxo principal da aplicação. Ele permite que o usuário registre um novo curso no sistema.

O fluxo consiste em:

1. Acessar a página de criação de cursos.
2. Preencher os campos disponíveis no formulário.
3. Submeter o formulário clicando no botão de cadastro.
4. O sistema processa os dados informados.
5. O curso é criado e disponibilizado na listagem de cursos.

Esse fluxo é considerado crítico pois representa a principal funcionalidade do sistema.

---

### 2.2 Fluxo de listagem de cursos

Após o cadastro, os cursos criados devem aparecer na página de listagem.

Esse fluxo permite:

* Visualizar todos os cursos cadastrados.
* Confirmar se as informações foram registradas corretamente.
* Verificar se novos cursos aparecem na listagem após o cadastro.

Esse fluxo é importante para validar se o sistema está armazenando e exibindo os dados corretamente.

---

### 2.3 Validação de campos do formulário

Outro fluxo importante é o comportamento da aplicação quando o usuário interage com o formulário de cadastro.

Esse fluxo envolve:

* Preenchimento correto dos campos.
* Tentativas de envio com campos vazios.
* Inserção de dados inválidos.
* Inserção de dados inesperados.

Esse tipo de validação é essencial para garantir a integridade dos dados cadastrados no sistema.

---

# 3. Pontos críticos para teste

Durante a análise da aplicação, alguns pontos foram considerados mais críticos para a execução dos testes.

### 3.1 Validação de campos obrigatórios

Um dos aspectos mais importantes a serem testados é se o sistema realiza corretamente a validação dos campos do formulário.

Os testes devem verificar se:

* O sistema impede o cadastro quando campos obrigatórios não são preenchidos.
* O sistema apresenta mensagens de erro claras para o usuário.
* Campos não aceitam dados inválidos ou inconsistentes.

Falhas nesse tipo de validação podem comprometer a qualidade dos dados cadastrados no sistema.

---

### 3.2 Funcionamento do fluxo de cadastro

Outro ponto crítico é garantir que o processo de cadastro funcione corretamente.

Os testes devem verificar se:

* O formulário permite o cadastro quando os dados são válidos.
* O sistema registra corretamente as informações enviadas.
* Não ocorrem erros durante o envio do formulário.

Esse fluxo é essencial pois representa a principal funcionalidade da aplicação.

---

### 3.3 Exibição correta dos dados na listagem

Após o cadastro, é importante verificar se os dados inseridos aparecem corretamente na listagem de cursos.

Os testes devem validar se:

* O curso recém-cadastrado aparece na lista.
* As informações exibidas correspondem aos dados informados no formulário.
* Não ocorrem inconsistências ou erros de exibição.

---

### 3.4 Tratamento de entradas inesperadas

Também é importante verificar como o sistema se comporta diante de dados inesperados.

Alguns exemplos incluem:

* Inserção de textos muito longos.
* Inserção de caracteres especiais.
* Inserção de valores inesperados nos campos.

Esse tipo de teste ajuda a identificar possíveis falhas de validação ou problemas de segurança.

---

# 4. Decisões tomadas para criação dos testes

A definição dos cenários e casos de teste foi baseada na análise das funcionalidades disponíveis na aplicação.

Inicialmente foi realizada uma **exploração funcional da aplicação**, com o objetivo de entender como o sistema se comporta e quais são seus fluxos principais.

Após essa análise, os testes foram organizados considerando diferentes tipos de cenários.

### Testes do fluxo principal

Foram criados testes para validar o funcionamento correto do cadastro de cursos quando os dados são preenchidos corretamente.

Esses testes verificam se:

* O formulário aceita os dados válidos.
* O sistema cria o curso corretamente.
* O curso aparece na listagem após o cadastro.

---

### Testes de cenários negativos

Também foram criados testes com o objetivo de verificar como o sistema se comporta diante de situações incorretas ou inesperadas.

Esses testes incluem:

* Tentativa de cadastro com campos vazios.
* Inserção de dados inválidos.
* Envio de dados incompletos.

Esse tipo de cenário é importante para avaliar a robustez do sistema.

---

### Testes de validação de dados

Foram considerados testes para verificar se o sistema valida corretamente os dados informados pelo usuário.

Esses testes buscam identificar possíveis falhas como:

* Falta de validação de campos obrigatórios.
* Aceitação de dados inválidos.
* Ausência de limites para entrada de texto.

---

### Testes de comportamento do sistema

Além dos testes funcionais, também foram considerados cenários exploratórios com o objetivo de identificar comportamentos inesperados da aplicação.

Esses testes ajudam a identificar falhas que não são facilmente detectadas em testes apenas baseados em fluxo principal.

---

# 5. Explicação do raciocínio durante a análise

O processo de análise começou com uma **exploração livre da aplicação**, com o objetivo de compreender como o sistema funciona e quais são suas funcionalidades principais.

Durante essa fase inicial foram observados os seguintes aspectos:

* Estrutura das páginas da aplicação
* Campos disponíveis no formulário de cadastro
* Comportamento da listagem de cursos
* Interações possíveis do usuário com o sistema

A partir dessa exploração foi possível identificar os principais fluxos da aplicação, que envolvem o cadastro e a visualização de cursos.

Com base nesses fluxos, foram definidos cenários de teste que contemplam:

* funcionamento esperado do sistema (cenários positivos)
* possíveis erros de uso do usuário (cenários negativos)
* validações de campos e entradas de dados
* comportamento da aplicação após o cadastro de cursos

O raciocínio adotado durante a análise buscou priorizar testes que validassem a **confiabilidade do fluxo principal da aplicação**, bem como identificar possíveis falhas de validação, inconsistências na listagem de cursos ou comportamentos inesperados do sistema.

Essa abordagem permite garantir uma cobertura adequada das funcionalidades disponíveis e identificar possíveis problemas que possam impactar a experiência do usuário ou a qualidade dos dados registrados no sistema.
