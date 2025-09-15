# Primeira Entrega: MBA em Engenharia de Software, USP/Esalq Luiz Fernando dos Santos Silva

## Pergunta de Pesquisa

"Como medir objetivamente a eficácia de diferentes estilos de prompts (simples, <i>as code</i>, em cadeia)?"

## Objetivo Geral

Avaliar de forma objetiva a eficácia de diferentes estilos de prompts (simples, em formato de código e em cadeia (<i>Chain-of-Thought</i>)) em tarefas de raciocínio e geração de respostas em modelos de linguagem de grande porte (LLMs),
utilizando como objeto de pesquisa uma iniciativa prática de aplicação de LLMs no suporte à gestão e acompanhamento de OKRs (Objectives and Key Results).

## Objetivos Específicos

<ol type="I">
  <li>Realizar uma revisão bibliográfica sistemática sobre prompt engineering, com foco nos estilos de prompt simples, como código e em cadeia, identificando métricas de avaliação de eficácia propostas na literatura.</li>
  <li>Analisar comparativamente os estilos de prompts selecionados a partir de experimentos conduzidos em um projeto prático de gestão de OKRs, avaliando sua eficácia em tarefas como:</li>
    <ul>
      <li>interpretação de objetivos estratégicos,</li>
      <li>associação entre objetivos e key results,</li>
      <li>clareza e consistência na formulação de métricas.</li>
    </ul>
  <li>Mensurar a eficácia dos estilos de prompt a partir de indicadores objetivos, tais como:   
    <ul>
      <li>acurácia e completude das respostas,</li>
      <li>consistência entre múltiplas execuções,</li>
      <li>custo de tokens e tempo de inferência,
      <li>clareza e interpretabilidade dos resultados.</li>
    </ul>
  </li>
  <li>Avaliar a influência de parâmetros do modelo (como temperatura) no desempenho dos estilos de prompts em tarefas relacionadas a OKRs, identificando variações significativas.</li>
  <li>Propor diretrizes práticas para a seleção e utilização de estilos de prompts em contextos de gestão estratégica com LLMs, de modo a apoiar equipes de negócios e tecnologia na utilização mais eficiente da IA.</li>
</ol>

## Hipóteses

<a id="citacao1"></a>
1. Prompts em cadeia (*Chain-of-Thought*) produzem maior acurácia em tarefas de raciocínio mais complexas (ex.: interpretação de dependências entre OKRs), em comparação a prompts simples e prompts como código [[1]](#ref1).
2. Prompts como código são mais eficientes em termos de custo computacional (tokens e tempo de inferência), mas menos eficazes em termos de clareza e interpretabilidade dos resultados [[2]](#ref2).
3. Em tarefas simples, como a identificação de um Key Result específico, não há diferença estatisticamente significativa entre os estilos de prompt [[3]](#ref3).
4. A eficácia relativa dos estilos de prompt varia conforme os parâmetros de configuração do modelo (como temperatura) e a complexidade dos OKRs analisados [[4]](#ref4).

## Justificativa do Estudo

A engenharia de prompts consolidou-se como um campo central para a utilização de Large Language Models (LLMs) em diferentes domínios, permitindo ajustar o comportamento do modelo
sem a necessidade de re-treinamento. Como os LLMs se baseiam em estatísticas matemáticas para escolher a próxima palavra em um dado contexto, a engenharia de prompt busca maximizar
esses resultados, estabilizando a saída e conduzindo-a para padrões mais próximos do esperado. Apesar disso, ainda há escassez de estudos que avaliem de forma objetiva e padronizada
a eficácia de diferentes estilos de prompts em cenários organizacionais.

Pesquisas como as de Wei et al. (2023) demonstraram que o Chain-of-Thought amplia a capacidade de raciocínio em tarefas complexas [[1]](#ref1), enquanto comparações recentes indicam que técnicas
mais sofisticadas nem sempre superam abordagens simples [[3]](#ref3). Estudos sistemáticos também ressaltam a ausência de métricas universais para mensuração de eficácia, dificultando comparações
consistentes entre abordagens [[2]](#ref2) [[5]](#ref5).

Nesse contexto, Rutledge & van der Kruk (2025) evidenciam que a eficácia dos prompts pode variar não apenas pelo estilo adotado, mas também pela configuração do modelo e pela natureza
da tarefa, utilizando métricas como precisão, recall e acurácia [[4]](#ref4).

Diante disso, este estudo justifica-se por propor uma análise comparativa estruturada entre estilos de prompts, aplicando-a a um caso prático de gestão de OKRs. Espera-se gerar evidências
científicas e diretrizes aplicáveis ao uso de LLMs no apoio à gestão estratégica, contribuindo tanto para a literatura de Engenharia de Software quanto para a adoção responsável da IA em
organizações. Adicionalmente, pretende-se facilitar a incorporação de LLMs em modelos organizacionais baseados em estruturas e equipes enxutas, no estilo self-service IA, em que os próprios
times possam utilizar APIs de IA para otimizar processos sem dependência excessiva de especialistas técnicos.

## Referências Bibliográficas

<a id="ref1"></a>
**[1]** WEI, Jason et al. **Chain-of-Thought Prompting Elicits Reasoning in Large Language Models**. *arXiv*, [S. l.], 2022. Disponível em: https://arxiv.org/abs/2201.11903. Acesso em: 15 set. 2025. [↩](#citacao1)

<a id="ref2"></a>
**[2]** SAHOO, Pranab et al. **A Systematic Survey of Prompt Engineering in Large Language Models: Techniques and Applications**. *arXiv*, [S. l.], 2024. Disponível em: https://arxiv.org/abs/2402.07927. Acesso em: 15 set. 2025. [↩](#citacao2)

<a id="ref3"></a>
**[3]** JEON, Sohyeon; KIM, Hong-Gee. **A comparative evaluation of chain-of-thought-based prompt engineering techniques for medical question answering**. *Computers in Biology and Medicine*, [S. l.], v. 196, p. 110614, 2025. DOI: 10.1016/j.compbiomed.2025.110614. Disponível em: https://doi.org/10.1016/j.compbiomed.2025.110614. Acesso em: 15 set. 2025. [↩](#citacao3)

<a id="ref4"></a>
**[4]** RUTLEDGE, Lloyd; VAN DER KRUK, Koen. **Prompt Engineering for Analyzing Acceptance Criteria for Functional Requirements**. In: SHISHKOV, Boris (ed.). *Business Modeling and Software Design*. Cham: Springer Nature Switzerland, 2026. p. 168-177. DOI: 10.1007/978-3-031-98033-6_11. Disponível em: https://doi.org/10.1007/978-3-031-98033-6_11. Acesso em: 15 set. 2025. [↩](#citacao4)

<a id="ref5"></a>
**[5]** SCHULHOFF, Sander et al. **The Prompt Report: A Systematic Survey of Prompt Engineering Techniques**. *arXiv*, [S. l.], 2025. DOI: 10.48550/arXiv.2406.06608. Disponível em: https://arxiv.org/abs/2406.06608. Acesso em: 15 set. 2025. [↩](#citacao5)
