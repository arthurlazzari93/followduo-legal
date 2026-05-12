# Data Safety — Google Play Console (Followduo)

> Respostas prontas para colar no formulário **Data safety** (Seção de Segurança dos Dados) do Google Play Console.
> Última revisão: maio de 2026.

---

## 0. Pré-perguntas (Overview)

| Pergunta | Resposta |
|---|---|
| Your app collects or shares any of the required user data types? | **Yes** |
| All of the user data collected by your app is encrypted in transit? | **Yes** (HTTPS / TLS em todas as chamadas) |
| Do you provide a way for users to request that their data is deleted? | **Yes** (in-app + e-mail `suporte@followduo.app`) |
| Has your app's data collection and security practices been independently validated against a global security standard? | **No** |

---

## 1. Dados coletados / compartilhados

Para cada item: marcar `Collected` (vai pro nosso backend Supabase) e/ou `Shared` (vai para terceiros).
Marcar **Optional** quando o usuário pode usar parte do app sem o dado; **Required** quando o dado é essencial para a funcionalidade central.

### 🔑 Personal info

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| **Email address** | ✅ | ❌ | Required | Account management, App functionality | Login Followduo e contato de suporte. |
| **User IDs** | ✅ | ✅ (RevenueCat, Supabase) | Required | Account management, App functionality, Analytics | UUID interno e IDs públicos das contas Instagram/TikTok conectadas. |
| Name | ❌ | ❌ | — | — | Não coletado. |
| Address | ❌ | ❌ | — | — | Não coletado. |
| Phone number | ❌ | ❌ | — | — | Não coletado. |
| Race / ethnicity | ❌ | ❌ | — | — | Não coletado. |
| Political or religious beliefs | ❌ | ❌ | — | — | Não coletado. |
| Sexual orientation | ❌ | ❌ | — | — | Não coletado. |
| Other info | ❌ | ❌ | — | — | Não coletado. |

### 💳 Financial info

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| Purchase history | ✅ | ✅ (RevenueCat) | Optional | App functionality, Account management | Status da assinatura premium. Não armazenamos cartão. |
| User payment info | ❌ | ❌ | — | — | Processado 100% por Google Play. Não temos acesso. |
| Credit score | ❌ | ❌ | — | — | Não coletado. |
| Other financial info | ❌ | ❌ | — | — | Não coletado. |

### 📍 Location

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| Approximate location | ❌ | ❌ | — | — | Não coletado. |
| Precise location | ❌ | ❌ | — | — | Não coletado. |

### 🩺 Health & fitness

Nada coletado.

### 📬 Messages

Nada coletado. **Não acessamos DMs nem qualquer mensagem.**

### 📷 Photos and videos

Nada coletado. Apenas exibimos a URL de avatar pública retornada pela API do Instagram / TikTok — não baixamos nem armazenamos a imagem.

### 🎙️ Audio files

Nada coletado.

### 📁 Files and docs

Nada coletado.

### 🗓️ Calendar

Nada coletado.

### 👥 Contacts

Nada coletado.

### 📱 App activity

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| App interactions | ✅ | ❌ | Optional | Analytics, App functionality | Telas visitadas, abas abertas, contagem de desbloqueios — usado para diagnosticar bugs e calcular limites diários. |
| In-app search history | ❌ | ❌ | — | — | Não coletado. |
| Installed apps | ❌ | ❌ | — | — | Não coletado. |
| Other user-generated content | ❌ | ❌ | — | — | Não coletado. |
| Other actions | ❌ | ❌ | — | — | Não coletado. |

### 🌐 Web browsing

Nada coletado.

### 📊 App info and performance

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| Crash logs | ✅ | ❌ | Required | App functionality, Analytics | Logs anonimizados de erro. |
| Diagnostics | ✅ | ❌ | Required | App functionality, Analytics | Modelo de device, versão OS, locale. |
| Other app performance data | ❌ | ❌ | — | — | Não coletado. |

### 🔌 Device or other identifiers

| Data type | Collected | Shared | Optional? | Purposes | Justificativa |
|---|---|---|---|---|---|
| Device or other IDs | ✅ | ✅ (Google AdMob) | Optional | Advertising or marketing, Fraud prevention, Analytics | Advertising ID (AAID) para anúncios e Expo Push Token para notificações. |

---

## 2. Resumo — "Why is this data collected?"

Marque os propósitos para cada tipo de dado:

| Dado | App functionality | Analytics | Developer communications | Advertising or marketing | Fraud prevention, security, and compliance | Personalization | Account management |
|---|---|---|---|---|---|---|---|
| Email address | ✅ | — | ✅ | — | ✅ | — | ✅ |
| User IDs | ✅ | ✅ | — | — | ✅ | — | ✅ |
| Purchase history | ✅ | — | — | — | ✅ | — | ✅ |
| App interactions | ✅ | ✅ | — | — | ✅ | — | — |
| Crash logs | ✅ | ✅ | — | — | — | — | — |
| Diagnostics | ✅ | ✅ | — | — | — | — | — |
| Device or other IDs | — | ✅ | — | ✅ | ✅ | — | — |

---

## 3. Práticas de segurança

| Pergunta | Resposta |
|---|---|
| Is your data encrypted in transit? | **Yes** — todas as conexões usam HTTPS/TLS. |
| Do you provide a way for users to request that their data is deleted? | **Yes** — pelo próprio app (Configurações → Desconectar todas as contas → Excluir conta) ou por e-mail para `suporte@followduo.app`. Exclusão completa em até 30 dias. |
| Is your app committed to following the Play Families Policy? | Selecionar conforme classificação etária definida (recomendado: **Not committed** — o app é direcionado a 13+, fora do escopo Families). |
| Has your app's data collection and security practices been independently validated against a global security standard? | **No** |

---

## 4. Compartilhamento com terceiros — checklist

| Terceiro | Dados compartilhados | Finalidade | Link da política |
|---|---|---|---|
| **Supabase** | Email, User IDs, snapshots de seguidores, tokens OAuth criptografados | Backend / Database / Auth | https://supabase.com/privacy |
| **Meta (Instagram Graph API)** | OAuth token (gerado pela própria Meta), leitura de dados da conta autorizada | Acesso aos dados da conta Instagram do usuário | https://www.facebook.com/privacy/policy/ |
| **TikTok for Developers** | OAuth token, leitura de dados da conta autorizada | Acesso aos dados da conta TikTok do usuário | https://www.tiktok.com/legal/privacy-policy |
| **Google AdMob** | Advertising ID (AAID), eventos de anúncio | Exibição de banner / interstitial / rewarded ads (apenas free) | https://policies.google.com/privacy |
| **RevenueCat** | User ID anônimo, status de assinatura, eventos de compra | Gestão de assinaturas | https://www.revenuecat.com/privacy |
| **Google FCM / Apple APNs / Expo Push** | Push token | Entrega de notificações push | https://firebase.google.com/support/privacy / https://expo.dev/privacy |

---

## 5. Dados que **explicitamente NÃO** coletamos

Útil para responder à Play se questionarem:

- Senha do Instagram ou TikTok (usamos OAuth oficial).
- Mensagens diretas (DMs).
- Fotos, vídeos ou stories do dispositivo.
- Localização (aproximada ou precisa).
- Microfone, câmera ou sensores biométricos.
- Lista de contatos da agenda.
- Histórico de navegação web.
- Apps instalados.
- Dados de cartão de crédito (Google Play processa direto).

---

## 6. Links a fornecer no Console

| Campo | URL |
|---|---|
| **Privacy policy URL** | `https://arthurlazzari93.github.io/followduo-legal/privacy-policy.html` |
| **Account deletion URL** | `https://arthurlazzari93.github.io/followduo-legal/privacy-policy.html#secao-8` *(ou criar página dedicada `delete-account.html` futuramente)* |
| **Support email** | `suporte@followduo.app` |

> ⚠️ Substituir `arthurlazzari93` pelo seu usuário GitHub real caso seja diferente.

---

## 7. Texto curto pronto para "Why do you collect/share this data?" (se a Play pedir justificativa por extenso)

```
O Followduo coleta o e-mail do usuário para criar a conta interna; os dados
públicos das contas Instagram e TikTok que o usuário voluntariamente conecta
via OAuth oficial para calcular unfollowers, não-recíprocos, fãs e perfis
inativos; o push token para enviar alertas configuráveis pelo próprio usuário;
o status da assinatura premium (sem dados de cartão) para liberar recursos
pagos; e o identificador de publicidade do Android (AAID) apenas para usuários
do plano gratuito, exclusivamente para a exibição de anúncios pela rede Google
AdMob. Nenhum dado é vendido. Todos os dados podem ser apagados a qualquer
momento dentro do app ou por solicitação ao e-mail suporte@followduo.app.
```
