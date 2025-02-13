# Batch

## Objetivo

## Comandos do Batch

### __Habilitando funções no .bat__:

- Para habilitar as funções necessárias para a gerenciação dos arquivos, digite o seguinte código:

```
@@echo off
```

### __Criando um diretório (pasta)__:

- Para criar um diretório/pasta no .bat, basta digitar o seguinte código:

```
  mkdir "nomeDoDiretório"
```

### __Removendo um diretório__:

- Para remover um diretório sem nenhum arquivo dentro, basta digitar o seguinte código:

```
  rmdir "nomeDoDiretório"
```

- Para remover um diretório com arquivos dentro, basta digitar o seguinte código:

```
  rmdir /s /q "nomeDoDiretório"
```

### __Criar arquivos__:

- Para criar arquivos com texto dentro, basta digitar o seguinte código:

```
  echo O conteúdo que você deseja escrever dentro do arquivo > "nomeDoArquivoTexto.txt"
```

- Para criar arquivos com texto de várias linhas dentro, basta digitar o seguinte código:

```
  (
  echo Linha de Texto 1
  echo Linha de Texto 2
  echo Linha de Texto 3
  ) > nomeDoArquivoTexto.txt
```

- Para criar arquivos sem nenhum texto dentro, basta digitar o seguinte código:

```
  echo null > "nomeDoArquivoTexto.txt"
```

### __Remover arquivos__:

- Para remover um arquivo em específico, basta digitar o seguinte código:

```
  del "nomeDoArquivoTexto.txt"
```

- Para remover todos os arquivos (.txt) dentro da pasta, basta digitar o seguinte código:

```
  del "*.txt"
```

### __Copiar arquivos__:

- Para copiar um arquivo de um lugar e colar em outro, basta digitar o seguinte código:

```
  copy "nomeDoArquivoTexto.txt" "C:\Users\ondeVocêDesejaColar\"
```

### __Mover arquivos__:

- Para mover um arquivo de um lugar para outro, basta digitar o seguinte código:

```
  move "nomeDoArquivoTexto.txt" "C:\Users\ondeVocêDesejaMover\"
```

### __Renomear arquivos__:

- Para renomear um arquivo em específico, basta digitar o seguinte código:

```
  rename ------------------------------------------------
```

### __Exibindo conteúdo do arquivo__:

- Para exibir o conteúdo de um arquivo, basta digitar o seguinte código:

```
  type "C:\Caminho\Origem\nomeDoArquivoTexto.txt"
```

