# Metodologia — knowledge da Bússola

> **Knowledge file da Bússola v2.** Subset operacional da metodologia Supernova — conteúdo que a skill consulta pra diagnosticar workflows, inferir criticidade, propor ações. Anexada em TODOS os modos (base + evento).
>
> A metodologia completa (substrato intelectual, ladder problem, ROI, hotspots teóricos, conclusões pra RH) mora em `../../conteudo/metodologia.md`. Este arquivo é a destilação operacional.

---

## Modelo mental — 3 camadas

A metodologia Supernova opera em 3 camadas conceituais. Entender a separação é crítico porque cada camada tem papel distinto no fluxo da Bússola:

- **7 sinais de prontidão** → **filtro de ideia** (Comando 1). *"Esse desafio está maduro pra virar iniciativa de IA?"* Filtragem binária pra chegar num recorte que valha o investimento.
- **5 princípios** → **lente de diagnóstico** (Comando 2). *"Que qualidades o processo tem hoje? Quais faltam? E quais importam pra esse caso específico?"* Leitura bidimensional (criticidade × estado).
- **5 primitivos** → **vocabulário de ação** (Comando 3). *"Onde na infraestrutura a gente mexe pra introduzir a qualidade que falta?"* Ferramenta pra desenhar plano concreto.

Princípios respondem *o quê*. Primitivos respondem *onde/como*. Sinais filtram *se vale o investimento agora*.

A Bússola **nunca nomeia** essas categorias pro usuário espontaneamente — usa como lente mental. Regra antijargão ao final.

---

## 7 sinais de prontidão (filtro do C1)

Filtros binários. Se um caso falha em **2 ou mais**, ainda não está pronto pra virar iniciativa de IA.

1. **Contexto articulável** — dá pra escrever o que o projeto é, quem é o cliente, critério de qualidade.
2. **Resultado verificável rápido** — em minutos/horas dá pra dizer se o output serve.
3. **Padrão repetível** — o trabalho volta a acontecer, de forma parecida o bastante pra compensar codificar.
4. **Decisão localizável** — dá pra apontar onde o humano decide e onde só executa.
5. **Erro recuperável** — quando o sistema errar, o custo cabe no aprendizado.
6. **Escopo contido** — caso se resolve sem envolver 5 áreas, 3 sistemas legados, aprovação jurídica. Atenção: "escopo contido" é sobre **contenção** (1–2 áreas), não sobre **granularidade**. Um workflow inteiro end-to-end pode ser contido.
7. **Valor nomeável** — o ganho é articulável em número ou resultado concreto, não promessa futura.

---

## 5 princípios (lente de diagnóstico do C2)

Qualidades que todo sistema humano-IA bem construído precisa ter. A Bússola usa como lente pra diagnosticar **o que o workflow tem e o que falta**.

### Diagnóstico bidimensional

Cada princípio é classificado em duas dimensões:

- **Criticidade pro workflow** (binário): **crítico** (fundamental pra esse caso) ou **não-crítico** (bom ter, não decisivo). É julgamento contextual — inferido pela natureza do workflow. Skill propõe, humano confirma.
- **Estado atual**: sólido / frágil / ausente / parcial / não-diagnosticado.

### Estados — definição geral

- **Sólido** — existe de forma articulada, estável, descentralizada. Fora da cabeça de pessoa específica.
- **Frágil** — existe na prática mas instável. Depende de conhecimento tácito, pessoa específica (*"só a Estela sabe"*), ou varia a cada rodada.
- **Ausente** — não existe nem em forma tácita. Workflow roda por inércia.
- **Parcial** — rubrica não fechou após 2 follow-ups. Info insuficiente apesar da tentativa.
- **Não-diagnosticado** — pessoa acionou escape antes de o princípio ser coberto.

**Desempate**: se não bate 100%, escolha mais próxima e registre ambiguidade na nota.

### Os 5 princípios em detalhe

#### 1. Visão de mundo compartilhada

Contexto do workflow (quem é o cliente, estado atual, histórico, decisões passadas) é acessível ao time.

**Distinção crítica — natureza do conhecimento**:
- **Dinâmico**: lista atualizada de clientes, estado de pipeline, inventário, status de projetos. Muda o tempo todo. Precisa de **ferramenta ativa** (CRM, ERP, dashboard, banco de dados).
- **Relacional**: quem é dono, quem decide, árvore de responsabilidades. Estável mas precisa estar articulado.
- **Estático**: briefing, definição do processo, critério de qualidade. Vive em doc.

**Estados aplicados**:
- **Sólido**: contexto em lugar único acessível, atualizado, alguém novo entende em horas
- **Frágil**: existe mas na cabeça de alguém, fragmentado entre sistemas, desatualizado
- **Ausente**: cada pessoa tem sua versão, nada articulável fora do tácito

#### 2. Codifique pra repetir com qualidade

Método/template/playbook vive em artefato versionado que **acumula** — não evapora com a pessoa que fez.

**Estados aplicados**:
- **Sólido**: template versionado (Notion, Confluence, GitHub), alguém novo aplica em X tempo com apoio
- **Frágil**: existe na prática mas não versionado, varia 10x entre aplicadores
- **Ausente**: cada rodada é artesanal, nada acumula

#### 3. Evolutivo e antifrágil

Erro vira aprendizado que **melhora o artefato**, não repetição da mesma dor.

**Estados aplicados**:
- **Sólido**: loop Force→Friction→Fix ativo — post-mortems voltam pro template, changelog visível
- **Frágil**: há post-mortem informal mas não volta pra doc, mesma dor reaparece em ciclos novos
- **Ausente**: erros não são capturados, cada ciclo redescobre os mesmos problemas

#### 4. Humanos convergem, decisões migram

Humano concentrado nos pontos de decisão; tudo entre decisões é execução scriptável que pode migrar pra agente.

**Estados aplicados**:
- **Sólido**: pontos de decisão nomeados, critério explícito, resto é execução sistematizável
- **Frágil**: decisões concentradas em alguns pontos mas diluídas em outros, decide-executa-decide em loop
- **Ausente**: tudo é decisão a cada passo, nada é automatizável sem perder qualidade

#### 5. Explainable (to a certain point)

Dá pra reconstruir raciocínio de decisão passada. Não cada token, mas o suficiente pra audit e pra pessoa nova entender por quê.

**Estados aplicados**:
- **Sólido**: log de decisões, rationale registrado, audit trail suficiente
- **Frágil**: algumas decisões rastreáveis, outras perdidas — rastro desigual
- **Ausente**: decisões não deixam rastro, inauditável

---

## 5 primitivos (vocabulário de ação do C3)

Categorias de infraestrutura onde a Bússola propõe **ações concretas** pra endereçar princípios frágeis/ausentes. Cada ação tem um primitivo-alvo. **1 ação = 1 primitivo.**

### Purpose — propósito + commitment + responsabilidade

Vai além de "objetivo declarado" — captura o **commitment organizacional real**. Se falta apoio da liderança, se falta budget/tempo, se falta aval formal, Purpose está frouxo, mesmo com objetivo lindamente escrito.

**Ações típicas**:
- Explicitar objetivo do workflow em 1 frase (doc ou wiki)
- Definir goals/indicadores (KPIs mensuráveis — opcional mas ajuda)
- Delimitar início e fim (o que dispara; o que encerra)
- Desenhar árvore de responsabilidades (quem faz o quê em cada ponto)
- Nomear dono do workflow (accountability única)
- **Conseguir sponsorship da liderança** (apoio executivo formal)
- **Alocar budget / tempo de time** (funding real, people capacity)
- **Demonstrar commitment do grupo** (não é só o dono — é o ecossistema envolvido)

### Context — informação, contexto, registros

Onde a informação necessária pra rodar o workflow **vive, atualiza e é acessada**.

**Ações típicas**:
- Criar artefato único de contexto (quando hoje é fragmentado)
- Nomear mantenedor ativo (quem atualiza, com que cadência)
- Definir critério de qualidade do contexto (o que precisa estar ali)
- Registrar decision records ("por que foi decidido X")
- Tornar acessível ao time (permissões, descoberta, link único)
- Estruturar informação antes dispersa em sistemas separados

### Skills — expertise codificada

Método, template, playbook, checklist — **artefato que perdura** e que alguém novo consegue aplicar.

**Ações típicas**:
- Escrever template versionado (Notion, Confluence, GitHub)
- Escrever playbook passo-a-passo
- Criar checklist operacional
- Documentar heurísticas ("como decidir entre X e Y")
- Gravar tutorial/onboarding pra alguém novo
- Codificar critério de "bom output"
- Versionar o artefato (changelog, histórico de mudanças)

### Decisions — governança, autonomia, critério

Quem decide o quê, com que critério, com que rastro, com que escalação.

**Ações típicas**:
- Nomear decisor em cada ponto de decisão
- Escrever critérios explícitos ("passa se X, não passa se Y")
- Definir escalação ("se Z, escale pra W")
- Criar log de decisões (quem, quando, por quê)
- Estabelecer governança (comitê, reuniões, cadência)
- Calibrar autonomia (o que cada papel pode decidir sozinho)
- Separar decisões "one-way door" de "two-way door"

### Tools — ferramentas, integrações, acesso

Instrumentos concretos. Integração entre sistemas. Automação. Conectores. Feedback loops. **Onde o conhecimento dinâmico vive.**

**Ações típicas**:
- Adotar ferramenta única pro workflow (CRM, ERP, sistema de registro)
- Integrar sistemas isolados (API, Zapier, automação)
- Criar loop de verificação rápida (feedback em minutos/horas)
- Acesso unificado ao time (SSO, permissões corretas)
- MCP/conectores pra IA acessar o contexto
- Dashboard/visualização do estado atual
- Automação das partes mecânicas (libera humano pro julgamento)

---

## Matriz princípio → primitivos (onde agir)

Quando um princípio aparece como **crítico-frouxo** (crítico × frágil/ausente) no C2, o C3 propõe ações nos primitivos abaixo. Não é 1:1 — a escolha depende da natureza do conhecimento/decisão em jogo.

### Visão de mundo compartilhada (frouxa)
- **Conhecimento dinâmico** (dados que mudam): **Tools** (adotar CRM/ERP/sistema de registro) + **Context** (artefato único + cadência de atualização)
- **Conhecimento relacional** (responsabilidades, quem-faz-o-quê): **Purpose** (árvore de responsabilidades, dono nomeado)
- **Conhecimento estático** (o que é o projeto): **Context** + **Skills** (doc versionado, wiki)

### Codifique pra repetir (frouxo)
- Primário: **Skills** (template versionado, playbook, checklist)
- Complementar: **Context** (critério de qualidade documentado)
- Se artefato disperso: **Tools** (wiki único — Confluence/Notion/base única)

### Evolutivo e antifrágil (frouxo)
- **Decisions** (log de decisões + post-mortems registrados)
- **Context** (learnings voltam pro artefato)
- **Skills** (versionamento — o template muda com aprendizado, changelog visível)
- **Tools** (sistema que faz captura acontecer — Linear, Notion com reviews)

### Humanos convergem, decisões migram (frouxo)
- Primário: **Decisions** (nomear decisor, critério explícito, escalação)
- **Skills** (codificar o que vira execução automatizável)
- **Tools** (pipeline que automatiza execução, deixando humano só na decisão)

### Explainable (frouxo)
- Primário: **Decisions** (log de decisões, rationale registrado)
- **Context** (decision records estruturados)
- **Tools** (audit trail, logs, sistemas que capturam automaticamente)

---

## Regras de priorização (C3)

1. **Máximo 2 princípios críticos-frouxos** no plano de ação.
2. Ordem: **Ausentes antes de Frágeis** (buraco estrutural > rachadura).
3. **Purpose ausente = sempre crítico #1** quando houver — sem commitment, nada mais sustenta.
4. Número de ações por princípio: **agente escolhe e afina com usuário**. Profundidade é bem-vinda; massante não é. Tipicamente 1–3 ações por princípio, cada uma com primitivo-alvo + primeiro passo concreto.
5. **Skill NUNCA expande espontaneamente** — não invente princípios críticos ou ações além dos 2 recomendados a não ser que a pessoa peça.

---

## Modo de aplicação — análise assimétrica

Tanto os **7 sinais** (C1) quanto o **diagnóstico de princípios** (C2) seguem o mesmo padrão. Esta é a regra central de como a Bússola interage.

### Não é questionário

Não percorra os itens perguntando um por um como checklist. Interrogatório desgasta o sênior e não adiciona valor — pessoa sênior quer ver a skill **pensando**, não coletando dados.

### É análise silenciosa + leitura devolvida

1. **Coleta** — skill absorve o que a pessoa descreveu em linguagem livre. Faz no máximo 1–2 follow-ups amplos se faltar contexto básico.
2. **Classificação silenciosa** — skill classifica mentalmente os 7 sinais (C1) ou os 5 princípios com criticidade + estado (C2).
3. **Leitura em 3 blocos, sempre nessa ordem**:
   - **Afirmativo primeiro** — *"O que torna isso um bom candidato"* (C1) ou *"O que sustenta esse fluxo hoje"* (C2). 2–4 pontos em linguagem direta.
   - **Risco/fragilidade depois** — *"Onde vejo risco"* (C1) ou *"Onde vejo fragilidade ou buraco"* (C2). 1–3 pontos mais críticos com justificativa no contexto.
   - **Reframe obrigatório ao fechar** — 1–2 frases enquadrando riscos/fragilidades como **material de trabalho do plano**, não defeitos. Ex: *"esses pontos não são bloqueios — são o que a gente vai atacar no plano"*. Sem esse reframe, a leitura soa como veredicto.
4. **Pergunta direcionada** — só se faltou info pra classificar. Uma pergunta por vez.
5. **Discussão focada** — só nos pontos frouxos, se a pessoa quiser pressionar.

### Criticidade: skill propõe, humano confirma

No C2 especificamente: skill **infere silenciosamente** a criticidade de cada princípio pela natureza do workflow. Ao devolver a leitura, sinaliza levemente que a criticidade foi um julgamento:
> *"Pelo que você me contou, os pontos que mais pesam pra esse caso são [A] e [B]. Os outros existem mas são secundários pra essa iniciativa. Bate ou você enxerga diferente?"*

Se humano discordar, ajuste criticidade e re-leia.

**Heurísticas de criticidade por natureza do workflow**:
- Produz informação/decisão pontual (CRM, análise) → *visão compartilhada* + *explainable* tendem a ser críticos
- Execução repetida em escala (onboarding, triagem) → *codifique repetir* + *humanos convergem* tendem a ser críticos
- Julgamento de alto impacto (empréstimo, performance review) → *humanos convergem* + *explainable* tendem a ser críticos
- Processo regulamentado (compliance, auditoria) → *explainable* + *antifrágil* tendem a ser críticos
- Processo experimental/iterativo (prototipação) → *antifrágil* tende a ser crítico

### Regra antijargão aplicada

**Nunca use os nomes técnicos dos sinais, princípios ou primitivos pra rotular na leitura.** Linguagem direta, no vocabulário da pessoa. Ex: não diga *"visão compartilhada tá frouxa"*, diga *"os dados dos clientes estão dispersos entre planilha e HubSpot — qualquer análise fica embasada em estimativa"*.

### Régua de decisão — 7 sinais (C1)

Número de sinais frouxos:
- **0** → segue direto pro enunciado.
- **1–2** → pessoa decide (ajusta, segue, ou troca).
- **3–4** → zona de atenção. Skill sugere recorte mais apertado; acata se pessoa insiste.
- **5+** → skill recomenda trocar ou fatiar.

### Régua do C2

Não tem "stop" — análise sempre vira Retrato. Decisão de onde agir fica pro C3.

### Por que esse modo

- **Demonstra valor ao sênior** — ele vê análise, não interrogatório
- **Concentra atenção onde importa** — discussão nos pontos tensos
- **Afirmativo antes de crítico** — preserva energia da conversa
- **Respeita tempo** — sênior quer pensamento estruturado, não checklist

---

## Exemplos-semente de workflows de RH

Usar quando a pessoa não tem workflow claro. **Filtre primeiro** — *"alto volume rotineiro ou raro alta consequência?"* — e ofereça 2–3 do cluster certo. Cada exemplo vem com **criticidades típicas** pra ajudar a skill a inferir rápido no C2.

### Cluster A — Alto volume, rotineiro

**Onboarding de novos funcionários**
- Natureza: volume alto, ciclo recorrente. Coordenação entre RH, gestor, IT, Facilities.
- Criticidades típicas: **codifique repetir (crítico)** · **visão compartilhada (crítico — quem sabe o quê)** · outros não-críticos.

**Escrita de Job Descriptions**
- Natureza: demanda recorrente de gestores, desperdício cumulativo alto.
- Criticidades típicas: **codifique repetir (crítico)** · **visão compartilhada (crítico — o que é a vaga)** · outros não-críticos.

**Triagem de CVs**
- Natureza: funil, volume massivo, critérios no "olho clínico" do sênior.
- Criticidades típicas: **codifique repetir (crítico)** · **humanos convergem (crítico — scriptável vs não)** · **explainable (crítico — evitar viés)** · visão compartilhada não-crítica.

### Cluster B — Raro, alta consequência

**Performance review / ciclo de feedback**
- Natureza: decisão de carreira, semestral/anual, alta consequência.
- Criticidades típicas: **humanos convergem (crítico)** · **codifique repetir (crítico — consistência entre líderes)** · **visão compartilhada (crítico — critérios)** · antifrágil menos.

**Plano de Desenvolvimento Individual (PDI)**
- Natureza: personalizado por pessoa, impacto de longo prazo.
- Criticidades típicas: **visão compartilhada (crítico — skills tácitas + aspiração + gaps)** · **humanos convergem (crítico)** · outros não-críticos.

**People analytics executivo**
- Natureza: inputs pra alocação, reorganização, budget.
- Criticidades típicas: **explainable (crítico)** · **visão compartilhada (crítico — dados das pessoas)** · **humanos convergem (crítico)**.

Se pessoa não se identifica → *"e se pegássemos [X] como rascunho? pensa no seu — onde difere?"*

---

## Regra antijargão

**Nunca use espontaneamente** (nem pra rotular o que a pessoa acabou de descrever):
- Os nomes dos 7 sinais, 5 princípios, 5 primitivos
- Termos técnicos: *case record*, *boundary object*, *hotspot*, *Autonomy Paradox*, *decision record*, *span of control*

Quando a pessoa pede embasamento, traduza em 1–2 frases em linguagem direta e volte pro fluxo. Não vire aula.

Razão: manter a conversa no vocabulário da pessoa. Jargão cria ruído cognitivo sem adicionar compreensão.
