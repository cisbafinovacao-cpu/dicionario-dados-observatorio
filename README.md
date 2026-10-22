# Catálogo e Dicionário de Dados do Observatório Regional de Saúde da Baixada Fluminense

Versão 1.0 – novembro de 2026

Convênio CISBAF/CEPESC nº 01/2023 – Plano de Trabalho 2025–2026, Meta 5 (Governança e integração de dados), Produto 5


## Para que serve

Reúne, em um só lugar, as fontes de dados usadas pelo Observatório nos boletins, programas, relatórios, painéis e apresentações aos gestores, com as variáveis, os indicadores, as chaves de ligação entre bases e os termos técnicos. Serve para que qualquer analista reproduza uma análise e para que os produtos usem as mesmas definições.


## Como está organizado

Catálogo de fontes: uma linha por base de dados, com órgão gestor, forma de acesso, recorte, atualização, chave de ligação e produtos que a utilizam.

Variáveis: campos e códigos usados de cada base, com o tratamento aplicado.

Indicadores: fórmula de cálculo, numerador, denominador, fonte e produto de cada indicador.

Municípios e chaves: códigos IBGE dos 12 municípios consorciados e regras de ligação entre bases.

Painéis: os seis painéis públicos do Observatório e do CISBAF, com endereço, fontes, atualização e páginas.

Glossário: termos técnicos usados nos produtos do Observatório.


## Como atualizar

Cada novo boletim, painel ou relatório deve acrescentar aqui as fontes e variáveis novas. A coluna "Situação" do catálogo indica se a ficha está completa ou se os campos ainda serão detalhados com a equipe responsável pelo sistema. Os dicionários próprios de cada edição são incorporados nas abas correspondentes.


## Produtos de origem desta versão

Boletim Informativo Ano 5, Edições 11 (saneamento por setores censitários), 12 (AVC hiperagudo 2021–2025) e 13 (arboviroses 2021–2025), e Edição 14 (cobertura da tríplice viral D1 e sarampo, 2016–2025); Programa de Atendimento dos Casos de AVC Hiperagudo (v1.0, 2026); Relatório Anual de Atividades da CRUR-BF 2025; apresentações ao Conselho Técnico do CISBAF de outubro de 2026 (regionalização das internações e Agora Tem Especialistas); relatórios de resultados dos cursos da Plataforma NEP CISBAF.


## Sumário

- [Catálogo de fontes](#catálogo-de-fontes) · [CSV](dados/catalogo_de_fontes.csv)
- [Variáveis](#variáveis) · [CSV](dados/variaveis.csv)
- [Indicadores](#indicadores) · [CSV](dados/indicadores.csv)
- [Municípios e chaves](#municípios-e-chaves) · [CSV](dados/municipios_e_chaves.csv)
- [Painéis](#painéis) · [CSV](dados/paineis.csv)
- [Glossário](#glossário) · [CSV](dados/glossario.csv)
- [Planilha original (.xlsx)](Dicionario_de_Dados_Observatorio.xlsx)


## Catálogo de fontes

| Código | Fonte | Órgão gestor | Tipo | Forma de acesso | Unidade de registro | Recorte temporal usado | Atualização | Chave de ligação | Tratamento e observações | Produtos que usam | Situação |
|---|---|---|---|---|---|---|---|---|---|---|---|
| F01 | Censo Demográfico 2022 – Agregados por setores censitários | IBGE | Público | Download de tabelas agregadas no portal do IBGE | Setor censitário (contagens e totais; sem microdados individuais) | 2022 | Decenal | Código do município + código do setor censitário | Base setorial única montada por chaves geográficas padronizadas; universo restrito ao Estado do RJ; setores classificados em CISBAF, RM1 sem CISBAF e RJ fora da RM1. No Boletim 14, a população de 1 ano por município dimensiona os bolsões de baixa cobertura. | Boletim 11 – Saneamento; Boletim 14 – Tríplice viral e sarampo | Documentado |
| F02 | Malha de setores censitários 2022 e malha municipal | IBGE | Público | Download de arquivos geográficos (shapefile) | Polígono de setor / município | 2022 | Por censo / anual (malha municipal) | Código do setor; código IBGE do município | Base cartográfica dos mapas de setores, dos fluxos de migração e dos bolsões de baixa cobertura vacinal (municípios com limite comum), elaborados no QGIS. | Boletim 11 – Saneamento; Apresentação Agora Tem Especialistas / painel NAG; Boletim 14 – Tríplice viral e sarampo | Documentado |
| F03 | SIH/SUS – Sistema de Informações Hospitalares (AIH aprovadas) | Ministério da Saúde / DATASUS; tabulação TabNet SES-RJ (inclui registros via RNDS) | Público | TabNet SES-RJ e DATASUS | Internação (AIH) | 2021–2025 (B12); jan–nov/2025 (AVC); 2023–2025 e jan–jul/2026 (REG) | Mensal | Município de residência e de internação (IBGE 6 dígitos); CNES do estabelecimento | Situação da base registrada em cada produto (ex.: 07/04/2026 no B12; 14/01/2026 no AVC). Defasagem habitual de 6 a 12 meses no processamento. | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo; Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F04 | SIM – Sistema de Informações sobre Mortalidade | Ministério da Saúde / DATASUS | Público | TabNet / DATASUS | Óbito | 2021–2025 | Anual (dados preliminares no ano corrente) | Município de residência (IBGE 6 dígitos) | Usado no indicador de mortalidade por AVC (I60–I64). | Boletim 12 – AVC hiperagudo | Documentado |
| F05 | SINAN – Sistema de Informação de Agravos de Notificação (dengue, chikungunya, Zika; sarampo e rubéola) | Ministério da Saúde / SVSA; SES-RJ | Público | TabNet SES-RJ / DATASUS; microdados preliminares no FTP do DATASUS (arquivo EXANBR de doenças exantemáticas) | Caso notificado | 2021–2025 (arboviroses); 2016–2025 e notificações de 2026 (sarampo) | Semanal (sujeito a revisão) | Município ou UF de residência; semana epidemiológica e ano do 1º sintoma ou do início do exantema | Arboviroses: universo restrito a casos confirmados com critério laboratorial ou clínico-epidemiológico; casos prováveis mantidos só para auditoria. Sarampo: dados preliminares, extraídos por script em 06/10/2026; 2026 analisado à parte da série histórica. | Boletim 13 – Arboviroses; Boletim 14 – Tríplice viral e sarampo | Documentado |
| F06 | SINASC – Sistema de Informações sobre Nascidos Vivos | Ministério da Saúde / DATASUS | Público | TabNet / DATASUS | Nascido vivo | 2024 | Anual | Município de residência da mãe | Base para estimar necessidade de leitos obstétricos e neonatais de alto risco. | Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F07 | Estimativas populacionais por município, idade e sexo (série RIPSA) | SES-RJ, a partir de RIPSA, CGIAE/SVSA/MS e IBGE | Público | TabNet SES-RJ | Município, ano, faixa etária e sexo | 2021–2025 | Anual | Código IBGE do município | Denominador padrão dos indicadores; cada taxa anual usa a população do mesmo ano do numerador (2024: 3.776.246 habitantes nos 12 municípios; 2025: 3.732.925). | Boletim 12 – AVC hiperagudo; Boletim 13 – Arboviroses; Programa AVC Hiperagudo; Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F08 | CNES – Cadastro Nacional de Estabelecimentos de Saúde | Ministério da Saúde / DATASUS | Público | TabNet / DATASUS e painel do NAG | Estabelecimento; leito; equipamento; profissional | Competência de dezembro de cada ano (REG); vigente (NAG) | Mensal | Código CNES; município do estabelecimento | Leitos SUS gerais (cirúrgicos, clínicos, obstétricos e pediátricos), leitos de UTI, tomógrafos, habilitações, esfera administrativa, natureza jurídica e gestão; diagnóstico de profissionais no NAG com dados agregados, sem identificação (LGPD). | Boletim 12 – AVC hiperagudo; Apresentação Regionalização (CT 15/10/2026); Apresentação Agora Tem Especialistas / painel NAG | Documentado |
| F09 | Beneficiários de planos de saúde | ANS | Público | ANS Tabnet | Município | Dezembro de 2025 | Mensal | Código IBGE do município | Percentual da população coberta por plano, usado para estimar a população dependente do SUS. | Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F10 | Cobertura Potencial da Atenção Primária | Ministério da Saúde / e-Gestor APS (tabulado no TabNet SES-RJ) | Público | e-Gestor APS / TabNet SES-RJ | Município | Dezembro de 2023 e de 2025 | Mensal | Código IBGE do município | Cobertura regional ponderada pela população. | Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F11 | Estimativa de incidência de câncer | INCA | Público | Publicação Estimativa 2026 | Estado / capital | 2026 | Bienal/trienal | UF | Base para estimar a necessidade de leitos de oncologia. | Apresentação Regionalização (CT 15/10/2026) | Documentado |
| F12 | Precipitação observada | CEMADEN | Público | Download de dados de pluviômetros | Estação, agregada por município e região | 2021–2025 | Diária/horária, agregada por semana e mês | Município; semana epidemiológica | Séries resumidas como anomalia em relação à mediana da mesma semana epidemiológica. | Boletim 13 – Arboviroses | Documentado |
| F13 | Temperatura do ar (média, máxima e mínima) | Open-Meteo Archive API | Público | API | Município (coordenada), agregado por região | 2018–2025 | Diária, agregada por semana e mês | Município; semana epidemiológica | Mesmo tratamento de anomalia da precipitação. | Boletim 13 – Arboviroses | Documentado |
| F14 | SSO – Sistema de Saúde Online (regulação do SAMU 192) | CISBAF – Central de Regulação de Urgências Regional | Próprio CISBAF | Extração do sistema pela equipe do Observatório | Chamado / ocorrência / atendimento | 2021–2025 (B12); 2025 (CRUR); 2025 (AVC) | Contínua | Número da ocorrência; município; estabelecimento de destino | Rotina de pré-crítica para validar registros e corrigir inconsistências antes da análise; dados tratados conforme a LGPD. Para o Portal SAMU, os dados são carregados do SSO no BigQuery a partir de janeiro de 2024, com data de extração exibida no painel. | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo; Relatório Anual CRUR-BF 2025; Painéis do Observatório (ver aba Painéis) | Documentado por indicador; nomes técnicos dos campos a detalhar com a equipe do sistema |
| F15 | Repasses do Fundo Nacional de Saúde | FNS / Ministério da Saúde | Público | Portal do FNS | Município; componente de financiamento | 2025 | Mensal | Código IBGE do município | Financiamento do componente SAMU 192 por município. | Relatório Anual CRUR-BF 2025 | Documentado |
| F16 | SUS 360º – painel OCI, Saldo Financeiro dos Gestores e Painel de Cirurgias | Ministério da Saúde | Público (acesso de gestor) | Painéis do SUS 360º | Procedimento aprovado; município de atendimento e de residência; estabelecimento | Fev/2025 a jul/2026 (OCI); jan/2025 a jul/2026 (cirurgias) | Mensal (data de processamento registrada, ex.: 12/09/2026) | Município de atendimento × município de residência; CNES | Base do monitoramento do Programa Agora Tem Especialistas na Metropolitana I. | Apresentação Agora Tem Especialistas / painel NAG | Documentado |
| F17 | e-SUS Regulação | Ministério da Saúde / municípios | Público (acesso de gestor) | Integrado ao painel do NAG | Solicitação regulada | Fev/2025 a jul/2026 | Contínua | Município; CNES | Valor informado como atendido, comparado ao valor aprovado no SIA. | Apresentação Agora Tem Especialistas / painel NAG | Documentado |
| F18 | SIA/SUS – Sistema de Informações Ambulatoriais | Ministério da Saúde / DATASUS | Público | Integrado ao painel do NAG | Procedimento ambulatorial aprovado | Fev/2025 a jul/2026 | Mensal | Município; CNES; código SIGTAP | Valor aprovado das OCI. | Apresentação Agora Tem Especialistas / painel NAG | Documentado |
| F19 | Relatório NAG – Núcleo de Apoio à Gestão, Metropolitana I (painel) e painel de migração | CISBAF – Núcleo de Apoio à Gestão | Próprio CISBAF (produto derivado) | Data Studio (13 páginas) e Power BI | Solicitação e procedimento OCI; estabelecimento; município; competência | Fev/2025 em diante | Semanal para municípios com e-SUS Regulação; mensal para os demais (produção do SIA no TabNet) | Município de residência e de atendimento; CNES; código OCI | Municípios agrupados pelo sistema de regulação: e-SUS Regulação (Belford Roxo, Duque de Caxias, Itaguaí, Magé, Mesquita, Seropédica e Nilópolis, esta desde 03/11/2025); sistemas próprios (Japeri, Nova Iguaçu e São João de Meriti); SISREG (Rio de Janeiro e Queimados). Dados do TabNet harmonizados com a nomenclatura do e-SUS. | Apresentação Agora Tem Especialistas / painel NAG; Painéis do Observatório (ver aba Painéis) | Documentado |
| F20 | Plataforma NEP CISBAF (Moodle) | CISBAF – Núcleo de Educação Permanente | Próprio CISBAF | Relatórios do Moodle | Inscrição em curso | Dez/2025 a out/2026 | Por oferta de curso | Curso; aluno (dados pessoais não saem da plataforma) | Inscritos, situação (concluinte, participante, abandono; não iniciado, cursando, concluinte com ou sem certificado nos relatórios de curso), nota final, cargo, tipo de estabelecimento, município onde trabalha, região do RJ, UF e pesquisa de satisfação. | Relatórios de cursos NEP (Produto 2); Painéis do Observatório (ver aba Painéis) | Documentado |
| F21 | Marque Fácil (agendamento de consultas e exames) | CISBAF | Próprio CISBAF | Sistema de agendamento; painel Power BI | Procedimento agendado / realizado | Competências de 2018 a 2023 no painel consolidado | Por competência | Município; procedimento; competência | Procedimentos realizados por ano e município, evolução por competência e faltas e atendimentos por município. | Painéis do Observatório (ver aba Painéis) | Documentado por indicador; nomes técnicos dos campos a detalhar com a equipe do sistema |
| F25 | Opera Fácil (cirurgias eletivas – emenda Opera Adulto/SES) | CISBAF | Próprio CISBAF | Sistema de cirurgias eletivas; painel Power BI | Consulta e cirurgia realizada; recurso financeiro | Vigência da emenda | Contínua | Especialidade; tipo de procedimento (consulta ou cirurgia) | Consultas e cirurgias por especialidade, absenteísmo, execução financeira (emenda recebida, gasto, rendimento e saldo) e edital. | Painéis do Observatório (ver aba Painéis) | Documentado por indicador; nomes técnicos dos campos a detalhar com a equipe do sistema |
| F22 | SI-PNI – Sistema de Informação do Programa Nacional de Imunizações (cobertura) | Ministério da Saúde / DATASUS | Público | TabNet/DATASUS, reextraído por script | Dose registrada (agregado municipal) | 2016–2022 | Mensal | Município de residência (IBGE 6 dígitos) | Cobertura baseada no registro agregado de doses, com população-alvo oficial do SI-PNI. Extração de 06/10/2026. | Boletim 14 – Tríplice viral e sarampo | Documentado |
| F23 | RNDS – Painel de Residência (vacinação) | Ministério da Saúde | Público | Painel web da RNDS | Pessoa vacinada (registro individualizado, validado e deduplicado) | 2023–2025; janeiro a agosto de 2026 (análise preliminar à parte) | Reprocessado diariamente | Município de residência | Ruptura metodológica em 2023 (Nota Técnica nº 84/2026-DPNI/SVSA/MS): 2022 e 2023 não formam série contínua. Extração de corte em 08/10/2026; entre três extrações comparadas, a cobertura estadual de 2025 variou menos de 0,1 ponto percentual. | Boletim 14 – Tríplice viral e sarampo | Documentado |
| F24 | Regiões de saúde do Estado do Rio de Janeiro | SES-RJ | Público | Documento oficial de regionalização + códigos IBGE | Município | Vigente no período do estudo | Quando houver nova regionalização | Código IBGE do município | Organiza os 92 municípios nas nove regiões de saúde; a Metropolitana I é desdobrada em Baixada Fluminense (11 municípios) e município do Rio de Janeiro. | Boletim 14 – Tríplice viral e sarampo | Documentado |

## Variáveis

| Fonte | Variável / código | Descrição | Tipo | Uso e tratamento | Produtos |
|---|---|---|---|---|---|
| F01 | V00508 | Moradores em domicílios particulares permanentes (DPP) ocupados que utilizam rede geral de distribuição de água | Contagem | Numerador do abastecimento de água adequado | Boletim 11 – Saneamento |
| F01 | V00580 | Moradores em DPP com destinação das dejeções em rede geral ou pluvial | Contagem | Parcela 1 do numerador do esgotamento adequado (V00580 + V00581) | Boletim 11 – Saneamento |
| F01 | V00581 | Moradores em DPP com fossa séptica ou fossa filtro ligada à rede | Contagem | Parcela 2 do numerador do esgotamento adequado | Boletim 11 – Saneamento |
| F01 | V00612 | Moradores em DPP com lixo coletado no domicílio por serviço de limpeza | Contagem | Parcela 1 do numerador da coleta de lixo adequada (V00612 + V00613) | Boletim 11 – Saneamento |
| F01 | V00613 | Moradores em DPP com lixo depositado em caçamba de serviço de limpeza | Contagem | Parcela 2 do numerador da coleta de lixo adequada | Boletim 11 – Saneamento |
| F01 | População residente em DPP | Denominador único das medidas de saneamento | Contagem | Percentual só é calculado com denominador positivo; parcela ausente vira zero quando a outra foi observada; ambas ausentes ficam como missing | Boletim 11 – Saneamento |
| F01 | V01006 | População total do setor | Contagem | Denominador dos marcadores de vulnerabilidade | Boletim 11 – Saneamento |
| F01 | V01031 | População de 0 a 4 anos | Contagem | Numerador da proporção de crianças | Boletim 11 – Saneamento |
| F01 | V01040; V01041 | Parcelas etárias de 60 anos ou mais | Contagem | Somadas no numerador da proporção de idosos | Boletim 11 – Saneamento |
| F01 | V00900; V00901 | Pessoas de 15 anos ou mais por condição de alfabetização | Contagem | Base da proporção de analfabetismo (não alfabetizadas sobre o total de 15+) | Boletim 11 – Saneamento |
| F01 | Cor ou raça (preta; parda) | Pessoas por cor ou raça em cinco categorias | Contagem | Pretas + pardas sobre o total = proporção de população negra | Boletim 11 – Saneamento |
| F01 | Renda nominal média mensal do responsável | Rendimento médio do responsável pelo domicílio | Valor (R$) | Transformada por logaritmo natural e padronizada (z-score) | Boletim 11 – Saneamento |
| F03 | Diagnóstico principal (CID-10) | I60, I61, I62, I63, I64 e G45 | Categórica | Seleciona as internações por AVC e AIT | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo |
| F03 | DIAS_PERM | Dias de permanência da internação | Numérica | Soma de dias / total de internações = tempo médio de permanência | Boletim 12 – AVC hiperagudo |
| F03 | Município de residência | Código IBGE de 6 dígitos | Categórica | Base das taxas por habitante e dos fluxos de migração | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo; Apresentação Regionalização (CT 15/10/2026) |
| F03 | Estabelecimento (CNES) | Hospital de internação | Categórica | Distribuição por hospital; cruzamento com esfera e gestão do CNES | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo; Apresentação Regionalização (CT 15/10/2026) |
| F03 | Sexo; faixa etária | Características do paciente | Categórica | Estratificação do perfil das internações | Boletim 12 – AVC hiperagudo |
| F03 | Especialidade / clínica do leito e grupo de alta complexidade | Obstetrícia, clínica médica, cirurgia, pediatria; cardiologia, neurocirurgia, traumato-ortopedia, oncologia | Categórica | Retenção por especialidade e índice de dependência na alta complexidade (parto de alto risco excluído) | Apresentação Regionalização (CT 15/10/2026) |
| F04 | Causa básica (CID-10) | I60 a I64 | Categórica | Numerador da taxa de mortalidade por AVC | Boletim 12 – AVC hiperagudo |
| F05 | Agravo | Dengue, chikungunya, Zika | Categórica | Séries separadas e soma das três arboviroses urbanas (exclui febre amarela e oropouche) | Boletim 13 – Arboviroses |
| F05 | Classificação final; critério de confirmação | Confirmado por critério laboratorial ou clínico-epidemiológico | Categórica | Define o universo analítico de casos confirmados | Boletim 13 – Arboviroses |
| F05 | Ano e semana epidemiológica do 1º sintoma | Dimensão temporal do caso | Data | Agregação anual e semanal | Boletim 13 – Arboviroses |
| F05 | Município de residência | Código IBGE | Categórica | Incidência municipal por 10 mil habitantes | Boletim 13 – Arboviroses |
| F12 | Precipitação | Chuva acumulada (mm) | Numérica | Média, máxima e mínima mensal; anomalia semanal em relação à mediana da mesma SE | Boletim 13 – Arboviroses |
| F13 | Temperatura média, máxima e mínima | Temperatura do ar (°C) | Numérica | Mesmo tratamento da precipitação | Boletim 13 – Arboviroses |
| F14 | Tipo de chamado | Trote, queda/mudo, engano, informação, atendimento primário (APH), atendimento secundário (paciente crítico/vaga zero), transporte inter-hospitalar (TIH) | Categórica | Distribuição mensal e por município; encaminhamentos à regulação médica | Relatório Anual CRUR-BF 2025; Painéis do Observatório (ver aba Painéis) |
| F14 | Grau de risco / gravidade | Classificação feita pelo médico regulador | Categórica | Tempo de atendimento do regulador por grau; perfil por município | Relatório Anual CRUR-BF 2025 |
| F14 | Recurso enviado | USA, USB e outros recursos | Categórica | Tipos de recursos por município | Relatório Anual CRUR-BF 2025 |
| F14 | Conduta médica; remoção | Orientação, envio, remoção ou não | Categórica | Atendimentos com remoção | Relatório Anual CRUR-BF 2025 |
| F14 | Destino e estabelecimento | Hospitalar, não hospitalar, unidade de destino | Categórica | Destinos por município e por estabelecimento | Relatório Anual CRUR-BF 2025; Programa AVC Hiperagudo |
| F14 | Recusa e motivo | Recusa do estabelecimento de destino e justificativa | Categórica | Percentual de recusas por estabelecimento, natureza e motivo | Relatório Anual CRUR-BF 2025 |
| F14 | Natureza do atendimento | Clínica, trauma, cirúrgica, obstétrica, pediátrica, psiquiátrica | Categórica | Agravos mais atendidos e recusados por natureza | Relatório Anual CRUR-BF 2025 |
| F14 | Hipótese diagnóstica | AVC, AIT, déficit neurológico súbito | Categórica | Seleção dos atendimentos de AVC | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo |
| F14 | Marcos de tempo T0 a T7 | Registros de horário do chamado, da regulação, do acionamento, da chegada à cena, da saída da cena e da chegada ao destino | Data/hora | Tempo de resposta total (T5 − T0) e tempo de transporte (T7 − T6) por município | Boletim 12 – AVC hiperagudo; Relatório Anual CRUR-BF 2025 |
| F14 | Dia da semana e hora; faixa etária e sexo | Distribuição temporal e perfil dos pacientes | Categórica | Gráficos de demanda por hora e dia; perfil demográfico | Relatório Anual CRUR-BF 2025 |
| F08 | Leitos SUS gerais | Leitos cirúrgicos, clínicos, obstétricos e pediátricos | Contagem | Razão de leitos por 1.000 habitantes; leitos operados e necessários | Apresentação Regionalização (CT 15/10/2026) |
| F08 | Esfera administrativa; natureza jurídica; gestão | Classificação do estabelecimento | Categórica | Análise por esfera (municipal, estadual, federal, privada contratada) | Apresentação Regionalização (CT 15/10/2026) |
| F08 | Leitos de UTI; tomógrafos; habilitações | Capacidade instalada para AVC | Contagem | Mapeamento da linha de cuidado do AVC | Boletim 12 – AVC hiperagudo |
| F16 | OCI aprovadas | Ofertas de Cuidados Integrados aprovadas por município do estabelecimento executante e de residência | Contagem | Percentual da meta do PAR; média mensal; retenção e migração | Apresentação Agora Tem Especialistas / painel NAG |
| F16 | Cirurgias do programa | Cirurgias do Agora Tem Especialistas por município de atendimento e de residência | Contagem | Ritmo, perfil, migração e encontro de contas | Apresentação Agora Tem Especialistas / painel NAG |
| F16 | Recursos antecipados; produção aprovada | Saldo financeiro dos gestores | Valor (R$) | Percentual comprovado dos recursos; mínimo de 20% em OCI | Apresentação Agora Tem Especialistas / painel NAG |
| F17; F19 | Status da solicitação OCI | Agendamento confirmado, agendamento com falta, atendimento agendado e demais status do e-SUS Regulação | Categórica | Base do absenteísmo, das pessoas beneficiadas e dos quadros por status | Apresentação Agora Tem Especialistas / painel NAG; Painéis do Observatório (ver aba Painéis) |
| F17; F19 | CNS do usuário | Cartão Nacional de Saúde | Identificador | Contagem de pessoas distintas beneficiadas (sem exibição individual) | Painéis do Observatório (ver aba Painéis) |
| F17; F19 | Grupo OCI; código OCI; CID | Especialidade (oftalmologia, ortopedia, cardiologia, ginecologia, oncologia, otorrinolaringologia), código da OCI e CID da solicitação | Categórica | Pactuado x informado; distribuição por CID | Apresentação Agora Tem Especialistas / painel NAG; Painéis do Observatório (ver aba Painéis) |
| F18; F19 | Quantidade apresentada e aprovada; valor aprovado | Produção ambulatorial por local de atendimento | Contagem / valor (R$) | Percentual de aprovação; comparação TabNet x base e-SUS | Apresentação Agora Tem Especialistas / painel NAG; Painéis do Observatório (ver aba Painéis) |
| F17 | Valor informado como atendido | Valor registrado no e-SUS Regulação | Valor (R$) | Comparado ao valor aprovado no SIA para medir perda de faturamento | Apresentação Agora Tem Especialistas / painel NAG |
| F22; F23 | Doses de D1 da tríplice viral | Primeira dose aplicada em residentes (registro de dose no SI-PNI; pessoa vacinada na RNDS) | Contagem | Numerador da cobertura; somado nos agregados regionais | Boletim 14 – Tríplice viral e sarampo |
| F22; F23 | População-alvo | Denominador oficial de cada sistema para a D1 | Contagem | Soma da população-alvo nos agregados regionais | Boletim 14 – Tríplice viral e sarampo |
| F05 | Classificação final (sarampo) | Confirmado, descartado ou em investigação | Categórica | Casos confirmados por residência; notificações de 2026 por situação | Boletim 14 – Tríplice viral e sarampo |
| F05 | Autoctone Mun Res | Infecção no próprio município de residência (Sim = autóctone; Não = importado) | Categórica | Classificação dos casos confirmados de sarampo | Boletim 14 – Tríplice viral e sarampo |
| F05 | Ano de início do exantema; UF de residência | Dimensões de tempo e lugar dos casos de sarampo | Data / categórica | Série 2016–2025 e recorte de 2026 | Boletim 14 – Tríplice viral e sarampo |
| F01 | População de 1 ano (Censo 2022) | Crianças de 1 ano residentes por município | Contagem | Dimensiona a população exposta em cada bolsão de baixa cobertura | Boletim 14 – Tríplice viral e sarampo |
| F20 | Situação do aluno | Não iniciado, cursando, concluinte certificado, concluinte sem certificação | Categórica | Taxa de certificação e de conclusão | Relatórios de cursos NEP (Produto 2) |
| F20 | Nota final | Questionário de 20 questões (0,5 ponto cada), nota mínima 7,0, duas tentativas | Numérica | Aprovação e devolutiva individual | Relatórios de cursos NEP (Produto 2) |
| F20 | UF; categoria profissional; pesquisa de satisfação | Perfil dos participantes e avaliação do curso | Categórica / texto | Alcance territorial e nuvem de palavras | Relatórios de cursos NEP (Produto 2) |

## Indicadores

| Indicador | Numerador / cálculo | Denominador | Unidade | Fontes | Desagregação | Produtos |
|---|---|---|---|---|---|---|
| Saneamento adequado – componente água | Moradores em DPP com rede geral de água (V00508) | População residente em DPP | × 100 | F01 | Setor censitário | Boletim 11 – Saneamento |
| Saneamento adequado – componente esgoto | V00580 + V00581 | População residente em DPP | × 100 | F01 | Setor censitário | Boletim 11 – Saneamento |
| Saneamento adequado – componente lixo | V00612 + V00613 | População residente em DPP | × 100 | F01 | Setor censitário | Boletim 11 – Saneamento |
| Saneamento adequado composto (estrito / flexível) | Média dos três componentes (estrito: só com os três presentes; flexível: média dos disponíveis) | — | 0 a 100 | F01 | Setor censitário | Boletim 11 – Saneamento |
| Índice de vulnerabilidade (sem e com dimensão racial) | Média dos z-scores de crianças 0–4, idosos 60+ e analfabetismo 15+ (com raça: acrescenta proporção de população negra) | — | z-score | F01 | Setor censitário | Boletim 11 – Saneamento |
| Taxa de internação por AVC | Internações por I60–I64 e G45 | População residente | × 100.000 | F03; F07 | Município, ano | Boletim 12 – AVC hiperagudo; Programa AVC Hiperagudo |
| Tempo médio de permanência | Soma de DIAS_PERM | Total de internações | dias | F03 | Município, hospital | Boletim 12 – AVC hiperagudo |
| Taxa de mortalidade por AVC | Óbitos por I60–I64 | População residente | × 100.000 | F04; F07 | Município, ano | Boletim 12 – AVC hiperagudo |
| Tempo médio de resposta total do SAMU | Soma de (T5 − T0) | Número de atendimentos | minutos | F14 | Município | Boletim 12 – AVC hiperagudo; Relatório Anual CRUR-BF 2025 |
| Tempo médio de transporte | Soma de (T7 − T6) | Número de atendimentos com remoção | minutos | F14 | Município | Boletim 12 – AVC hiperagudo; Relatório Anual CRUR-BF 2025 |
| Variação percentual de chamados | Chamados do ano − chamados do ano anterior | Chamados do ano anterior | × 100 | F14 | Região, ano | Relatório Anual CRUR-BF 2025 |
| Percentual por tipo de chamado | Chamados do tipo | Total de chamados do mês ou do município | × 100 | F14 | Mês, município | Relatório Anual CRUR-BF 2025; Painéis do Observatório (ver aba Painéis) |
| Incidência de arboviroses | Casos confirmados no ano | População do mesmo ano | × 10.000 | F05; F07 | Município, ano | Boletim 13 – Arboviroses |
| Correlação por defasagem clima × dengue | Anomalia semanal de precipitação ou temperatura | Casos confirmados nas semanas seguintes (defasagem 0 a 12) | ρ de Spearman | F05; F12; F13 | Região, semana epidemiológica | Boletim 13 – Arboviroses |
| Leitos SUS gerais por habitante | Leitos SUS gerais (CNES, dezembro) | População | × 1.000 | F08; F07 | Município, região | Apresentação Regionalização (CT 15/10/2026) |
| Retenção regional das internações | Internações de residentes realizadas na própria região | Total de internações de residentes | × 100 | F03 | Região, especialidade | Apresentação Regionalização (CT 15/10/2026) |
| Índice de dependência na alta complexidade | Internações de alta complexidade de residentes feitas fora da região | Total de internações de alta complexidade de residentes | × 100 | F03 | Região | Apresentação Regionalização (CT 15/10/2026) |
| Leitos necessários para autossuficiência | Parâmetros da Portaria GM/MS nº 1.631/2015 (taxa de internação, permanência e ocupação de 82%) aplicados à população SUS-dependente | — | leitos | F03; F07; F08; F09 | Região, linha de cuidado | Apresentação Regionalização (CT 15/10/2026) |
| Cobertura potencial da APS regional | Soma da população coberta | População total | × 100 (ponderada pela população) | F10; F07 | Região | Apresentação Regionalização (CT 15/10/2026) |
| Percentual da meta de OCI do PAR | OCI aprovadas | Meta de OCI pactuada no PAR | × 100 | F16 | Município | Apresentação Agora Tem Especialistas / painel NAG |
| Retenção de OCI e de cirurgias no município | Procedimentos de residentes realizados no próprio município | Total de procedimentos de residentes | × 100 | F16; F19 | Município | Apresentação Agora Tem Especialistas / painel NAG |
| Cobertura vacinal municipal da D1 da tríplice viral | Registros válidos de D1 em residentes | População-alvo residente | × 100 (comparação com a meta de 95% sempre pelo valor não arredondado) | F22; F23 | Município, ano | Boletim 14 – Tríplice viral e sarampo |
| Cobertura regional da D1 | Soma das doses dos municípios | Soma das populações-alvo (não é média das coberturas) | × 100 | F22; F23 | Região de saúde, Baixada Fluminense, estado | Boletim 14 – Tríplice viral e sarampo |
| Proporção de municípios abaixo da meta | Municípios com cobertura < 95% | Total de municípios do recorte | × 100 | F22; F23 | Região, ano | Boletim 14 – Tríplice viral e sarampo |
| Persistência abaixo da meta | Anos com cobertura < 95% | Anos completos da fase (7 no SI-PNI, 3 na RNDS, 10 no total) | × 100 | F22; F23 | Região, município, fase | Boletim 14 – Tríplice viral e sarampo |
| Bolsão de baixa cobertura | Dois ou mais municípios com limite comum e cobertura < 95% em todos os anos da fase | — | população de 1 ano exposta | F22; F23; F02; F01 | Fase (2016–2018; 2019; 2020–2022; 2023–2025) | Boletim 14 – Tríplice viral e sarampo |
| Pessoas beneficiadas pelo Agora Tem Especialistas | CNS distintos com status Agendamento Confirmado | — | pessoas | F17; F19 | Município, mês | Painéis do Observatório (ver aba Painéis) |
| Taxa de absenteísmo nas OCI | Pacientes com status Agendamento com Falta | Agendamento Confirmado + Agendamento com Falta + Atendimento Agendado | × 100 | F17; F19 | Município, mês da solicitação | Painéis do Observatório (ver aba Painéis) |
| Percentual de CID por grupo OCI | Quantidade de CID por grupo OCI e status | Total geral de OCI | × 100 | F17; F19 | Município, grupo OCI | Painéis do Observatório (ver aba Painéis) |
| Percentual de aprovação da produção OCI | Quantidade aprovada | Quantidade apresentada | × 100 | F18; F19 | Município, procedimento, mês | Apresentação Agora Tem Especialistas / painel NAG; Painéis do Observatório (ver aba Painéis) |
| Taxa de certificação de curso EAD | Concluintes certificados | Inscritos | × 100 | F20 | Curso | Relatórios de cursos NEP (Produto 2) |
| Adesão às aulas in loco | Profissionais presentes | Profissionais da base | × 100 | Listas de presença | Base SAMU, mês | Relatórios de cursos NEP (Produto 2) |

## Municípios e chaves

| Município consorciado | Código IBGE (7 dígitos) | Código DATASUS (6 dígitos) |
|---|---|---|
| Belford Roxo | 3300456 | 330045 |
| Duque de Caxias | 3301702 | 330170 |
| Itaguaí | 3302007 | 330200 |
| Japeri | 3302270 | 330227 |
| Magé | 3302502 | 330250 |
| Mesquita | 3302858 | 330285 |
| Nilópolis | 3303203 | 330320 |
| Nova Iguaçu | 3303500 | 330350 |
| Paracambi | 3303609 | 330360 |
| Queimados | 3304144 | 330414 |
| São João de Meriti | 3305109 | 330510 |
| Seropédica | 3305554 | 330555 |

Regras de ligação entre bases


O DATASUS (SIH, SIM, SINASC, SINAN, SIA, CNES) usa o código do município com 6 dígitos; o IBGE e a SES-RJ usam 7 dígitos (o 7º é dígito verificador). Para ligar as bases, usar os 6 primeiros dígitos.


Estabelecimentos são ligados pelo código CNES (7 dígitos) entre SIH, SIA, CNES, SUS 360º e e-SUS Regulação.


Setores censitários são ligados pelo código do setor do Censo 2022 entre as tabelas agregadas e a malha.


Análises de fluxo sempre registram os dois municípios: o de residência do paciente e o de atendimento ou do estabelecimento executante.


Recorte territorial padrão do Observatório: os 12 municípios consorciados. O município do Rio de Janeiro entra apenas como comparação, quando indicado no produto.


Toda base extraída registra a data de acesso ou a situação da base, que é citada no produto.


## Painéis

| Painel | Ferramenta | Endereço | Fontes (código) | Atualização | Páginas e indicadores |
|---|---|---|---|---|---|
| Relatório NAG – Núcleo de Apoio à Gestão, Metropolitana I | Data Studio | https://datastudio.google.com/u/0/reporting/611f3a44-9c74-4cf1-b02c-04c253129808/page/G22MF | F16; F17; F18; F08; F19 | Semanal (e-SUS Regulação) e mensal (TabNet) | Monitoramento; Pactuado; Pactuado x Informado; Pessoas beneficiadas; Absenteísmo nas OCI; OCI por CID; CNES habilitados por status; Geolocalização dos estabelecimentos; Quantidade apresentada e executada; Compara TabNet x base e-SUS; CNES habilitações; Etapas do plano de ação; Check list – quadro geral (13 páginas) |
| Relatório Analítico – Portal SAMU CISBAF | Data Studio (base BigQuery) | https://datastudio.google.com/u/0/reporting/a3262ae0-6721-4bd1-a62a-76d6aebbe034/page/p_t3rrx82lkd | F14 | Diária a partir do SSO; período desde janeiro de 2024 | Estrutura: disponibilidade de viatura. Processo: tipos de chamadas, unidades solicitantes de vaga zero, classificação de risco, regulações, saídas de viaturas, envios em conduta médica, tipos de estabelecimentos, destino. Resultado: tempo-resposta. Morbidade: naturezas das urgências. Demográficos: segmento de tempo do chamado e do envio, sexo e idade do paciente. Nota metodológica (Portaria de Consolidação nº 3/2017). |
| Relatório Consolidado Marque Fácil | Power BI | https://app.powerbi.com/view?r=eyJrIjoiODA5MTc2ZjItZDY4Ny00MjIzLWIxZjYtNTY4YzZiZjczODJhIiwidCI6ImU3NjcxOWI5LTA2NjQtNDZkOC04YzVmLWFhMTJlNTcyOTkwMyJ9&pageName=ReportSection9839edde80045e636e88 | F21 | Por competência (2018 a 2023) | Procedimentos realizados por ano e município; evolução por competência; faltas e atendimentos por município (versões para computador e celular) |
| Opera Fácil – Emenda Opera Adulto (SES) | Power BI | https://app.powerbi.com/view?r=eyJrIjoiMWRjYjA4ZTItODczZi00YTA3LThiMDMtNGYzMDE5MDc3YTlmIiwidCI6ImU3NjcxOWI5LTA2NjQtNDZkOC04YzVmLWFhMTJlNTcyOTkwMyJ9 | F25 | Contínua | Home (emenda, gasto, saldo, consultas e cirurgias por especialidade); Procedimentos; Absenteísmo; Financeiro; Edital |
| Estatísticas em Números – NEP (Cursos NEP Plataforma) | Data Studio incorporado no Moodle | https://plataforma.cisbaf.org.br/mod/page/view.php?id=537 | F20 | Periódica | Inscritos por curso; status (concluinte, participante, abandono); cargo; UF; tipo de estabelecimento; município onde trabalha e região do RJ |
| Dashboards de cursos do NEP (2024, 2025 e 2026) e Pesquisa de Satisfação | Power BI incorporado no site de cursos | https://cursosonline.nep.cisbaf.org.br/dashRelBi.html | F20 | Por oferta de curso | Painéis anuais por curso e resultados da pesquisa de satisfação |

## Glossário

| Termo | Definição |
|---|---|
| AIH | Autorização de Internação Hospitalar, registro de cada internação no SIH. |
| AIT | Ataque isquêmico transitório (CID-10 G45). |
| Alta complexidade | Internações em cardiologia, neurocirurgia, traumato-ortopedia e oncologia, conforme recorte do Observatório; exclui parto de alto risco. |
| APH / atendimento primário | Atendimento do SAMU a chamado de domicílio ou via pública. |
| Atendimento secundário (paciente crítico / vaga zero) | Atendimento a chamado de um serviço de saúde sem a capacidade técnica exigida pelo caso. |
| D1 | Primeira dose da vacina tríplice viral (sarampo, caxumba e rubéola). |
| DPP | Domicílio particular permanente, unidade do Censo usada no denominador do saneamento. |
| Defasagem (lag) | Número de semanas entre a condição meteorológica e os casos comparados. |
| Índice de dependência | Parcela das internações de residentes feitas fora da região. |
| Migração / retenção | Internação ou procedimento feito fora (migração) ou dentro (retenção) do município ou região de residência. |
| NAG | Núcleo de Apoio à Gestão da Região Metropolitana I, do CISBAF. |
| OCI | Oferta de Cuidados Integrados, conjunto de procedimentos ambulatoriais do Programa Agora Tem Especialistas. |
| PAR | Plano de Ação Regional da Metropolitana I no Agora Tem Especialistas. |
| Persistência | Percentual de anos de uma fase em que a cobertura ficou abaixo da meta de 95%. |
| PMAE | Programa Mais Acesso a Especialistas, atual Agora Tem Especialistas. |
| Pré-crítica | Rotina de validação e correção de inconsistências dos registros antes da análise. |
| Ruptura metodológica | Mudança de fonte e de regra de cálculo (SI-PNI para RNDS, em 2023) que impede ler dois períodos como série contínua. |
| RIPSA | Rede Interagencial de Informações para a Saúde; origem da série populacional padrão. |
| Semana epidemiológica (SE) | Semana padronizada de domingo a sábado usada pela vigilância. |
| TIH | Transporte inter-hospitalar de paciente com leito já regulado. |
| Versão estrita / flexível | Estrita: indicador composto só com todos os componentes presentes. Flexível: média dos componentes disponíveis. |
| z-score | Valor padronizado: (valor − média) / desvio-padrão no universo estadual. |
