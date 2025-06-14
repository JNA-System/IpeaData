
# 📊 IpeaData

Automação de coleta, tratamento e atualização de dados econômicos e agropecuários utilizando dados públicos do [IpeaData](https://www.ipeadata.gov.br/) e do IBGE.

O projeto possui scripts para ETL (Extração, Transformação e Carga) que geram datasets organizados e dashboards interativos com Streamlit.

---

## 🚀 Funcionalidades

- 🔄 Coleta automática de dados do IpeaData e IBGE.
- 🧠 Tratamento e padronização dos dados (municípios, estados, mesorregiões e microrregiões).
- 📈 Geração de dashboards interativos com Streamlit.
- ⏰ Workflows automatizados com GitHub Actions.
- 💾 Exportação de dados para arquivos CSV.

---

## 🗂️ Estrutura do Projeto

```
├── .github/workflows       # Workflows do GitHub Actions
│   ├── entrar_site.yml     # Acessa e baixa dados do site
│   └── etl_update.yml      # Executa o pipeline de ETL
├── data                    # Pasta onde ficam os dados gerados (CSV)
├── src                     # Scripts principais
│   ├── area colhida        # Scripts de área colhida
│   ├── Despesas            # Scripts de despesas
│   ├── Efetivos            # Dados de efetivo animal
│   ├── Produção            # Scripts de produção agropecuária
│   ├── utils               # Funções auxiliares
│   └── entrar_no_site.py   # Script de automação web para acessar dados
├── app.py                  # Dashboard Streamlit
├── config.yaml             # Configurações gerais
├── requirements.txt        # Dependências do projeto
└── README.md               # Documentação
```

---

## 🧰 Tecnologias utilizadas

- 🐍 Python 3.11
- 📊 Streamlit
- 🌐 Selenium (acesso web automatizado)
- 📦 Pandas, NumPy
- 🔗 Requests, YAML
- 🔧 GitHub Actions (automação)

---

## ⚙️ Instalação e execução local

1. **Clone o repositório:**

```bash
git clone https://github.com/JNA-System/IpeaData.git
cd IpeaData
```

2. **Crie um ambiente virtual (opcional, recomendado):**

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
```

3. **Instale as dependências:**

```bash
pip install -r requirements.txt
```

4. **Execute o dashboard:**

```bash
streamlit run app.py
```

5. O dashboard abrirá automaticamente no navegador padrão.

---

## 🔄 Executar o ETL manualmente

```bash
python src/Efetivos/passo3.py
python src/Produção/passo1.py
python src/Produção/passo3.py
```

---

## 🤖 Workflows automáticos (GitHub Actions)

- **`etl_update.yml`** → Executa o pipeline de ETL periodicamente ou sob demanda.
- **`entrar_site.yml`** → Acessa e baixa dados diretamente do site com browser headless (Selenium).

---

## 🗺️ Fontes de dados

- [IpeaData](https://www.ipeadata.gov.br/)
- [IBGE](https://www.ibge.gov.br/)

---

## 🤝 Contribuição

Contribuições são bem-vindas! Abra uma issue ou envie um pull request.

---

## 📜 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---

## 👨‍💻 Autor

Desenvolvido por [@JNA System](https://github.com/JNA-System) 💻🚀
