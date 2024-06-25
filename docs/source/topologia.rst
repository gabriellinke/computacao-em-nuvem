Topologia da Aplicação
======================

Neste documento, discutiremos a topologia da aplicação e as máquinas virtuais necessárias para hospedar toda a aplicação.

Máquinas Necessárias
--------------------

1. **Servidor CA**: Gerencia os certificados de autenticação.
2. **Servidor DNS**: Gerencia as configurações de DNS para a aplicação.
3. **Servidor OpenStack**: Hospeda as máquinas virtuais da aplicação.
   - **Servidor Web no OpenStack**: Hospeda o servidor da aplicação web.
   - **Servidor Banco de Dados no OpenStack**: Armazena os dados da aplicação.

Detalhes das Máquinas Virtuais
------------------------------

### Servidor CA

- Sistema Operacional: Ubuntu 22.04
- Recursos: 1 CPU, 1GB RAM, 10GB de armazenamento
- Funções: Gerenciar certificados de autenticação para a aplicação.

### Servidor DNS

- Sistema Operacional: Ubuntu 22.04
- Recursos: 1 CPU, 1GB RAM, 10GB de armazenamento
- Funções: Gerenciar registros DNS para a aplicação.

### Servidor OpenStack

- Sistema Operacional: Ubuntu 22.04
- Recursos: 4 CPUs, 8GB RAM, 80GB de armazenamento
- Funções: Hospedar as máquinas virtuais da aplicação (servidor web e servidor de banco de dados).

#### Servidor Web no OpenStack

- Sistema Operacional: Ubuntu 22.04
- Recursos: Configurado dentro do ambiente OpenStack
- Funções: Servir a aplicação web.

#### Servidor Banco de Dados no OpenStack

- Sistema Operacional: Ubuntu 22.04
- Recursos: Configurado dentro do ambiente OpenStackOutra 
- Funções: Armazenar os dados da aplicação.
