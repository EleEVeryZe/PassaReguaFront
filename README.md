# 💸 PassaRegua - Divisor de Despesas em Grupo

PassaRegua é uma aplicação web desenvolvida em Angular que permite aos usuários se conectarem via Google ou Facebook, criarem grupos de pessoas e registrarem despesas compartilhadas. O app divide automaticamente os valores e informa quem deve quanto a quem.

---

## 🚀 Funcionalidades Principais

- Login via **Google** ou **Facebook**
- Criação de **grupos personalizados**
- Adição de **participantes** em grupos
- Registro de **despesas individuais** dentro dos grupos
- Cálculo automático da **divisão igualitária** de despesas
- Exibição clara de **dívidas entre participantes**

---

## 🧠 Como Funciona?

### 1. Autenticação
O usuário deve realizar o login utilizando:
- **Google OAuth**
- **Facebook OAuth**

> Nenhum outro método de login é permitido.

### 2. Grupos
Após autenticação:
- O usuário pode **criar novos grupos**
- Cada grupo contém uma **lista de participantes**

### 3. Participantes
- Os participantes são identificados por nome (ou e-mail, dependendo da implementação do login)
- Não é necessário que todos os participantes estejam cadastrados no app (modo convidado permitido)

### 4. Despesas
- Dentro de cada grupo, o usuário pode adicionar **despesas** com:
  - Quem pagou
  - Descrição (ex: "Jantar")
  - Valor total

Exemplo:  
`Maurício Matheus → Jantar → R$ 100`

### 5. Divisão de Despesas
- O app divide o valor **igualmente entre todos os participantes do grupo**
- A pessoa que pagou tem seu crédito calculado
- Os demais recebem débitos proporcionais

### 6. Cálculo de Dívidas
O app gera um **relatório simples** indicando:
> "João deve R$ 25 para Maurício Matheus"  
> "Ana deve R$ 25 para Maurício Matheus"

---

## 🛠️ Tecnologias Utilizadas

- **Angular 17+**
- **Firebase Auth** (ou outro backend com suporte a OAuth)
- **RxJS** para reatividade
- **Angular Material** para UI
- **Firestore ou Supabase** como backend opcional para persistência

---

## 📁 Estrutura Sugerida do Projeto

src/
├── app/
│ ├── auth/
│ ├── core/
│ ├── groups/
│ ├── expenses/
│ ├── shared/
│ └── app.component.ts
├── assets/
├── environments/
└── index.html


---

## 🔐 Autenticação (OAuth)

Utilize os provedores sociais com suporte nativo:

- Google: [Google Cloud Console](https://console.cloud.google.com/)
- Facebook: [Facebook Developers](https://developers.facebook.com/)

---

## ✅ Requisitos para Rodar o Projeto

- Node.js 18+
- Angular CLI
- Conta configurada no Firebase (ou backend alternativo)
- Chaves de API para Google e Facebook

```bash
npm install 
ng serve
 
