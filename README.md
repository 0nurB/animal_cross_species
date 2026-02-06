![Python](https://img.shields.io/badge/python-v3.7-blue)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
![Status](https://img.shields.io/badge/status-up-brightgreen)


<h4 align="center">Descoberta de redes de interações proteína-proteína em plantas: uma abordagem para inovação no melhoramento genético e estudo da biodiversidade da America do Sul</h4>

<h4 align="center">Explorando a Biodiversidade da América do Sul</h4>

<p align="center">
  <a href="https://github.com/0nurB/Plantas-ppi">Entrada</a> •
  <a href="http://autoaipandemics.icmc.usp.br">AutoAI-Pandemics</a> •
  <a href="#installing-dependencies-and-package">Instalando</a> •
  <a href="#how-to-use">Como usar</a> •
  <a href="#citation">Citações</a> 
</p>

<h1 align="center"></h1>


## Principal

Este projeto faz parte de uma série de estudos sobre predição de interações proteína-proteína (PPIs), buscando agilizar sua descoberta. Ele possui dois pilares:  
1. Desenvolver modelos que atendam às necessidades do Sul Global, especialmente da América do Sul;  
2. Criar modelos de IA acessíveis, que demandem pouca intervenção manual para aplicação (aspecto ainda em andamento para o modelo de PPI no clado **Viridiplantae**).

Com esse modelo, propomos o **Brazilian Repositorium For Protein-Protein Interactions (BRFPPI)**, o primeiro banco brasileiro de PPIs minerados por IA. O principal objetivo dessa base é reunir a maior quantidade possível de interações de proteínas da fauna e flora da América do Sul, oferecendo suporte para aprimorar bancos genéticos da biodiversidade única dessa região. A partir desse repositório, podem ser realizados estudos de melhoramento genético de plantas para enfrentar mudanças climáticas e aumentar a produtividade agrícola, visando o combate à insegurança alimentar.

* No melhor do nosso conhecimento, este é o modelo mais bem validado do estado da arte para predição binária de PPIs;  
  - Inclui validação por conceitos evolutivos e por estrutura de proteína, abrangendo espécies de todo o domínio Eukaryota.  
  - Propõe métodos de comparação estrutural integrados à validação.  
  - Apresenta estimativa da fração de verdadeiros positivos em novas amostras, permitindo estudar o desbalanceamento de classes.  
    - Primeiro modelo a estimar a **precisão no mundo real** (amostras aleatórias).  

* Mineração de **3 milhões de interações de muito alta probabilidade** para plantas e algas, incluindo espécies de importância agrícola como arroz, feijão, soja, mandioca, café, laranja, kiwi, maçã, banana e diversos cereais.  

* Este projeto faz parte de uma iniciativa maior, o **AutoIA-Pandemics**, que visa desenvolver aplicações de IA para auxiliar no estudo de pandemias.  

* As interações mineradas no artigo podem ser acessadas em:  
   [Google Drive - BRFPPI](https://drive.google.com/drive/folders/1giwBwA-OgdLy0V_FuLLZjDoqxpJhKvyR?usp=drive_link)


## Resumo

Apesar da elevada capacidade agrícola de países do MERCOSUL, a América Latina figura entre as regiões mais afetadas pela insegurança alimentar, que em 2024 já alcançou mais de 2 bilhões de pessoas no mundo. A intensificação das mudanças climáticas contribui diretamente para esse cenário: fenômenos como o El Niño intensificam secas, enquanto a redução da disponibilidade de água e o aumento das temperaturas comprometem a estabilidade da produção agrícola global. Nesse contexto, torna-se urgente repensar estratégias para garantir a segurança alimentar. Entre as alternativas mais promissoras estão as inovações biotecnológicas, em especial o melhoramento genético, que busca desenvolver cultivos mais resistentes a estresses abióticos e capazes de sustentar a produtividade diante de condições climáticas cada vez mais adversas.
O desenvolvimento de organismos geneticamente modificados depende da identificação de genes associados à resistência a estresses abióticos, processo que passa pela compreensão das interações proteína–proteína (PPIs). Embora técnicas laboratoriais para caracterização de PPIs sejam eficazes, apresentam alto custo e baixa escalabilidade. Métodos in silico baseados em inteligência artificial (IA) têm avançado nesse campo, especialmente aqueles que exploram a estrutura primária das proteínas para prever interações de forma rápida e em larga escala.
Neste estudo, propomos um modelo preditivo baseado em IA voltado para o clado Viridiplantae, englobando espécies agrícolas relevantes da América do Sul. O modelo alcançou 93% de acurácia em dados balanceados de plantas e 85% em eucariotos em geral, superando métodos publicados anteriormente. A principal contribuição está no equilíbrio entre alta especificidade e robuste frente à diversidade estrutural, mesmo em cenários desbalanceados, situação que engloba a procura de interações por amostragem aleatória, onde a fração de positivas estimada é de apenas 1,5 a cada 100 pares aleatórios.
Além da validação em múltiplas espécies, o modelo foi utilizado para minerar 3 milhões de novas interações de muita alta probabilidade, envolvendo mais de 200 mil proteínas que antes não tinham interações nessa categória. Esses resultados sustentam a proposta de criação do Brazilian Repositorium for Protein–Protein Interactions, que reunirá interações de confiança e dados exclusivos da biodiversidade sul-americana. Tal iniciativa visa apoiar pesquisas em biotecnologia vegetal, acelerar a descoberta de alvos para o melhoramento genético e contribuir para a resiliência agrícola frente às mudanças climáticas.



## Participantes

* Bruno Rafael Florentino  

**Contato:** brunorf1204@usp.br  

---

## Rode no Google Colab  

Está em progresso uma versão dos arquivos para rodar diretamente no **Google Colab**, online e sem necessidade de instalar o Python localmente.





## Rode localmente

### Instale as dependências e pacotes

#### Via Miniconda (Terminal)

Baixando os dados e dependências:

```sh
$ git clone https://github.com/0nurB/BioPredictionPPI.git Plantas-ppi

$ cd Plantas-ppi

```

**1 - Instale Miniconda:** 

```sh

See documentation: https://docs.conda.io/en/latest/miniconda.html

$ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

$ chmod +x Miniconda3-latest-Linux-x86_64.sh

$ ./Miniconda3-latest-Linux-x86_64.sh

$ export PATH=~/miniconda3/bin:$PATH

```

**2 - Crie o ambiente:**

```sh

conda env create -f ambiente_base.yml

```

**3 - Ative o ambiente:**

```sh

conda activate ambiente_base

```
## Como usar

Existem dois arquivos tipo jupter notebook para serem utilizados:

- novas_predicoes.ipynb : para dados não rotulados, permite a predição, alinhamento e calculado da precisão média em amostras aleatórias. Exemplo com as proteínas da jabuticabeira.
- performance_testes.ipynb : para dados rotulados, permite mensurar performance em qualquer conjunto de dados, contém um exemplo completo de como utilizar.


## Citação

Em processo de finalização para submissão a revista...
