# File Encrypter & Decrypter (Python)

Projeto simples desenvolvido para fins educacionais durante estudos de
cibersegurança.

O objetivo é demonstrar, de forma prática, como arquivos podem ser
criptografados e descriptografados utilizando AES em Python.

## Aviso

Este projeto é apenas para aprendizado sobre criptografia e segurança da
informação.

## Conceitos Utilizados

-   Criptografia AES (Advanced Encryption Standard)
-   Modo de operação CTR (Counter Mode)
-   Manipulação de arquivos em Python
-   Uso da biblioteca `pyaes`

## Requisitos

Para executar os scripts é necessário:

-   Python 3
-   Biblioteca `pyaes`

Instalação da biblioteca:

``` bash
pip install pyaes
```

Ambiente utilizado nos testes:

-   Kali Linux

## Estrutura do Projeto

    .
    ├── encrypter.py
    ├── decrypter.py
    ├── teste.txt
    └── README.md

## Como Criptografar um Arquivo

O script `encrypter.py` lê o arquivo `teste.txt`, criptografa seu
conteúdo e gera um novo arquivo criptografado.

Executar:

``` bash
python3 encrypter.py
```

### O que acontece

1.  O script abre o arquivo `teste.txt`
2.  Lê todo o conteúdo
3.  Remove o arquivo original
4.  Criptografa os dados usando AES
5.  Cria um novo arquivo chamado:

```
    teste.txt.ransomwaretroll
```

## Como Descriptografar o Arquivo

O script `decrypter.py` realiza o processo inverso.

Executar:

``` bash
python3 decrypter.py
```

### O que acontece

1.  O script abre o arquivo criptografado:


```
    teste.txt.ransomwaretroll
```

2.  Descriptografa o conteúdo utilizando a mesma chave
3.  Remove o arquivo criptografado
4.  Recria o arquivo original:


```
    teste.txt
```

## Chave de Criptografia

A chave utilizada no exemplo é:

``` python
key = b"testeransomwares"
```

Importante:

Para descriptografar corretamente, a mesma chave deve ser utilizada nos
dois scripts.

## Exemplo de Uso no Kali Linux

Criar arquivo de teste:

``` bash
echo "Arquivo de teste de criptografia" > teste.txt
```

Criptografar o arquivo:

``` bash
python3 encrypter.py
```

Descriptografar o arquivo:

``` bash
python3 decrypter.py
```

## Objetivo do Projeto

Este projeto foi criado para demonstrar na prática:

-   Como malwares de criptografia funcionam
-   Como arquivos podem ser protegidos utilizando AES
-   Conceitos básicos de segurança ofensiva e defensiva
