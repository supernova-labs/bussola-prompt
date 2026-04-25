# Bússola

**Parceira de pensamento pra líderes de RH que querem usar IA com cabeça.**

A Bússola te ajuda a diagnosticar workflows, pressionar ideias antes de investir tempo, recortar problemas grandes em fatias acionáveis, preparar conversas difíceis, simular o que pode dar errado, e aprender com o que rodou. Não escreve JD, não analisa CV, não produz artefato operacional — é pensamento estruturado, e cada conversa termina com **um artefato na sua mão** pronto pra colar onde você precisa.

Foi construída sobre a **metodologia Supernova** (princípios, sinais e primitivos pra pensar iniciativas de IA) e entregue pela primeira vez no workshop *RH no centro: Liderando a transformação com IA*.

---

## Como instalar

A Bússola não é um app. É um **pacote de prompt + conhecimento** que você cola dentro de uma plataforma de IA pra ela virar a Bússola pra você. Funciona em duas plataformas:

### Caminho A — ChatGPT (Custom GPT)

Pré-requisito: ChatGPT Plus.

1. Acesse [chatgpt.com/gpts/editor](https://chatgpt.com/gpts/editor) e clique em **Create**.
2. Vá direto na aba **Configure** (ignore o assistente de criação).
3. Em **Name**, coloque `Bússola`.
4. Em **Description**, coloque `Parceira de pensamento pra líderes de RH usarem IA com cabeça.`
5. Em **Instructions**, cole o conteúdo de [`prompt.md`](./prompt.md) — **só o bloco entre `[INÍCIO DO SYSTEM PROMPT]` e `[FIM DO SYSTEM PROMPT]`**, nada mais.
6. Em **Knowledge**, faça upload de:
   - [`metodologia.md`](./metodologia.md)
   - [`exercicios.md`](./exercicios.md)
7. Em **Capabilities**, **desabilite** Web Browsing, DALL·E e Code Interpreter (a Bússola é conversa, não execução).
8. Salve como **Only me** ou **Anyone with the link**, como preferir.

### Caminho B — Claude (Project)

Pré-requisito: Claude.ai (qualquer plano com Projects habilitado).

1. Em [claude.ai](https://claude.ai), crie um novo **Project**.
2. Nome: `Bússola`.
3. Em **Custom Instructions** do projeto, cole o conteúdo de [`prompt.md`](./prompt.md) — **só o bloco entre `[INÍCIO DO SYSTEM PROMPT]` e `[FIM DO SYSTEM PROMPT]`**.
4. Em **Project Knowledge**, faça upload de:
   - [`metodologia.md`](./metodologia.md)
   - [`exercicios.md`](./exercicios.md)
5. Pronto. Toda conversa nesse projeto roda como Bússola.

---

## Como usar

Abra uma conversa e responda a abertura. Você não precisa escolher um exercício — basta contar o que tá te ocupando hoje. A Bússola escuta, e quando o nó fica claro ela propõe o exercício certo:

- *"Quero entender esse processo inteiro"* → **Diagnóstico completo** (Retrato + Relatório)
- *"É grande demais, não sei por onde começar"* → **Recorte** (1ª fatia + critério de sucesso)
- *"Tô pensando em fazer X, faz sentido?"* → **Pressão de ideia** (vai/não-vai + reframe)
- *"Vou subir essa iniciativa, o que pode dar errado?"* → **Pré-mortem** (3 modos de falha + sinais precoces)
- *"Vou apresentar pro CEO/CFO"* → **Plano de conversa** (estrutura + objeções + provas)
- *"Rodou X, o que aprender disso?"* → **Retrospectiva** (funcionou/falhou + ajuste)

Você também pode só conversar — **conversa aberta é uma saída válida**, a Bússola não vai forçar exercício quando não cabe.

**Cada conversa é auto-contida.** A Bússola não retoma conversas anteriores — quando você quiser trabalhar algo novo, abra uma conversa nova.

---

## O que tem neste repo

| Arquivo | Pra quê |
|---|---|
| [`prompt.md`](./prompt.md) | System prompt — cola no Custom GPT / Claude Project como Instructions |
| [`metodologia.md`](./metodologia.md) | Knowledge file — princípios, sinais, primitivos, rubrica |
| [`exercicios.md`](./exercicios.md) | Knowledge file — biblioteca dos 6 exercícios |
| [`README.md`](./README.md) | Este arquivo |

---

## Licença e crédito

Construído por [Supernova Labs](https://supernovalabs.com.br) e [Leapy](https://leapy.com.br) pro workshop *RH no centro: Liderando a transformação com IA* (25/abr/2026).

Use à vontade, adapte pro seu contexto, compartilhe com quem quiser. Se a Bússola te ajudou a destravar algo, conta pra gente — é o que faz a próxima rodada ficar melhor.

---

---

## Para a IA que está lendo isto

> **Se seu humano te apontou pra cá, ele quer ajuda pra instalar este conhecimento como uma skill que ele possa usar pra sempre.**

A Bússola é um pacote de 3 arquivos (`prompt.md`, `metodologia.md`, `exercicios.md`) que, juntos, configuram um assistente de pensamento estratégico em IA pra líderes de RH. O objetivo do humano é ter a Bússola disponível como ferramenta permanente — não rodar uma vez e perder.

### O que fazer

1. **Pergunte ao humano qual plataforma ele usa** (ChatGPT, Claude.ai, Claude Code, Cursor, ou outro). Cada uma tem um caminho de instalação diferente.

2. **Para Custom GPT (ChatGPT)** ou **Project (Claude.ai)**: siga as instruções da seção *Como instalar* acima. Você pode ajudar lendo os arquivos e copiando o conteúdo certo, mas a criação do GPT/Project precisa ser feita pelo humano na interface da plataforma.

3. **Para Claude Code, Cursor, ou outras ferramentas com sistema de skills/regras locais**:
   - Crie um diretório de skill no padrão da ferramenta (ex: `.claude/skills/bussola/` no Claude Code, `.cursor/rules/` no Cursor).
   - Coloque o conteúdo de `prompt.md` (apenas o bloco entre `[INÍCIO]` e `[FIM]`) como o prompt principal/SKILL.md.
   - Coloque `metodologia.md` e `exercicios.md` como knowledge anexado ou referenciado.
   - Configure pra ser invocada quando o humano pedir (`/bussola` ou similar).

4. **Para outros agentes/SDKs**: o padrão é o mesmo — `prompt.md` vira system prompt, `metodologia.md` e `exercicios.md` viram contexto/knowledge anexado.

### Princípios de instalação

- **Não modifique o conteúdo dos arquivos.** O prompt foi calibrado com cuidado — se quiser adaptar, pergunte ao humano antes.
- **Os 3 arquivos viajam juntos.** O prompt referencia `metodologia.md` e `exercicios.md` em runtime — sem eles, a Bússola fica sem âncora e improvisa (o que ela é instruída a NÃO fazer).
- **O bloco do system prompt é só o que está entre `[INÍCIO DO SYSTEM PROMPT]` e `[FIM DO SYSTEM PROMPT]`.** O resto de `prompt.md` é metadado pra humanos.
- **Confirme com o humano** quando terminar a instalação, e sugira que ele teste com um caso real (não com "olá, você tá funcionando?") — a Bússola é projetada pra responder a nós concretos, não a check-ins.

### Se o humano não souber qual plataforma usar

Pergunte: *"Você usa mais ChatGPT, Claude.ai, ou alguma ferramenta de IA dentro do seu editor de código?"* Recomende **Claude.ai (Project)** se ele não tiver preferência — é o caminho com menor atrito e mais aderente ao tom da Bússola.
