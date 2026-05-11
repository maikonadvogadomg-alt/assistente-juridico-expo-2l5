# Como gerar o APK com EAS

## Passo 1 — Colocar a URL do seu app

Abra o arquivo `App.tsx` e troque a linha:

```
const APP_URL = 'https://SEU-APP.replit.app';
```

Pela URL real do seu app publicado no Replit (ex: `https://assistente-juridico-maikon.replit.app`).

---

## Passo 2 — Instalar dependências

Na pasta `expo-app`, rode:

```bash
npm install
```

---

## Passo 3 — Login no EAS

```bash
npx eas login
```

---

## Passo 4 — Configurar o projeto (só na primeira vez)

```bash
npx eas build:configure
```

Quando perguntar o slug, coloque: `assistente-juridico`

---

## Passo 5 — Gerar o APK

Para gerar APK direto (sem Google Play):

```bash
npx eas build --platform android --profile preview
```

- Vai fazer upload do código para o servidor da Expo
- Leva ~5-10 minutos
- No final aparece um link para baixar o APK
- Instala direto no celular!

---

## Passo 6 — Instalar no celular

1. Baixe o APK pelo link
2. No celular Android: Configurações → Segurança → Fontes desconhecidas → Ativar
3. Abra o APK baixado e instale

---

## Observação importante

O app abre o seu site dentro do celular como app nativo.
Precisa de internet para funcionar (igual WhatsApp Web, Gmail, etc.).
Todas as suas chaves de IA ficam salvas no servidor — não precisa configurar de novo.
