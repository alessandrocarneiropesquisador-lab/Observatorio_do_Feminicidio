# Observatório do Feminicídio: Calculadora de Risco Institucional do Feminicídio (CRIF)
NEVID-UFJF 2026
## 1. Manifesto de Auditoria
O CRIF não é um instrumento de acompanhamento; é uma ferramenta de auditoria forense aplicada à falência do Estado. O projeto visa mapear, via Ciência de Dados, o hiato temporal e substantivo entre a notificação da violência de gênero e o desfecho letal. A premissa central é que a letalidade não é um evento aleatório, mas um subproduto mensurável da omissão institucional e da seletividade penal.

## 2. Metodologia: O Núcleo do CRIF
O sistema opera através de quatro eixos de análise (Ratio Analytics):
- **Ingestão Ontológica:** Extração e estruturação de dados judiciais brutos (acórdãos e sentenças) em matrizes de covariáveis de risco.
- **Análise de Sobrevivência (Regressão de Cox):** Mensuração do tempo até a falência do sistema de proteção (o $T_0$ marcado pelo primeiro acionamento do Estado e o evento de censura à direita definido pelo óbito ou pela persistência da vida).
- **Fluxo de Sankey:** Visualização dos pontos críticos de vazamento e omissão na rede de proteção (SUAS, Delegacias, Ministério Público, Judiciário).
- **Processamento Lexicográfico:** Uso de NLP para desconstrução dos "eufemismos institucionais" e a correlação entre a retórica de decisão judicial e a reincidência de violência.
- Função de risco: \(h(t|X)=h_{0}(t)\times \exp (\beta _{1}X_{1}+\beta _{2}X_{2}+\dots +\beta _{p}X_{p})\)
- O modelo calcula a Função de Risco h(t|X), que representa o risco do evento ocorrer no tempo t, dado um conjunto de variáveis explicativas X
- h₀(t) (Risco Basal): É o risco quando todas as covariáveis são iguais a zero (parte não-paramétrica do modelo
- \(\exp(\beta X)\): É o efeito multiplicativo das variáveis explicativas sobre o risco (parte paramétrica)
- O que é o Hazard Ratio (Razão de Perigos)?O resultado mais importante da Regressão de Cox é o Hazard Ratio (HR), obtido pela exponenciação dos coeficientes (\(\exp(\beta)\)). O HR indica a magnitude do efeito de uma variável sobre o risco do evento
- HR = 1: A variável não tem efeito sobre o risco do evento.HR > 1: A variável aumenta o risco do evento ocorrer mais rapidamente (ex: fumar aumenta a taxa de falha/doença).HR < 1: A variável atua como um fator de proteção, reduzindo o risco do evento acontecer no tempo analisado

## 3. Stack Tecnológico (Stack de Excelência)
* **Engenharia de Dados:** Python (Scrapy, Pandas, Geopandas).
* **Armazenamento:** DuckDB (OLAP local para alta performance) e PostgreSQL.
* **Modelagem Estatística:** R/Python para Regressão de Cox e modelagem de risco.
* **Semântica:** IRAMUTEQ (análise de similitude e CHD). Coeficiênte e co-variáveis 
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
*OBSERVATÓRIO DO FEMINICÍDIO | NEVIDH - UFJF*
