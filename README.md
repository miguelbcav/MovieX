# MovieX

MovieX é um aplicativo de exibição de filmes e vídeos, criado com **Python** e utilizando **Flet**, uma biblioteca para construção de interfaces gráficas, e **Baserow** como banco de dados para armazenar e recuperar informações sobre filmes. A aplicação exibe uma lista de filmes com suas capas e, ao clicar em um filme, exibe o vídeo associado, juntamente com informações adicionais como a sinopse.

## 🚀 Funcionalidades

- **Visualização de filmes**: Exibe uma lista de filmes com informações como nome, capa, sinopse e link para o vídeo.
- **Navegação intuitiva**: A interface permite navegar entre a lista de filmes e a página de exibição do vídeo, com uma transição suave entre as telas.
- **Carregamento assíncrono**: A aplicação carrega os filmes e vídeos de forma assíncrona para garantir desempenho e uma experiência de usuário sem interrupções.
- **Integração com Baserow**: Todos os dados dos filmes são armazenados e recuperados de uma tabela no Baserow.

## 📋 Pré-requisitos

Para rodar o projeto, você precisará do seguinte:

- **Python 3.8+**
- **Bibliotecas**: A aplicação utiliza várias bibliotecas Python, incluindo `flet`, `aiohttp`, e `asyncio`.
- **Conta no Baserow**: A aplicação se conecta a uma tabela de banco de dados Baserow para carregar os dados dos filmes.

## 🛠️ Como rodar o projeto

### Passo 1: Clone o repositório

Clone o repositório para sua máquina local:

```bash
git clone https://github.com/seu-usuario/moviex.git
cd moviex
Passo 2: Crie e ative um ambiente virtual (opcional, mas recomendado)
Crie um ambiente virtual para isolar as dependências do projeto:

bash
Copiar código
python -m venv venv
Ative o ambiente virtual:

No Windows:
bash
Copiar código
.\venv\Scripts\activate
No Linux/MacOS:
bash
Copiar código
source venv/bin/activate
Passo 3: Instale as dependências
Instale as dependências do projeto usando o pip:

bash
Copiar código
pip install -r requirements.txt
O arquivo requirements.txt deve conter as dependências necessárias para o projeto, como flet, aiohttp, e outras.

Passo 4: Configure a conexão com o Baserow
No código, o token de autenticação e o table_id do Baserow são fornecidos como variáveis:

python
Copiar código
TOKEN = "RytmH5pJHn6kAFQi2HRpSaGh0og8V0LW"
table_id = 338693
Você precisa garantir que essas variáveis contenham o token de API correto e o ID da tabela onde os dados dos filmes estão armazenados. Para obter essas informações, crie uma conta no Baserow e configure sua tabela com os campos necessários para os filmes, como:

Nome: Nome do filme
Capa: URL da capa do filme
Link: URL do vídeo
Sinopse: Descrição do filme
Passo 5: Execute a aplicação
Após configurar o ambiente e as dependências, execute a aplicação com o seguinte comando:

bash
Copiar código
python main.py
A aplicação será aberta em seu navegador no endereço http://localhost:8501.

🖥️ Como funciona
A aplicação utiliza a biblioteca Flet para criar a interface gráfica, e a biblioteca Aiohttp para realizar requisições assíncronas à API do Baserow, recuperando as informações sobre os filmes armazenadas no banco de dados.

Carregamento Assíncrono: O carregamento dos filmes e vídeos é feito de forma assíncrona com Aiohttp e Asyncio, o que melhora a performance, especialmente em grandes listas de filmes.
Integração com o Baserow: Os dados dos filmes são recuperados diretamente de uma tabela no Baserow através da API. A aplicação faz uma requisição para cada linha da tabela e carrega os dados como nome, capa, link de vídeo e sinopse.
Navegação no App
Tela Inicial: Exibe uma lista de filmes com suas capas. Ao clicar em um filme, o vídeo é carregado em uma nova página.
Página do Vídeo: Mostra o vídeo do filme, junto com o nome, sinopse e outros detalhes.
🎨 Personalização
Você pode personalizar a aparência da aplicação modificando o código de interface do usuário. A aplicação usa o modo dark para a interface, mas você pode facilmente mudar isso ajustando as configurações de tema no Flet.

📂 Estrutura do Projeto
A estrutura do projeto é a seguinte:

bash
Copiar código
moviex/
│
├── main.py          # Código principal da aplicação
├── requirements.txt # Dependências do projeto
├── assets/          # Pasta para armazenar arquivos estáticos como imagens
└── README.md        # Este arquivo
📝 Licença
Este projeto está licenciado sob a MIT License.

💬 Como Contribuir Faça um fork do repositório. Crie uma nova branch (git checkout -b minha-contribuicao). Faça suas modificações e commit. Push para a branch (git push origin minha-contribuicao). Abra uma pull request. 📚 Mais Informações 🎓 Curso FLET 360 Python: Aprofunde-se no Python e na construção de interfaces gráficas com o Flet! 👉 https://go.hotmart.com/J91353466S?dp=1
