Vendas Interestaduais
=====================
Projeto de Software apresentado como trabalho para obtenção de aprovação no curso de núcleo livre de Análise Estatística de Dados Usando R no semestre 2016/2 do Instituto de Física da Universidade Federal de Goiás (UFG).

#### Facilitador

[Prof. Dr. Ricardo Avelino Gomes](mailto:ragomes@ufg.br)

Descrição
---------
**Vendas Interestaduais** é um projeto de um script na linguagem *R* para facilitar o trabalho de fornecedores e clientes cujos produtos são transportados por vários estados do Brasil.

Através do **Vendas Interestaduais** eles poderiam conhecer qual a melhor possibilidade de rota para a logística de um determinado produto buscando sempre passar pelos estados que existem as menores cargas tributárias ([ICMS](https://pt.wikipedia.org/wiki/Imposto_sobre_Circula%C3%A7%C3%A3o_de_Mercadorias_e_Servi%C3%A7os)).

### *Exemplo*:

***Uma indústria de CDs situada em Goiânia (Goiás), quer enviar uma remessa de CDs gravados para Manaus, no*** **Amazonas**, ***pagando as menores cargas tributárias possíveis no transporte entre os estados.***

Geograficamente falando, a rota mais "direta" que o transporte dos produtos dessa indústria poderia fazer seria: "**Goiás > Mato Grosso > Amazonas**". Simples.

Mas baseado nos dados [desta pesquisa](http://arquivos.portaldaindustria.com.br/app/conteudo_24/2014/05/12/438/1909-TributaosobreMPE.pdf) a respeito da carga tributária de cada estado, percebemos que essa rota daria prejuízos para o empresário:

![Mapa da carga tributária no Brasil](assets/images/mapa-carga-tributaria-brasil.png)
*<small><center>Figura 1. Mapa da carga tributária no Brasil</center></small>*

![Ranking da carga tributaria em Indústria no Brasil](https://cdn.rawgit.com/gustavosotnas/Vendas-Interestaduais/master/assets/images/ranking-carga-tributaria_industria-brasil.svg)
*<small><center>Figura 2. Ranking da carga tributaria em Indústria no Brasil</center></small>*

A rota "direta" passa pelo estado do Mato Grosso, que é o estado que tem **a maior carga tributária do Brasil** (8.62% no ranking geral, 23.17% no ranking de produtos de indústria). Portanto, a melhor rota nesse caso seria passando por rodovias nos seguintes estados:

<center>
"**Goiás > Tocantins > Pará > Amazonas**"
</center>

Usagem
------
O script pode ser usado apenas executando-o com o **`R`**, usando o comando:

```sh
Rscript src/vendas-interestaduais.R
```

na linha de comandos do seu computador ou

```sh
R
source("src/vendas-interestaduais.R")
```
dentro do **R** (modo interativo).

Entrando com o nome do estado de origem e o de destino do(s) produto(s) no Brasil, e o preço total dele(s)&ast;. O **Vendas Interestaduais** indicará a melhor rota de acordo com as estatísticas de carga tributária de cada estado, contando com um arquivo YAML que contém os dados das cargas tributárias de todos os estados do Brasil.

&ast; _Preço total do produto = preço inicial + frete + IPI + seguro + descontos incondicionais + outras possíveis despesas previamente calculadas pelo usuário._

Licenciamento
-------------
**Vendas Interestaduais** é distribuído sob os termos da [MIT License](https://opensource.org/licenses/MIT). Consulte o arquivo [COPYING](./COPYING) para mais detalhes.

Autor
-----
 * Gustavo Moraes dos Santos - <gustavo_moraiss@hotmail.com>
