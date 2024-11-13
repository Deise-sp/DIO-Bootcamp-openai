# DIO-Bootcamp-openai
Tradutor de artigos com o Openai

Nome do projeto: Extrator e tradutor de texto (Projeto Bootcamp)

Descrição:

Este projeto Python, criado durante um Bootcamp, fornece funcionalidades para extrair texto de um site e traduzir o conteúdo extraído usando um grande modelo de linguagem (LLM).

Características:

Extrai texto de uma determinada URL, removendo elementos desnecessários, como scripts e estilos.
Traduz o texto extraído para um idioma especificado usando o Azure Chat OpenAI.
Produz o texto traduzido no formato Markdown.
Instalação:

Instale as bibliotecas necessárias usando pip:

Bash

pip install requests beautifulsoup4 openai langchain-openai


Uso:

Substituir marcadores de posição:

Atualize as variáveis azure_endpoint​​, api_key, api_versione deployment_namedentro da AzureChatOpenAIclasse com sua configuração específica do Azure OpenAI (se você tiver uma). Você pode encontrar esses detalhes no seu painel do Azure OpenAI.
Execute o script:

Bash

python your_script_name.py


Substitua your_script_name.pypelo nome real do arquivo do seu script.

Explicação:

1. extrair_texto_de_url(url)

Busca o conteúdo da página da web usando requests.get(url).
Verifica a recuperação bem-sucedida com base no código de status (200).
Analisa o conteúdo HTML com BeautifulSoup.
Remove scripts e estilos para obter um texto mais limpo.
Extrai texto soup.get_text(separator= ' ')e o limpa por:
Removendo espaços extras usando remoção de linhas e palavras.
Unindo as partes limpas com novas linhas.

2. translate_article(texto, idioma)

Define prompts de conversação para o LLM, simulando uma interação do usuário.
Solicita tradução do idioma especificado ( lang) usando o AzureChatOpenAIcliente.
Imprime o conteúdo da resposta contendo o texto traduzido.
Observação:

Este código demonstra um exemplo básico usando o Azure Chat OpenAI. Você pode adaptá-lo para integrar com diferentes LLMs ou plataformas de nuvem, dependendo de seus requisitos.
Notas adicionais:
Esteja ciente dos limites de uso e custos associados a LLMs como o OpenAI.
