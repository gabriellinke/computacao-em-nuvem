Deploy
======

Nesta seção, abordaremos os passos necessários para realizar o deploy da aplicação web CRUD no servidor configurado.

1. **Configurações de SSH e Git**:
   - Configure as chaves SSH e o acesso ao Git para clonar o repositório do GitHub que contém o código da aplicação.

2. **Obtenção do Código Fonte**:
   - Clone o repositório do GitHub que contém o código da aplicação. O código está disponível em: `https://github.com/gabriellinke/computacao-em-nuvem`

3. **Configuração das Credenciais do Banco de Dados**:
   - Adicione as credenciais necessárias para conectar a aplicação ao banco de dados MySQL configurado anteriormente. Isso pode ser feito modificando o arquivo `config.php`.

4. **Criação das Tabelas no Banco de Dados**:
   - Conecte-se ao banco de dados e execute os scripts SQL (`company.sql`) para criar as tabelas necessárias.

5. **Disponibilização no Nginx**:
   - Copie os arquivos da aplicação para a pasta configurada no Nginx (`/var/www/html/`) para que sejam servidos pelo servidor web.

Este processo garantirá que a aplicação esteja pronta para ser acessada e utilizada conforme configurado no ambiente de produção.
