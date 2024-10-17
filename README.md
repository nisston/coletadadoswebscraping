# Coleta de Dados com o Web Scraping

## Apresentação

**Web scraping**, ou simplesmente "**scraping**", é uma técnica de extração de dados usada para coletar informações de sites da web. O processo envolve fazer solicitações HTTP para páginas da web, analisar o conteúdo dessas páginas e extrair os dados desejados para uso posterior.

## Alguns exemplos do Google Colab:

- Exemplo_Prático_01 - Trabalhando com os principais elementos da biblioteca Selenium - [Link](https://drive.google.com/file/d/1Vm2LYzPuGBJdnKcugOLnhqlRQdMXaPV6/view?usp=sharing)
- Exemplo_Prático_02 - Construção de um código para pegar todos os títulos, quantidade em estoque e valores das páginas do site - [Link](https://colab.research.google.com/drive/1_fcKkUhvea-4lWO8-6wi6At3fzKVLLqb?usp=sharing)
- Exemplo_Prático_03 -
- Exemplo_Prático_04 -
- Exemplo_Prático_05 -

## Conceitos-chave relacionados ao web scraping:

**Requisições HTTP**: No web scraping, o primeiro passo é fazer solicitações para os servidores web que hospedam as páginas desejadas. Isso é feito usando métodos como GET ou POST. As bibliotecas Python, como requests, são comumente usadas para esse propósito.

**HTML Parsing**: Depois de obter a resposta do servidor, o conteúdo da página é geralmente em HTML (Hypertext Markup Language). O HTML é a linguagem de marcação usada para estruturar o conteúdo em páginas da web. Bibliotecas como BeautifulSoup e lxml ajudam a analisar e extrair informações específicas do HTML.

**Seletores CSS e XPath**: Para localizar e extrair dados específicos de uma página, são utilizados seletores CSS e XPath. Essas são linguagens de consulta que ajudam a identificar elementos HTML com base em suas características, como tags, classes ou IDs.

**Robots.txt**: Ao realizar web scraping, é importante respeitar as regras definidas pelo arquivo robots.txt de um site. Esse arquivo fornece diretrizes sobre quais partes do site podem ser acessadas por bots da web.

**Ética e Legalidade**: O web scraping deve ser realizado de maneira ética e legal. Nem todos os sites permitem que seus dados sejam raspados, e alguns podem ter termos de serviço que proíbem explicitamente essa prática. É importante garantir que você tenha permissão ou esteja aderindo aos termos do site ao realizar scraping.

## Boas Práticas e Estratégias para Extração de Dados

### 1. **Respeitar o `robots.txt` e Termos de Serviço**
   - Antes de começar a extração, verifique o arquivo `robots.txt` do site para entender quais áreas são permitidas para crawling.
   - Leia os Termos de Serviço do site para garantir que o web scraping seja permitido e esteja de acordo com as diretrizes do site.

### 2. **Usar Cabeçalhos HTTP Adequados**
   - Configure cabeçalhos HTTP, como `User-Agent`, `Referer`, e outros, para que sua solicitação pareça mais natural e pareça vir de um navegador real.
   - Evite valores padrão de bibliotecas de scraping que podem ser facilmente detectados como atividades de bot.

### 3. **Implementar Delays Aleatórios**
   - Use delays entre as requisições para simular o comportamento humano. Isso reduz a chance de detecção e bloqueio por firewalls e sistemas de proteção de sites.
   - Delays aleatórios são melhores que delays constantes, pois adicionam variabilidade ao padrão de scraping.

### 4. **Rotação de Proxies e IPs**
   - Use proxies para alternar entre diferentes IPs e evitar que um único IP seja bloqueado por excesso de requisições.
   - Proxies rotativos ou serviços de proxy dedicados são mais eficazes para grandes volumes de scraping.

### 5. **Gerenciamento de Sessão**
   - Use cookies e gerencie sessões para simular um usuário contínuo. Isso pode ser útil para acessar áreas que exigem login ou que exibem informações diferentes com base na sessão do usuário.
   - Mantenha cookies válidos e renove-os conforme necessário para evitar quebras no fluxo de scraping.

### 6. **Manter o Código Flexível para Mudanças no Site**
   - Estruture o código de scraping para que ele seja fácil de atualizar caso o layout ou os seletores do site mudem.
   - Considere usar técnicas de scraping baseadas em **XPath** ou **CSS Selectors**, com scripts configuráveis para facilitar a manutenção e atualização do código.

### 7. **Lidar com Requisições e Respostas de Erro**
   - Implemente um sistema para detectar e lidar com erros de conexão, como HTTP 403 (Proibido), 404 (Não Encontrado), e 429 (Muitas Requisições).
   - Recoloque as requisições que falharem e implemente limites para o número de tentativas de reenvio.

### 8. **Agendamento e Limite de Requisições**
   - Se estiver fazendo scraping em grande escala, distribua as requisições ao longo do tempo e evite sobrecarregar o servidor do site.
   - Use **ferramentas de agendamento** (como `cron jobs` em sistemas Unix) para automatizar e escalonar seu processo de scraping.

### 9. **Uso de Selenium e Headless Browsers com Moderação**
   - Ferramentas como **Selenium** são úteis para interagir com sites dinâmicos, mas são mais lentas e pesadas que métodos de scraping direto com **requests** e **BeautifulSoup**.
   - Headless browsers devem ser usados apenas quando necessário, como em sites com JavaScript complexo que requer interação.

### 10. **Limpar e Armazenar Dados de Forma Estruturada**
   - Organize os dados extraídos em estruturas padronizadas, como **DataFrames**, **JSON**, ou **bancos de dados**, para facilitar o processamento e análise futura.
   - Verifique e normalize os dados para garantir que as informações estejam completas e sejam consistentes.

### 11. **Lidar com Captchas e Outros Mecanismos de Segurança**
   - Para sites com captchas, considere técnicas como **OCR** (Reconhecimento Óptico de Caracteres) ou soluções de terceiros, como **2Captcha** e **Anti-Captcha**.
   - Sempre que possível, evite sites com proteções complexas que possam dificultar a extração automatizada.

### 12. **Documentar o Código e Processo**
   - Documente o código e o processo de scraping para ajudar na manutenção futura e para que outras pessoas possam entender o fluxo.
   - Inclua comentários no código explicando a lógica principal, e mantenha um registro de quaisquer seletores, cabeçalhos ou configurações importantes.

### 13. **Monitoramento e Alerta de Mudanças no Site**
   - Implemente notificações que alertem quando o processo de scraping falha ou quando a estrutura do site muda, causando problemas de extração.
   - Ferramentas de monitoramento, como o **Pingdom** ou **UptimeRobot**, podem ser úteis para verificar se um site está acessível e funcionando conforme esperado.

### 14. **Utilizar API Quando Disponível**
   - Se o site oferecer uma **API pública**, use-a em vez de scraping direto no site. APIs são mais estáveis, e o uso delas geralmente é permitido, desde que em conformidade com os limites de uso.
   - APIs também fornecem dados em formatos estruturados, como **JSON** ou **XML**, facilitando o processamento.

### 15. **Considerações Legais e Éticas**
   - Sempre respeite as leis e regulamentos locais relacionados a web scraping, e siga práticas éticas na coleta de dados.
   - Não colete informações pessoais sem permissão, e esteja ciente de regulamentações como o **GDPR** (na União Europeia) e o **CCPA** (na Califórnia, EUA) para proteger a privacidade dos usuários.

## Bibliotecas Python essenciais para **Web Scraping**:

### 1. **BeautifulSoup** [Link](https://pypi.org/project/beautifulsoup4/): 
   - Facilita a extração de dados de arquivos HTML e XML. Permite navegar, buscar e modificar a estrutura da página de forma eficiente.
   - **Uso comum**: Analisar o conteúdo HTML e extrair informações específicas, como tags e atributos.

### 2. **Requests** [Link](https://requests.readthedocs.io/en/latest/): 
   - Simples e poderosa para fazer requisições HTTP. Permite obter o conteúdo de páginas web de forma fácil e segura.
   - **Uso comum**: Baixar o HTML de uma página, essencial para iniciar o processo de scraping.

### 3. **Selenium** [Link](https://selenium-python.readthedocs.io/index.html):
   - Uma ferramenta de automação de navegadores que pode ser usada para interagir com páginas dinâmicas (JavaScript).
   - **Uso comum**: Realizar scraping em sites com conteúdo carregado dinamicamente, como clicar em botões e rolar páginas.

### 4. **Pandas** [Link](https://pandas.pydata.org/): 
   - Biblioteca poderosa para manipulação e análise de dados tabulares.
   - **Uso comum**: Organizar e estruturar os dados extraídos de páginas web em formatos como DataFrames, facilitando a análise.

### 5. **lxml**: 
   - Uma biblioteca rápida para processar e manipular documentos XML e HTML.
   - **Uso comum**: Alternativa ao BeautifulSoup para parsing de HTML, especialmente quando o desempenho é um fator importante.

