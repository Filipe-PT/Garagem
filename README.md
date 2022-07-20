# Garagem para o aspirador ! 

Olá, este projeto foi criado para aquelas pessoas que não tem grande local para guardar o seu robot aspirador e não gosta de o ver ali encostado a uma parede. A ideia foi então criar uma garagem para o guardar. Quando ele começa a trabalhar ( estado cleaning ) a porta da garagem abre acende a luz verde e ele sai, depois de um delay de 35 segundos ( pode ser alterado ) a porta fecha e a luz apaga, depois da aspiração terminar ( estado returning ), a porta volta a abrir mas neste caso acende a luz vermelha. Quando ele começa a carregar a porta fecha ( estado dock) e a luz apaga.
Deixo video de demonstração... nas pastas. 


# Requisitos:

- Home Assistent
- Addon ESPHome
- Integração NodeRed
- Robot integrado no Home Assistent


## Material :

- 2x [Servos](https://www.amazon.es/gp/product/B088NJRFD7) ( usados neste projeto ).

- 1x [ESP32-WROOM-32](https://www.amazon.es/dp/B071P98VTG/ref=sr_1_1_sspa?crid=10L8C4C4UDED0&keywords=esp32&qid=1658250876&refinements=p_76%3A13956313031&rnid=831276031&rps=1&s=computers&sprefix=esp32+%2Ccomputers%2C84&sr=1-1-spons&psc=1&smid=A1X7QLRQH87QA3&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyN1FETlRCMzdGTUJIJmVuY3J5cHRlZElkPUEwMDA0NjYyOTVWTkVaQjFDVjI5JmVuY3J5cHRlZEFkSWQ9QTA1MTA1MTBVMzNLQVFCVFo2Nlgmd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl) ( também funciona com [ESP8266](https://www.amazon.es/dp/B06Y1LZLLY/ref=sr_1_2_sspa?crid=7MZPZB29QQ2C&keywords=esp8266+nodemcu&qid=1658251693&sprefix=ESP8266%2Caps%2C88&sr=8-2-spons&psc=1&smid=A1X7QLRQH87QA3&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyMzZaM0hTVUxLRFNEJmVuY3J5cHRlZElkPUEwOTM3MjQ1M043SzdKNFlOR0VEQyZlbmNyeXB0ZWRBZElkPUEwNTg5OTQxNzhPREpSQ0dKQzlUJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==) ).

- 1x [Fita LED WS2812B ](https://pt.aliexpress.com/item/32682015405.html?pdp_npi=2%40dis%21EUR%21€%205%2C90%21€%203%2C89%21%21%21%21%21%40210318be16582511088073757e411e%2112000027369115512%21sh&spm=a2g0o.store_pc_home.productList_2400537.pic_0) ( foram usados somente 16 leds ).

- 2x [Reguladores de tensão  LM2596](https://amzn.to/2V7blBq) .

- 1x [Fonte Alimentação 12v](https://www.amazon.es/alimentación-universal-conmutación-cortocircuito-Sobrecarga/dp/B073GLDKMH/ref=sr_1_8?__mk_es_ES=ÅMÅŽÕÑ&crid=BHWZ3PO8ADGH&keywords=fuente%2Balimentación%2Bled%2B12v%2F24&qid=1658251483&s=lighting&sprefix=fuente%2Balimentacion%2Bled%2B12v%2F24%2Clighting%2C88&sr=1-8&th=1) ou [24v](https://www.amazon.es/Output-Supply-Converter-Adapter-Strips/dp/B01M4PI4E3/ref=sr_1_10?keywords=fuente%2Balimentación%2B24v&qid=1658251922&sr=8-10&th=1) .

- 2x [Dobradiças](https://www.leroymerlin.pt/Produtos/Ferragens/Ferragens-para-moveis/Dobradicas-de-movel/WPR_REF_15040256) . 

- 2x Braços para empurrar a porta da garagem.

## Esquema elétrico :

Existe várias maneira de o fazer neste repositório tem 2 soluções, uma mais económica, outra mais profissional, as duas funcionam bem por igual.
- [Solução económica ](https://im.ge/i/FOcz1C)
- [Solução profissional](https://im.ge/i/FOce7r)


## Instalação no móvel :

A instalação vai depender da imaginação de cada um, bem como o espaço que quer abrir, de salientar que neste projeto não foi estragado qualquer peça dos moveis da cozinha. Por isso, de hoje para amanhã é só desligar e tirar tudo e voltar a encaixar as peças do rodapé para ficar completamente de origem. Dentro do movel foi feita uma pequena "caixa" em U para ele não ir para debaixo do restante movel, podem ver na foto.

- [Local da instalação ](https://im.ge/i/FOgXwc)
- [Local interior ](https://im.ge/i/FOgo2T)

## Instalação Home Assistent :

Aqui no projeto vou deixar os códigos usados em ficheiro para adicionar na configuração do seu ESP32 no ESPHome. Também deixo aqui um flow para abrir/fechar e ligar/desligar a fita led com a cor verde/vermelho já preparado para adicionarem ao vosso NodeRed , bastando mudar as entidades para as vossas.

## Ter em ATENÇÃO :

Quando tiver tudo instalado, cabe a cada um ir aumentando o nível de abertura e fecho da porta no NodeRed, por segurança baixei os valores para não terem problemas, agora cabe a cada um ir aumentando e diminuindo esses valores consoante o vosso rodapé. Deixo foto a indicar onde têm de mudar esses valores ( ficheiro  alterarvalores.jpg e nivel.jpg ) dentro da pasta Flow NodeRed .

- [Alterarvalores.jpg](https://im.ge/i/FOgMAW)
- [Valores.jpg](https://im.ge/i/FOgQp0)


# Segurança:
Muito cuidado a mexer com corrente elétrica ... não me responsabilizo por qualquer dano causado.

# Agradecimentos :
Desde já agradeço a todos os membros que me ajudaram a realizar este projeto em ESPHome/NodeRed, já o tinha feito por outros caminhos que não este, tinha-o feito por um projeto já existente mas por mqtt.
Não vou citar nomes , quem ajudou sabe . Grande Abraço para todos e OBRIGADO.
