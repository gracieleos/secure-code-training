# form-projeto-2

Este repositório contém a solução do exercício de segurança web do curso de **Cibersegurança da Pretalab**.

## 📌 Contexto

O desafio proposto foi analisar um formulário HTML inseguro (`Form-zero.html`) e aplicar **correções em três vulnerabilidades comuns** em aplicações web. O objetivo é reforçar os fundamentos de segurança no front-end, focando em **boas práticas de codificação segura**.

---

## ✅ Objetivos do Exercício

- Utilizar o formulário `Form-zero.html` como base
- Corrigir **3 vulnerabilidades** específicas
- Comentar no código qual vulnerabilidade foi resolvida
- Subir o arquivo corrigido neste repositório como `form-projeto-2.html`

---

## 🔐 Vulnerabilidades Corrigidas

### 1. 🛡️ **XSS (Cross-Site Scripting)**
Os dados inseridos pelo usuário eram exibidos diretamente na página sem nenhuma sanitização. Corrigido com uma função de escaping (`escaparHTML`) para neutralizar caracteres perigosos antes de exibir o conteúdo na tabela.

### 2. 🛡️ **Falta de Validação de Entrada**
Nenhum campo era validado, permitindo a submissão de dados inválidos. Foi implementada validação com `required`, `pattern` para telefone e regex para e-mail e nome.

### 3. 🛡️ **Uso Inseguro do `document.write`**
A nova aba com os dados era gerada com `document.write`, que pode ser explorado em ataques de injeção. Foi substituído por manipulação controlada e segura com escaping e `window.open`.

---

## 🧪 Como testar

1. Abra o arquivo `form-projeto-2.html` em seu navegador.
2. Preencha o formulário com seus dados.
3. Clique em "Salvar!" e veja os dados cadastrados em uma nova aba.
4. Os dados ficam armazenados no `localStorage` do navegador.
5. A cada novo envio, os dados anteriores permanecem (sem sobrescrever).

---

