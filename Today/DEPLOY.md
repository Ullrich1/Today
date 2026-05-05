# Como publicar o Today como PWA

## Arquivos necessários (todos na mesma pasta)

```
index.html       ← renomeie day-planner.html para isso
manifest.json
sw.js
icon-192.png
icon-512.png
```

---

## Opção A — Netlify (arrasta e solta, 2 minutos)

1. Acesse **https://app.netlify.com/drop**
2. Crie uma pasta no seu computador com os 5 arquivos acima
3. **Arraste a pasta** inteira para a área indicada no site
4. O Netlify gera uma URL pública com HTTPS automaticamente
   → Ex: `https://meu-today.netlify.app`
5. Pronto — abra essa URL no celular e siga o passo "Instalar no celular"

---

## Opção B — GitHub Pages (gratuito e permanente)

1. Crie uma conta em **https://github.com** (se não tiver)
2. Crie um repositório público novo → nome: `today-planner`
3. Faça upload dos 5 arquivos (botão "Add file → Upload files")
4. Vá em **Settings → Pages → Branch: main → Save**
5. URL gerada: `https://seu-usuario.github.io/today-planner`

---

## Instalar no celular

### Android (Chrome)
1. Abra a URL no Chrome
2. Aparece um banner "Adicionar à tela inicial" — toque nele
3. Ou: menu ⋮ → **"Adicionar à tela inicial"**
4. O app abre em tela cheia, sem barra do navegador ✓

### iPhone (Safari)
1. Abra a URL no **Safari** (não Chrome — só Safari suporta PWA no iOS)
2. Toque no ícone de compartilhar **⎙**
3. Role para baixo → **"Adicionar à Tela de Início"**
4. Toque em **Adicionar**
5. O app aparece na tela inicial com o ícone e abre em tela cheia ✓

---

## Funciona offline?

Sim. Depois da primeira visita, o service worker cacheia tudo.
O app funciona sem internet — incluindo fontes.

## Dados ficam salvos?

Sim, em `localStorage` do navegador do celular.
Não sincroniza entre dispositivos (proposital — é local e privado).

---

## Atualizar o app no futuro

Edite os arquivos e faça novo upload/push.
O service worker detecta a mudança e atualiza automaticamente no próximo reload.
