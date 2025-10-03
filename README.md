# 📘 Criação de Máquinas Virtuais na Azure  

Este repositório demonstra como criar e gerenciar **Máquinas Virtuais (VMs)** na **Microsoft Azure**, utilizando o **Azure CLI** para provisionamento e configuração.  

---

## 🔹 Objetivos  
- Aprender os conceitos básicos de **Máquinas Virtuais na Azure**.  
- Criar, configurar e acessar uma VM Linux na nuvem.  
- Aplicar boas práticas de segurança (SSH, firewall e NSG).  
- Servir como guia inicial para estudos de **Computação em Nuvem**.  

---

## 🛠️ Tecnologias e Ferramentas Utilizadas  
- **Microsoft Azure**  
- **Azure CLI** (`az`)  
- **SSH** (para acesso remoto)  

---

## 🚀 Passo a Passo para Criação de uma VM na Azure  

### 1️⃣. Criar um Grupo de Recursos  
Um **Resource Group** é um container lógico para organizar recursos da Azure.  

az group create --name MeuGrupoRecursos --location eastus

### 2️⃣. Criar a Máquina Virtual
Aqui será criada uma VM Ubuntu LTS com usuário azureuser e chave SSH gerada automaticamente.

az vm create \
  --resource-group MeuGrupoRecursos \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys

### 3️⃣. Abrir Porta para Acesso Remoto
Para permitir conexão via SSH (porta 22):

az vm open-port --port 22 --resource-group MeuGrupoRecursos --name MinhaVM

## 4️⃣. Conectar-se à VM
Após a criação, a Azure fornece o IP público da VM.
Use o comando abaixo para acessar:

ssh azureuser@IP_Publico_Da_VM

### Boas Práticas de Segurança

Preferir autenticação com chaves SSH em vez de senha.
Usar NSG (Network Security Group) para controlar o tráfego de rede.
Manter a VM sempre atualizada com patches de segurança.
Habilitar Monitoramento (Azure Monitor, Log Analytics).
