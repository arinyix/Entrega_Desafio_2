# Desafio 2 — Índice de Adoção e Letramento em IA do IEG

Projeto desenvolvido para a disciplina de **Introdução à Ciência de Dados** da Universidade Federal do Oeste do Pará (UFOPA), Instituto de Engenharia e Geociências (IEG).

## Objetivo do Desafio 2

Construir e revisar um instrumento de coleta para medir, entre discentes do IEG:

- frequência e formas de adoção de inteligência artificial;
- proficiência teórica em IA tradicional e aprendizado de máquina;
- uso prático de IA generativa e LLMs;
- capacidade de verificar respostas, códigos e referências produzidos por IA;
- postura ética, transparência e proteção de dados;
- dependência cognitiva e autoimagem acadêmica relacionada ao uso de IA.

A atividade integra psicologia cognitiva e ciência de dados para reduzir problemas de medição causados por enquadramento, ancoragem, desejabilidade social, ambiguidades linguísticas e fadiga cognitiva.

Os entregáveis definidos pelo professor são:

1. **Dicionário de variáveis:** relação entre perguntas, variáveis, tipos de dados, codificações e hipóteses analíticas.
2. **Instrumento estruturado:** questionário com lógica condicional, validações de consistência e duração estimada inferior a sete minutos.
3. **Pipeline de teste com LLMs:** script ou prompt estruturado para simular personas sintéticas e identificar problemas antes do envio a participantes reais.

## Integrantes do grupo

- **Ana Clara Lages Maia**
- **Jullian Silva Gemaque**
- **Maria de Fatima Mota da Silva**
- **Matheus Calderaro Maciel**
- **Rayssa de Sousa Simões**

## Responsabilidade de cada integrante

| Integrante | Responsabilidade | Atividades principais |
|---|---|---|
| **Jullian Silva Gemaque** | Coordenação e estrutura do formulário | Definir dimensões, organizar seções, ordenar perguntas, configurar fluxos e integrar o trabalho do grupo. |
| **Ana Clara Lages Maia** | Proficiência teórica e IA tradicional | Elaborar questões situacionais sobre estatística, algoritmos clássicos, aprendizado supervisionado, métricas e compreensão conceitual de IA. |
| **Matheus Calderaro Maciel** | IA generativa, LLMs e uso prático | Elaborar questões sobre ferramentas, chatbots, copilots, APIs, frameworks, validação de respostas e identificação de erros produzidos por IA. |
| **Rayssa de Sousa Simões** | Ética, vieses e dependência cognitiva | Elaborar questões sobre transparência, autoria, privacidade, uso ético e dependência; revisar desejabilidade social, enquadramento e perguntas tendenciosas. |
| **Maria de Fatima Mota da Silva** | Dicionário de variáveis e teste com LLMs | Classificar variáveis, definir codificações e hipóteses, criar personas, executar o prompt de teste e consolidar ambiguidades e erros de fluxo. |

## Conteúdo dos arquivos

| Arquivo | Finalidade |
|---|---|
| `RELATORIO_DESAFIO_2_SBC_ABNT.docx` | Relatório principal em formato de artigo, com identidade visual da UFOPA, estrutura SBC, elementos ABNT, resultados, limitações e apêndices. |
| `DICIONARIO_VARIAVEIS_FINAL.csv` | Dicionário operacional com 48 variáveis ou derivações, tipos de dados, codificação, ausências e hipóteses. |
| `PROMPT_TESTE_LLM.txt` | Prompt estruturado que implementa o pipeline solicitado pelo professor. |
| `PERSONAS_SINTETICAS.csv` | Dez personas usadas para testar perfis, saltos, alternativas e coerência do questionário. |
| `RESULTADOS_SIMULACAO_LLM.csv` | Resumo das dez execuções sintéticas realizadas. |
| `ACHADOS_TESTE_LLM.csv` | Problemas identificados, com evidência, categoria, gravidade e revisão sugerida. |
| `TESTES_FLUXO.csv` | Casos de teste da lógica condicional e regras de consistência. |
| `REGISTRO_EXECUCAO_LLM.csv` | Registro da versão do formulário, modelo, configuração disponível e quantidade de execuções. |

## Como executar o pipeline com LLMs

O professor permitiu a entrega de **script ou prompt estruturado**. Neste projeto, o pipeline está implementado pelo arquivo `PROMPT_TESTE_LLM.txt`.

### Etapa 1 — Congelar o instrumento

1. Salve a versão das perguntas, alternativas, seções, obrigatoriedade e saltos.
2. Identifique a versão, por exemplo: `v1_publicada_2026-10-05`.
3. Não altere o formulário durante uma rodada de testes.

### Etapa 2 — Selecionar uma persona

1. Abra `PERSONAS_SINTETICAS.csv`.
2. Escolha uma persona, de `S01` a `S10`.
3. Copie todas as características da persona selecionada.

### Etapa 3 — Executar a simulação

1. Abra uma conversa nova com o modelo de linguagem.
2. Copie o conteúdo de `PROMPT_TESTE_LLM.txt`.
3. Preencha os campos:
   - versão do instrumento;
   - persona;
   - perguntas, alternativas e regras de salto.
4. Não forneça o gabarito à etapa que representa o respondente.
5. Execute uma conversa separada para cada persona.

### Etapa 4 — Executar a auditoria

1. Abra outra conversa com o modelo.
2. Forneça o instrumento e a resposta sintética gerada.
3. Solicite a auditoria prevista no prompt.
4. Registre somente problemas com evidência textual.
5. Classifique cada achado por categoria e gravidade.

### Etapa 5 — Consolidar os resultados

1. Registre as execuções em `REGISTRO_EXECUCAO_LLM.csv`.
2. Salve os caminhos e respostas em `RESULTADOS_SIMULACAO_LLM.csv`.
3. Consolide os problemas em `ACHADOS_TESTE_LLM.csv`.
4. Verifique os casos de aceitação em `TESTES_FLUXO.csv`.
5. Revise manualmente cada crítica produzida pela LLM.

### Etapa 6 — Corrigir e testar novamente

1. Aplique no formulário somente as correções aprovadas pelo grupo.
2. Salve a versão corrigida como `v2`.
3. Repita as personas afetadas pela alteração.
4. Repita todos os testes de fluxo.
5. Faça um piloto com participantes humanos e cronometre o preenchimento.

## Aviso sobre os dados sintéticos

> **As respostas deste repositório são simulações sintéticas e não são dados de estudantes reais.**

As personas não representam pessoas específicas. Os resultados foram usados somente para testar linguagem, alternativas, consistência e fluxo. Eles não devem ser:

- incorporados à amostra da pesquisa;
- interpretados como prevalência entre estudantes;
- usados para validar psicometricamente o instrumento;
- apresentados como evidência de comportamento real.

O teste com LLM não substitui o piloto humano.

## Modelo utilizado

- **Modelo:** OpenAI Codex
- **Identificador:** `openai-codex/gpt-5.6-sol`
- **Nível de raciocínio:** `high`
- **Temperatura:** não disponível no ambiente
- **Semente:** não disponível no ambiente
- **Execuções:** dez simulações, uma por persona, seguidas por uma auditoria independente

A ausência de temperatura e semente foi registrada explicitamente; nenhum parâmetro foi inventado.

## Principais problemas metodológicos encontrados

### Gravidade alta

1. **Anonimato contraditório:** o formulário exige login e registro de e-mail, mas afirma que as respostas são anônimas.
2. **Salto prematuro em Q03:** quem responde “Nunca” deixa de receber perguntas de teoria e ética que poderiam ser respondidas sem experiência prévia.
3. **Triagem posterior à identificação:** pessoas externas ao IEG fornecem identificação e ainda visualizam a pergunta de período antes do encerramento.
4. **Grade Q17 opcional:** as cinco linhas estão opcionais, apesar de o documento integrador afirmar que as perguntas seriam obrigatórias.

### Gravidade média

5. A linha de atenção está misturada aos itens de autoimagem e não deve integrar qualquer escore.
6. Q15 e Q16 não possuem período de referência; Q16 combina raciocínio, análise e julgamento.
7. A escala de frequência de Q03 usa categorias vagas como “algumas vezes”.
8. Q10 mistura funções, interfaces e infraestrutura e não apresenta a alternativa “Nenhuma”.
9. A opção “Outro” de Q01 não informa se significa outro curso do IEG.
10. Q04 combina o diagnóstico de overfitting com intervenções possíveis.
11. Q08 e Q09 dependem de política institucional, autorização, sensibilidade dos dados e risco de reidentificação.
12. A duração inferior a sete minutos ainda precisa ser confirmada em piloto humano cronometrado.

## Situação do instrumento

A documentação, o dicionário e o teste sintético estão concluídos. Antes da coleta definitiva, o grupo deve:

1. corrigir os problemas de alta gravidade;
2. publicar a versão revisada como `v2`;
3. repetir os testes de fluxo;
4. realizar o piloto humano;
5. confirmar o tempo de preenchimento.

## Privacidade e publicação

Não devem ser enviados ao GitHub:

- respostas reais de estudantes;
- nomes, e-mails ou identificadores de participantes;
- exportações identificadas do Google Forms;
- chaves de API, senhas ou tokens.

Este repositório contém somente documentação e dados sintéticos de teste.
