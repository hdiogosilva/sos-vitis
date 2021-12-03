---
title: Novos Processos
---

# Desafio 1 - Novos Processos

Tendo como base o [processo atual descrito pela PORVID](/Desafio 1/processo-atual/) e adotando um modelo de co-criação foram desenhados dois novos processos de acordo com os [objetivos deste primeiro desafio](/Desafio 1/resumo/#objetivo):

+ Um novo processo que tem em conta o quão critico é para a PORVID a integração desta informação para a PORVID e então adapta-se o mais possível aos atuais métodos de trabalho da PORVID;
+ Um novo processo, com um horizonte de implementação a médio prazo, que prevê uma maior digitalização dos processos da PORVID. Mais detalhe sobre a implementação deste processo e outras recomendações [aqui](/Desafio 1/recomendacoes/).

## Estrutura

Cada um dos novos processos desenhados é aqui representado em [notação BPMN](https://wikipedia.org/wiki/Business_Process_Model_and_Notation), seguido de uma descrição detalhada de cada atividade, pressupostos e outras considerações.  
Alguns destaques a seguementos especificos do digrama são também apresentados para (1) facilitar a leitura e (2) destacar as diferenças entre o Novo Processo e o Novo Processo Digitalizado.

Uma divisão, apesar de não estrita, entre os sub-desafios 1a e 1b é também representado segundo o seguinte esquema de cores:

<figure markdown>
![Diagrama BPMN Legenda - Desafio 1a](/diagramas/desafio1/export/parciais/desafio1-corte-1a.png)
    <figcaption>Desafio 1a</figcaption>
</figure>

<figure markdown>
![Diagrama BPMN Legenda - Desafio 1b](/diagramas/desafio1/export/parciais/desafio1-corte-1b.png)
    <figcaption>Desafio 1b</figcaption>
</figure>

## Desafio 1 - Novo Processo

### BPMN

![Diagrama BPMN Desafio 1 - Novo Processo](/diagramas/desafio1/export/desafio1-novo.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio1/desafio1-novo.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio1/export/desafio1-novo.png).

### Descrição
    
1. O processo é despontado pelas candidaturas VITIS, por qualquer viticultor, através do portal do IFAP.
    1. Em descrições mais exaustivas, deverão ser considerados outros inicio para este processo. A especificação das necessidades caso este, por exemplo, seja despontado diretamente de um contacto de uma DRAP, não foram do âmbito deste projeto.
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 1](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-01.png)
    </figure>

2. Seguindo os seus trâmites habituais, estas candidaturas são partilhadas com a tutela, sobre a forma do IVV, onde dão entrada em sistema informação (SI)  próprio, o [Sistema De Informação Da Vinha E Do Vinho](https://sivv.ivv.gov.pt/sivv3-frontend/login.xhtml) (SIVV).
    1. Não tendo acontecido interações formais com o IVV, esta representação do processo é feita de forma aproximada, tendo como ponto de vista a PORVID, e a última finalidade do processo: informação sobre parcelas chegar aos seus SI.
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 2](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-02.png){ width="400" }
    </figure>
    
3. Após a avaliação das candidaturas VITIS (e contemplando todas as candidaturas aprovadas e não apenas as financiadas) é espectável que dados sobre estas parcelas seja partilhado com a PORVID.
    1. Dados de interesse para a PORVID serão aqueles definidos no [modelo de dados](/Desenvolvimento/modelo-dados/), e incluem não apenas informação do formulário VITIS submetido pelo viticultor, mas também informação detida pelo SIVV.
    2. Apesar de serem modeladas atividades de validação da informação recebida, foi assumido que esta terá sido processada pelo SIVV. Poderá haver necessidade de mover esta camada de processamento agora _implícita_ do lado do IVV para os SI internos da PORVID.
    
4. Recebida esta informação pela PORVID, há necessidade de esta ser de alguma forma processada antes de ser utilizada.
    1. Esta atividade foi mantinda propositadamente genérica para assegurar se assegurar que independentemente da forma como a informação chega à PORVID, esta é capaz de ser encaminhada para a atividade de _Decisão sobre parcelas a prospetar_.
    2. Prevê-se que a forma comum de esta informação ser partilhada ser por e-mail, e então há aqui a necessidade de, por exemplo, reencaminhar estas mensagens para os diferentes atores internos da PORVID.
    3. Em descrições mais exaustivas deste processo, esta atividade deve ser desdobrada.
    
5. Esta atividade intermédia leva-nos à atividade de **decisão sobre parcelas a prospetar**, especificada no sub-processo PN2.
    1. A especificação deste processo encorre no âmbito do [Desafio 2](/Desafio 2/resumo/). Descrição do [processo atual aqui](/Desafio 2/processo-atual/) e descrição do [novo processo aqui](/Desafio 2/novo-processo/).
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 3](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-03.png){ width="400" }
    </figure>
    
6. Como resultado desta atividade, para cada parcela é validado o interesse ou não interesse da prospeção. Caso não seja identificado interesse de prospeção, o processo termina para essa parcela em particular.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 4](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-04.png){ width="400" }
    </figure>
    
7. Por cada parcela em que seja identificado um interesse de prospeção duas atividades em paralelo são despontadas: a validação do consentimento de partilha de informação e, desde já, é iniciado o sub-processo de otimização de recolhas.
    1. A especificação do processo de agendamento de prospeção a parcelas encorre no âmbito do [Desafio 2b](/Desafio 2/resumo/). Descrição do [processo atual aqui](/Desafio 2/processo-atual/) e descrição do [novo processo aqui](/Desafio 2/novo-processo/#desafio-2-novo-processo).
    2. A especificação do processo de optimização de recolhas encorre no âmbito do [Desafio 3](/Desafio 3/resumo/). Descrição do [processo atual aqui](/Desafio 3/processo-atual/) e descrição do [novo processo aqui](/Desafio 3/novo-processo/#desafio-3-novo-processo).
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 5](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-05.png){ width="400" }
    </figure>

8. Com todos os elementos recolhidos a próxima atividade no processo é a recolha das amostras em si.
    1. Fora do âmbito deste projeto ficou também a especificação do (sub-)processo de recolha das amostras.
9. Após a recolha, os registos da PORVID devem ser atualizados, mantendo-se fiéis ás amostras já recolhidas e mantendo um historio o mais fiel possível de recolhas.
10. A DRAP correspondente à região da parcela deve ser notificada após cada recolha. Para tal, contactos diretos devem ser estabelecidos pelos membros da PORVID para assegurar o envio de toda a informação requerida.
11. Fim do processo.
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 - Corte 6](/diagramas/desafio1/export/parciais/desafio1-novo-parcial-06.png){ width="400" }
    </figure>

## Desafio 1 - Novo Processo Digitalizado

### BPMN

![Diagrama BPMN Desafio 1 - Novo Processo SI](/diagramas/desafio1/export/desafio1-novo-SI.png)

!!! note "Editável"
    Diagramas editáveis (em [draw.io](https://diagrams.net)) disponíveis [aqui](/diagramas/desafio1/desafio1-novo-SI.drawio).  
    Imagem em resolução completa [disponível aqui](/diagramas/desafio1/export/desafio1-novo-SI.png).
    
### Descrição
    
As principais implicações deste Novo Processo Digitalizado são concentradas no sub-desafio 1b, uma vez que dizem respeito aos sistemas internos à PORVID. Neste sentido, e não havendo alterações quando ao processo acima descrito, o detalhe deste abaixo inicia-se com a chegada à PORVID da informação vinda do SIVV.

1. Recebida esta informação, existem um conjunto de atividades de validação e sanitização da informação. Estas, diferenciando-se do processo anterior, **ocorrendo de forma automática** e garantem que as seguintes atividades podem acontecer com algum grau de automação.
    1. Caso algum erro não ultrapassável pelo próprio sistema seja encontrado, um utilizador deve ser notificado, tendo assim a possibilidade de:
        1. Corrigir os dados em falta/mal formados;
        2. Ignorar o campo em falta/mal formados;
        2. Descartar a parcela em questão.
    2. Em simultâneo devem ser validados campos como a idade das vinhas, a identificação das castas e a percentage de "outras castas".
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 Digitalizado - Corte 1](/diagramas/desafio1/export/parciais/desafio1-novo-SI-parcial-01.png)
    </figure>
    
2. Após assegurada a integridade dos dados recebidos decorre a atividade de **decisão sobre parcelas a prospetar**, especificada no sub-processo PN2.
    1. A especificação deste processo encorre no âmbito do [Desafio 2](/Desafio 2/resumo/). Descrição do [processo atual aqui](/Desafio 2/processo-atual/) e descrição do [novo processo digitalizado aqui](/Desafio 2/novo-processo/#desafio-2-novo-processo-digitalizado).
3. Como resultado desta atividade, para cada parcela é validado o interesse ou não interesse da prospeção.
    1. Caso não seja identificado um interesse de prospeção, **toda a informação desta parcela deverá ser mantida nos SI da PORVID** para futura referência e o processo para essa parcela específica termina.
    
    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 Digitalizado - Corte 2](/diagramas/desafio1/export/parciais/desafio1-novo-SI-parcial-02.png)
    </figure>
    
4. Por cada parcela em que seja identificado um interesse de prospeção duas atividades em paralelo são despontadas: a validação do consentimento de partilha de informação e, desde já, é iniciado o sub-processo de otimização de recolhas.
    1. A especificação do processo de agendamento de prospeção a parcelas encorre no âmbito do [Desafio 2b](/Desafio 2/resumo/). Descrição do [processo atual aqui](/Desafio 2/processo-atual/) e descrição do [novo processo digitalizado aqui](/Desafio 2/novo-processo/#desafio-2-novo-processo-digitalizado).
    2. A especificação do processo de optimização de recolhas encorre no âmbito do [Desafio 3](/Desafio 3/resumo/). Descrição do [processo atual aqui](/Desafio 3/processo-atual/) e descrição do [novo processo digitalizado aqui](/Desafio 3/novo-processo/#desafio-3-novo-processo-digitalizado).
5. À semelhança do processo anterior, a próxima atividade é a recolha das amostras em si, esta um processo manual.
6. Após à uma atualização dos SI com todos os dados inerentes ao processo de recolha, de acordo com a arquitetura de informação definida.
7. A DRAP correspondente à região da parcela deve ser notificada após cada recolha. **Este processo deverá ser automatizado** e enviar toda a informação requerida.
    1. Interações diretas com elementos da tutela são necessárias para especificar que dados/informação necessitam ser partilhados.
8. Fim do processo.

    <figure markdown> 
    ![Diagrama Parcial BPMN Desafio 1 Digitalizado - Corte 3](/diagramas/desafio1/export/parciais/desafio1-novo-SI-parcial-03.png)
    </figure>
