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

1. De acordo com o novo processo principal  descrito no [Desafio 1](/Desafio 1/processo-atual/), as novas atividades de decisão sobre as parcelas a prospetar são desencadeadas após um inicial processamento manual de informação que chega do IVV.
2. Com esta informação validada, o processo inicia-se paralelamente para as várias parcelas indicadas.
3. À semelhança do processo atual, o envolvimento da DRAP respetiva à parcela em análise é mantido, sendo o parcer destas importante para a última decisão de prospeção de cada parcela.
4. Quanto às atividades de validação interna (ano de plantação e castas), estas são mantidas de forma manual, com os mesmos critérios do processo atual.
5. Terminadas estas atividades, e definidas as parcelas com e aquelas sem interesse de prospeção, esta informação é _enviada_ para o processo principal (descrito no [Desafio 1](/Desafio 1/processo-atual/)) para se proceder ao agendamento de prospeções, sub-process descrito em [PN3. Agendamento de prospeção](/Desafio 2/novos-processos/#pn3-agendamento-de-prospecao).

### PN3. Agendamento de prospeção

Despontado pelo processo principal, após existir uma decisão sobre quais parcelas são de interesse prospetar (descrito acima com o [PN2. Decisão sobre parcelas a prospetar](#pn2-decisao-sobre-parcelas-a-prospetar)), e em paralelo com o sub-processo [PN4. Optimização de recolhas](/Desafio 3/novos-processos/#pn4-optimizacao-de-recolhas), este sub-processo é responsável por (1) assegurar que existe consentimento por parte da PORVID para contactar o viticultor da parcela em questão; (2) utilizar a DRAP como intermédio de contacto com viticultores caso consentimento não tenha sido dado; e (3) agendar a prospeção junto do viticultor.

1. O processo inicia-se com uma validação manual do consentimento de partilha de informação, dado aquando da candidatura VITIS.
    1. Aqui partimos do pressuposto que mesmo para aquelas candidaturas para as quais não tenha sido dado o consentimento por parte do viticultor existe um conjunto de informação, não identificativa, que pode ser partilhada com a PORVID.
2. Caso exista este consentimento, a PORVID por iniciar o seu contacto direto com o viticultor para proceder ao agendamento.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 3 Novo - Corte 1](/diagramas/desafio2/export/parciais/desafio2-novo-parcial-01.png)
    </figure>

3. Caso este consentimento não exista, a DRAP correspondente à parcela em questão, poderá servir como intermediário para a identificação e contacto do viticultor. Para isto uma notificação é enviada para a DRAP, que se encarrega que proceder a este agendamento e subsequentemente comunicar com a PORVID.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 3 Novo - Corte 2](/diagramas/desafio2/export/parciais/desafio2-novo-parcial-02.png)
    </figure>

4. Este agendamento feito pela DRAP é depois validado pela PORVID.
5. Fim do processo.

## Desafio 2 - Novo Processo Digitalizado

![Diagrama BPMN Desafio 2 - Novo Processo SI](/diagramas/desafio2/export/desafio2-novo-SI.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio2/desafio2-novo-SI.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio2/export/desafio2-novo-SI.png).
