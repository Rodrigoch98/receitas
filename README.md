# 🍰 ReceitaPro — Gestão de Receitas & Precificação

Sistema profissional para cadastro de receitas, controle de preços e cálculo automático de precificação com sincronização em tempo real via Firebase.

## ✨ Funcionalidades

### 📖 Receitas
- Cadastro completo: ingredientes, modo de preparo, rendimento, categoria
- **Importação rápida** — cole texto bruto e o sistema organiza automaticamente
- **Conversão de unidades** — g, kg, ml, L, xícaras, colheres e mais
- Cada receita tem configurações individuais de embalagem, energia e gás

### 💰 Tabela de Preços
- Cadastro de ingredientes com preço, quantidade e unidade
- Cálculo automático do preço por unidade base (R$/g, R$/ml)
- Busca rápida por nome ou marca

### 🧮 Calculadora de Custos
- Custo detalhado por ingrediente
- Energia elétrica e gás por receita
- Embalagem individual por receita
- Margem de lucro configurável (padrão 200%)
- Taxa de maquininha (débito e crédito)
- Preço por unidade

### 🔥 Sincronização em Tempo Real
- Firebase Realtime Database (gratuito)
- Qualquer pessoa com o link vê os mesmos dados
- Atualização instantânea entre dispositivos

---

## 🚀 Como Configurar

### 1. Hospedar no GitHub Pages (Gratuito)
1. Crie um repositório no GitHub
2. Faça upload do `index.html`
3. Vá em **Settings → Pages → Source: main branch**
4. Acesse: `https://seu-usuario.github.io/nome-do-repo`

### 2. Configurar Firebase (Gratuito)
Para que todos vejam os mesmos dados:

1. Acesse [console.firebase.google.com](https://console.firebase.google.com)
2. Clique em **Adicionar projeto** → Dê um nome → Criar
3. No menu lateral, clique em **Criação → Realtime Database**
4. Clique em **Criar banco de dados** → Selecione a região → **Modo de teste** → Ativar
5. Clique na ⚙️ engrenagem → **Configurações do projeto**
6. Role até "Seus aplicativos" → Clique em **</>** (Web)
7. Registre o app com qualquer nome → Copie o bloco `firebaseConfig`
8. No ReceitaPro, vá em **Config** → Cole o config → **Conectar**

**Pronto!** Todos que acessarem o site verão os mesmos dados em tempo real.

> ⚠️ O modo de teste expira em 30 dias. Para manter permanente, vá em Realtime Database → Regras e coloque:
> ```json
> {
>   "rules": {
>     ".read": true,
>     ".write": true
>   }
> }
> ```

---

## 📱 Compatibilidade
- ✅ Celulares (qualquer tamanho)
- ✅ Tablets
- ✅ Computadores (sidebar de navegação)
- ✅ Chrome, Firefox, Safari, Edge

## 💾 Dados
- **Com Firebase**: Dados na nuvem, sincronizados em tempo real
- **Sem Firebase**: Dados locais no navegador (localStorage)
- **Backup**: Exporte/importe JSON a qualquer momento

---

Desenvolvido com 🧡
