# Desafio de Automoção

## Objetivo:
O objetivo desta tarefa é que você crie um arquivo README.md no GitHub, onde você irá explicar o que aprendeu ao desenvolver o seu próprio script em batch. O script deve abordar algum processo automatizado utilizando a linguagem batch no ambiente Windows, como organização de arquivos, criação de pastas, ou outro processo que tenha sido relevante para o aprendizado. Além disso, o README deve conter a explicação detalhada de como o seu script funciona e o que você aprendeu ao implementá-lo.

## Explicação do código:

- Cria uma pasta (se ele não existir) com o primeiro parâmetro escrito e entra nesse diretório:

```
  if not exist "%1" (
      mkdir "%1"
  )
  cd "%1"
```
- Dentro do primeiro diretório, cria uma pasta (se el não existir) com o segundo parâmetro escrito e entra nesse diretório:

```
  if not exist "%2" (
      mkdir "%2"
  )
  cd "%2"
```

- Cria duas váriaveis uma chamada "ano" que recebe o primeiro parâmetro, e outra chamada "mes" que recebe o segundo parametro:

```
  set ano=%1
  set mes=%2
```

- Cria três váriaveis: "resto1", "resto2" e "resto3":
  - Cada uma recebe o resto de uma divisão diferente;
  - A primeira recebe o resto da divisão "ano / 4";
  - A segunda recebe o resto da divisão "ano / 100";
  - A terceira recebe o resto da divisão "ano / 400".
Como mostrado abaixo:

```
  set /a resto1=%ano% %% 4
  set /a resto2=%ano% %% 100
  set /a resto3=%ano% %% 400
```

- Depois é feito um cálculo que decide se bissexto é igual a "0" (não é um ano bissexto) ou "1" (é um ano bissexto):

```
  if %resto1%==0 (
      if %resto2%==0 (
          if %resto3%==0 (
              set bissexto=1
          ) else (
              set bissexto=0
          )
      ) else (
          set bissexto=1
      )
  )
```

- Após isso, é onde a váriavel "dias" é definida de acordo com seu mês:

```
  if %mes%==1 set dias=31
  
  if %mes%==2 (
      if %bissexto%==1 (
          set dias=29
      ) else (
          set dias=28
      )
  )
  
  if %mes%==3 set dias=31
  if %mes%==4 set dias=30
  if %mes%==5 set dias=31
  if %mes%==6 set dias=30
  if %mes%==7 set dias=31
  if %mes%==8 set dias=31
  if %mes%==9 set dias=30
  if %mes%==10 set dias=31
  if %mes%==11 set dias=30
  if %mes%==12 set dias=31
```

Cada uma recebe um número de dias específico de acordo com a váriavel "mes", apenas o "mes 2", o mês de fevereiro que pergunta se o ano é bissexto ou não, pra definir se a váriavel "dias" vai receber "28" ou "29", respectivamente

- O terminal diz o seguinte: "O número de dias, no mês --- do ano --- é ---." (Os traços irá se transformar em números, portadas pelas váriaveis)

`echo O numero de dias no mes %mes% do ano %ano% é %dias%.`
