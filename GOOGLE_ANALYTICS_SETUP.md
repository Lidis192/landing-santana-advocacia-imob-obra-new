# Configuração do Google Analytics 4 (GA4)

## 📊 Rastreamento de Conversões Implementado

A landing page Santana Advocacia agora possui rastreamento de eventos de clique em todos os botões de CTA (Call-To-Action). Os eventos rastreados são:

### Eventos Configurados

**Evento:** `cta_click`
**Categoria:** `engagement`
**Labels (Botões):**
- `Fale com especialista - Hero` - Botão na seção azul (hero)
- `Fale com um Especialista - FAQ` - Botão na seção de FAQ
- `Agende uma Consulta - Advogada` - Botão na seção da advogada

---

## 🔧 Como Configurar seu Google Analytics ID

### Passo 1: Obter seu ID de Rastreamento GA4

1. Acesse [Google Analytics](https://analytics.google.com/)
2. Faça login com sua conta Google
3. Crie uma nova propriedade ou selecione uma existente
4. Vá para **Admin** → **Propriedades** → **Informações da propriedade**
5. Copie o **ID de medição** (formato: `G-XXXXXXXXXX`)

### Passo 2: Atualizar o arquivo `client/index.html`

Localize as linhas com `G-XXXXXXXXXX` e substitua pelo seu ID real:

```html
<!-- Google Analytics 4 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-SEU_ID_AQUI"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-SEU_ID_AQUI');
</script>
```

**Exemplo com ID real:**
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-ABC123XYZ"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-ABC123XYZ');
</script>
```

### Passo 3: Verificar a Implementação

1. Abra a landing page no navegador
2. Abra o **DevTools** (F12)
3. Vá para a aba **Network**
4. Clique em um dos botões de CTA
5. Procure por requisições para `googletagmanager.com` ou `google-analytics.com`
6. Confirme que o evento foi enviado

---

## 📈 Visualizar os Eventos no Google Analytics

### Verificação em Tempo Real

1. Acesse [Google Analytics](https://analytics.google.com/)
2. Vá para **Relatórios** → **Tempo real**
3. Clique em um botão da landing page
4. Você deve ver o evento aparecer em tempo real

### Criar um Evento Personalizado

1. Vá para **Admin** → **Eventos**
2. Clique em **Criar evento**
3. Configure:
   - **Nome do evento:** `cta_click`
   - **Condição:** `event_name = cta_click`
4. Salve o evento

### Criar um Relatório de Conversões

1. Vá para **Relatórios** → **Aquisição** → **Eventos**
2. Procure por `cta_click` nos eventos principais
3. Analise o desempenho de cada botão usando o `event_label`

---

## 🎯 Métricas Disponíveis

Após configurar o GA4, você poderá acompanhar:

| Métrica | Descrição |
|---------|-----------|
| **Cliques por Botão** | Quantos cliques cada CTA recebeu |
| **Taxa de Conversão** | Porcentagem de visitantes que clicaram |
| **Tempo até Clique** | Quanto tempo o usuário levou para clicar |
| **Dispositivo** | Mobile, tablet ou desktop |
| **Localização** | Cidade/país do usuário |
| **Fonte de Tráfego** | De onde o usuário veio (Google, Facebook, etc.) |

---

## 💡 Dicas Importantes

1. **Aguarde 24-48 horas** para que os dados apareçam completamente no Google Analytics
2. **Use o modo de depuração** do GA4 para testar em tempo real
3. **Configure metas** para rastrear conversões específicas (ex: cliques que levam a WhatsApp)
4. **Analise regularmente** os dados para otimizar a landing page

---

## 🔍 Troubleshooting

**Problema:** Eventos não aparecem no GA4

**Soluções:**
1. Verifique se o ID de rastreamento está correto
2. Confirme que JavaScript está habilitado no navegador
3. Aguarde 24-48 horas para que os dados sincronizem
4. Use o **DebugView** do GA4 para diagnosticar problemas

---

## 📞 Suporte

Para mais informações sobre Google Analytics 4:
- [Documentação oficial do GA4](https://support.google.com/analytics/answer/10089681)
- [Guia de implementação](https://developers.google.com/analytics/devguides/collection/ga4)
