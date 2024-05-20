# Criação de MASHUP em Qlik Sense

## Entendimento do Problema

Este projeto tem como objetivo desenvolver um mashup utilizando o Qlik Sense, que consiste em uma página, site ou aplicativo da web que incorpora objetos do Qlik Sense de um ou mais aplicativos. A proposta é criar um serviço com uma interface gráfica exclusiva, facilitando a visualização e interação com os dados de forma customizada.

### Alternativa

Hoje o QLik Sense possibilita a criação de dashboards mais elaborados atráves da inserção de backgroud e o sistemas de botões vinculado aos indicadores, muito similar ao Power BI.

Esses backgrouds podem ser criados em diversas ferramentas de edição, atento apenas as parametros de grades, segue modelo criado no Figma:

   <p align="center">
   <img src= "FIGMA LAYOUT.jpeg">   

Para esse projeto foi utilizado o ambiente Dev, para criação de MushUp para publicação dos objetos em pagina web.

#### Passos Seguidos

1. **Criação de Gráficos**: Vamos utilizar o Dash que construimos.

   <p align="center">
   <img src= "P1 - OVERVIEW.jpeg">   

3. **Editor de Texto**: O editor de texto que utilizo é o Notepad++

   <p align="center">
   <img src= "NOTEPAD++.jpeg">   

4. **Integração dos Objetos HTML**:

O primeiro passo é localiza o ID do Objeto na configurações do gráfico dentro do QLIK SENSE.

   <p align="center">
   <img src= "ID GRAF.jpeg">   

 A exportação é feito no ambiente dev ou no editor de texto, referenciando a div do objeto com o ID do gráfico obtido na etapa anterior:

   <p align="center">
   <img src= "EXPORT.jpeg">   
 
Criação de KPI para:
- Receita
- Ticket Médio
- Lucro
- Vendas

Além dessas métricas principais, o dashboard pode incluir filtros interativos que permitem aos usuários segmentar os dados por período, região, produto ou qualquer outra dimensão relevante. Isso proporciona uma visão personalizada e detalhada das finanças, adaptada às necessidades de diferentes usuários dentro da empresa.

4. **Multiplos Visuais**

   <p align="center">
   <img src= "GRAF.jpeg">   

4. **Graficos Gerais**
   
   <p align="center">
   <img src= "P2 - GERAL.jpeg">
    
    MÉDIA DE DIAS DE ENTREGA = 
        
        avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)


     Comprimento de Meta = 
        
       if((avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)/21)>1,1-((avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)/21)-1),1)

5. **MAPA**: Configuração do gráfico de mapa

   <p align="center">
   <img src= "MAPA 1.jpeg">
   
## Resultado Final

O dashboard desenvolvido oferece uma visão completa dos indicadores financeiros da empresa, permitindo um monitoramento eficaz das métricas essenciais e facilitando a tomada de decisões estratégicas. Utilizando o Qlik Sense, a empresa pode acompanhar em tempo real a receita, o ticket médio, o lucro e as vendas, promovendo uma gestão financeira mais eficiente e proativa.
