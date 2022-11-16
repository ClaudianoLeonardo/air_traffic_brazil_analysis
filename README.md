# Air traffic Brazil analysis

## Sobre o projeto:
Esse projeto faz parte da avaliação da disciplina [DCA0209 - ALGORITMOS E ESTRUTURAS DE DADOS II](https://github.com/ivanovitchm/datastructure), tem como objetivo analisar algumas caracteristas do tráfego aéreo brasileiro e seus aeroportos, aplicando conceitos de análise de redes. Base de dados utilizada: (https://github.com/alvarofpp/dataset-flights-brazil)

## Descrição do projeto:
Para esse projeto foram implentados 4 requisitos:

**Assortatividade**

**Análise bivarida**

**Aplicação do conceito de caminho mais curto**

**Estudo do coeficente de clustering**

### Assortatividade:
Para esse requisito calculou-se o coeficiente de assortatividade para verificar se a rede é assortativa, e plotou-se um gráfico para vizualizar as conexões entre os  aeroportos considerando as regiões em que estão localizados.

```python
coeficiente de assortatividade = 0.36858192263245576
```

```python
c = nv.CircosPlot(airports_brazil,
                  node_color="region",
                  node_grouping="region",
                  node_order="region",
                  group_order="alphabetically",
                  group_legend=False,
                  node_labels=False,
                  group_label_position="middle",
                  group_label_color=False,figsize=(10,8))


c.draw()
```
![Circus plot](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/Circus_plot.png)
