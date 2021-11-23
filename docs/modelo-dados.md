title: Modelo de Dados

# Modelo de Dados

Nesta página são mantidas as diferentes iterações do modelo de dados modelados para representar as diferentes atividades da PORVID.



## v0.01 - Versão preliminar

Versão preliminar do modelo de dados, representando apenas relações básicas.

```mermaid
classDiagram
	parcela "1" --> "*" casta
	colheitas "1" --> "*" parcela
	casta "1" --> "1" selecoes_clonais
	class colheitas{
		+String id
		+date data
		+String parcelas
		+bool ensaio_campo
		+bool vaso
		+String ensaio
		+int clones
	}
	class casta{
		+String id
		+String nome
		+String descricao
		+String observacoes
		+int genotipos
	}
	class parcela{
		+String id
		+int geocodigo
		+String castas
		+date ano_platancao
	}
	class selecoes_clonais{
		+String id
		+String nome
	}
```

![Processo de Alto Nível](diagramas/modelo-dados/modelo-dadosv001.png)