# Observatório do Feminicídio: Calculadora de Risco Institucional (CRI)
NEVID-UFJF 2026
## 1. Manifesto de Auditoria
O CRI não é um instrumento de acompanhamento; é uma ferramenta de auditoria forense aplicada à falência do Estado. O projeto visa mapear, via Ciência de Dados, o hiato temporal e substantivo entre a notificação da violência de gênero e o desfecho letal. A premissa central é que a letalidade não é um evento aleatório, mas um subproduto mensurável da omissão institucional e da seletividade penal.

## 2. Metodologia: O Núcleo do CRI
O sistema opera através de quatro eixos de análise (Ratio Analytics):
- **Ingestão Ontológica:** Extração e estruturação de dados judiciais brutos (acórdãos e sentenças) em matrizes de covariáveis de risco.
- **Análise de Sobrevivência (Regressão de Cox):** Mensuração do tempo até a falência do sistema de proteção (o $T_0$ marcado pelo primeiro acionamento do Estado e o evento de censura à direita definido pelo óbito ou pela persistência da vida).
- **Fluxo de Sankey:** Visualização dos pontos críticos de vazamento e omissão na rede de proteção (SUAS, Delegacias, Ministério Público, Judiciário).
- **Processamento Lexicográfico:** Uso de NLP para desconstrução dos "eufemismos institucionais" e a correlação entre a retórica de decisão judicial e a reincidência de violência.

## 3. Stack Tecnológico (Stack de Excelência)
* **Engenharia de Dados:** Python (Scrapy, Pandas, Geopandas).
* **Armazenamento:** DuckDB (OLAP local para alta performance) e PostgreSQL.
* **Modelagem Estatística:** R/Python para Regressão de Cox e modelagem de risco.
* **Semântica:** IRAMUTEQ (análise de similitude e CHD).
* **Geoprocessamento:** QGIS/Folium para sobreposição espacial de seletividade operacional.

## 4. O Protocolo de Segurança e Rigor
- **PII (Personally Identifiable Information):** Todos os dados que permitem a identificação de vítimas e agressores são anonimizados e excluídos do pipeline de processamento público.
- **Reprodutibilidade:** O projeto utiliza ambientes virtuais (`venv`) e arquivos de dependências (`requirements.txt`) para garantir a integridade da tese em qualquer ambiente de computação científica.
- **Rigor Matemático:** Ausência de dados resulta em `NULL`. Não haverá inferências generativas em valores faltantes (Missing Values).

## 5. Diretrizes de Desenvolvimento
1. A inércia burocrática não é desculpa para a lentidão.
2. A análise sem evidência quantitativa é puramente especulativa e, portanto, descartável.
3. A estrutura do diretório (`data/`, `scripts/`, `docs/`) deve ser mantida com rigor absoluto para evitar a contaminação do pipeline.

---
*CRI - Calculadora de Risco Institucional | NEVIDH - UFJF*
