[Link do vídeo](https://youtu.be/y3cEBz_s48w)

# 📘 Plano de Experimento – Scoping e Planejamento

## 1. Identificação Básica

### 1.1 Título do experimento
Avaliação do desempenho de modelos de IA na detecção de padrões sazonais de vendas por segmento em uma empresa de arames.

### 1.2 ID / código
**EXP-SAZ-IA-001**

### 1.3 Versão do documento e histórico de revisão
* **Versão Atual:** v1.0
* **Histórico:** Criação inicial em 21/11/2025 (Foco: Identificação e Contexto).

### 1.4 Datas (criação, última atualização)
* **Criação:** 21/11/2025
* **Última atualização:** 21/11/2025

### 1.5 Autores (nome, área, contato)
* **Luiz Felipe** (Engenharia de Software) – `lfcamposdemorais@gmail.com`

### 1.6 Responsável principal (PI / dono do experimento)
Luiz Felipe.

### 1.7 Projeto / produto / iniciativa relacionada
Projeto de Trabalho de Conclusão de Curso (TCC) focado na aplicação de métodos estatísticos e IA para planejamento de estoque e produção no setor metalúrgico.

## 2. Contexto e Problema

### 2.1 Descrição do problema / oportunidade
**Problema:** A empresa não possui um método robusto para identificar e medir a sazonalidade das vendas, resultando em previsões imprecisas e falhas no planejamento de estoque.
**Oportunidade:** Utilizar modelos de IA e estatísticos para detectar padrões sazonais segmentados, melhorando a precisão das previsões.

### 2.2 Contexto organizacional e técnico
* **Organização:** Indústria metalúrgica (fábrica de arames) – cenário simulado.
* **Técnico:** Ambiente de análise de dados (Python, Pandas, Scikit-Learn), processamento de séries temporais históricas.

### 2.3 Trabalhos e evidências prévias (internos e externos)
* **Internos:** Planilhas básicas indicando picos/quedas sazonais, porém sem rigor estatístico.
* **Externos:** Literatura sobre crescimento da previsão de demanda baseada em IA na indústria.

### 2.4 Referencial teórico e empírico essencial
* Conceitos de Séries Temporais (tendência, sazonalidade, estacionariedade).
* Fundamentação de que a IA pode aumentar a precisão ao capturar não-linearidades em comparação a métodos clássicos.

## 3. Objetivos e Questões (Goal / Question / Metric)

### 3.1 Objetivo geral (Goal template)
Avaliar a eficácia de modelos estatísticos e de IA na identificação e previsão da sazonalidade de vendas em múltiplos segmentos de uma empresa de arames.

### 3.2 Objetivos específicos
1.  Identificar se existe sazonalidade significativa em cada segmento.
2.  Avaliar a acurácia dos modelos de previsão.
3.  Comparar o desempenho entre segmentos diferentes.
4.  Medir o impacto da segmentação nos resultados.

### 3.3 Questões de pesquisa / de negócio
* **Q1.1:** Existe sazonalidade estatisticamente significativa?
* **Q2.1:** Os modelos estatísticos superam modelos de IA?
* **Q3.1:** Segmentos possuem diferenças significativas de sazonalidade?
* **Q4.1:** A previsão segmentada é melhor que a previsão agregada?

### 3.4 Métricas associadas (GQM)
* **M1 (Índice de Sazonalidade):** % de repetição anual.
* **M2 (Teste ADF):** Estacionariedade (p-value).
* **M6 (MAE):** Erro Médio Absoluto (unidade da série).
* **M7 (RMSE):** Raiz do Erro Quadrático Médio (unidade da série).
* **M10 (MAPE):** Erro Percentual Absoluto Médio (%).
* **M9 (Teste de Wilcoxon):** Comparação estatística de erros.

## 4. Escopo e Contexto do Experimento

### 4.1 Escopo funcional / de processo (incluído e excluído)
* **Incluído:** Análise de séries temporais, avaliação de modelos (ARIMA, Prophet, Random Forest), análise segmentada.
* **Excluído:** Previsões em tempo real, integração com ERP, otimização logística, dashboards interativos.

### 4.2 Contexto do estudo (tipo de organização, projeto, experiência)
Estudo acadêmico aplicado a um dataset simulado de indústria, executado em ambiente de desenvolvimento (Notebooks).

### 4.3 Premissas
* Dados fornecidos estão corretos.
* Segmentos possuem comportamentos distintos e comparáveis.
* Métricas padronizadas são suficientes para avaliação.

### 4.4 Restrições
* Base de dados limitada ao histórico (Jan/2019 a Dez/2024).
* Sem variáveis externas (ex: inflação, PIB).

### 4.5 Limitações previstas
A generalização dos resultados pode ser limitada por se tratar de dados específicos de uma única empresa/setor.

## 5. Stakeholders e Impacto Esperado

### 5.1 Stakeholders principais
* Equipe de Planejamento e Controle da Produção (PCP) – *Simulado*.
* Orientador Acadêmico / Banca Avaliadora.

### 5.2 Interesses e expectativas dos stakeholders
* **Acadêmico:** Validação da metodologia científica e comparação robusta.
* **Negócio (Simulado):** Redução de erro na previsão para evitar ruptura de estoque ou excesso de produção.

### 5.3 Impactos potenciais no processo / produto
Melhoria na tomada de decisão operacional para compras e produção baseada em dados quantitativos.

## 6. Riscos de Alto Nível, Premissas e Critérios de Sucesso

### 6.1 Riscos de alto nível
* **Vazamento de Dados (Data Leakage):** Modelo aprender com dados futuros.
* **Eventos Exógenos (COVID-19):** Distorção dos padrões de 2020/2021.

### 6.2 Critérios de sucesso globais (go / no-go)
O experimento é um sucesso se for possível rejeitar ou falhar em rejeitar as hipóteses com significância estatística (p < 0.05) e entregar um ranking claro de modelos.

### 6.3 Critérios de parada antecipada
Inconsistência grave nos dados históricos que impeça a convergência dos modelos.

## 7. Modelo Conceitual e Hipóteses

### 7.1 Modelo conceitual do experimento
Entrada (Vendas Históricas) → Processamento (Estatística Clássica vs ML vs Prophet) → Saída (Previsão 2024 + Métricas de Erro).

### 7.2 Hipóteses formais (H0, H1)
* **H1 (IA vs Estatística):** H1 = Modelos de IA têm menor RMSE que estatísticos.
* **H2 (Segmentação):** H1 = Modelagem por segmento tem menor MAPE que agregada.
* **H3 (Sazonalidade):** H1 = Existem diferenças significativas de amplitude sazonal entre segmentos.

### 7.3 Nível de significância e considerações de poder
* **Nível de Significância ($\alpha$):** 0.05 (5%).
* Testes como Wilcoxon e Kruskal-Wallis serão usados para validar as diferenças.

## 8. Variáveis, Fatores, Tratamentos e Objetos de Estudo

### 8.1 Objetos de estudo
Séries temporais de vendas mensais de arames.

### 8.2 Sujeitos / participantes
Não se aplica (estudo baseado em dados, sem participantes humanos).

### 8.3 Variáveis independentes (fatores) e seus níveis
* **Fator A (Técnica):** A1 (Estatístico/ARIMA), A2 (ML/Random Forest), A3 (Híbrido/Prophet).
* **Fator B (Segmento):** B1 (Indústria), B2 (Varejo), B3 (Agro).

### 8.4 Tratamentos (condições experimentais)
Desenho fatorial completo resultando em 9 combinações (ex: E1 = ARIMA + Indústria; E9 = Prophet + Agro).

### 8.5 Variáveis dependentes (respostas)
MAE, RMSE, MAPE, Amplitude Sazonal.

### 8.6 Variáveis de controle / bloqueio
Janela de treinamento (2019-2023) e Horizonte de previsão (12 meses - 2024).

### 8.7 Possíveis variáveis de confusão conhecidas
Impactos da pandemia (2020/21) e mudanças internas de classificação de produtos (maturação).

## 9. Desenho Experimental

### 9.1 Tipo de desenho
Fatorial Completo (3 Técnicas x 3 Segmentos).

### 9.2 Randomização e alocação
Não aplicável para a divisão treino/teste (deve ser temporal). Randomização pode ser usada internamente no Random Forest (bootstrap).

### 9.3 Balanceamento e contrabalanço
Todos os segmentos serão submetidos a todos os modelos.

### 9.4 Número de grupos e sessões
9 execuções experimentais principais.

## 10. População, Sujeitos e Amostragem

### 10.1 População-alvo
Histórico completo de transações de vendas da empresa.

### 10.2 Critérios de inclusão de sujeitos
Registros de vendas válidos e confirmados.

### 10.3 Critérios de exclusão de sujeitos
Devoluções e valores negativos.

### 10.4 Tamanho da amostra planejado
Dados mensais de Jan/2019 a Dez/2024 (72 meses por segmento).

### 10.5 Método de seleção / recrutamento
Amostragem não-probabilística por conveniência (base histórica disponível).

### 10.6 Treinamento e preparação dos sujeitos
*N/A.*

## 11. Instrumentação e Protocolo Operacional

### 11.1 Instrumentos de coleta
Scripts Python para leitura de arquivos `.csv`.

### 11.2 Materiais de suporte
Documentação das bibliotecas (Statsmodels, Prophet, Scikit-Learn).

### 11.3 Procedimento experimental (protocolo)
1. Ingestão e limpeza de dados.
2. Engenharia de features (lags, datas).
3. Treinamento (2019-2023) com GridSearch para ARIMA.
4. Inferência na base de teste (2024).
5. Cálculo e consolidação de métricas.

   ![Fluxograma](fluxograma.png)

### 11.4 Plano de piloto
Análise exploratória inicial (EDA) servirá como piloto para validar a qualidade dos dados.

## 12. Plano de Análise de Dados

### 12.1 Estratégia geral de análise
Comparação direta de erros (Real vs Previsto) na base de teste oculta.

### 12.2 Métodos estatísticos planejados
* Teste de Shapiro-Wilk (Normalidade).
* Teste de Wilcoxon Signed-Rank (Comparação de modelos).
* Teste de Kruskal-Wallis (Comparação de segmentos).

### 12.3 Tratamento de dados faltantes e outliers
Interpolação linear para *missing values* e análise de robustez para outliers (ex: pandemia).

### 12.4 Plano de análise para dados qualitativos
*N/A.*

## 13. Avaliação de Validade

### 13.1 Validade de conclusão
Garantida pelo uso de testes estatísticos formais (p-valor) e métricas robustas (RMSE).

### 13.2 Validade interna
Mitigação de *Data Leakage* através de divisão temporal estrita. Uso de variáveis *dummy* para períodos anômalos.

### 13.3 Validade de constructo
Uso de bibliotecas padrão de mercado para cálculo das métricas, evitando erros de fórmula manual.

### 13.4 Validade externa
Limitada ao contexto específico da empresa parceira; generalização focada na metodologia, não nos hiperparâmetros.

### 13.5 Resumo das principais ameaças e estratégias
* Ameaça: Vazamento de dados → Mitigação: Separação cronológica via código.
* Ameaça: Eventos atípicos → Mitigação: Análise de robustez/dummies.

## 14. Ética, Privacidade e Conformidade

### 14.1 Questões éticas
Uso responsável de dados corporativos (simulados).

### 14.2 Consentimento informado
*N/A (Dados empresariais simulados).*

### 14.3 Privacidade e proteção de dados
Dados anonimizados, sem identificação de clientes finais (foco em vendas agregadas).

### 14.4 Aprovações necessárias
Aprovação do orientador do TCC.

## 15. Recursos, Infraestrutura e Orçamento

### 15.1 Recursos humanos e papéis
1 Pesquisador/Desenvolvedor (Luiz Felipe).

### 15.2 Infraestrutura técnica necessária
Computador com Python 3.9+, Jupyter Notebook e bibliotecas instaladas.

### 15.3 Materiais e insumos
Base de dados histórica (arquivos digitais).

### 15.4 Orçamento e custos estimados
Custo zero (utilização de ferramentas open-source e equipamento próprio).

## 16. Cronograma, Marcos e Riscos Operacionais

### 16.1 Macrocronograma
* Entrega 1 (Planejamento): 21/11/2025.
* Execução e Análise: [Data a definir].

### 16.2 Dependências entre atividades
A fase de modelagem depende da conclusão da limpeza e pré-processamento dos dados.

### 16.3 Riscos operacionais e plano de contingência
Risco de bugs em bibliotecas: Utilizar versões estáveis (LTS).

## 17. Governança do Experimento

### 17.1 Papéis e responsabilidades formais
Luiz Felipe (Execução e Decisão), Orientador (Revisão).

### 17.2 Rites de acompanhamento
Reuniões de orientação periódicas.

### 17.3 Processo de controle de mudanças
Versoamento do código e documentação via GitHub.

## 18. Plano de Documentação e Reprodutibilidade

### 18.1 Repositórios e convenções
GitHub. Convenção de nomes de arquivos clara (ex: `data_raw`, `model_arima`).

### 18.2 Templates e artefatos padrão
Jupyter Notebooks estruturados.

### 18.3 Plano de empacotamento
Arquivo `requirements.txt` para dependências e `README.md` com instruções de execução.

## 19. Plano de Comunicação

### 19.1 Públicos e mensagens-chave
Orientador e Banca: Resultados da comparação e validação das hipóteses.

### 19.2 Canais e frequência
E-mail e reuniões presenciais/remotas conforme demanda.

### 19.3 Pontos de comunicação obrigatórios
Entrega das versões parciais e final do TCC.

## 20. Critérios de Prontidão para Execução (Definition of Ready)

### 20.1 Checklist de prontidão
* [x] Plano definido.
* [ ] Dados brutos recebidos e acessíveis.
* [ ] Ambiente Python configurado.

### 20.2 Aprovações finais
Validação do plano pelo orientador.
