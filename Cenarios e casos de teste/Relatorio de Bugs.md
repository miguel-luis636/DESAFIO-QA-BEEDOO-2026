# 5️⃣ Registro de Bugs 

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


#Observação baseada nos princípios de teste (CTFL)

De acordo com os princípios de teste definidos no **ISTQB Certified Tester Foundation Level (CTFL)**, é importante destacar 3 conceitos relevantes para a análise dos resultados obtidos:

**1. Testes mostram a presença de defeitos, não a sua ausência**

Durante a execução dos testes foram identificados diversos bugs no sistema. Entretanto, isso não significa que todos os defeitos existentes foram encontrados. Os testes apenas evidenciam problemas que foram detectados nos cenários executados.

**2. Teste exaustivo é impossível**

Não é possível testar todas as combinações de entradas, estados e fluxos de um sistema. Por isso, mesmo após a execução dos testes documentados neste relatório, ainda podem existir defeitos não identificados.

**3. Falácia da ausência de erros**

Mesmo que todos os bugs encontrados sejam corrigidos, isso não garante automaticamente que o sistema esteja completamente livre de problemas ou que atenda perfeitamente às necessidades do usuário. A qualidade também depende da adequação do sistema aos requisitos e às regras de negócio.

Além disso, durante a análise foram identificados potenciais riscos relacionados a **duplicação de dados**, inconsistência de informações e registros inválidos. Em alguns casos, esses problemas estão diretamente relacionados à ausência de validações no formulário de cadastro.

Por exemplo, a implementação correta de validações de campos obrigatórios, validação de datas e validação numérica no campo **número de vagas** tende a corrigir múltiplos problemas simultaneamente. Ao impedir o envio de dados inválidos, o sistema também reduz a possibilidade de **registros duplicados ou inconsistentes**, melhorando a integridade da base de dados.

Dessa forma, a correção de determinadas validações pode resolver não apenas um bug isolado, mas também **evitar efeitos colaterais como duplicação de dados, inconsistência de registros e falhas em relatórios ou cálculos futuros**.


---

# 🐞 Bug 1 — Cadastro de curso aceita campos vazios

### Severidade

🔴 Crítica

### Passos para reproduzir

1. Acessar a página de cadastro de cursos
2. Deixar todos os campos do formulário vazios
3. Clicar no botão **Criar Curso**

### Resultado atual

O sistema cria o curso mesmo com todos os campos vazios.

### Resultado esperado

O sistema deve impedir o cadastro e exibir mensagens informando que os campos obrigatórios precisam ser preenchidos.

### Evidências

*[Bug 1 — Cadastro de curso aceita campos vazios](https://drive.google.com/file/d/11Y3J8Y5-rwSY-9G8-nP4yBJSscOaIlkg/view?usp=sharing)*

### Possíveis melhorias no sistema

* Implementar validação de campos obrigatórios
* Destacar visualmente campos inválidos
* Exibir mensagens claras de erro ao usuário
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 2 — Número de vagas aceita valores negativos

### Severidade

🔴 Alta

### Passos para reproduzir

1. Acessar a página de cadastro de cursos
2. Preencher os campos normalmente
3. Informar **-10** no campo **Número de vagas**
4. Clicar em **Criar Curso**

### Resultado atual

O sistema permite cadastrar o curso com número de vagas negativo.

### Resultado esperado

O sistema deve impedir o cadastro e exibir mensagem informando que o número de vagas deve ser maior que zero.

### Evidências

[*(Bug 2 — Número de vagas aceita valores negativos)*](https://drive.google.com/file/d/1j3HkniPSOZlZkRNEXupuEsGc9wlVA0NV/view?usp=sharing)

### Possíveis melhorias no sistema

* Validar valores numéricos no formulário
* Definir limites mínimos para campos numéricos
* Exibir mensagem de erro quando o valor for inválido
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 3 — Datas inconsistentes são aceitas

### Severidade

🔴 Alta

### Passos para reproduzir

1. Acessar a página de cadastro de cursos
2. Informar uma **data de início maior que a data final**
3. Preencher os demais campos
4. Clicar em **Criar Curso**

### Resultado atual

O sistema permite cadastrar cursos com datas inconsistentes.

### Resultado esperado

O sistema deve validar a ordem das datas e impedir o cadastro.

### Evidências

[*(Bug 3 — Datas inconsistentes são aceitas)*](https://drive.google.com/file/d/1j3HkniPSOZlZkRNEXupuEsGc9wlVA0NV/view?usp=sharing)

### Possíveis melhorias no sistema

* Implementar validação entre datas
* Exibir alerta quando a data inicial for maior que a final
* Definir limites aceitáveis para datas
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 4 — URL da imagem aceita qualquer tipo de link

### Severidade

🟠 Média

### Passos para reproduzir

1. Acessar o formulário de cadastro de cursos
2. Inserir um link inválido no campo de imagem (exemplo: youtube.com)
3. Clicar em **Criar Curso**

### Resultado atual

O sistema aceita qualquer URL e tenta exibir a imagem.

### Resultado esperado

O sistema deve validar se a URL corresponde a uma imagem válida.

### Evidências

[*(Bug 4 — URL da imagem aceita qualquer tipo de link*](https://drive.google.com/file/d/1j3HkniPSOZlZkRNEXupuEsGc9wlVA0NV/view?usp=sharing)

### Possíveis melhorias no sistema

* Validar formato da URL
* Verificar extensão da imagem
* Exibir mensagem de erro caso a URL seja inválida
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 5 — Página de detalhes do curso inexistente

### Severidade

🟠 Média

### Passos para reproduzir

1. Acessar a listagem de cursos
2. Tentar visualizar detalhes de um curso

### Resultado atual

O sistema não possui página individual de detalhes.

### Resultado esperado

O sistema deve possuir uma página dedicada com informações completas do curso.

### Evidências

*(Ao clicar no card de um curso para tentar acessar os seus detalhes)*

### Possíveis melhorias no sistema

* Implementar página de detalhes do curso
* Permitir navegação a partir da listagem
* Exibir informações completas do curso
* Exibir mensagem informativa ao usuário

---

# 🐞 Melhoria 6 — Header não redireciona para a home

### Severidade

🟡 Baixa

### Passos para reproduzir

1. Acessar qualquer página do sistema
2. Clicar no título ou logo no cabeçalho

### Resultado atual

Nenhum redirecionamento acontece.

### Resultado esperado

O usuário deve ser redirecionado para a página inicial.

### Evidências

[*(Melhoria 6 — Header não redireciona para a home)*](https://drive.google.com/file/d/1VjFBXsbKW35CvMIh-r-gIPVTUJI2PM2R/view?usp=sharing)

### Possíveis melhorias no sistema

* Implementar navegação padrão no header
* Adicionar link para homepage
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 7 — Exclusão de cursos não funciona

### Severidade

🔴 Crítica

### Passos para reproduzir

1. Acessar a listagem de cursos
2. Selecionar um curso existente
3. Clicar no botão **Excluir**

### Resultado atual

A requisição retorna erro **HTTP 405 Method Not Allowed** e o curso não é excluído.

### Resultado esperado

O sistema deve excluir o curso selecionado com sucesso.

### Evidências

[*(Bug 7 — Exclusão de cursos não funciona)*](https://drive.google.com/file/d/1Qfsjh2RjoNQW21cWCrMCYfmOLkeHAzXG/view?usp=sharing)

### Possíveis melhorias no sistema

* Implementar corretamente o endpoint DELETE na API
* Validar métodos HTTP permitidos
* Exibir mensagem adequada caso ocorra erro
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 8 — Sistema mostra mensagem falsa de exclusão

### Severidade

🔴 Alta

### Passos para reproduzir

1. Acessar a listagem de cursos
2. Tentar excluir um curso
3. Observar a mensagem exibida pelo sistema

### Resultado atual

O sistema informa que o curso foi excluído, porém ele continua na lista.

### Resultado esperado

A mensagem de sucesso deve ser exibida apenas quando a exclusão realmente ocorrer.

### Evidências

[*(Bug 8 — Sistema mostra mensagem falsa de exclusão)*](https://drive.google.com/file/d/1Qfsjh2RjoNQW21cWCrMCYfmOLkeHAzXG/view?usp=sharing)

### Possíveis melhorias no sistema

* Validar resposta da API antes de mostrar mensagens
* Atualizar a lista após exclusão real
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 9 — Falta de mensagens de erro no formulário

### Severidade

🟠 Média

### Passos para reproduzir

1. Acessar o formulário de cadastro
2. Inserir dados inválidos
3. Enviar o formulário

### Resultado atual

Nenhuma mensagem de erro é exibida.

### Resultado esperado

O sistema deve informar claramente os erros encontrados no formulário.

### Evidências

[*(Bug 9 — Falta de mensagens de erro no formulário)*](https://drive.google.com/file/d/1Kka1OX995y8KyjqWhOjvx2g2bwh0U1e9/view?usp=sharing)

### Possíveis melhorias no sistema

* Implementar mensagens de validação
* Destacar campos com erro
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 10 — Campos sem limite de caracteres

### Severidade

🟠 Média

### Passos para reproduzir

1. Acessar o formulário de cadastro
2. Inserir texto muito longo nos campos
3. Criar o curso

### Resultado atual

O sistema aceita conteúdo extremamente longo.

### Resultado esperado

Os campos devem possuir limite de caracteres.

### Evidências

[*(Bug 10 — Campos sem limite de caracteres)*](https://drive.google.com/file/d/10KHS9SJpTpaLDRQm632V8TrNEHRObCl8/view?usp=sharing)

### Possíveis melhorias no sistema

* Definir limite de caracteres
* Mostrar contador de caracteres
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 11 — Textarea pode quebrar o layout

### Severidade

🟡 Baixa

### Passos para reproduzir

1. Acessar o formulário de cadastro
2. Inserir grande quantidade de texto no campo descrição

### Resultado atual

O campo cresce indefinidamente e quebra o layout.

### Resultado esperado

O campo deve possuir limite visual e manter o layout estável.

### Evidências

[*(Bug 11 — Textarea pode quebrar o layout)*](https://drive.google.com/file/d/1_IIYYia2Y0G86JdC8jtrFYKC0apOqere/view?usp=sharing)

### Possíveis melhorias no sistema

* Definir altura máxima para textarea
* Utilizar scroll interno
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 12 — Grid da listagem desproporcional

### Severidade

🟡 Baixa

### Passos para reproduzir

1. Acessar a listagem de cursos
2. Visualizar os cards em diferentes resoluções

### Resultado atual

Os cards possuem tamanhos inconsistentes.

### Resultado esperado

Os cards devem manter proporção e alinhamento padronizados.

### Evidências

[*(Bug 12 — Grid da listagem desproporcional)*](https://drive.google.com/file/d/1s0Is4r00vzbJzK76DKr6j-A8mgjFc51J/view?usp=sharing)
[*(Evicencia 2)*](https://drive.google.com/file/d/155uLLl_4fGQrP8NIscoF8dniAdTw4zzZ/view?usp=sharing)
[*(Bug 12 — Grid da listagem desproporcional)*](https://drive.google.com/file/d/1s0Is4r00vzbJzK76DKr6j-A8mgjFc51J/view?usp=sharing)
[*(Bug 12 — Grid da listagem desproporcional)*](https://drive.google.com/file/d/1s0Is4r00vzbJzK76DKr6j-A8mgjFc51J/view?usp=sharing)

### Possíveis melhorias no sistema

* Ajustar layout CSS do grid
* Padronizar tamanho dos cards
* Exibir mensagem informativa ao usuário

---

# 🐞 Bug 13 — Tela vazia quando não há cursos

### Severidade

🟡 Baixa

### Passos para reproduzir

1. Acessar o sistema sem cursos cadastrados
2. Abrir a listagem de cursos

### Resultado atual

A tela aparece completamente vazia.

### Resultado esperado

O sistema deve exibir mensagem informando que não há cursos cadastrados.

### Evidências

[*(Bug 13 — Tela vazia quando não há cursos)*](https://drive.google.com/file/d/1sR_2LwqIzQ_TDlTNnhZ-fhfwIvqSAyYw/view?usp=sharing)

### Possíveis melhorias no sistema

* Criar estado vazio da interface
* Exibir mensagem informativa ao usuário

---

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
| 13 | Tela vazia quando não há cursos            | 🟡 Baixa   | P3 – Prioridade média     | Usuário não entende o estado da aplicação               | Falta de tratamento de estado vazio na interface      
