# Criando um Phishing com Kali Linux

> Exercício prático de Engenharia Social e Phishing com Social-Engineering Toolkit (SET)
> Curso Cybersecurity Specialist (Digital Innovation One)
> Autor: Samuel Luiz Lidio
> Data: 18/10/2026

## 📋 Objetivo

Tem como objetivo por em pratica os conhecimentos adquiridos em Engenharia Social e Kali Linux, na unidade de "Testes de Invasão e Busca por Vulnerabilidades" do curso voltado a segurança da Informação

## ⚠️ Escopo e Ética

- Exercício realizado **exclusivamente em ambiente isolado** (sem acesso à internet real)
- Nenhuma credencial real foi utilizada — apenas dados fictícios de teste
- Atividade realizada para fins educacionais, como parte da disciplina 

## 🔧 Passo a Passo

### 1. Preparação do ambiente
Ambas as maquinas foram configuradas na ferramenta Oracle VirtualBox conectadas em uma Rede Nat apenas para teste do exercício proposto 

### 2. Configuração do SET
Comando utilizado:
```
sudo setoolkit
```
Caminho no menu: `Social-Engineering Attacks` → `Website Attack Vectors` → `Credential Harvester Attack Method` → `Web Templates`

!(cibersecurity-desafio-phishing/menuSE.png)

### 3. Definição do IP de escuta
IP configurado: `192.168.56.101`

!(cibersecurity-desafio-phishing/serverIP.png)

### 4. Acesso simulado da vítima
!(cibersecurity-desafio-phishing/fake-site.png)

### 5. Envio de credenciais de teste
Dados fictícios utilizados: `usuário: maria@gmail.com` / `senha: maria123456`

### 6. Verificação da captura
!(cibersecurity-desafio-phishing/data-harvested.png)

## 🔍 Análise Técnica

**Como o ataque funciona:**
Essa ferramennta atua com técnicas de engenharia social onde um site ou domínio falso é hospedado em um servidor do atacante, esse domínio falso é acessado pela vitima omde a mesma insere suas credenciais e ao clicar para realizar o "login" seus dados são enviados para o servidordo atacante pelo listener e a vítima é redirecionada ao domínio oficial.

**Por que seria eficaz em um cenário real:**
Muitos individuos não se atentam a detalhes dos dominios que acessam, e a falta de uma verifiação de acesso adequada como MFA(Multi Factor Access) e uma grande semelhança com o domínio oficial pode facilitar a obtençao dos dados ilegalmente por criminosos por meio de ferramentas como essa. assim como falta de concientização dos usuarios com acesso a dados sensiveis.

**Limitações observadas no exercício:**
Exercício realizado em ambiente controlado sem acesso a rede externa, com maquinas virtuais sem configurações avançadas de segurança.

## 🛡️ Contramedidas e Recomendações

-  Autenticação multifator (MFA)
-  Treinamento de conscientização de usuários
-  Filtros de e-mail (SPF, DKIM, DMARC)
-  Verificação de URL/certificado antes de inserir credenciais

