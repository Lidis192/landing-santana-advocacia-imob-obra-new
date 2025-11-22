# 📥 Guia Passo-a-Passo: Como Baixar o Código Atualizado da Landing Page

## 🎯 O que você vai fazer

Você vai baixar a versão mais recente do código da landing page do Manus e substituir a pasta antiga no seu computador.

---

## 📋 Pré-requisitos

Você já tem:
- ✅ Conta no Manus
- ✅ VS Code instalado
- ✅ Node.js instalado

Se não tiver algum desses, me avise antes de continuar.

---

## 🚀 Passo-a-Passo Completo

### **PASSO 1: Acessar o Manus e Encontrar o Projeto**

#### 1.1 Abra seu navegador e acesse:
```
https://manus.im
```

#### 1.2 Faça login com sua conta

#### 1.3 Procure pelo projeto "santana_advocacia_landing"

Você deve ver um card com o nome do projeto.

---

### **PASSO 2: Baixar o Código Atualizado**

#### 2.1 Clique no card do projeto

Você verá várias opções.

#### 2.2 Procure por um botão que diz "Code" ou "Download"

Pode estar em um menu (três pontinhos) ou como um botão direto.

#### 2.3 Clique em "Download" ou "Export Code"

Uma pasta `.zip` será baixada para seu computador.

**Onde fica?** Geralmente em `C:\Users\[seu-usuario]\Downloads\`

---

### **PASSO 3: Extrair a Pasta Baixada**

#### 3.1 Abra a pasta Downloads

Procure pelo arquivo que termina em `.zip`

Deve ser algo como: `santana-advocacia-landing.zip`

#### 3.2 Clique com botão direito no arquivo

#### 3.3 Selecione "Extrair tudo..." (Windows)

Ou "Descompactar" (Mac)

#### 3.4 Escolha onde extrair

**IMPORTANTE:** Escolha um local fácil de encontrar, como:
```
C:\Users\[seu-usuario]\Documents\Projetos\
```

Não coloque em Downloads (pode ser deletado depois).

#### 3.5 Clique "Extrair"

Aguarde alguns segundos. Uma nova pasta será criada.

---

### **PASSO 4: Deletar a Pasta Antiga (OPCIONAL mas RECOMENDADO)**

Se você já tem uma pasta antiga do projeto no seu computador, delete-a para não ficar confuso.

#### 4.1 Encontre a pasta antiga

Procure por: `santana-advocacia-landing` (a versão antiga)

#### 4.2 Clique com botão direito

#### 4.3 Selecione "Deletar"

Pronto! Agora você tem apenas a versão nova.

---

### **PASSO 5: Abrir no VS Code**

#### 5.1 Abra o VS Code

#### 5.2 Clique em "File" (Arquivo) → "Open Folder" (Abrir Pasta)

#### 5.3 Navegue até a pasta que você extraiu

Procure por: `santana-advocacia-landing`

#### 5.4 Clique "Select Folder" (Selecionar Pasta)

Aguarde alguns segundos. O VS Code vai carregar o projeto.

---

### **PASSO 6: Instalar Dependências**

Agora você precisa instalar os pacotes que o projeto precisa para funcionar.

#### 6.1 Abra o Terminal no VS Code

Pressione: `Ctrl + ~` (backtick, aquele acento grave)

Ou vá em: "View" (Visualizar) → "Terminal"

#### 6.2 Você verá uma janela preta na parte inferior

#### 6.3 Digite este comando:

```bash
npm install --legacy-peer-deps
```

Pressione **Enter**

#### 6.4 Aguarde a instalação

Vai levar alguns minutos. Você verá muitas linhas de texto passando.

Quando terminar, você verá:
```
added XXX packages in XXs
```

---

### **PASSO 7: Rodar o Projeto Localmente**

Agora você vai testar se o código novo está funcionando.

#### 7.1 No terminal, digite:

```bash
npm run dev
```

Pressione **Enter**

#### 7.2 Você verá algo como:

```
  VITE v7.2.2  ready in 234 ms

  ➜  Local:   http://localhost:5173/
  ➜  press h to show help
```

#### 7.3 Abra seu navegador

Acesse: `http://localhost:5173/`

#### 7.4 Verifique se está a versão nova

Procure por uma frase que você sabe que foi alterada:
- "DÚVIDAS FREQUENTES"
- "Conheça a advogada que conduzirá seu caso"
- "Dra. Leidiane Santos de Santana"

Se encontrar, é a versão nova! ✅

---

### **PASSO 8: Fazer o Build (Preparar para Hostinger)**

Quando tudo estiver funcionando localmente, você precisa fazer o build.

#### 8.1 Parar o servidor local

No terminal, pressione: `Ctrl + C`

Você verá: `^C`

#### 8.2 Fazer o build

Digite:

```bash
npm run build
```

Pressione **Enter**

#### 8.3 Aguarde

Vai levar alguns segundos. Quando terminar, você verá:

```
✓ built in 2.5s
```

#### 8.4 Verifique a pasta dist

Uma pasta chamada `dist` será criada na raiz do projeto.

Essa é a pasta que você vai enviar para Hostinger!

---

## 📊 Resumo Visual do Processo

```
1. Baixar do Manus
   ↓
2. Extrair a pasta
   ↓
3. Abrir no VS Code
   ↓
4. npm install --legacy-peer-deps
   ↓
5. npm run dev (testar localmente)
   ↓
6. npm run build (preparar para Hostinger)
   ↓
7. Enviar pasta "dist" para Hostinger
```

---

## ✅ Checklist Completo

- [ ] **1. Acessei o Manus e fiz login**
- [ ] **2. Encontrei o projeto "santana_advocacia_landing"**
- [ ] **3. Cliquei em Download e baixei o .zip**
- [ ] **4. Extraí a pasta em um local seguro**
- [ ] **5. Deletei a pasta antiga (se tinha)**
- [ ] **6. Abri a pasta no VS Code**
- [ ] **7. Abri o Terminal no VS Code**
- [ ] **8. Executei `npm install --legacy-peer-deps`**
- [ ] **9. Executei `npm run dev`**
- [ ] **10. Verifiquei no navegador se é a versão nova**
- [ ] **11. Parei o servidor (Ctrl + C)**
- [ ] **12. Executei `npm run build`**
- [ ] **13. Verifiquei se a pasta "dist" foi criada**

---

## 🎯 Próximo Passo

Após fazer o build com sucesso, você estará pronto para enviar para Hostinger!

A pasta `dist` contém todos os arquivos que você precisa fazer upload.

---

## ❓ Dúvidas Comuns

### **P: Onde fica o arquivo que baixei?**
R: Em `C:\Users\[seu-usuario]\Downloads\`

### **P: Posso deletar o arquivo .zip após extrair?**
R: Sim! Você pode deletar. Você já tem a pasta extraída.

### **P: E se eu clicar em "npm install" e der erro?**
R: Tente: `npm install --legacy-peer-deps`

Se ainda der erro, me envie um screenshot do erro.

### **P: Quanto tempo leva para instalar as dependências?**
R: Geralmente 2-5 minutos, dependendo da sua internet.

### **P: Posso fechar o VS Code enquanto está instalando?**
R: Não! Deixe rodando até terminar.

---

## 📞 Se Tiver Dúvida em Algum Passo

Me envie:
1. **Qual passo você está**
2. **Screenshot do que está na tela**
3. **Qualquer mensagem de erro** (se houver)

Vou ajudar! 🚀

---

## 🎉 Parabéns!

Você conseguiu baixar e preparar o código atualizado da sua landing page!

Agora você está pronto para fazer upload para Hostinger e deixar seu site ao vivo! 🌐
