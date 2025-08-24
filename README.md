***Agente de IA para Análise de Dados***
---

Este repositório é um clone do projeto original disponível em [[REPOSITÓRIO_ORIGINAL](https://github.com/vqrca/projeto-langchain)], utilizado exclusivamente para fins de aprendizado e exploração de conceitos de agentes de inteligência artificial aplicados à análise de dados.

O objetivo é estudar a estrutura, o funcionamento e as técnicas utilizadas no projeto original, bem como realizar experimentações e adaptações conforme necessário para aprofundar o entendimento dos métodos envolvidos.

📊 ***O que é esse projeto?***

Este projeto é uma ferramenta interativa de análise de dados com IA construída com Streamlit + LangChain + LLaMA 3, que permite:

- Carregar um arquivo .csv
- Fazer perguntas sobre os dados em linguagem natural
- Gerar relatórios e visualizações automaticamente
- Utilizar o poder dos LLMs para explorar os dados com agilidade
- Ideal para analistas de dados, cientistas, profissionais de BI ou qualquer pessoa que queira entender seus dados rapidamente com ajuda de IA.

🧠 ***O que é um LLM (Large Language Model)?***

Um LLM (Large Language Model) é um modelo de linguagem treinado com grandes volumes de texto, capaz de compreender e gerar linguagem natural de forma autônoma. No projeto, utilizamos o modelo LLaMA 3 da Meta, acessado via a plataforma Groq, que oferece respostas rápidas e custo-benefício competitivo.
Esses modelos são utilizados para interpretar perguntas dos usuários, gerar relatórios, escrever código Python e até criar visualizações de dados automaticamente.

🔗 ***O que é o LangChain?***

LangChain é um framework que facilita a criação de aplicações que combinam modelos de linguagem (LLMs) com ferramentas externas, como bancos de dados, APIs, arquivos e scripts Python.
Ele permite criar agentes inteligentes capazes de raciocinar, escolher ações, executar código e retornar respostas complexas em linguagem natural, com base nos dados disponíveis.

🤖 ***O que é um Agente LangChain?***

Um Agente LangChain é uma estrutura que permite ao LLM tomar decisões de forma autônoma. Ele funciona como um "assistente de IA" que:

- Recebe uma pergunta ou comando do usuário
- Analisa o contexto
- Escolhe uma ou mais ferramentas para executar tarefas
- Processa as respostas dessas ferramentas
- E devolve um resultado final em linguagem natural

No projeto, o agente decide automaticamente se deve gerar um relatório, fazer um cálculo, criar um gráfico ou simplesmente responder usando o LLM.

🛠️ ***O que são Ferramentas no LangChain?***

Ferramentas são funções externas que o agente pode utilizar para cumprir tarefas específicas. No projeto, definimos 4 ferramentas principais:

- Informações do DataFrame – Gera um relatório com tipos, colunas, dados nulos, duplicados e sugestões.
- Resumo Estatístico – Analisa colunas numéricas com média, desvio, outliers, etc.
- Geração de Gráficos – Cria visualizações automáticas com seaborn/matplotlib a partir de descrições em linguagem natural.
- Execução de Código Python – Permite cálculos, filtros e consultas diretamente via código Python gerado pelo LLM.

🛠️ ***Tecnologias utilizadas:***

- Python 3.10+
- LangChain
- Groq (LLaMA 3 70B)
- Streamlit – Interface web simples e interativa
- pandas, matplotlib, seaborn – Manipulação e visualização de dados
- dotenv – Gestão de chaves de API com segurança

## 🚀 Aplicação
 [**Acesse a aplicação online aqui**](https://agente-ia-dados.streamlit.app/)

Ou execute localmente:
```bash
   streamlit run streamlit-app.py
```

## 💻 Como Executar

1- Clone o repositório:
```bash
   git clone https://github.com/rugellioliveira/Agente-de-IA-para-Analise-de-Dados.git
```
2- Instale as dependências:
```bash
   pip install -r requirements.txt
```
🔐 Configuração da Chave de API (GROQ)

Para utilizar este projeto, é necessário configurar uma chave de API do Groq
. Siga os passos abaixo:

- Crie um arquivo chamado .env na raiz do projeto, se ainda não existir.

- Acesse https://console.groq.com/keys
 e gere sua chave de API.

- Adicione a seguinte linha no arquivo .env, substituindo "SUA_CHAVE_AQUI" pela chave que você obteve:
```bash
GROQ_API_KEY=SUA_CHAVE_AQUI
```

- Abra o arquivo ferramentas.py e verifique se a chave está sendo lida corretamente com a linha:
```bash
GROQ_API_KEY=os.getenv("GROQ_API_KEY")
```

🔁 Caso esteja utilizando o projeto no Streamlit Cloud, lembre-se de adicionar a variável GROQ_API_KEY na aba Secrets com o mesmo valor.
