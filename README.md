# 📋 Descrição da Tarefa

Este projeto tem como objetivo a instalação e configuração da ferramenta de monitoramento **Zabbix**. A atividade está dividida em duas etapas principais:

## Etapa 1 – Instalação do Zabbix

Nesta fase, será demonstrado que o Zabbix foi corretamente instalado e está operacional no ambiente.

## Etapa 2 – Monitoramento de Dispositivos

Após a instalação, serão configurados dois dispositivos distintos para serem monitorados pelo Zabbix. Essa etapa comprova a funcionalidade prática da ferramenta.

O objetivo final é garantir que o Zabbix esteja instalado, funcionando corretamente e monitorando os dois dispositivos definidos no escopo da tarefa.

## 🚀 Como Fazer Funcionar

# ETAPA 1

### 1. **Instalar o Docker Desktop**

* Baixe e instale o [Docker Desktop](https://www.docker.com/products/docker-desktop) em sua máquina.

### 2. **Iniciar o Docker Desktop**

* Abra o Docker Desktop e certifique-se de que o Docker está em execução.

### 3. **Limpeza de Containers e Volumes (opcional, mas recomendada)**

Antes de rodar o projeto, é uma boa prática garantir que o ambiente Docker esteja limpo.
**Atenção**: os comandos abaixo removerão todos os containers e volumes existentes.

No terminal, onde o arquivo `docker-compose.yml` está localizado, execute os comandos abaixo:

```bash
docker system prune
docker system prune -a --volumes
```

### Rodar o Projeto

Após garantir que o ambiente esteja limpo, execute o seguinte comando para rodar o projeto:

```bash
docker-compose up --build
```

Acesse em: [http://localhost:8080](http://localhost:8080)
Login padrão:
Usuário: **Admin**
Senha: **zabbix**

# Configurações Para ETAPA 2

## Dependências

* O Zabbix no servidor está na versão **7.2**
* O Zabbix Agent na máquina monitorada está na versão **6.0**

Instale a versão do Agent na máquina que será monitorada:
👉 [https://www.zabbix.com/br/download\_agents](https://www.zabbix.com/br/download_agents)

![image](https://github.com/user-attachments/assets/34d936e0-b580-4bda-9807-30422998cc9b)

Mantenha estas configurações:
![image](https://github.com/user-attachments/assets/791cb91e-0f93-4e90-a42d-e10fe6a36e0f)

**Faça o download do Agent (não o Agent 2):**
![image](https://github.com/user-attachments/assets/bf73fd19-1fbb-4525-ac0e-acf9117be53a)

No instalador, clique em *Next* até chegar à seguinte tela:
![image](https://github.com/user-attachments/assets/62057bd6-3203-4c0c-86b4-6d86a777ea3f)

Preencha com o nome do host que será monitorado e o IP da máquina onde está o servidor (Zabbix Server).



### Na interface do Zabbix ([http://localhost:8080](http://localhost:8080)):

1. Vá em **Data Collection** -> **Host groups** -> **Create host group**
   Adicione conforme a tela abaixo:
   ![image](https://github.com/user-attachments/assets/7cc6f1b0-7fea-494f-9f32-9fa54e59d086)

2. Ainda em **Data Collection** -> **Hosts** -> **Create Host**

   * *Host Name* deve ser o nome definido durante a instalação do Zabbix Agent na máquina monitorada.
     ![image](https://github.com/user-attachments/assets/298d7d9d-c638-46f9-ab67-c981f32527dd)

3. No *Template*, selecione exatamente como mostrado, utilizando **Windows by Zabbix agent**:
   ![image](https://github.com/user-attachments/assets/881d9d43-7be1-4564-bef0-6e495a0b898c)

4. O *Host Group* ficará assim:
   ![image](https://github.com/user-attachments/assets/0e947a03-d748-42d3-b9a1-246f2a9641b2)

5. Adicione a interface da máquina que está sendo monitorada, com o IP correspondente:
   ![image](https://github.com/user-attachments/assets/0e1d592f-7447-4cb8-aa82-43bdf6cfd526)



# Verificando o Monitoramento

Vá na opção **Monitoring** -> **Hosts** -> **Graphs** da máquina que foi adicionada.

Nos gráficos, é possível monitorar a máquina, como por exemplo a utilização da CPU.

Na imagem abaixo, a máquina está desligada:
![image](https://github.com/user-attachments/assets/bef2445d-bfef-41a3-a46c-04d972106f4c)

Após ligar a máquina e iniciar alguns processos:
![image](https://github.com/user-attachments/assets/ec13f0c2-383d-4965-a0da-2154e7bcea8a)

# Verificando em uma segunda máquina
![image](https://github.com/user-attachments/assets/7bcaa29c-e3b0-48e2-92f3-729dd796bd24)
![image](https://github.com/user-attachments/assets/ce1ec9bd-6c30-4b17-a786-3bd606deb5bc)


## Contribuidores
Luis Eduardo

Francisco Aparício

Victor Macêdo
