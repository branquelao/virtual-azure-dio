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

### 1. Criar um Grupo de Recursos  
Um **Resource Group** é um container lógico para organizar recursos da Azure.  
```bash
az group create --name MeuGrupoRecursos --location eastus
