# 🎵 A curadoria do Spotify está gerando valor?

> **Projeto 1 — Análise de Dados | Bootcamp Laboratoria**
> Análise de 839 músicas para entender se a curadoria de playlists do Spotify gera valor em streams — e onde estão as oportunidades de melhoria.

---

## 📌 Sobre o projeto

O Spotify lança milhares de músicas por dia e a curadoria de playlists decide quais chegam ao público. Este estudo de caso analisa o impacto real dessas estratégias no volume de reproduções, cruzando dados de três plataformas (Spotify, Apple Music e Deezer) para identificar padrões de sucesso, gêneros subaproveitados e o potencial comercial de catálogos antigos.

**Pergunta central:** Como saber se a curadoria do Spotify está gerando valor de forma consistente?

**Perguntas respondidas:**
1. Músicas em mais playlists têm mais streams?
2. Músicas em múltiplas plataformas têm mais streams?
3. Certos gêneros se destacam em playlists e streams?
4. Streams variam por ano de lançamento?

---

## 🗂️ Estrutura do repositório

```
spotify-analise/
├── 📁 data/
│   └── Sheets_Spotify_Final.xlsx           ← planilha completa (bases originais, limpeza e final)
├── 📁 docs/
│   ├── Ficha_Tecnica_Spotify.pdf           ← documentação técnica completa
│   └── Dashboard_Spotify.pdf               ← versão estática do dashboard
└── README.md
```

---

## 🔗 Dashboard interativo

👉 [Acesse o painel no Looker Studio](https://datastudio.google.com/reporting/233bf2de-1ff9-4c05-8b8d-361d913baf6c)
📄 [Versão PDF estática](docs/Dashboard_Spotify.pdf)

---

## 🛠️ Ferramentas utilizadas

| Ferramenta | Uso |
|---|---|
| Google Sheets | Limpeza, tratamento e modelagem dos dados |
| Looker Studio | Visualização e dashboard interativo |
| Claude & Gemini | Apoio na análise e documentação |

---

## 📋 Etapas do projeto

**1. Coleta**
Importação de duas bases externas via `IMPORTRANGE`: dados do Spotify (839 músicas, 12 colunas) e dados de plataformas concorrentes (Apple Music, Deezer e Shazam).

**2. Limpeza**
- Remoção de 4 registros 100% idênticos (linhas 841–844)
- Padronização de gêneros musicais: `"Disco-pop"` → `"Disco Pop"` / `"Main genre"` → `"Alternative rock"`
- Padronização geográfica: `"USA"` → `"United States"`, `"MX"` → `"Mexico"`
- Tratamento de valores negativos, nulos e strings em colunas numéricas
- Unificação de data de lançamento (ano + mês + dia → campo `DATE`)

**3. Análise**
Correlação entre playlists e streams por plataforma, sumarização por gênero musical e por ano de lançamento, e busca cruzada de desempenho multiplataforma via `XLOOKUP`.

**4. Visualização**
Dashboard no Looker Studio com gráficos de dispersão, barras comparativas e tabela dinâmica por gênero.

---

## 💡 Principais insights

**✅ Curadoria funciona**
Correlação de 0,79 entre playlists e streams — mais playlists equivale diretamente a mais reproduções. The Weeknd: 43.899 playlists → 3,7 bi de streams.

**✅ Multiplataforma reforça o resultado**
Apple Music (0,77) e Deezer (0,60) confirmam o padrão. A consistência entre plataformas indica estratégia, não coincidência.

**⚠️ Oportunidade: Pop punk**
Olivia Rodrigo atingiu 1,89 bi de streams com apenas 15.563 playlists — alto retorno orgânico com baixo investimento de curadoria.

**⚠️ Revisão: New wave**
Tears for Fears: 41.751 playlists → apenas 1,2 bi de streams. Muito esforço de curadoria com retorno abaixo do esperado.

**🕰️ Catálogo antigo ainda gera valor**
1983 (The Police · Rock) e 1985 (Tears for Fears · New wave / Kate Bush · Synth-pop) lideram as médias de streams — clássicos bem curados continuam rentáveis décadas depois.

---

## ✅ Conclusão

**Sim — a curadoria está gerando valor de forma consistente.**
A presença em playlists é o principal motor de streams em todas as plataformas analisadas.

**Recomendações:**
1. Investir mais em curadoria de Pop punk — alto potencial orgânico subaproveitado
2. Revisar estratégia para New wave — muitas playlists sem retorno proporcional
3. Manter curadoria de catálogo antigo — clássicos de 1983 e 1985 continuam gerando retorno
4. Expandir presença multiplataforma — Apple e Deezer amplificam os resultados do Spotify

---

## 📄 Documentação técnica

A ficha técnica completa com dicionário de abas, fórmulas utilizadas e decisões metodológicas está disponível em 📄 [Versão PDF estática](Dashboard_Spotify.pdf).

---

<p align="center">
  Desenvolvido por <strong>Cintia Alves</strong> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/">LinkedIn</a> &nbsp;·&nbsp;
  Bootcamp de Dados/IA — <strong>Laboratoria</strong>
</p>
