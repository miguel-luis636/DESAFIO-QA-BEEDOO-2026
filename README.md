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

Além disso, foi elaborado um **Plano de Testes** contendo a estratégia de testes adotada, abordagem utilizada, escopo, técnicas consideradas e organização da execução dos testes realizados neste desafio.

O plano de testes completo pode ser acessado no seguinte link:

Plano de Testes – Sistema de Cadastro de Cursos (Beedoo):
[https://github.com/miguel-luis636/DESAFIO-QA-BEEDOO-2026/blob/main/Plano%20de%20Testes%20%E2%80%93%20Sistema%20de%20Cadastro%20de%20Cursos%20(Beedoo).md](https://github.com/miguel-luis636/DESAFIO-QA-BEEDOO-2026/blob/main/Plano%20de%20Testes%20%E2%80%93%20Sistema%20de%20Cadastro%20de%20Cursos%20%28Beedoo%29.md)

Esse documento complementa a análise apresentada neste README e descreve de forma mais detalhada a estratégia utilizada para condução das atividades de teste.

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

### 3.5 Usabilidade e experiência do usuário

Além das validações funcionais, também é importante avaliar a **usabilidade da aplicação**, mesmo sendo um sistema simples.

Um sistema de cadastro deve permitir que o usuário compreenda facilmente como utilizar suas funcionalidades, reduzindo dúvidas ou dificuldades durante a interação.

Durante os testes, é importante observar aspectos como:

* Clareza das informações exibidas na interface.
* Facilidade de navegação entre as páginas do sistema.
* Compreensão dos campos do formulário.
* Facilidade para identificar ações como cadastro e visualização de cursos.

Problemas de usabilidade podem impactar diretamente a experiência do usuário, mesmo quando a funcionalidade técnica está funcionando corretamente.

---

### 3.6 Qualidade visual e consistência de design

Outro ponto relevante para avaliação é a **qualidade visual da interface e consistência do design**.

Mesmo em aplicações simples, é importante que o sistema apresente uma interface organizada, clara e visualmente agradável, pois isso contribui para a percepção de qualidade do produto.

Durante a análise foram considerados aspectos como:

* Organização dos elementos na tela.
* Alinhamento de componentes.
* Legibilidade dos textos.
* Consistência visual entre páginas.
* Clareza dos botões e ações disponíveis.

Interfaces bem organizadas e visualmente consistentes ajudam a tornar o sistema **mais intuitivo e fácil de utilizar**, contribuindo para uma melhor experiência do usuário e maior qualidade do produto final.

---

# 4. Decisões tomadas para criação dos testes

A definição dos cenários e casos de teste foi baseada na análise das funcionalidades disponíveis na aplicação.

Inicialmente foi realizada uma **exploração funcional da aplicação**, com o objetivo de entender como o sistema se comporta e quais são seus fluxos principais.

Durante essa etapa também foi realizada uma **avaliação dos fluxos de risco do sistema**, considerando quais funcionalidades poderiam gerar maior impacto caso apresentassem falhas. Essa análise ajudou a priorizar os testes nas áreas mais críticas da aplicação, como o fluxo de cadastro e a exibição correta das informações na listagem de cursos.

Após essa análise, os testes foram organizados considerando diferentes tipos de cenários.

---

## Análise de riscos dos fluxos da aplicação

Durante a análise foi realizada uma avaliação simples de riscos com o objetivo de identificar quais partes do sistema poderiam causar maior impacto em caso de falha.

| Fluxo / Funcionalidade                     | Gravidade | Probabilidade | Impacto                                              | Mitigação                                          |
| ------------------------------------------ | --------- | ------------- | ---------------------------------------------------- | -------------------------------------------------- |
| Cadastro de cursos não salvar corretamente | Alta      | Média         | Usuário não consegue registrar cursos no sistema     | Testes funcionais completos do fluxo de cadastro   |
| Cursos não aparecerem na listagem          | Alta      | Média         | Dados cadastrados não podem ser visualizados         | Testar integração entre cadastro e listagem        |
| Falha na validação de campos obrigatórios  | Média     | Alta          | Dados inconsistentes podem ser cadastrados           | Testes de validação de campos e cenários negativos |
| Aceitação de dados inesperados             | Média     | Média         | Pode gerar inconsistências ou falhas no sistema      | Testes exploratórios e entradas inválidas          |
| Problemas de usabilidade no formulário     | Baixa     | Média         | Usuário pode ter dificuldade para utilizar o sistema | Avaliação de interface e experiência de uso        |

Essa análise de risco foi utilizada para **priorizar os testes nos fluxos mais críticos**, garantindo maior cobertura nas funcionalidades principais da aplicação.

---

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

# 5. Estratégia de testes

A abordagem de testes utilizada neste desafio foi baseada em uma combinação de diferentes técnicas de análise e validação do sistema.

Inicialmente foi realizada uma fase de **testes exploratórios**, com o objetivo de compreender o comportamento da aplicação, identificar seus fluxos principais e entender como o sistema responde às interações do usuário.

A partir dessa exploração inicial, foram aplicadas as seguintes abordagens de teste:

- **Testes exploratórios** para entender o comportamento geral da aplicação e identificar possíveis comportamentos inesperados.
- **Testes funcionais** para validar os fluxos principais do sistema, principalmente o processo de cadastro e visualização de cursos.
- **Testes negativos** para verificar como o sistema reage a entradas inválidas ou cenários de erro.
- **Testes baseados em risco**, priorizando os fluxos considerados mais críticos para o funcionamento da aplicação.

Essa abordagem permitiu avaliar tanto o funcionamento esperado do sistema quanto identificar possíveis falhas de validação, inconsistências de comportamento ou problemas na experiência do usuário.

---

# 6. Limitações da análise

Durante a execução deste desafio, alguns tipos de testes não foram aprofundados devido ao escopo e ao tempo disponível para a atividade.

Entre os tipos de testes que poderiam ser explorados em uma etapa posterior estão:

- **Testes de performance**, para avaliar como a aplicação se comporta sob maior volume de uso.
- **Testes de segurança**, para verificar possíveis vulnerabilidades relacionadas a entradas de dados ou manipulação de informações.
- **Testes automatizados**, que poderiam ser implementados para validar automaticamente os fluxos principais da aplicação.
- Técnicas formais de design de teste como **Partição de Equivalência** e **Análise de Valor Limite**, que poderiam ampliar a cobertura e profundidade dos cenários de teste.

Essas técnicas poderiam ser aplicadas em fases futuras do projeto com o objetivo de aumentar a robustez da estratégia de testes e garantir uma cobertura ainda mais completa das funcionalidades do sistema.

---

# 7. Explicação do raciocínio durante a análise
O raciocínio adotado durante a análise buscou priorizar testes que validassem a **confiabilidade do fluxo principal da aplicação**, bem como identificar possíveis falhas de validação, inconsistências na listagem de cursos ou comportamentos inesperados do sistema.

Essa abordagem permite garantir uma cobertura adequada das funcionalidades disponíveis e identificar possíveis problemas que possam impactar a experiência do usuário ou a qualidade dos dados registrados no sistema.
