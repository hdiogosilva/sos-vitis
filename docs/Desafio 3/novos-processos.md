---
title: Novos Processos
---

# Desafio 3 - Novos Processos

Tendo como base o [processo atual descrito pela PORVID](/Desafio 3/processo-atual/) e adotando um modelo de co-criação foram desenhados dois novos processos de acordo com os objetivos deste segundo desafio:

+ Um novo processo que tem em conta o quão critico é para a PORVID a integração desta informação para a PORVID e então adapta-se o mais possível aos atuais métodos de trabalho da PORVID;
+ Um novo processo, com um horizonte de implementação a médio prazo, que prevê uma maior digitalização dos processos da PORVID. Mais detalhe sobre a implementação deste processo e outras recomendações [aqui](/Desafio 1/recomendacoes/).

## Estrutura

Cada um dos novos processos desenhados é aqui representado em [notação BPMN](https://wikipedia.org/wiki/Business_Process_Model_and_Notation), seguido de uma descrição detalhada de cada atividade, pressupostos e outras considerações.  
Alguns destaques a seguementos especificos do digrama são também apresentados para (1) facilitar a leitura e (2) destacar as diferenças entre o Novo Processo e o Novo Processo Digitalizado.

## Desafio 3 - Novo Processo

![Diagrama BPMN Desafio 3 - Novo Processo SI](/diagramas/desafio3/export/desafio3-novo.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio3/desafio3-novo.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio3/export/desafio3-novo.png).
    
### PN4. Optimização de recolhas

De forma a otimizar as deslocações realizadas pela PORVID, este sub-processo tem em conta um conjunto de fatores para a ordenação e priorização das recolhas efetuadas.

1. O sub-processo de otimização de recolhas inicia-se após o interesse de uma parcela/vinha é definido no sub-processo PN2. Decisão sobre parcelas a prospetar, e em paralelo com o sub-processo PN3. Agendamento de prospeção.
    1. A especificação dests sub-processo encorre no âmbito do [Desafio 2](/Desafio 2/resumo/). Descrição do [processo atual aqui](/Desafio 2/processo-atual/) e descrição do [novo processo aqui](/Desafio 2/novo-processo/).
2. Uma vez que a PORVID tem, a partir de agora, acesso a informação do IVDP, o primeiro passo deste processo é a validação da localização da parcela. Caso esta pertença à região demarcada do Douro, e portanto abrangida pelos registos provenientes do IVDP, esta informação deve ser associada, de forma a mais fácilmente proceder a esta recolha e contacto com o viticultor.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 3 Novo - Corte 1](/diagramas/desafio3/export/parciais/desafio3-novo-parcial-01.png)
    </figure>

3. O próximo passo de priorização prede-se com o programa VITIS. Dada a sua natureza, parcelas que chegem através deste programa devem ser priorizadas uma vez que há um interesse explícitos dos viticultores em atualizar as vinhas destas parcelas específicas. Desta forma outras parcelas de interesse identificadas pela PORVID, devem ser processadas apenas depois destas.
4. Dentro das parcelas abrangidas pelo VITIS, no entanto, existe ainda a necessidade de priorizar aquelas parcelas para qual o financiamento foi aprovado. Estas serão as que irão sofrer intervenções em primeiro lugar, logo devem ter prioridade em relação a todas as outras.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 3 Novo - Corte 1](/diagramas/desafio3/export/parciais/desafio3-novo-parcial-02.png)
    </figure>

5. Após terminadas as atividades de priorização de parcelas, é necessário identificar parcelas geograficamente próximas, de forma a optimizar as deslocações dos elementos da PORVID. Esta identificação é feita de forma manual através do geo-códigos associados a cada parcela.
    1. As atividades de validação destes geo-códigos é dependente de plataformas e serviços externos e não foi aqui representada. Descrições mais exaustivas deste processo devem sistematizar estas atividades.
6. Com toda esta informação agregada, é assim possível aos membros da PORVID agrupar as parcelas para intervenção, da forma que mais seja vantajosa.
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 3 Novo - Corte 1](/diagramas/desafio3/export/parciais/desafio3-novo-parcial-03.png)
    </figure>
7. Fim do processo.

### PN5. Integração Informção IVDP

O sub-processo PN5. Integração Informção IVDP foi um dos que surgiu durante o processo de co-criação do Desafio 3. Neste, o IVDP disponibiliza-se a periodicamente partilhar com a PORVID informação dos seus SI, para que mais facilmente a PORVID consiga proceder à prospeção de parcelas na Região Demarcada do Douro.

1. Este processo é despontado a cada 12 meses, de forma autónoma pelo IVDP.
    1. Os 12 meses definidos podem ser alterados de acordo com as diferentes necessidades ou requisitos posteriormente definidos.
2. Quando este processo é despontado existe uma atividade intermédia de preparação dos dados a partilhar de forma a assegurar a sua integridade.
3. Depois do envio desta informação para a PORVID, é necessário que exista uma integração desta informação com os atuais registos mantidos para a PORVID, para que possa facilmente ser integradas nos restantes processos.
4. Fim do processo.

## Desafio 3 - Novo Processo Digitalizado

![Diagrama BPMN Desafio 3 - Novo Processo SI](/diagramas/desafio3/export/desafio3-novo-SI.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio3/desafio3-novo-SI.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio3/export/desafio3-novo-SI.png).
