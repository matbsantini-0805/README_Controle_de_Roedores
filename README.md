# README_Controle_de_Roedores
Este repositório contém a documentação completa do processo de controle de roedores, incluindo instruções de preenchimento das planilhas, uso dos dashboards no Power BI e interpretação dos resultados.
---
Antes de começar, é obrigatório ler e compreender o POP 10-05 para garantir que os registros estejam de acordo com o procedimento oficial. 
--
## 1️⃣ Caminho de Acesso

As planilhas e dashboards estão armazenados em:
`"X:\Gerencia de Produção\Leitura Roedores Bisavós - BI"`

Dentro dessa pasta
- Cada unidade possui sua própria pasta, planilha e dashboard.
- Existe também um dashboard geral para visualização consolidada de todas as granjas.

---

## 2️⃣ Estrutura das Tabelas

O controle é composto por duas tabelas principais:

- **Tabela "Coordenadas ratoeiras"** – armazena as posições X e Y de cada ratoeira.
- **Tabela "Roedores"** – armazena as leituras quinzenais e os dados de consumo.

---

## 🟥 Tabela Coordenadas Ratoeiras

Tabela contendo as posições X e Y de cada ratoeira.

### ✔ Como foi construída  
- Baseada nos mapas das unidades (DSV).  
- Cada ratoeira tem suas coordenadas X/Y conforme o mapa.
   - Coordenadas podem ser retiradas de forma simples utilizando o Paint.  

### ✔ Para que serve  
- Geração do **mapa interativo** no Power BI.   

### ✔ Alterações  
Caso seja necessário inserir novas ratoeiras ou mover alguma:
- Inserir novas ratoeiras seguindo o padrão.  
- Atualizar coordenadas em caso de mudança de posição.

<img width="563" height="410" alt="image" src="https://github.com/user-attachments/assets/ccddb5dd-3db3-4475-85c4-1e8e77266326" />

---

## 🟥 Tabela Roedores

Esta tabela registra quinzenalmente as ratoeiras de acordo com o local, área, leiturista e registros de consumo (segundo a tabela de Leitura, que possui as leituras e avaliações dos leituristas). Dessa forma, a tabela traz o consumo numérico, status e nível de consumo de cada ratoeira.

<img width="864" height="286" alt="image" src="https://github.com/user-attachments/assets/a1556706-60e1-4ded-8885-a8f01fe0e9f9" />

O consumo numérico é calculado com base nas somas obtidas a partir dos registros de consumo de cada ratoeira:

**SOMA Neg × 0 + SOMA Toque × 0,1 + SOMA 1/4 × 0,25 + SOMA 1/2 × 0,5 + SOMA 3/4 × 0,75 + SOMA 1 × 1**

### Padrões para Classificação (Consumo)

O consumo indica no mapa o nível de consumo que a ratoeira apresenta, podendo ser:
Negativo, Toque, Baixo, Médio ou Alto.

### Legenda no mapa:
🔴 Alto 🟡 Médio 🔵 Baixo 🟣 Toque 🗙 Negativo  

A classificação é feita a partir do padrão abaixo:

---

### Passo a Passo para Preenchimento

1. Abrir a tabela de Leitura fornecida pelo administrativo.  
   - É possível também fazer o preenchimento manual direto na tabela "Roedores" sem passar pelos passos 1 e 4.

## Exemplo Tabela de Leitura
<img width="846" height="343" alt="image" src="https://github.com/user-attachments/assets/ab2b7b93-4bab-48f2-9d92-1b4e540fe77f" />

2. Abrir a aba que estiver sendo registrada na tabela "Roedores".

3. Preencher as colunas **Data, Local, Área, Número da Ratoeira e Leiturista** de acordo com a Tabela de Leitura para um registro quinzenal.  
   - Copie as colunas da última leitura e cole embaixo.

<img width="866" height="287" alt="image" src="https://github.com/user-attachments/assets/59371374-72a0-4e85-a11e-b4db16ca3268" />

4. Copiar os dados dos valores de consumo das linhas de **Negativo até Troca** das ratoeiras da Tabela de Leitura.

<img width="460" height="128" alt="image" src="https://github.com/user-attachments/assets/497b5733-0898-45f8-a43d-41af8e38bbf6" />

5. Colar **transpondo** na tabela "Roedores" os dados.  
   Atalho: **CTRL + V → CTRL + T**

<img width="864" height="289" alt="image" src="https://github.com/user-attachments/assets/b01aeed7-cbe5-44dd-ada0-2b63dd175ec0" />

6. Preencher motivos da troca + observações.

<img width="866" height="286" alt="image" src="https://github.com/user-attachments/assets/53ed7ca8-ba06-4f9e-b175-56dcffa1cb55" />

⚠️ **Atenção:** Podem haver erros de digitação e/ou de preenchimento da planilha de Leitura. É necessário conferir se as informações da coluna *Motivo de Troca* batem com as trocas na coluna *Troca*.

7. Salvar planilha.

---
## 3️⃣ Visualização Power BI

Para abrir arquivos .pbix, é necessário ter o Power BI instalado.  
Se não tiver acesso, solicitar instalação ao TI (via Microsoft Store).

Como o Qlik é o software oficial da empresa, utilizamos apenas a versão gratuita do Power BI, sem recursos de compartilhamento online corporativo.

---
🟥 **Controle Roedores Geral**

Esse dashboard permite ter uma visualização geral de um conjunto de unidades. Ele mostra o consumo numérico total das unidades, permitindo a comparação entre elas. É possível visualizar o consumo mensal selecionando um intervalo de tempo, além do consumo de iscas por unidade e áreas, com filtros específicos para áreas dos núcleos.

Os gráficos inferiores indicam consumo dentro dos núcleos no período selecionado, permitindo ação rápida caso haja risco.

<img width="948" height="539" alt="image" src="https://github.com/user-attachments/assets/d0cf2a43-2704-448f-8c40-c896e476481e" />

✔ Atualizar dados  
- Sempre clicar em **Atualizar** ao abrir o arquivo .pbix da pasta.

<img width="1365" height="720" alt="image" src="https://github.com/user-attachments/assets/7458398a-e9e7-4ec7-be3c-142a33f7bb5d" />

✔ Publicar relatório  
- Para visualizar o dashboard em tela cheia, é necessário publicar o relatório.  
- Acessar o link gerado no Power BI Online.

<img width="1360" height="717" alt="image" src="https://github.com/user-attachments/assets/f7fa20fa-6d09-4859-9fbb-eb0a40c86d83" />

✔ Modo apresentação  
- Para visualizar em tela cheia:

<img width="1359" height="671" alt="image" src="https://github.com/user-attachments/assets/605ce595-e2e2-4ab2-b86c-54abc1d23c6c" />

---

🟥 **Controle Roedores de cada Unidade**

Esse dashboard permite visualizar as leituras de ratoeiras para agir de forma mais rápida e precisa em caso de risco ao aviário. Ele mostra o consumo geral da unidade, possui guias individuais para cada área e uma guia de controle de estoque de iscas utilizadas.

A guia *Evolução Mensal* exibe o consumo da unidade por data e área, permitindo identificar rapidamente consumo em núcleos.

<img width="946" height="538" alt="image" src="https://github.com/user-attachments/assets/fe04774a-4cb0-4b94-ae19-9ef621142108" />

A guia de cada área mostra o **mapa interativo** das ratoeiras com a legenda de consumo, filtros de data e área, além da tabela com motivos de troca e observações.  

Também há:
- Gráfico de evolução de consumo por ratoeira  
- Seleção direta via mapa ou tabela  
- Gráfico de evolução por área  

<img width="750" height="581" alt="image" src="https://github.com/user-attachments/assets/57c9fddc-9f97-44a9-b2d6-bbf3ae6487e1" />

A guia *Controle de Troca de Iscas* exibe a quantidade de trocas por área, permitindo avaliar se estão dentro do esperado, se o colaborador está trocando corretamente e em quais épocas do ano ocorrem mais trocas e seus motivos.

<img width="920" height="512" alt="image" src="https://github.com/user-attachments/assets/9ab80e07-4d9c-4da9-9074-b13b4ecbfa63" />

---

## 4️⃣ Limitações e Possíveis Erros

- A planilha de leitura pode conter erros de digitação.
- Sempre conferir o documento original em caso de erros de digitação ou falta de algum dado.
- Mudanças nos mapas devem ser atualizados no mapa do Power BI e nas coordenadas das ratoeiras.
- A falta ou implementação de uma ratoeira pode gerar erros nas referências de visualização do mapa ou da ratoeira.
- Certifique-se de estar conectado à rede/VPN ao salvar.

## 5️⃣ Sugestões

- Sugestões de layout, melhorias nas tabelas ou dashboards são muito bem-vindas.
Este material foi criado para facilitar o trabalho de todos.

## 6️⃣ Créditos / Referências

Matheus Santini
Trainee de Produção — Bisavós
📧 msanini@aviagen.com







