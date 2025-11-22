# Passo 4: Preparar Projeto para Produção - Guia Completo

## 🎯 Objetivo

Preparar o projeto React + Vite para ser enviado à Hostinger e fazer o build de produção sem erros.

---

## ⚠️ Entendendo o Erro que Você Recebeu

```
npm error ERESOLVE unable to resolve dependency tree
npm error Could not resolve dependency:
npm error peer vite@"^4.0.0 || ^5.0.0" from @builder.io/vite-plugin-jsx-loc@0.1.1
```

**O que significa:** Há um conflito entre as versões de dependências. Seu projeto usa Vite 7.2.2, mas um pacote espera Vite 4.0 ou 5.0.

---

## ✅ Solução Passo-a-Passo (Ordem de Prioridade)

### **Solução 1: Usar --legacy-peer-deps (RECOMENDADO - 90% de chance de funcionar)**

Esta é a solução mais rápida e segura para este tipo de erro.

#### Passo 1: Abra o terminal na pasta do projeto

```bash
# No seu caso, a pasta é:
cd "C:\Users\santa\OneDrive\Documents\MEU ESCRITÓRIO\31 LANDING PAGE IMOB\santana-advocacia-landing"
```

#### Passo 2: Limpe o cache do npm

```bash
npm cache clean --force
```

**O que faz:** Remove arquivos antigos que podem estar causando conflito.

#### Passo 3: Delete a pasta node_modules e package-lock.json

```bash
# No Windows (Command Prompt):
rmdir /s /q node_modules
del package-lock.json

# Ou no PowerShell:
Remove-Item -Recurse -Force node_modules
Remove-Item package-lock.json
```

**O que faz:** Remove todas as dependências instaladas e o arquivo de lock, forçando uma reinstalação limpa.

#### Passo 4: Instale com --legacy-peer-deps

```bash
npm install --legacy-peer-deps
```

**O que faz:** Instala as dependências ignorando conflitos menores de versão de peer dependencies.

#### Passo 5: Verifique se funcionou

```bash
npm run build
```

Se você vir uma mensagem como `✓ built in 2.5s`, funcionou! ✅

---

### **Solução 2: Se a Solução 1 não funcionar - Usar pnpm (ALTERNATIVA)**

O seu projeto foi criado com `pnpm`, então use isso em vez de `npm`:

```bash
# Limpe o cache
pnpm store prune

# Delete node_modules
rmdir /s /q node_modules

# Reinstale com pnpm
pnpm install

# Build
pnpm build
```

**Por que funciona:** `pnpm` gerencia dependências de forma mais eficiente que `npm`.

---

### **Solução 3: Se ambas não funcionarem - Atualizar package.json**

Edite o arquivo `package.json` na raiz do projeto:

1. Abra `package.json` com um editor de texto (VS Code, Notepad, etc.)
2. Procure por `"devDependencies"` (deve estar perto do final)
3. Procure por `@builder.io/vite-plugin-jsx-loc` e remova essa linha
4. Salve o arquivo
5. Execute:

```bash
npm cache clean --force
rmdir /s /q node_modules
del package-lock.json
npm install --legacy-peer-deps
npm run build
```

---

## 🔍 Verificação Final

Após executar `npm run build`, você deve ver:

```
✓ 1234 modules transformed.
✓ built in 2.5s
```

E uma nova pasta `dist` deve aparecer na raiz do projeto.

---

## 📋 Checklist Completo para Passo 4

- [ ] **1. Abrir terminal na pasta do projeto**
- [ ] **2. Executar `npm cache clean --force`**
- [ ] **3. Deletar `node_modules` e `package-lock.json`**
- [ ] **4. Executar `npm install --legacy-peer-deps`**
- [ ] **5. Executar `npm run build`**
- [ ] **6. Verificar se a pasta `dist` foi criada**
- [ ] **7. Fazer upload do conteúdo de `dist` para Hostinger**

---

## 🚀 Próximo Passo: Upload para Hostinger

Após o build bem-sucedido:

1. Abra a pasta `dist` (criada na raiz do projeto)
2. Selecione TODOS os arquivos dentro de `dist`
3. Faça upload para o File Manager da Hostinger (pasta `public_html`)
4. Acesse seu site: `www.santanasadvocacia.com.br`

---

## ❓ Se Ainda Não Funcionar

Se nenhuma solução funcionar, envie-me:

1. **Screenshot do erro completo** (como você fez)
2. **Conteúdo do arquivo `package.json`** (a parte de devDependencies)
3. **Versão do Node.js** (execute `node --version` no terminal)

Assim posso ajudar com uma solução mais específica.

---

## 💡 Dica Importante

**Sempre use a mesma ferramenta de gerenciamento de pacotes:**
- Se o projeto foi criado com `pnpm`, use `pnpm` (não `npm`)
- Se foi criado com `npm`, use `npm` (não `pnpm`)

Misturar as duas pode causar conflitos!

---

## 📞 Suporte

Qualquer dúvida, me envie:
- Screenshot do erro
- Qual solução você tentou
- Qual foi o resultado

Vou ajudar a resolver! 🎯
