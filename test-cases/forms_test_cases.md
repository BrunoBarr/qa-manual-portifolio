## FORM VALIDATION – TEST CASES

---

### TC-FORM-01 — Campo obrigatório vazio

**Objetivo:**  
Garantir que o campo obrigatório acusa erro quando está vazio.

**Passos:**
1. Acessar a página de formulário
2. Deixar todos os campos obrigatórios vazios
3. Tentar enviar o formulário

**Resultado esperado:**  
Mensagem de erro indicando que o campo é obrigatório.

---

### TC-FORM-02 — Validação de email inválido

**Objetivo:**  
Verificar a validação do formato de email.

**Dados de teste:**
- Email: `testemail` (sem @ ou domínio)

**Passos:**
1. Preencher o campo email com formato inválido
2. Preencher os demais campos com valores válidos
3. Enviar o formulário

**Resultado esperado:**  
Mensagem de erro informando **“Formato de email inválido”**.

---

### TC-FORM-03 — Limite de caracteres ultrapassado

**Objetivo:**  
Garantir que existe limite de tamanho para campos de texto.

**Dados de teste:**
- Campo texto com mais de 255 caracteres (ex: repetição de `AAAAA...`)

**Passos:**
1. Inserir um valor maior que o permitido
2. Enviar o formulário

**Resultado esperado:**  
O sistema impede o envio ou exibe mensagem de erro informando limite excedido.

---

### TC-FORM-04 — Campo numérico com caractere inválido

**Objetivo:**  
Verificar a validação de campos numéricos.

**Dados de teste:**
- Número: `abc123`

**Passos:**
1. Inserir caracteres alfabéticos em um campo numérico
2. Enviar o formulário

**Resultado esperado:**  
Mensagem de erro indicando formato inválido.

---

### TC-FORM-05 — Validação de senha de acordo com padrão

**Objetivo:**  
Verificar se a senha segue os padrões de segurança definidos.

**Dados de teste:**
- Senha: `123` (curta ou sem requisitos mínimos)

**Passos:**
1. Preencher o campo senha com um valor que não atende às regras
2. Enviar o formulário

**Resultado esperado:**  
Mensagem indicando os requisitos mínimos de senha (ex: “mínimo 8 caracteres”).

---

### TC-FORM-06 — Envio com dados válidos

**Objetivo:**  
Verificar que o formulário aceita inputs corretos.

**Dados de teste:**
- Email: `user@example.com`
- Número: `12345`
- Texto: `Teste QA`

**Passos:**
1. Preencher todos os campos com valores válidos
2. Clicar em **Enviar**

**Resultado esperado:**  
Formulário enviado com sucesso, exibindo mensagem de confirmação.

---

### TC-FORM-07 — Campo read-only

**Objetivo:**  
Validar que campos marcados como **read-only** não podem ser editados.

**Passos:**
1. Tentar alterar o campo configurado como read-only

**Resultado esperado:**  
Campo não pode ser editado.

---

### TC-FORM-08 — Campo desabilitado

**Objetivo:**  
Confirmar que campos desabilitados não aceitam entrada de dados.

**Passos:**
1. Tentar inserir qualquer valor no campo desabilitado

**Resultado esperado:**  
Campo não aceita valores.

---

### TC-FORM-09 — Upload de arquivo permitido

**Objetivo:**  
Testar a funcionalidade de upload de arquivos válidos.

**Dados de teste:**
- Arquivo válido (`.jpg`, `.pdf`)

**Passos:**
1. Selecionar um arquivo permitido
2. Realizar o upload

**Resultado esperado:**  
Upload realizado com sucesso.

---

### TC-FORM-10 — Upload de arquivo inválido

**Objetivo:**  
Verificar as restrições de tipo de arquivo no upload.

**Dados de teste:**
- Arquivo inválido (`.exe` ou formato não permitido)

**Passos:**
1. Selecionar um arquivo inválido
2. Tentar realizar o upload

**Resultado esperado:**  
Mensagem de erro informando que o formato do arquivo não é permitido.
