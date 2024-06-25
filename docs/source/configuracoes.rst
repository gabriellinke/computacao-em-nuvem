Configurações da Aplicação
==========================

Neste documento, detalharemos as configurações necessárias para o deploy da aplicação.

Configurações do Servidor CA
----------------------------

Caso o certificado seja criado apenas para desenvolvimento ou uso interno:

1. **Configuração da Autoridade Certificadora**:

   - Utilize a ferramenta easy-rsa para configurar a autoridade certificadora.
   - Crie o certificado da autoridade e instale-o no navegador para que ele seja reconhecido como confiável.


Configurações DNS e Certificado Digital
---------------------------------------

Servidor DNS:
~~~~~~~~~~~~~~~~~~~~~~

1. **Instalação do Bind9**:

   - Instale o Bind9, um software de servidor DNS amplamente utilizado.

2. **Configuração do Bind9**:

   - Edite o arquivo `named.conf.options` para permitir consultas da rede local e do multipass. Certifique-se de incluir as redes apropriadas, por exemplo `10.106.43.0/24` e `127.0.0.0/8`.
   - Crie um domínio editando o arquivo `named.conf.local`.
   - Configure os registros DNS no arquivo especificado na criação do domínio, por exemplo `db.linke-company.com`.

3. **Aplicação das Alterações**:

   - Reinicie o Bind9 para aplicar as novas configurações.

Certificado Digital:
~~~~~~~~~~~~~~~~~~~~~~

1. **Geração do Certificado**:

   - No servidor web, instale o easy-rsa para gerar o certificado.
   - Transfira o certificado gerado para a máquina da autoridade certificadora.

2. **Assinatura do Certificado**:

   - Na máquina da autoridade certificadora, assine o certificado utilizando a chave privada.
   - Devolva o certificado assinado para o servidor web.

3. **Configuração do Servidor Web**:

   - Utilize os certificados assinados na configuração do Nginx no servidor web para habilitar HTTPS.

Configurações do Banco de Dados
-------------------------------

1. **Instalação do MySQL Server**:

   - Instale o MySQL Server no servidor de banco de dados.

2. **Configuração do Banco de Dados**:

   - Crie um novo usuário e um banco de dados.
   - Conceda as permissões necessárias para o usuário no banco de dados criado.
   - Guarde as credenciais do usuário para uso futuro.

3. **Abertura da Porta 3306**:

   - Libere a porta 3306 para permitir que o servidor web possa se conectar ao banco de dados.

Configurações do Servidor Web
-----------------------------

1. **Instalação do Nginx e PHP**:

   - Instale o Nginx e PHP no servidor web.
   - Configure o Nginx para funcionar com o PHP, ajustando as configurações necessárias.

2. **Configuração do HTTPS**:

   - Configure o Nginx para funcionar com HTTPS utilizando o certificado e a chave gerados anteriormente.

3. **Instalação do PHP-MySQL**:

   - Instale a extensão PHP-MySQL para permitir a comunicação entre o PHP e o banco de dados MySQL.