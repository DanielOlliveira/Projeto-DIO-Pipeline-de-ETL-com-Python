# Projeto DIO - Pipeline de ETL com Python

Este projeto foi desenvolvido como parte de um desafio da **Digital Innovation One (DIO)** e tem como objetivo construir um **pipeline de ETL (Extract, Transform, Load)** utilizando Python, Google Colab e a API da Cohere para geração de mensagens personalizadas.

---

## 🚀 Objetivo
O projeto demonstra como:
- Extrair dados de um arquivo CSV contendo informações de usuários.
- Transformar os dados com enriquecimento de mensagens personalizadas usando IA (Cohere).
- Carregar os dados transformados em um novo dataset pronto para análise ou integração.

---

## 🛠️ Tecnologias Utilizadas
- **Python 3**
- **Pandas** para manipulação de dados
- **Google Colab** como ambiente de execução
- **Cohere API** (`co.chat` e `co.generate`) para geração de mensagens personalizadas
- **Git/GitHub** para versionamento e compartilhamento do projeto
- **gdown** para baixar arquivos do Google Drive para o ambiente local

---

## 📂 Estrutura do Projeto
- `usuarios.csv` → Arquivo de entrada com dados dos usuários (ID, Nome, Conta, Cartão, Interesses).
- `Projeto_Pipeline_ETL_Python.ipynb` → Notebook principal com todo o pipeline ETL.
- `README.md` → Documentação do projeto.

---

## 🔄 Pipeline ETL
1. **Extract**  
   - Leitura do arquivo `usuarios.csv` com Pandas.

2. **Transform**  
   - Criação de mensagens personalizadas para cada usuário, considerando seus interesses.  
   - Uso da API da Cohere para gerar textos amigáveis e práticos.  
   - Ajustes de parâmetros como `temperature` e `max_tokens` para controlar criatividade e tamanho das respostas.

3. **Load**  
   - Geração de um novo DataFrame com a coluna `Mensagem_Personalizada`.  
   - Exportação dos dados transformados para análise ou integração futura.

---

## 📌 Como Executar
1. Clone este repositório:
   ```bash
   git clone https://github.com/DanielOlliveira/Projeto-DIO-Pipeline-de-ETL-com-Python.git

2. Abra o notebook no Google Colab ou Jupyter.

3. Instale as dependências:
  !pip install cohere gdown pandas

4. Configure sua chave da Cohere:
  co = cohere.Client("SUA_API_KEY_AQUI")

5. Execute as células para rodar o pipeline completo.

📊 Exemplo de Saída

| ID | Nome | Interesses | Mensagem_Personalizada |
| --- | --- | --- | --- |
| 1 | Ana | investimentos, viagens | Olá Ana! Aqui vão 3 dicas... |
| 2 | Bruno | tecnologia, esportes | Olá Bruno! Pensando nos seus interesses... |

📖 Aprendizados
Diferença entre co.chat (respostas curtas e conversacionais) e co.generate (respostas mais longas e detalhadas).

Importância de ajustar o prompt para controlar o tamanho e formato das respostas.

Uso do gdown para baixar arquivos do Google Drive sem precisar montar o drive no Colab.

Integração do Colab com GitHub para versionamento e compartilhamento do projeto.

👨‍💻 Autor
Projeto desenvolvido por Daniel Oliveira como parte do desafio da DIO.
