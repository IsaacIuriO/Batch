# Batch

## Objetivo

## Comandos do Batch

### Criando um diretório (pasta):

1. Abra o Bloco de Notas em .bat
2. Em seguida, digite o seguinte código:

```
  @echo off
  mkdir "C:\Caminho\Para\NovoDiretorio"
```

### Removendo um diretório:

#### Sem nenhum arquivo dentro:
1. Abra o arquivo .bat que deseja remover
2. Em seguida, digite o seguinte código:

```
  @echo off
  rmdir "C:\Caminho\Para\Diretorio"
```

#### Se houver algum arquivo dentro:

```
  @echo off
  rmdir /s /q "C:\Caminho\Para\Diretorio"
```

### Criar arquivos:

#### Criando arquivo de texto (`.txt`) :

```
  @echo off
  echo Este é um arquivo de teste > C:\Caminho\Para\Arquivo.txt
```

#### Criando arquivo com várias linhas:

```
  @echo off
  (
  echo Linha 1
  echo Linha 2
  echo Linha 3
  ) > C:\Caminho\Para\Arquivo.txt
```

### Remover arquivos:

#### Removendo um arquivo em específico:

```
@echo off
del "C:\Caminho\Para\Arquivo.txt"
```

#### Removendo vários arquivos:

```
@echo off
del "C:\Caminho\Para\*.txt"
```


