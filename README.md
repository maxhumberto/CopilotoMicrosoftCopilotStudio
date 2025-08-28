# CopilotoMicrosoftCopilotStudio
Este projeto descreve a criação de um copiloto especializado em viagens internacionais, desenvolvido no Microsoft Copilot Studio. O objetivo principal é fornecer informações detalhadas sobre os requisitos para viagens ao exterior partindo do Brasil, utilizando uma base de dados de exemplo em Excel.

# 🤖 Agente de Viagens DIO — Microsoft Copilot Studio

---

## 🚀 Objetivo
Construir um chatbot inteligente (Copiloto) que:
- Responda perguntas sobre requisitos de viagens internacionais.  
- Utilize dados armazenados em Excel (ex: vistos, vacinas, documentos).  
- Sirva como exemplo prático de uso no Copilot Studio.  

---

## 📂 Pré-requisitos
- Conta no **Microsoft 365** com acesso ao Copilot Studio.  
- **Excel Online** com tabela estruturada (por exemplo: `RequisitosViagem.xlsx`).  
- **Power Automate** (para conectar o Excel ao Copilot).  

---

## 🛠️ Passo a passo

### 1. Criar o ambiente
1. Acesse [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).  
2. Crie um **ambiente Sandbox ou Developer**.  

![Exemplo criação ambiente](./imagens/criacao-ambiente.png)

---

### 2. Criar a base de dados no Excel
1. Abra o Excel Online.  
2. Crie uma tabela com colunas como:  
   - País  
   - Visto Necessário  
   - Vacinas  
   - Documentos  

Exemplo:  

| País         | Visto Necessário | Vacinas         | Documentos              |
|--------------|-----------------|-----------------|-------------------------|
| EUA          | Sim             | Nenhuma         | Passaporte válido       |
| Portugal     | Não             | Febre Amarela   | Passaporte válido       |

Salve o arquivo como **RequisitosViagem.xlsx** no OneDrive ou SharePoint.  

---

### 3. Criar o Copilot no Microsoft Copilot Studio
1. Acesse [Copilot Studio](https://copilotstudio.microsoft.com).  
2. Clique em **Criar Copilot**.  
3. Defina o nome: **Agente de Viagens DIO**.  
4. Configure as boas-vindas, ex:  
   > "Olá! Eu sou o Agente de Viagens da DIO. Pergunte-me sobre requisitos para viajar ao exterior."  

![Exemplo tela Copilot](./imagens/copilot-config.png)

---

### 4. Conectar ao Excel via Power Automate
1. Dentro do Copilot Studio, vá em **Ações → Chamar fluxo Power Automate**.  
2. Crie um fluxo que:  
   - Receba o país informado pelo usuário.  
   - Consulte a tabela no **Excel Online**.  
   - Retorne os requisitos (visto, vacinas, documentos).  

---

### 5. Publicar e testar
1. Publique seu Copilot.  
2. Teste perguntando:  
   - “Quais documentos preciso para viajar para os EUA?”  
   - “Preciso de vacina para ir a Portugal?”  

