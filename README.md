# imersao-agentes-ia-alura
Criamos juntos um agente de IA especializado em tirar dúvidas sobre as políticas de uma empresa.

Assistente de Políticas Internas
Este projeto demonstra a criação de um assistente virtual utilizando Langchain e Google Gemini para triagem e resposta a perguntas sobre políticas internas de uma empresa, baseando-se em documentos PDF fornecidos.

Funcionalidades
Triagem de Mensagens: Classifica as perguntas dos usuários em categorias como AUTO_RESOLVER (resposta automática), PEDIR_INFO (necessita de mais informações) ou ABRIR_CHAMADO (requer abertura de chamado).
Resposta Baseada em Documentos (RAG): Utiliza a técnica Retrieval Augmented Generation (RAG) para buscar informações relevantes em documentos PDF e gerar respostas baseadas no contexto encontrado.
Interface Web com Gradio: Fornece uma interface web simples e interativa para que os usuários possam interagir com o assistente.
Tecnologias Utilizadas
Python
Langchain: Framework para desenvolvimento de aplicações com modelos de linguagem.
Google Gemini: Modelo de linguagem utilizado para triagem e geração de respostas.
Gradio: Biblioteca para criação rápida de interfaces web para modelos de Machine Learning.
PyMuPDF: Para carregamento de documentos PDF.
FAISS: Para criação e busca em vetores de documentos.
Langgraph: Para orquestração do fluxo do agente.
Como Executar
Configurar o Ambiente:

Certifique-se de ter o Python instalado.
Instale as bibliotecas necessárias executando os pip install presentes no notebook.
Obtenha uma chave de API do Google Gemini e configure-a no seu ambiente (por exemplo, usando as Secrets do Google Colab com o nome GEMINI_API_KEY).
Preparar os Documentos:

Coloque os arquivos PDF com as políticas internas na mesma pasta onde o notebook será executado (ou ajuste o caminho no código).
Executar o Notebook:

Execute todas as células do notebook sequencialmente.
A célula que lança a interface do Gradio irá gerar um link para acessar a interface web.
Estrutura do Código
O código está organizado em células que realizam as seguintes etapas:

Instalação das bibliotecas necessárias.
Configuração da API Key do Google Gemini.
Inicialização do modelo Gemini.
Definição do prompt e função para triagem.
Definição do modelo Pydantic para a saída da triagem.
Carregamento e processamento dos documentos PDF (splitting, embedding, vector store).
Configuração do RAG chain.
Definição dos nós e grafo do Langgraph para orquestrar o fluxo.
Definição da função para processar a pergunta e formatar a saída para o Gradio.
Criação e lançamento da interface do Gradio.
