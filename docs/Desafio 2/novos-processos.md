---
title: Novos Processos
---

# Desafio 2 - Novos Processos

Tendo como base o [processo atual descrito pela PORVID](/Desafio 2/processo-atual/) e adotando um modelo de co-criação foram desenhados dois novos processos de acordo com os objetivos deste segundo desafio:

+ Um novo processo que tem em conta o quão critico é para a PORVID a integração desta informação para a PORVID e então adapta-se o mais possível aos atuais métodos de trabalho da PORVID;
+ Um novo processo, com um horizonte de implementação a médio prazo, que prevê uma maior digitalização dos processos da PORVID. Mais detalhe sobre a implementação deste processo e outras recomendações [aqui](/Desafio 1/recomendacoes/).

## Estrutura

Cada um dos novos processos desenhados é aqui representado em [notação BPMN](https://wikipedia.org/wiki/Business_Process_Model_and_Notation), seguido de uma descrição detalhada de cada atividade, pressupostos e outras considerações.  
Alguns destaques a seguementos especificos do digrama são também apresentados para (1) facilitar a leitura e (2) destacar as diferenças entre o Novo Processo e o Novo Processo Digitalizado.

Uma divisão, apesar de não estrita, entre os sub-desafios 2a e 2b é também representado segundo o seguinte esquema de cores:

<figure markdown>
![Diagrama BPMN Legenda - Desafio 2a](/diagramas/desafio2/export/parciais/desafio2-corte-2a.png)
    <figcaption>Desafio 2a</figcaption>
</figure>

<figure markdown>
![Diagrama BPMN Legenda - Desafio 2b](/diagramas/desafio2/export/parciais/desafio2-corte-2b.png)
    <figcaption>Desafio 2b</figcaption>
</figure>

## Desafio 2 - Novo Processo

![Diagrama BPMN Desafio 2 - Novo Processo SI](/diagramas/desafio2/export/desafio2-novo.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio2/desafio2-novo.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio2/export/desafio2-novo.png).
    
### PN2. Decisão sobre parcelas a prospetar

De acordo com o novo processo principal  descrito no [Desafio 1](/Desafio 1/processo-atual/), as novas atividades de decisão sobre as parcelas a prospetar são desencadeadas após um inicial processamento manual de informação que chega do IVV.

1. Com esta informação validada, o processo inicia-se paralelamente para as várias parcelas indicadas.
2. À semelhança do processo atual, o envolvimento da DRAP respetiva à parcela em análise é mantido, sendo o parcer destas importante para a última decisão de prospeção de cada parcela.
3. Quanto às atividades de validação interna (ano de plantação e castas), estas são mantidas de forma manual, com os mesmos critérios do processo atual.
4. Terminadas estas atividades, e definidas as parcelas com e aquelas sem interesse de prospeção, esta informação é _enviada_ para o processo principal (descrito no [Desafio 1](/Desafio 1/processo-atual/)) para se proceder ao agendamento de prospeções, sub-process descrito em [PN3. Agendamento de prospeção](/Desafio 2/novos-processos/#pn3-agendamento-de-prospecao).

### PN3. Agendamento de prospeção

Despontado pelo processo principal, após existir uma decisão sobre quais parcelas são de interesse prospetar (descrito acima com o [PN2. Decisão sobre parcelas a prospetar](#pn2-decisao-sobre-parcelas-a-prospetar)), e em paralelo com o sub-processo [PN4. Optimização de recolhas](/Desafio 3/novos-processos/#pn4-optimizacao-de-recolhas), este sub-processo é responsável por (1) assegurar que existe consentimento por parte da PORVID para contactar o viticultor da parcela em questão; (2) utilizar a DRAP como intermédio de contacto com viticultores caso consentimento não tenha sido dado; e (3) agendar a prospeção junto do viticultor.

1. O processo inicia-se com uma validação manual do consentimento de partilha de informação, dado aquando da candidatura VITIS.
    1. Aqui partimos do pressuposto que mesmo para aquelas candidaturas para as quais não tenha sido dado o consentimento por parte do viticultor existe um conjunto de informação, não identificativa, que pode ser partilhada com a PORVID.
2. Caso exista este consentimento, a PORVID por iniciar o seu contacto direto com o viticultor para proceder ao agendamento.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 2 Novo - Corte 1](/diagramas/desafio2/export/parciais/desafio2-novo-parcial-01.png)
    </figure>

3. Caso este consentimento não exista, a DRAP correspondente à parcela em questão, poderá servir como intermediário para a identificação e contacto do viticultor. Para isto uma notificação é enviada para a DRAP, que se encarrega que proceder a este agendamento e subsequentemente comunicar com a PORVID.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 2 Novo - Corte 2](/diagramas/desafio2/export/parciais/desafio2-novo-parcial-02.png)
    </figure>

4. Este agendamento feito pela DRAP é depois validado pela PORVID.
5. Fim do processo.

## Desafio 2 - Novo Processo Digitalizado

![Diagrama BPMN Desafio 2 - Novo Processo SI](/diagramas/desafio2/export/desafio2-novo-SI.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio2/desafio2-novo-SI.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio2/export/desafio2-novo-SI.png).

### PN2. Decisão sobre parcelas a prospetar

O processo PN2. Decisão sobre parcelas a prospetar é um dos que mais pode beneficiar com a introdução de sistemas de informação. Isto porque, mantendo o processo em tudo semelhante à forma de trabalho atual da PORVID e trazendo este corpo de informação explicita e ferramentas que tirem partido dela, conseguimos automatizar todo o processo.  
Desde a partilha de informação com a DRAP, até à validação do ano plantação e validação das castas, todas as atividades deste processo são passíveis de ser automatizadas com relativo pouco esforço.

1. Para cada uma das parcelas em que seja identificado este potencial interesse de prospeção, este sub-processo é despontado.
2. notificações automáticas são enviadas à DRAP correspondente, com toda a informação pertinente, que novamente poderá interromper este processo a qualquer momento.
3. A validação de ano de plantação das vinhas é feita nos mesmos parâmetros que acontecem atualmente.
4. A validação das castas é feita também autonomamente, uma vez que o sistema inclui lógica para, recorrendo aos SI, ser capaz de listar quais as castas de interesse e assim as sinalizar.
5. Atualizar novamente todos os SI refletindo esta decisão, tanto para parcelas com interesse de prospeção, como para parcelas sem interesse de prospeção.
6. Fim do processo.

### PN3. Agendamento de prospeção

Apesar de o sub-processo PN3. Agendamento de prospeção, ainda contemplar algumas atividades manuais, para além daquelas de validação, este é também um processo que pode em muito beneficiar do apoio do SI.

1. O processo inicia-se com uma do consentimento de partilha de informação, dado aquando da candidatura VITIS, que agora acontece de forma automatizada.
2. Para aquelas parcelas em que existe um consentimento explicito do lado do viticultor, atores da PORVID são automaticamente notificados que podem proceder ao agendamento de prospeção da parcela junto do viticultor.
    1. Esta notificação deverá já conter informação referente à optimização de prospeção, atividade que despontada em paralelo a esta e descrita no sub-processo [PN4. Optimização de recolhas](/Desafio 3/novos-processos/#pn4-optimizacao-de-recolhas).
3. Para aquelas parcelas onde não exista consentimento, informação pode automaticamente ser partilhada com a DRAP correspondente para novamente servir como intermédio deste sub-processo de agendamento.
4. Com os agendamentos definidos, chegamos ao fim do processo.
