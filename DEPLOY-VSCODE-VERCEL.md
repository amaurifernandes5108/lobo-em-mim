# 🚀 DEPLOY VIA VS CODE + VERCEL
## Landing "O Lobo em Mim" - Deploy profissional em 10 minutos

---

## 🎯 ESTRATÉGIA

**GitHub (código) → Vercel (hospedagem) → DNS (domínio)**

**Vantagens:**
- ✅ Deploy automático (git push = site atualizado)
- ✅ HTTPS grátis e automático
- ✅ CDN global (site ultra rápido)
- ✅ Zero configuração de servidor
- ✅ Rollback fácil (voltar versões)

---

## 📁 PASSO 1: PREPARAR ARQUIVOS (2 min)

**1. Crie uma pasta no seu PC:**
```
C:\lobo-em-mim\
```

**2. Baixe os 3 arquivos e coloque dentro:**
- `index-CONFIGURADO-COMPLETO.html`
- `O_Lobo_em_Mim.png`
- `Capitulo1_OLoboEmMim.pdf`

**3. Renomeie:**
- `index-CONFIGURADO-COMPLETO.html` → `index.html`

**4. Abra no VS Code:**
- Botão direito na pasta → "Abrir com Code"
- Ou: VS Code → File → Open Folder

---

## 🌐 PASSO 2: GITHUB (3 min)

**1. Acesse:** https://github.com (crie conta se não tiver)

**2. New Repository** (botão verde +)

**3. Preencha:**
- Nome: `lobo-em-mim`
- Descrição: Landing O Lobo em Mim
- Public ✅
- **NÃO** marque "Add README"

**4. Create repository**

**5. DEIXE ESSA ABA ABERTA** (vamos precisar)

---

## 💻 PASSO 3: VS CODE - GIT (3 min)

**No VS Code:**

**1. Abra Terminal:**
- Menu: Terminal → New Terminal
- Ou: Ctrl + `

**2. Cole esses comandos (um por vez):**

```bash
git init
git add .
git commit -m "Landing O Lobo em Mim"
git branch -M main
```

**3. Conecte com GitHub:**

Copie a URL do SEU repositório (está na página do GitHub):
```
https://github.com/SEU_USUARIO/lobo-em-mim.git
```

Cole no terminal (substitua pela sua URL):
```bash
git remote add origin https://github.com/SEU_USUARIO/lobo-em-mim.git
git push -u origin main
```

**4. Login GitHub:**
- Username: seu usuário
- Password: **Personal Access Token** (veja abaixo)

---

### **CRIAR TOKEN GITHUB:**

1. GitHub → Foto perfil (canto) → **Settings**
2. Rolar até embaixo → **Developer settings**
3. **Personal access tokens** → **Tokens (classic)**
4. **Generate new token (classic)**
5. Note: `VS Code Deploy`
6. Marque: ✅ `repo` (marque tudo em repo)
7. **Generate token**
8. **COPIE O TOKEN** (só aparece uma vez!)
9. Use como senha no VS Code

---

## 🚀 PASSO 4: VERCEL DEPLOY (2 min)

**1. Acesse:** https://vercel.com

**2. Sign Up with GitHub** (botão)

**3. Autorize Vercel** (conecta com GitHub)

**4. Import Project** ou **Add New...**

**5. Import Git Repository**

**6. Selecione:** `lobo-em-mim`

**7. Configure Project:**
- Framework Preset: **Other**
- Root Directory: `./`
- Build Command: (deixe vazio)
- Output Directory: (deixe vazio)

**8. Deploy** (botão azul)

**Aguarde 30-60 segundos...**

**9. PRONTO! 🎉**

Você tem uma URL:
```
https://lobo-em-mim-xyz.vercel.app
```

**Clique e teste!** A landing já está no ar.

---

## 🌐 PASSO 5: DOMÍNIO PERSONALIZADO (5 min)

**Na Vercel (Dashboard do projeto):**

**1. Settings → Domains**

**2. Add:**
```
lobo.ministeriopastoramauri.com
```

**3. Vercel vai mostrar instruções DNS:**

Copie os valores (algo como):
```
Type: CNAME
Name: lobo
Value: cname.vercel-dns.com
```

---

**No Hostinger hPanel:**

**1. Menu lateral → Domínios**

**2. Clique em:** `ministeriopastoramauri.com`

**3. Procure:** "Registros DNS" ou "DNS Zone" ou "DNS Records"

**4. Adicionar Novo Registro:**
- Tipo: `CNAME`
- Nome: `lobo`
- Aponta para: `cname.vercel-dns.com` (o valor que Vercel mostrou)
- TTL: `3600` (ou deixe padrão)

**5. Salvar**

**6. Aguardar:** 5-30 minutos (propagação DNS)

---

## 🧪 TESTE FINAL

Após 10-30 minutos:

```
https://lobo.ministeriopastoramauri.com
```

**Deve abrir com:**
- ✅ Cadeado verde (HTTPS)
- ✅ Capa aparecendo
- ✅ Formulário funcionando
- ✅ Ultra rápido (CDN Vercel)

---

## 🔄 ATUALIZAR NO FUTURO

**Para QUALQUER mudança:**

1. Edite arquivo no VS Code
2. Salve (Ctrl+S)
3. Terminal:
   ```bash
   git add .
   git commit -m "Atualização XYZ"
   git push
   ```
4. **Vercel deploya automaticamente em 30s!**

Sem FTP, sem upload manual, sem dor de cabeça.

---

## 📊 MONITORAMENTO

**Vercel Dashboard:**
- Analytics (quantos acessos, de onde)
- Deploy logs (sucesso/erro)
- Performance

**GitHub:**
- Histórico completo
- Rollback (voltar versão anterior)

---

## 🎯 COMPARAÇÃO

| Vercel | Hostinger FTP |
|--------|---------------|
| git push = deploy | Upload manual |
| HTTPS automático | Configurar SSL |
| CDN global | 1 servidor |
| Rollback 1 clique | Backup manual |
| R$ 0 | Incluído hospedagem |

---

## 🚨 TROUBLESHOOTING

**Git not found:**
```
Baixe: https://git-scm.com/downloads
Reinicie VS Code
```

**Authentication failed:**
```
Use Personal Access Token (não senha)
GitHub → Settings → Developer settings
```

**DNS não propaga:**
```
Aguarde 30 min - 48h
Teste: https://dnschecker.org
```

**Vercel deploy failed:**
```
Verifique se index.html está na raiz
git status (ver arquivos commitados)
```

---

## ✅ CHECKLIST

- [ ] Pasta criada com 3 arquivos
- [ ] VS Code aberto na pasta
- [ ] Git inicializado
- [ ] Repositório GitHub criado
- [ ] Código pushed para GitHub
- [ ] Vercel conectada ao GitHub
- [ ] Deploy feito
- [ ] URL Vercel funcionando
- [ ] DNS CNAME configurado no Hostinger
- [ ] Aguardando propagação (10-30 min)
- [ ] Domínio customizado funcionando

---

**VOCÊ ESTÁ A 10 MINUTOS DE TER:**

```
https://lobo.ministeriopastoramauri.com
```

**Rodando em infraestrutura de classe mundial (mesma da Netflix)!** 🐺⚔️
