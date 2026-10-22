# Documentação do Painel NAG · Agora Tem Especialistas

**Metropolitana I (RJ) · Núcleo de Apoio à Gestão (NAG) · CISBAF**

| | |
|---|---|
| Arquivo | `Painel_NAG_Agora_Tem_Especialistas.html` (arquivo único, abre em qualquer navegador) |
| Publicação | painel-nag.htmly.com.br (acesso com senha) |
| Versão desta documentação | 22/10/2026 |
| Produção coberta | jan/25 a jul/26 (jul/26 ainda recebe aprovações) |
| Saldo do gestor (encontro de contas) | SUS 360º, processamento de 12/09/2026 |
| TABNET SES-RJ | extraído em 20/10/2026 (SIA até jul/26; SIH até ago/26) |
| Totais de referência | 127.029 OCI e 183.652 cirurgias, conferidos com o relatório do Conselho Técnico |

---

## Sumário

1. [Para que serve](#1-para-que-serve)
2. [Como usar](#2-como-usar)
3. [Mapa das páginas](#3-mapa-das-páginas)
4. [Página por página](#4-página-por-página)
5. [Fontes de dados](#5-fontes-de-dados)
6. [Conceitos e regras que valem para todo o painel](#6-conceitos-e-regras-que-valem-para-todo-o-painel)
7. [Indicadores e fórmulas](#7-indicadores-e-fórmulas)
8. [Critérios dos alertas](#8-critérios-dos-alertas)
9. [Pontos a confirmar](#9-pontos-a-confirmar)
10. [Estrutura técnica do arquivo](#10-estrutura-técnica-do-arquivo)
11. [Acesso e LGPD](#11-acesso-e-lgpd)
12. [Histórico de versões](#12-histórico-de-versões)
13. [Como atualizar](#13-como-atualizar)

---

## 1. Para que serve

O Programa Agora Tem Especialistas (Lei nº 15.233/2025) busca encurtar a espera por consulta, exame e cirurgia com especialista. O Ministério da Saúde **adianta o dinheiro**, e os 12 municípios da Metropolitana I **comprovam com atendimentos registrados e aprovados no SUS**.

O painel responde a quatro perguntas, na ordem do menu:

1. **O que foi pactuado?** Metas do PAR e catálogo de OCI.
2. **O que foi produzido?** OCI e cirurgias aprovadas, ritmo e migração.
3. **O que foi pago?** Dinheiro adiantado × comprovado.
4. **Onde se perde?** Alertas e produção que não vira pagamento.

Ele é usado como pauta das visitas do NAG aos municípios e nas apresentações ao Conselho Técnico do CISBAF.

## 2. Como usar

- **Filtro do topo:** escolha o **município** e o período (**De / Até**). O filtro vale para todas as páginas.
- **Clique num mês** do gráfico de evolução para fixar o período nele. Clique de novo para voltar.
- **Clique num município** (num quadro ou numa linha de tabela) para filtrar o painel inteiro. O **×** no filtro ativo desfaz.
- **Passe o mouse** nas barras, pontos e células para ver valores, variação e posição.
- **☾** alterna entre o modo claro e o escuro.
- Cada página tem: **O que mostra / Por que importa**, **Palavras desta página** (glossário) e, no rodapé, **Fontes, normas e regras desta página**.

## 3. Mapa das páginas

| Grupo | Página | Endereço interno | Situação |
|---|---|---|---|
| Comece aqui | Início | `#/inicio` | ativa |
| O que foi pactuado | PAR e metas | `#/pactuado/par` | ativa (financeiro incluído em 22/10/2026) |
| O que foi pactuado | Catálogo de OCI | `#/pactuado/catalogo` | ativa |
| O que foi produzido | Produção de OCI | `#/produzido/oci` | ativa |
| O que foi produzido | Curva de aprendizado | `#/produzido/curva` | ativa |
| O que foi produzido | Cirurgias do programa | `#/produzido/cirurgias` | ativa |
| O que foi produzido | Quais cirurgias entram | `#/produzido/quais` | ativa |
| O que foi produzido | Migração das OCI | `#/produzido/mig_oci` | ativa |
| O que foi produzido | Migração das cirurgias | `#/produzido/mig_cir` | ativa |
| O que foi pago | Encontro de contas | `#/pago/encontro` | ativa |
| O que foi pago | TABNET × SUS 360º | `#/pago/confronto` | ativa |
| Onde se perde | Alertas | `#/perde/alertas` | ativa (competências sem aprovação incluídas em 22/10/2026) |
| Onde se perde | Atendido e não faturado | `#/perde/nao_faturado` | planejada |
| Onde se perde | Potencial de OCI | `#/perde/potencial` | planejada |
| Onde se perde | CNES e habilitação | `#/perde/cnes` | planejada |
| Nota metodológica | Fontes, regras e pendências | `#/nota` | ativa |

## 4. Página por página

### Comece aqui

Apresenta o programa e quatro números-resumo: **OCI aprovadas** (jan/25 a jul/26), **% da meta física do PAR**, **cirurgias do programa** e **adiantamento sem comprovação** (prazo 31/12/2026). Traz os atalhos para cada bloco, o "Como usar" e os avisos "Antes de ler os números".

### O que foi pactuado › PAR e metas

- **O que mostra:** quanto de cada OCI o município pactuou no Plano de Ação Regional e quanto já fez, físico e financeiro, somando desde o início do programa até o mês escolhido.
- **Por que importa:** o PAR é o compromisso do município com o Ministério. A meta vale para o plano inteiro: o que importa é o caminho percorrido até agora, não o mês isolado.
- **Indicadores (cards):** Meta física do PAR · OCI aprovadas até o "Até" · Da meta física cumprida (%) · **Do financeiro consumido (%)** · Pactuadas sem nenhuma aprovação.
- **Quadros:**
  - **Financeiro do PAR × valor consumido por município:** Financeiro do PAR, Valor consumido, % financeiro, Físico pactuado, Aprovado, % físico, Saldo físico, com o total da Metropolitana I. Ordenado pelo % financeiro e clicável para filtrar.
  - **% do financeiro consumido por município e área:** matriz município × área, com cor mais forte quanto maior o percentual.
  - **Financeiro do PAR por OCI:** as mesmas colunas, por área (subtotal) e por OCI, com o valor unitário usado. Tem filtro local de área e respeita o município do filtro do topo.
  - **Meta × realizado por município:** físico, com a contagem de OCI com meta sem produção.
  - **Por área:** meta e realizado acumulado por subgrupo de OCI.
  - **Pactuadas e ainda sem aprovação:** pares município × OCI com meta e zero aprovação.
- **Fontes:** PAR da Metropolitana I (tabela TFísico do NAG); SUS 360º, Painel de OCI; SIGTAP (valor unitário).

### O que foi pactuado › Catálogo de OCI

- **O que mostra:** as 52 OCI vigentes no SIGTAP e, para cada uma, se o município já realizou, se estava no PAR e ainda não saiu, ou se ficou fora do plano.
- **Por que importa:** mostra o que ainda não começou. Uma portaria nova que cria OCI faz a OCI aparecer aqui com zero até o primeiro paciente ser aprovado.
- **Indicadores:** OCI aprovadas no período · Já realizadas · No PAR, sem produção · Fora do PAR.
- **Filtros locais:** Situação e Área.
- **Fontes:** SIGTAP competência 09/2026; SUS 360º, Painel de OCI; PAR.

### O que foi produzido › Produção de OCI

- **O que mostra:** quantas OCI o Ministério aprovou, mês a mês, em cada área do cuidado. Cada quadro tem a sua escala e as 3 colunas cheias são o último trimestre.
- **Por que importa:** só conta o que foi registrado e aprovado no SIA. OCI feita e não registrada não aparece e não comprova o dinheiro recebido.
- **Indicadores:** OCI aprovadas · Média mensal dos 3 últimos meses · Último trimestre × anterior · Valor aprovado no SIA.
- **Fonte:** SUS 360º, Painel de OCI (mês de atendimento, município do estabelecimento). As OCI registradas pelo CMD (carretas e créditos financeiros) ficam fora desta versão.

### O que foi produzido › Curva de aprendizado

- **O que mostra:** como o número de OCI cresceu desde o primeiro mês com aprovação de cada município (M1).
- **Por que importa:** mostra quem já engrenou, quem parou de crescer e quem ainda está começando, sem comparar municípios de tamanhos diferentes pelo total.
- **Indicadores:** Ritmo atual · Ritmo atual ÷ começo · Tendência (3 últimos ÷ 3 anteriores) · Municípios acelerando.
- **Fases (a confirmar):** Começando = até 3 meses de produção; Acelerando = +10% ou mais; Desacelerando = −10% ou mais; Estável = entre os dois; Parado = 2 últimos meses sem OCI.

### O que foi produzido › Cirurgias do programa

- **O que mostra:** quantas cirurgias do programa foram aprovadas por mês, em cada município e por tipo.
- **Por que importa:** as cirurgias não têm meta no PAR, mas usam o mesmo dinheiro das OCI.
- **Indicadores:** Cirurgias aprovadas · Média mensal dos 3 últimos meses · Último trimestre × anterior · Valor aprovado.
- **Fonte:** SUS 360º, Painel de Cirurgias. O sistema de registro (SIH, SIA) vem do TABNET SES-RJ.

### O que foi produzido › Quais cirurgias entram

- **O que mostra:** os tipos de cirurgia feitos, em quais hospitais, e a lista oficial do programa com a forma de registro (AIH ou APAC).
- **Por que importa:** só conta a cirurgia que está na lista oficial e foi registrada do jeito certo.
- **Normas:** Portaria SAES/MS nº 3.245/2025 (alterada pelas nº 4.182/2026 e 4.654/2026).

### O que foi produzido › Migração das OCI e Migração das cirurgias

- **O que mostra:** onde os moradores de cada município foram atendidos ou operados: no próprio município (retenção) ou em outro (migração).
- **Por que importa:** o procedimento conta para quem atendeu e faturou, não para o município de residência. Muita migração indica falta de oferta local.
- **Indicadores:** Moradores atendidos/operados · Retenção · Migração · Não residentes recebidos.
- **Fontes:** TABNET SES-RJ, SIA (OCI, grupo 09) e SIH (AIH eletivas da lista do programa), por residência × atendimento, mês de processamento. As cirurgias por APAC não entram na migração das cirurgias.

### O que foi pago › Encontro de contas

- **O que mostra:** quanto o Ministério adiantou a cada município e quanto já foi comprovado com OCI e cirurgias aprovadas.
- **Por que importa:** o que não for comprovado até **31/12/2026** fica descoberto.
- **Indicadores:** Adiantado pelo Ministério · Comprovado com OCI · Comprovado com cirurgias · Ainda sem comprovação · Ritmo necessário (por mês até dez/26).
- **Quadros:** Adiantado × comprovado por município; O que comprovou: cirurgia ou OCI.
- **Atenção:** é uma **foto do saldo de 12/09/2026**. O filtro de período não se aplica a esta página.

### O que foi pago › TABNET × SUS 360º

- **O que mostra:** os mesmos números contados nas duas fontes oficiais, onde batem, onde diferem e por quê.
- **Por que importa:** os municípios comprovam pelo SUS 360º, mas o TABNET permite conferir cada número e mostra quem foi atendido fora da região.
- **Motivo principal da diferença:** o SUS 360º usa o mês do atendimento e o TABNET usa o mês de processamento. O BPA consolidado não tem município de residência (cerca de 605 mil registros na região).

### Onde se perde › Alertas

- **O que mostra:** uma lista do que pede atenção agora, montada com os dados das outras páginas.
- **Por que importa:** serve de pauta para a visita do NAG ao município.
- **Indicadores:** Alertas · Críticos · De atenção · Municípios com algum alerta.
- **Quadros:**
  - **Quadro por município:** uma coluna por tipo de alerta.
  - **Competências sem OCI aprovada · por município** (novo em 22/10/2026): grade município × mês. O **✕ vermelho** marca a competência sem nenhuma OCI aprovada depois da 1ª aprovação do município, e o **cinza** marca os meses antes da 1ª aprovação. A última coluna conta as competências sem aprovação.
  - **Lista de alertas:** críticos primeiro.

### Onde se perde › páginas planejadas

| Página | Pergunta que vai responder | Fonte | O que falta |
|---|---|---|---|
| Atendido e não faturado | Quantas OCI foram atendidas no e-SUS Regulação e não viraram APAC aprovada? | e-SUS Regulação (BigQuery) × TABNET SIA | Retomar a coleta do e-SUS e definir a regra de casamento solicitação × APAC. Cobre só 8 municípios com acesso do NAG. |
| Potencial de OCI | Quais exames e consultas feitos fora das OCI poderiam ter sido faturados como OCI? | SUS 360º, Panorama Clínico × SIGTAP | Testar a extração do Power BI público do Panorama Clínico. |
| CNES e habilitação | Há profissional sem vínculo, carga horária ou CBO incompatível no estabelecimento que emite a APAC? | CNES (BigQuery) e habilitação 38.01 × TABNET SIA | Conferir o frescor da base de vínculos e definir as regras CBO × procedimento. |

### Nota metodológica

Reúne as fontes, a data de atualização de cada uma, as regras aplicadas, os pontos a confirmar e o aviso de acesso e LGPD (seções 5 a 11 deste documento).

## 5. Fontes de dados

| Fonte | O que traz | Atualização nesta versão | Situação |
|---|---|---|---|
| SUS 360º · Painel de OCI | OCI aprovadas no SIA por estabelecimento, OCI, mês de atendimento e município do paciente | jan/25 a jul/26 | integrada |
| SUS 360º · Painel de Cirurgias | Cirurgias do programa por procedimento, estabelecimento, mês e residência × atendimento | até jul/26 | integrada |
| SUS 360º · Saldo do Gestor | Recursos antecipados, comprovados, saldo e pós-produção por gestor | processamento de 12/09/2026 | integrada |
| TABNET SES-RJ · SIA | Produção ambulatorial do grupo 09 (OCI) por residência × atendimento, mês de processamento | até jul/26, extraído em 20/10/2026 | integrada |
| TABNET SES-RJ · SIH | AIH eletivas da lista do programa por residência × estabelecimento | até ago/26, extraído em 20/10/2026 | integrada |
| SIGTAP | As 52 OCI vigentes (grupo 09) e os procedimentos cirúrgicos (grupo 04) | competência 09/2026 | integrada |
| PAR da Metropolitana I | Meta física por OCI e município (tabela TFísico do NAG) | quando houver reprogramação | integrada |
| IBGE, Censo 2022 | População dos municípios | 2022 | integrada |
| SUS 360º · OCI versão nova (SIA + CMD) | Soma as OCI do CMD (carretas e créditos financeiros) | semanal | pendente (adaptar `sus360_oci.py`) |
| e-SUS Regulação | Solicitações e atendimentos (8 municípios com acesso do NAG) | diária | pendente |
| SUS 360º · Panorama Clínico | Exames e consultas fora das OCI que poderiam entrar como OCI | mensal | pendente |
| CNES | Habilitação 38.01, profissionais, vínculos, carga horária e CBO | mensal | pendente |

Esta versão lê os números já agregados do layout do NAG de 20/10/2026. O próximo passo previsto é ler direto do BigQuery `pmaemonitoramentodashboard`, como no Painel SAMU.

## 6. Conceitos e regras que valem para todo o painel

Estes conceitos são fixos: o layout pode mudar, eles não.

1. **Município** = o município do **estabelecimento que atendeu e faturou**. Nas páginas de migração entra também o de **residência**.
2. **Mês:** o SUS 360º usa o **mês do atendimento** e o TABNET usa o **mês de processamento**. Por isso as duas fontes não batem mês a mês.
3. **Último mês parcial:** jul/26 ainda recebe aprovações tardias. Ele aparece com **\*** e toda variação que o inclui também leva **\***.
4. **Último trimestre** = os 3 meses que terminam no "Até", comparados com os 3 anteriores.
5. **PAR acumulado:** o realizado (físico e financeiro) é **acumulado desde o início da base até o "Até"** e comparado com a **meta do plano inteiro**.
6. **Curva de aprendizado:** cada município começa no **seu** primeiro mês com OCI aprovada (M1), não no primeiro mês do filtro.
7. **Encontro de contas** é uma **foto** do SUS 360º (12/09/2026) e não muda com o período. O prazo é **31/12/2026**.
8. **Só conta o que foi aprovado** (SIA ou SIH). Produção não registrada não comprova o adiantamento.
9. **Procedimentos sem sistema no TABNET** entram como "Outros" em todas as contagens.
10. **Filtro global:** município e período valem para todas as páginas, e clicar em mês ou município filtra o painel inteiro.

## 7. Indicadores e fórmulas

| Indicador | Fórmula | Fonte | Página |
|---|---|---|---|
| % da meta física do PAR | OCI aprovadas acumuladas até o "Até" ÷ meta física do PAR × 100 | SUS 360º OCI; PAR | PAR e metas |
| **Financeiro do PAR** | Σ (meta física da OCI × valor unitário da OCI no PAR) | PAR; SIGTAP | PAR e metas |
| **Valor consumido** | Σ valor aprovado no SIA das OCI, acumulado até o "Até" | SUS 360º OCI | PAR e metas |
| **% do financeiro consumido** | Valor consumido ÷ financeiro do PAR × 100 | idem | PAR e metas |
| Saldo físico | Meta física − OCI aprovadas | PAR; SUS 360º | PAR e metas |
| Pactuadas sem aprovação | Nº de pares município × OCI com meta > 0 e zero aprovação até o "Até" | PAR; SUS 360º | PAR e metas; Alertas |
| Média mensal, 3 últimos meses | Soma dos 3 meses que terminam no "Até" ÷ 3 | SUS 360º | Produção |
| Último trimestre × anterior | (média dos 3 últimos ÷ média dos 3 anteriores) − 1 | SUS 360º | Produção; Curva |
| Retenção | Procedimentos de residentes feitos no próprio município ÷ total de procedimentos de residentes × 100 | TABNET SIA/SIH | Migração |
| Produção ÷ adiantado | (Comprovado com OCI + cirurgias) ÷ recurso antecipado × 100 | SUS 360º Saldo | Encontro de contas |
| Ritmo necessário | Falta comprovar ÷ 5 meses de competência (ago a dez/26) | SUS 360º Saldo | Encontro de contas |
| **Competências sem OCI aprovada** | Nº de meses, entre a 1ª aprovação do município e o "Até", com zero OCI aprovada | SUS 360º OCI | Alertas |

**Valor unitário do PAR:** é o valor da OCI no SIGTAP, **exceto** a OCI 09.03.01.004-6 (avaliação diagnóstica em ortopedia com radiologia e ressonância magnética), que no PAR vale **R$ 360,00** (SIGTAP: R$ 616,76). Com essa regra, Cardiologia, Oftalmologia, Otorrinolaringologia, Saúde da Mulher e Ortopedia batem com o relatório do NAG. A Oncologia está a confirmar (ver seção 9).

## 8. Critérios dos alertas

Critérios propostos, **A CONFIRMAR com o NAG**.

| Alerta | Nível | Critério |
|---|---|---|
| Sem OCI nos 2 últimos meses | Crítico | Nenhuma OCI aprovada nos 2 últimos meses até o "Até" |
| Menos de 20% do adiantamento comprovado | Crítico | Produção ÷ adiantamento < 20% no saldo de 12/09/2026 |
| Queda de OCI acima de 20% no trimestre | Atenção | Média dos 3 últimos meses pelo menos 20% abaixo dos 3 anteriores |
| Queda de cirurgias acima de 20% no trimestre | Atenção | Idem, para cirurgias |
| Meses sem OCI depois de começar | Atenção | Mês com zero OCI depois da 1ª aprovação, sem contar os 2 últimos |
| OCI pactuada sem nenhuma aprovação | Atenção | OCI com meta no PAR e nenhuma aprovação até o "Até" |
| Retenção de cirurgias abaixo de 50% | Atenção | Menos da metade dos moradores operados no próprio município (TABNET SIH) |

O quadro **Competências sem OCI aprovada** mostra **em quais meses** aconteceu cada buraco, incluindo os 2 últimos. Quando o "Até" é jul/26, as quedas podem estar exageradas, porque o mês ainda recebe aprovações. Para conferir, escolha jun/26 no filtro.

## 9. Pontos a confirmar

1. **Valor financeiro do PAR em Oncologia.** O relatório do NAG traz R$ 10.343.337, e meta × SIGTAP dá R$ 19.726.242. As candidatas são as OCI de câncer gástrico (R$ 600,11) e câncer colorretal (R$ 700,63). Enquanto não houver a tabela de valores do PAR, o painel usa o SIGTAP, e o financeiro total fica em **R$ 134,8 mi** contra **R$ 125,5 mi** do relatório. Com os valores da Oncologia, os totais passam a bater.
2. **Vigência do PAR e reprogramação de ginecologia (aditivo).**
3. **Critérios de fases e alertas** (±10% na tendência, 2 meses sem OCI, queda acima de 20%).
4. **Residentes operados:** o Conselho Técnico cita 87.588 pessoas, mas a base agregada só tem cirurgias, não pessoas distintas.
5. **CMD fora da conta:** no Rio e em Duque de Caxias são 2.120 OCI (cerca de 2% da produção), segundo o documento de 18/10/2026.
6. **Nefrologia:** as 6 OCI (Portaria SAES/MS nº 4.940/2026) já constam entre as 52 do catálogo.

## 10. Estrutura técnica do arquivo

- **Formato:** um único arquivo HTML (cerca de 2,5 MB) com a aplicação em React, os gráficos (GSAP e Three.js para os ícones 3D) e **todos os dados embutidos**. Funciona sem internet e sem servidor.
- **Dados:** ficam no objeto `../data/dados.json`, dentro do arquivo. Principais campos:

| Campo | Conteúdo |
|---|---|
| `mun` | Os 12 municípios (a posição na lista é o índice usado nas demais tabelas) |
| `pop` | População por município (IBGE 2022) |
| `cat` | Catálogo das 52 OCI: subgrupo, código, nome, valor SIGTAP e portaria |
| `meta` | PAR: `[município, OCI, meta física]` |
| `oci` | Produção de OCI: `[município, OCI, mês, quantidade aprovada, valor aprovado, estabelecimento]` |
| `cir`, `procs`, `lista` | Cirurgias do programa, procedimentos e lista oficial |
| `est` | Estabelecimentos: CNES, nome e gestão |
| `fluxo`, `ofluxo` | Residência × atendimento (cirurgias e OCI) |
| `ec`, `ec_atual` | Encontro de contas por município e a data do saldo |
| `tsia`, `tsih`, `tsiaapac`, `tsiabpa`, `tproc` | Tabelas do TABNET usadas no confronto |
| `meses` | Competências da base (2025-01 a 2026-07) |
| `info` | Data de geração, origem, período, datas de extração e totais de conferência |

- **Endereços internos:** cada página tem um endereço próprio depois do `#` (ver seção 3), que pode ser usado em links diretos.
- **Hospedagem:** ao publicar no htmly, o serviço inclui sozinho um contador de acessos e um script da Cloudflare. Esses scripts não devem ser salvos dentro do arquivo-fonte.

## 11. Acesso e LGPD

O arquivo traz **só números agregados**, sem dado nominal. Mesmo assim, mostra os 12 municípios para quem o abrir: não há restrição por município em HTML. O acesso de cada secretaria só ao próprio município (RLS) depende do modelo no Power BI Service com login.

- Manter o painel publicado **com senha** (htmly).
- Guardar o arquivo em **repositório privado**.
- **Nunca publicar em link aberto** uma versão que tenha dado nominal do e-SUS ou do CNES.

## 12. Histórico de versões

| Data | Versão | O que mudou |
|---|---|---|
| 20/10/2026 | Layout NAG original | Dez páginas: Comece aqui, Produção de OCI, Catálogo, Curva de aprendizado, Cirurgias do programa, Quais cirurgias entram, Migração das OCI, Migração das cirurgias, TABNET × SUS 360º e Encontro de contas. |
| 21/10/2026 | Painel reformulado | Reorganizado em 5 blocos (pactuado, produzido, pago, onde se perde, nota). Novas páginas: PAR e metas e Alertas. O PAR passou a ser acumulado contra a meta do plano inteiro, e o M1 da curva passou a ser o 1º mês com OCI na base. O quadro "cirúrgico × ambulatorial" foi para o Encontro de contas. Saiu o botão "Modo apresentação". |
| 22/10/2026 | Financeiro do PAR e competências | **PAR e metas:** novo card "Do financeiro consumido"; tabela financeiro × consumido por município; matriz % financeiro por município × área; detalhe financeiro por OCI. O card "Da meta cumprida" passou a se chamar "Da meta física cumprida". **Alertas:** novo quadro "Competências sem OCI aprovada · por município". **Nota metodológica:** regra do valor do PAR (ressonância a R$ 360,00) e pendência da Oncologia. |

## 13. Como atualizar

1. **Novos dados:** atualizar o `dados.json` (produção, saldo, TABNET) e conferir os totais de referência com o relatório do Conselho Técnico antes de publicar.
2. **Mudanças no painel:** manter os conceitos da seção 6. Toda página nova precisa ter "O que mostra / Por que importa", o glossário e as fontes, normas e regras no rodapé.
3. **Esta documentação:** a cada versão, acrescentar uma linha no histórico (seção 12) e atualizar fontes, fórmulas e pendências.
4. **Dicionário do Observatório:** levar os indicadores novos (por exemplo, % do financeiro consumido e competências sem OCI aprovada) para o `Dicionario_de_Dados_Observatorio.xlsx`, abas Variáveis e Indicadores.
