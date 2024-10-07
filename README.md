# Palestra Sobre Web Scraping

## Apresentação

**Web scraping**, ou simplesmente "**scraping**", é uma técnica de extração de dados usada para coletar informações de sites da web. O processo envolve fazer solicitações HTTP para páginas da web, analisar o conteúdo dessas páginas e extrair os dados desejados para uso posterior.

## Conceitos-chave relacionados ao web scraping:

**Requisições HTTP**: No web scraping, o primeiro passo é fazer solicitações para os servidores web que hospedam as páginas desejadas. Isso é feito usando métodos como GET ou POST. As bibliotecas Python, como requests, são comumente usadas para esse propósito.

**HTML Parsing:** Depois de obter a resposta do servidor, o conteúdo da página é geralmente em HTML (Hypertext Markup Language). O HTML é a linguagem de marcação usada para estruturar o conteúdo em páginas da web. Bibliotecas como BeautifulSoup e lxml ajudam a analisar e extrair informações específicas do HTML.

**Seletores CSS e XPath: **Para localizar e extrair dados específicos de uma página, são utilizados seletores CSS e XPath. Essas são linguagens de consulta que ajudam a identificar elementos HTML com base em suas características, como tags, classes ou IDs.

**Robots.txt:** Ao realizar web scraping, é importante respeitar as regras definidas pelo arquivo robots.txt de um site. Esse arquivo fornece diretrizes sobre quais partes do site podem ser acessadas por bots da web.

**Ética e Legalidade: **O web scraping deve ser realizado de maneira ética e legal. Nem todos os sites permitem que seus dados sejam raspados, e alguns podem ter termos de serviço que proíbem explicitamente essa prática. É importante garantir que você tenha permissão ou esteja aderindo aos termos do site ao realizar scraping.
