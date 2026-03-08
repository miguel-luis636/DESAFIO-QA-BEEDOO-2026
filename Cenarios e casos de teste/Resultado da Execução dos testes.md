# 📝 Relatório de Testes Exploratórios – Sistema de Cadastro de Cursos

---

# 🔹 Informações Gerais

* **Projeto:** Sistema de Cadastro de Cursos
* **Data do Teste:** 07/03/2026
* **Testador:** Miguel Luis
* **Tipo de Teste:** Testes (Funcional, Exploratorio, UX, Validação de Dados)

---

# 🔹 Ambiente de Teste

| Item                   | Descrição                                                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------ |
| Aplicação              | Sistema de Cadastro de Cursos                                                              |
| Ambiente               | Produção                                                                                   |
| URL da aplicação       | [https://creative-sherbet-a51eac.netlify.app](https://creative-sherbet-a51eac.netlify.app) |
| Navegador              | Firefox 148  64 bits                                                                              |
| Sistema Operacional    | Windows 11                                                                                 |
| Ferramentas utilizadas | DevTools, Console do navegador                                                             |

---

# 🔹 Escopo dos Testes

Os testes exploratórios consideraram principalmente os seguintes fluxos:

* Cadastro de cursos
* Listagem de cursos
* Exclusão de cursos
* Validações de formulário
* Cenários negativos
* Comportamentos inesperados

---

# 🔹 Resultados da Execução dos Testes

Durante a execução dos testes manuais foram avaliados **18 cenários de teste** relacionados aos fluxos principais do sistema.

Os cenários cobriram principalmente:

* Cadastro de cursos
* Listagem de cursos
* Exclusão de cursos
* Validações de formulário
* Cenários negativos
* Comportamentos inesperados

---

# 📊 Resumo da Execução

| Métrica                   | Quantidade | Percentual |
| ------------------------- | ---------- | ---------- |
| **Total de Cenários**     | 18         | 100%       |
| **Cenários OK**           | 5          | 27,78%     |
| **Cenários NOK**          | 13         | 72,22%     |
| **Cenários não testados** | 0          | 0%         |

---

# 📈 Interpretação dos Resultados

Os resultados indicam que **a maioria dos cenários apresentou falhas durante a execução dos testes**.

Dos **18 cenários executados**:

* **5 cenários passaram com sucesso**
* **13 cenários apresentaram falhas**

Isso representa aproximadamente **72,22% de cenários com problemas**, indicando que o sistema ainda possui **diversas inconsistências funcionais e técnicas**.

---

# 📉 Distribuição dos Resultados

A análise gráfica dos testes demonstra claramente a diferença entre cenários aprovados e reprovados.

* 🟢 **Cenários OK:** 27,8%
* 🔴 **Cenários NOK:** 72,2%

A maior concentração de falhas está relacionada principalmente a:

* **validação de dados do formulario**
* **integração com API**
* **comportamento incorreto do sistema em cenários negativos**

---

# 🔎 Análise dos Resultados

Os cenários que falharam estão diretamente relacionados aos seguintes tipos de problemas:

### Validação de dados

Foram identificadas falhas como:

* campos obrigatórios aceitando valores vazios
* número de vagas aceitando valores negativos
* datas incoerentes sendo aceitas
* Possível vulnerabilidade de Cross-Site Scripting
  

Esses problemas indicam ausência de validações adequadas no sistema.

---

### Feedback inadequado ao usuário

O sistema também apresenta problemas de feedback, por exemplo:

* mensagens de sucesso exibidas mesmo quando a operação falha
* ausência de mensagens de erro no formulário

Esse tipo de problema prejudica a **experiência do usuário e a confiabilidade do sistema**.

---

# 📊 Conclusão da Execução dos Testes

Os resultados obtidos indicam que o sistema **ainda não está estável para uso em produção**, pois apresenta uma taxa elevada de falhas nos cenários avaliados.

As principais áreas que necessitam de correção são:

* validação de dados no formulário
* integração com a API
* tratamento de erros e mensagens ao usuário

A correção desses pontos deve ser priorizada para garantir **maior confiabilidade, integridade dos dados e melhor experiência para o usuário**.


# 🔹 Observações por Sistema

---

# 1️⃣ **Frontend – Sistema de Cadastro de Cursos**

### URL

[https://creative-sherbet-a51eac.netlify.app](https://creative-sherbet-a51eac.netlify.app)

---

# ⚠️ Problemas encontrados(Mais detalhes dos bugs no relatorio de bug)

---

### Link do relatorio de bugs: https://github.com/miguel-luis636/DESAFIO-QA-BEEDOO-2026/blob/main/Cenarios%20e%20casos%20de%20teste/Relatorio%20de%20Bugs.md

# 1. Cadastro de curso aceita campos vazios

O sistema permite criar cursos mesmo quando **nenhum campo do formulário é preenchido**.

### Impacto

* Base de dados pode ser preenchida com registros inválidos
* Falta de integridade dos dados
* Possível quebra em funcionalidades futuras


### Recomendação

Adicionar validação obrigatória nos campos do formulário.

---

# 2. Número de vagas aceita valores negativos

### Descrição

O campo **Número de vagas** aceita valores negativos.

Exemplo:

```
-10 vagas
```

### Impacto

* Dados inconsistentes
* Problemas em relatórios ou cálculos futuros

### Recomendação

Implementar validação:

```
vagas > 0

```
---

# 3. Datas inconsistentes são aceitas

### Descrição

O sistema aceita datas absurdas ou incoerentes.

Exemplo:

```
Data de início: 2300
Data final: 2021
```

### Impacto

* Dados inválidos
* Possível falha em ordenações ou relatórios

### Recomendação

Validar:

* Data início menor que data fim
* Datas dentro de limites aceitáveis

---

# 4. URL da imagem aceita qualquer tipo de link

### Descrição

O campo de imagem aceita qualquer URL.

Exemplo:

```
youtube.com
```

### Impacto

* Quebra de layout
* Falha na renderização da imagem

### Recomendação

Validar se a URL é realmente uma imagem.

---

# 5. Página de detalhes do curso inexistente

### Descrição

O sistema não possui página individual de visualização do curso.

Existe apenas a listagem.

### Impacto

* Fluxo incompleto
* Experiência limitada para o usuário

---

# 6. Header não redireciona para a home


### Descrição

O título do sistema não redireciona para a página inicial ao ser clicado.

### Impacto

* Pequena quebra de padrão de usabilidade.

### Recomendação

Adicionar redirecionamento para a homepage.

---

### 7. Exclusão de cursos não funciona

### Descrição

A exclusão de cursos retorna erro na API.

Erro identificado:

```
DELETE /test-api/courses/1
HTTP 405
```

### Explicação do erro

O erro **HTTP 405 – Method Not Allowed** significa que o servidor recebeu a requisição, porém **o método HTTP utilizado não é permitido para o recurso solicitado**.

Nesse caso, o sistema está enviando uma requisição **DELETE**, porém o servidor não permite esse método para esse endpoint.

Isso pode ocorrer por diversos motivos, como:

* endpoint da API não implementado para o método DELETE
* configuração incorreta do servidor
* erro na rota da API
* restrições de métodos HTTP no backend
* regras incorretas de configuração do servidor (como `.htaccess` ou configuração da API)

### Impacto

* Usuário não consegue excluir cursos
* Fluxo principal do sistema quebrado

### Recomendação

Verificar a implementação do endpoint responsável pela exclusão de cursos na API e garantir que o método **DELETE** esteja corretamente configurado e permitido para essa rota.

---

# 8. Sistema mostra mensagem falsa de exclusão

### Descrição

O sistema informa que o curso foi excluído, porém ele **continua existindo na lista**.

### Impacto

* Feedback enganoso
* Falta de confiabilidade do sistema

# 9. Falta de mensagens de erro no formulário


### Descrição

Quando o usuário envia o formulário com dados inválidos:

* nenhuma mensagem de erro é exibida

### Impacto

Usuário não entende o que está errado.

---

# 10. Campos sem limite de caracteres


### Descrição

Campos de texto permitem inserir conteúdo extremamente longo.

### Impacto

* Possível quebra de layout
* Problemas de armazenamento

---

# 11. Textarea pode quebrar o layout


### Descrição

O campo textarea pode crescer indefinidamente.

### Impacto

Quebra visual do formulário.

---

# 12. Grid da listagem desproporcional

### Descrição

Os cards da listagem não mantêm proporção consistente.

Mesmo em diferentes resoluções.

### Impacto

Experiência visual inconsistente.

---

# 13. Tela vazia quando não há cursos

### Descrição

Quando não há cursos cadastrados, a tela fica totalmente vazia.

### Recomendação

Exibir mensagem:

```
Não há cursos cadastrados.
```

---

# 🔹 Problemas Técnicos Observados

Durante os testes também foram identificados avisos no console.

### Avisos de cookies

```
cookie __Secure-YEC rejected SameSite Lax
```

### Possível causa

Configuração inadequada de cookies para contextos cross-site.

---

# 🔹 Observações Gerais

Grande parte dos defeitos encontrados poderia ser evitada com:

* validação de formulários
* revisão de regras de negócio
*  integridade de dados
*  API

---

# 📊 Tabela de Prioridade de Correção e Severidade

| ID | Bug                                        | Severidade | Prioridade                | Impacto no Sistema                                      | Possível Causa Raiz                                             |
| -- | ------------------------------------------ | ---------- | ------------------------- | ------------------------------------------------------- | --------------------------------------------------------------- |
| 1  | Cadastro de curso aceita campos vazios     | 🔴 Crítica | 🔥 P1 – Correção imediata | Permite registros inválidos na base de dados            | Falta de validação de campos obrigatórios no frontend e backend |
| 2  | Número de vagas aceita valores negativos   | 🔴 Alta    | 🔥 P1 – Correção imediata | Dados inconsistentes podem afetar cálculos e relatórios | Ausência de validação numérica e regra de negócio no campo      |
| 3  | Datas inconsistentes são aceitas           | 🔴 Alta    | 🔥 P1 – Correção imediata | Permite dados impossíveis que quebram lógica do sistema | Falta de validação de lógica entre datas (start < end)          |
| 4  | URL da imagem aceita qualquer tipo de link | 🟠 Média   | P2 – Alta prioridade      | Quebra de layout e falha no carregamento da imagem      | Validação insuficiente do formato da URL ou ausência de regex   |
| 5  | Página de detalhes do curso inexistente    | 🟠 Média   | P3 – Prioridade média     | Fluxo de navegação incompleto                           | Funcionalidade não implementada ou backlog incompleto           |
| 6  | Header não redireciona para a home         | 🟡 Baixa   | P4 – Baixa prioridade     | Pequena quebra de padrão de navegação                   | Falta de evento de navegação ou rota não configurada            |
| 7  | Exclusão de cursos não funciona            | 🔴 Crítica | 🔥 P1 – Correção imediata | Usuário não consegue excluir cursos                     | Endpoint DELETE da API não implementado ou método não permitido |
| 8  | Sistema mostra mensagem falsa de exclusão  | 🔴 Alta    | 🔥 P1 – Correção imediata | Feedback enganoso ao usuário                            | Frontend não valida resposta da API antes de exibir mensagem    |
| 9  | Falta de mensagens de erro no formulário   | 🟠 Média   | P2 – Alta prioridade      | Usuário não entende erros ao preencher formulário       | Ausência de tratamento de erros e validações visuais            |
| 10 | Campos sem limite de caracteres            | 🟠 Média   | P2 – Alta prioridade      | Pode causar problemas de layout ou banco de dados       | Falta de definição de limite de caracteres nos inputs           |
| 11 | Textarea pode quebrar o layout             | 🟡 Baixa   | P4 – Baixa prioridade     | Problema visual na interface                            | CSS sem limite de tamanho ou auto-resize mal configurado        |
| 12 | Grid da listagem desproporcional           | 🟡 Baixa   | P4 – Baixa prioridade     | Inconsistência visual na listagem                       | Problemas no CSS do grid ou flex layout                         |
| 13 | Tela vazia quando não há cursos            | 🟡 Baixa   | P3 – Prioridade média     | Usuário não entende o estado da aplicação               | Falta de tratamento de estado vazio na interface                |

---

# 🔎 Principais Causas Raiz Identificadas

Durante a análise dos bugs, foram identificados alguns **padrões de falha**:

### 1️⃣ Falta de validação de dados

Problemas relacionados:

* Campos vazios
* Valores negativos
* Datas inválidas
* URLs inválidas
* Campos sem limite

**Possível causa**

* Falta de validação no frontend
* Falta de validação no backend
* Ausência de regras de negócio documentadas

---

### 2️⃣ Problemas de integração com API

Problemas relacionados:

* Exclusão não funciona
* HTTP 405
* Feedback falso de exclusão

**Possível causa**

* Endpoint DELETE não implementado
* Método HTTP incorreto
* Frontend não trata erro da API

---

### 3️⃣ Problemas de UX / Usabilidade

Problemas relacionados:

* Falta de mensagens de erro
* Tela vazia
* Header não navegável

**Possível causa**

* Falta de testes de usabilidade
* Falta de estados da interface

---

### 4️⃣ Problemas de UI / CSS

Problemas relacionados:

* Grid quebrado
* Textarea expandindo demais

**Possível causa**

* Falta de padronização de layout
* Falta de testes responsivos

---

# 🎯 Conclusão Técnica

Os bugs indicam que o sistema precisa principalmente de melhorias em:

### 🔧 Backend / API

* validação de dados
* endpoint DELETE funcional
* regras de negócio

### 💻 Frontend

* validação de formulário
* tratamento de erro da API
* mensagens de feedback

### 🎨 UX/UI

* estados vazios
* feedback ao usuário
* consistência visual

---

# 🔹 Conclusão

Os testes manuais identificaram **diversos problemas críticos** que impactam diretamente:

* confiabilidade do sistema
* integridade dos dados
* experiência do usuário

Os principais problemas estão concentrados em:

* validação de dados
* integração com API
* feedback ao usuário

A correção desses pontos é essencial para que o sistema possa evoluir para um ambiente de produção mais estável.

---

### Observação final

“Qualidade não é algo que se adiciona no final.
Ela é construída desde o início, através de boas práticas de desenvolvimento, testes contínuos e colaboração entre equipes.”

