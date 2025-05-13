# 📋 Descrição da Tarefa
Este projeto tem como objetivo a instalação e configuração da ferramenta de monitoramento Zabbix. A atividade é dividida em duas etapas principais:

## Etapa 1 – Instalação do Zabbix
Nesta fase, será demonstrado que o Zabbix foi corretamente instalado e está operacional no ambiente.

## Etapa 2 – Monitoramento de Dispositivos
Após a instalação, serão configurados dois dispositivos distintos para serem monitorados pelo Zabbix. Essa etapa comprova a funcionalidade prática da ferramenta.

O objetivo final é garantir que o Zabbix esteja instalado, funcionando corretamente e monitorando os dois dispositivos definidos no escopo da tarefa.

## 🚀 Como Fazer Funcionar

# ETAPA 1

### 1. **Instalar o Docker Desktop**
   - Baixe e instale o [Docker Desktop](https://www.docker.com/products/docker-desktop) em sua máquina.

### 2. **Iniciar o Docker Desktop**
   - Abra o Docker Desktop e certifique-se de que o Docker está em execução.

### 3. **Limpeza de Containers e Volumes (opcional, mas recomendado)**
   Antes de rodar o projeto, é uma boa prática garantir que o ambiente Docker esteja limpo. **Atenção**: os seguintes comandos removerão todos os containers e volumes existentes.

   No terminal, onde o arquivo `docker-compose.yml` está localizado, execute os comandos abaixo:

   ```
   docker system prune
   docker system prune -a --volumes

   ```
## Rodar o Projeto
Após garantir que o ambiente esteja limpo, execute o seguinte comando para rodar o projeto:

```
docker-compose up --build
```
Acessar em: http://localhost:8080
Login padrão:
   Usuário: Admin
   Senha: zabbix
   
# Configurações Para ETAPA 2

## Dependências
O zabbix no server está na versão 7.2
O Zabbix Agent na máquina monitorada está em 6.0

![image](https://github.com/user-attachments/assets/34d936e0-b580-4bda-9807-30422998cc9b)





