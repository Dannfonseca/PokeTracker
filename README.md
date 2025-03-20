# Sistema de Gerenciamento de Pokémons

Este projeto é um sistema de gerenciamento de Pokémons desenvolvido para a mansão do Raito. Ele permite o controle de Pokémons por clãs, o registro de uso de Pokémons por treinadores, e a devolução dos mesmos. O sistema é composto por uma API backend em Node.js com Express e um banco de dados SQLite, além de uma interface frontend em HTML, CSS e JavaScript.

## 📌 Principais Funcionalidades

### 1. **Gerenciamento de Clãs e Pokémons**
   - Visualização de Pokémons disponíveis por clã.
   - Adição de novos Pokémons a um clã específico.
   - Seleção de múltiplos Pokémons para uso.

### 2. **Registro de Uso de Pokémons**
   - Registro de Pokémons emprestados por treinadores.
   - Visualização de Pokémons atualmente em uso.

### 3. **Devolução de Pokémons**
   - Devolução de Pokémons individualmente ou em grupo.
   - Histórico de devoluções.

### 4. **Histórico Completo**
   - Visualização de todo o histórico de uso de Pokémons.
   - Filtragem por status (em uso, devolvidos).
   - Deleção de registros individuais ou de todo o histórico.

### 5. **Interface Amigável**
   - Design responsivo e intuitivo.
   - Navegação fácil entre clãs e seções do sistema.

---

## 🛠 Como Instalar e Rodar na Máquina

### 🔹 **Pré-requisitos**

- Node.js (versão 14 ou superior)
- NPM (geralmente vem com o Node.js)

### 🔹 **Passos para Instalação**

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/sistema-pokemon.git
   cd sistema-pokemon
   ```
2. **Instale as dependências**:
   ```bash
   npm install
   ```
3. **Inicie o servidor**:
   ```bash
   npm start
   ```
4. **Acesse a aplicação**:
   - Abra o navegador e acesse `http://localhost:3000`.

---

## 📂 Estrutura do Projeto

- `database.js`: Configuração do banco de dados SQLite e criação das tabelas necessárias.
- `index.js`: Servidor Express com todas as rotas da API.
- `index.html`: Interface do usuário.
- `script.js`: Lógica do frontend, interação com a API e manipulação do DOM.
- `styles.css`: Estilos CSS para a interface do usuário.

---

## 🔗 Rotas da API

### 🔹 **Histórico**
- `POST /history` → Registra o uso de múltiplos Pokémons por um treinador.
- `GET /history` → Retorna todo o histórico de uso de Pokémons.
- `GET /history/active` → Retorna os Pokémons atualmente em uso.
- `PUT /history/:id/return` → Marca um Pokémon como devolvido pelo ID.
- `PUT /history/group/:groupId/return` → Marca um grupo de Pokémons como devolvido por treinador e data.
- `DELETE /history/:id` → Deleta um item específico do histórico pelo ID.
- `DELETE /history` → Deleta todo o histórico.
- `DELETE /history/trainer/:trainer/date/:date` → Deleta um grupo de registros do histórico por treinador e data.

### 🔹 **Clãs e Pokémons**
- `GET /clans/:clan/pokemons` → Retorna a lista de Pokémons de um clã específico.
- `POST /clans/:clan/pokemons` → Adiciona um Pokémon a um clã.

---

## 📌 Exemplos de Uso

### ➕ **Adicionar um Pokémon a um clã**
1. Navegue até a seção do clã desejado.
2. Insira o nome do Pokémon no campo de texto e clique em "Adicionar Pokémon".
3. Insira a senha `raito123` quando solicitado.

### 📝 **Registrar o uso de Pokémons**
1. Selecione os Pokémons desejados na lista.
2. Insira o nome do treinador e clique em "Confirmar Seleção".

### 🔄 **Devolver Pokémons**
1. Na seção de Pokémons em uso, clique em "Devolver" ao lado do grupo desejado.
2. Escolha se deseja devolver todos os Pokémons ou apenas alguns específicos.

### 📜 **Visualizar Histórico**
1. Clique no botão "Histórico" no cabeçalho.
2. Use os filtros para visualizar Pokémons em uso, devolvidos ou todo o histórico.

---

## 🎯 Considerações Finais

Este sistema foi desenvolvido para facilitar o gerenciamento de Pokémons em um ambiente controlado, como a mansão do Raito. Ele oferece uma interface simples e eficiente para registrar e monitorar o uso de Pokémons, além de permitir a devolução e a exclusão de registros quando necessário.

Para qualquer dúvida ou sugestão, sinta-se à vontade para abrir uma issue no repositório ou entrar em contato diretamente. 🚀
