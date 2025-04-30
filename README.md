# 🛣️ App de Preenchimento de Coordenadas - Rodovias SP

Este aplicativo em Streamlit preenche automaticamente as coordenadas geográficas (`x`, `y`) de ocorrências rodoviárias com base em rodovia e quilômetro. Utiliza uma base interna de geolocalização do estado de São Paulo.

---

## 📥 Como usar

1. Faça upload de uma planilha `.xlsx` contendo as colunas:
   - `Rodovia`: nome da rodovia no padrão DER (ex: `SP 008`, `SPA 099/060`)
   - `km`: valor do quilômetro (inteiro ou decimal com vírgula)

2. O app irá:
   - Pedir para você selecionar a **aba da planilha**
   - Cruzar com a base interna de geolocalização
   - Preencher os campos `x` e `y`
   - Indicar em vermelho os valores preenchidos automaticamente
   - Disponibilizar o download da planilha final

---

## ⚠️ Formato da planilha de entrada

| Rodovia     | km   |
|-------------|------|
| SP 058      | 12,3 |
| SPA 099/060 | 3    |

- Os **nomes das colunas** devem estar **exatamente** como mostrado acima.
- A coluna `km` deve usar vírgula para separação decimal (padrão brasileiro).

---

## 🚀 Publicação no Streamlit Cloud

1. Faça login em [https://streamlit.io/cloud](https://streamlit.io/cloud) com sua conta GitHub
2. Crie um repositório no GitHub com os seguintes arquivos:
   - `app_geolocalizacao_spa.py`
   - `NOVA_BASE_DE_GEOLOCALIZACAO_COM_SPA.xlsx`
   - `requirements.txt`
3. No `Streamlit Cloud`, clique em **“New app”**
4. Escolha:
   - Repositório: `seu-usuario/app-geolocalizacao-sp`
   - Branch: `main`
   - Arquivo: `app_geolocalizacao_spa.py`
5. Clique em **Deploy**

---

## 📦 requirements.txt

Você **deve incluir** este arquivo no repositório com o seguinte conteúdo:


---

## 💻 Rodar localmente (opcional)

Instale as dependências com:

```bash
pip install streamlit pandas openpyxl
streamlit run app_geolocalizacao_spa.py


---

