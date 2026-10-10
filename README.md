# GeoLog — Plataforma de Telemetria Logística e Persistência Poliglota

Dashboard em Streamlit para a transportadora fictícia LogiTech Express, integrando:

- **SQLite** (`logitech.db`): motoristas e veículos (dados transacionais, com chave estrangeira)
- **MongoDB** (`geolog_db.telemetria`): telemetria GPS/sensores em GeoJSON com índice `2dsphere`

## Funcionalidades

- Busca de veículos por raio (`$near` / `$geoWithin`) com mapa interativo (Folium)
- Visão unificada: join em memória entre SQLite e MongoDB (pandas)
- Dashboard com KPIs e gráficos Plotly
- Bônus: simulador de movimentação em tempo real

## Como executar

```bash
pip install -r requirements.txt
# MongoDB rodando em mongodb://localhost:27017 (ou defina MONGO_URI)
streamlit run geolog_app.py
```

Variáveis opcionais: `MONGO_URI`, `SQLITE_PATH`.

## Entregáveis

- `geolog_app.py` — aplicação
- `GeoLog_Relatorio_Tecnico.pdf` — relatório técnico com diagrama de arquitetura

## Equipe

- [nomes dos integrantes]
#luiz henrique da paz Silva
