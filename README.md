# 🤖 Sistema de Climatização Fuzzy Inteligente

Sistema de controle de ar-condicionado baseado em Lógica Fuzzy com interface web interativa e assistente virtual com IA.

## 📋 Descrição

Este projeto implementa um sistema de controle fuzzy para ar-condicionado que ajusta automaticamente a velocidade do ventilador com base na temperatura e umidade do ambiente. A aplicação inclui:

- **Sistema Fuzzy**: Controle inteligente baseado em regras fuzzy
- **Interface Web**: Dashboard interativo construído com Streamlit
- **Tutor IA**: Assistente virtual powered by Google Gemini para explicar decisões do sistema
- **Visualizações**: Gráficos das funções de pertinência em tempo real

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- scikit-fuzzy
- Streamlit
- Google Generative AI (Gemini)
- NumPy
- Matplotlib

## 📦 Pré-requisitos

### Para Windows

1. **Python 3.8 ou superior**
  
### Para WSL/Linux

1. **Python 3.8 ou superior**
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip python3-venv
   ```

2. **Git** (opcional)
   ```bash
   sudo apt install git
   ```

## 🚀 Instalação e Configuração

### 1. Clone ou baixe o repositório

### 2. Crie um ambiente virtual

**Windows (CMD):**
```cmd
python -m venv venv
venv\Scripts\activate
```

**Windows (PowerShell):**
```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

**WSL/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Configure a API Key do Google Gemini

#### 4.1. Obtenha sua API Key

1. Acesse: https://aistudio.google.com/app/apikey
2. Faça login com sua conta Google
3. Clique em "Create API Key"
4. Copie a chave gerada (formato: `AIza...`)

#### 4.2. Crie o arquivo de secrets

1. Crie a pasta `.streamlit` na raiz do projeto:

**Windows:**
```cmd
mkdir .streamlit
```

**WSL/Linux:**
```bash
mkdir .streamlit
```

2. Crie o arquivo `secrets.toml` dentro da pasta `.streamlit`:

**Windows:**
```cmd
type nul > .streamlit\secrets.toml
notepad .streamlit\secrets.toml
```

**WSL/Linux:**
```bash
nano .streamlit/secrets.toml
```

3. Adicione o seguinte conteúdo (substitua pela sua chave):

```toml
GEMINI_API_KEY = "SUA_CHAVE_AQUI"
```

## ▶️ Como Executar

### 1. Ative o ambiente virtual (se não estiver ativo)

**Windows:**
```cmd
venv\Scripts\activate
```

**WSL/Linux:**
```bash
source venv/bin/activate
```

### 2. Execute a aplicação

```bash
streamlit run app.py
```