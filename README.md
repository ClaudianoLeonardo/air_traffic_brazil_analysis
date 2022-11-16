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

### Análise bivariada:
Essa análise foi realizada utilizando a correlação entre os graus dos nós, considerando o grau do nó e a média dos graus dos vizinhos, para o Brasil e as suas regiões.

**Brasil:**

![bv_br](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_br.png)

```python
degree_assortativity_coefficient = -0.19522933769365391
```

**Região norte:**

![bv_nt](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_nt.png)

```python
degree_assortativity_coefficient = -0.2177920212034003
```

**Região Nordeste:**

![bv_ndr](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_nrd.png)

```python
degree_assortativity_coefficient = -0.31740910282280993
```

**Região sudeste:**

![bv_sds](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_sds.png)

```python
degree_assortativity_coefficient = -0.370867581172046
```

**Região sul:**

![bv_sl](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_sl.png)

```python
degree_assortativity_coefficient = -0.3586586878829849
```

**Região centro-oeste:**

![bv_cdo](https://github.com/ClaudianoLeonardo/air_traffic_brazil_analysis/blob/main/images/bv_cdo.png)

```python
degree_assortativity_coefficient = -0.35656661170467585
```

### Aplicação do conceito de caminho mais curto
Para essa análise foi selecionada uma cidade de cada região e avaliado o caminho mais curto entre elas na seguinte ordem: 
Manaus(Norte) -> Porto alegre(Sul) -> Salvador(Nordeste) -> Belo horizonte(Centro-oeste) -> Rio de Janeiro(Sudeste)

```md
Manaus(Norte) -> Porto alegre(Sul) = ['SBEG', 'SBPA']
```
```md
 Porto alegre(Sul) -> Salvador(Nordeste) = ['SBPA', 'SBSV']
 ```
 ```md
 Salvador(Nordeste) -> Belo horizonte(Centro-oeste) = ['SBSV', 'SBCF']
 ```
 ```md
 Belo horizonte(Centro-oeste) -> Rio de Janeiro(Sudeste) = ['SBCF', 'SBRJ']
 ```
 
 ### Estudo do coeficente de clustering:
 
 
 

