# Crawler Bot - README

## Descrição

Este programa é um crawler web que navega automaticamente por páginas da internet a partir de um URL inicial, respeitando as regras definidas no ficheiro robots.txt de cada site.

## Funcionalidades

- Navegação automática por links encontrados nas páginas
- Respeito pelo robots.txt (bloqueio de URLs não permitidas)
- Limite configurável de páginas a visitar
- Captura de títulos das páginas e links encontrados
- Registo de erros (páginas inacessíveis, timeout, etc.)
- Geração de um grafo de navegação (quais páginas ligam para quais)
- Pausa manual com Ctrl+C para guardar os dados antes de terminar

## Como usar

1. Executar o programa
2. Inserir o URL inicial (ex: https://exemplo.com)
3. Escolher o limite:
   - Um número (ex: 20) para definir o máximo de páginas
   - Escrever 'tudo' para correr sem limite
4. Aguardar a execução
5. Pressionar Ctrl+C para interromper e guardar os dados

## Ficheiros gerados

Os resultados são guardados numa pasta com o nome do domínio visitado, contendo:

- `crawler_sucesso.json` - URLs visitadas com sucesso, títulos e links encontrados
- `crawler_erros.json` - URLs que falharam com o respetivo código de erro
- `crawler_grafico.json` - Mapeamento das ligações entre páginas

## Requisitos

- Python 3
- Bibliotecas: requests, beautifulsoup4
