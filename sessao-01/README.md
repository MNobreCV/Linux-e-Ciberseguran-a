<h1> Laboratório — Sessão 1 </h1>

<h2> Introdução ao Linux para Segurança e Comandos de Rede </h2>

Curso   | Reskilling
--------- | ----------
Modulo  | Linux e Cibersegurança
Formador| Péricles Borges
Formando| Mauro Nobre
Laboratório | Sessão 01

<h3> Contexto </h3>

> Mapeamento e análise da superfície de exposição de um servidor alvo na rede local. Nesta sessão assume o papel de auditor de sistemas: o objetivo é identificar a interface de rede do próprio ambiente, listar os serviços em escuta e, de seguida, mapear um alvo remoto com o Nmap.

<h3> Ambiente Virtual </h3>

+ > KillerCoda Ubuntu Playground — terminal Linux gratuito no browser, sem instalação: https://killercoda.com/playgrounds/scenario/ubuntu

+ > TryHackMe — Further Nmap (gratuito): https://tryhackme.com/room/ furthernmap

<h3> tarefas a executar </h3>

+ > Aceder ao KillerCoda Ubuntu Playground para familiarização com o CLI

+ > Executar o comando e identificar o endereço IP da interface principal: ip a

+ > Usar o comando para listar todos os portos abertos em escuta no ambiente local: ss-tuln

+  > Aceder à sala TryHackMe Further Nmap e iniciar a máquina alvo

+  > Executar um scan básico Nmap contra o alvo fornecido, com deteção de versões e scripts padrão: nmap-sV-sC <IP_DO_ALVO>

<h3> Critérios de Entrega </h3>

1. Número de portas abertas identificadas: 5 portas

2. Serviços em execução em cada porta:

PORT   | SERVICE
------ | ----------
21     | FTP
53     | DOMAIN
80     | HTTP
135    | MSRPC
3389   | MS-WBT-SERVER

3. Versões exatas detetadas pelo Nmap:

PORT     | VERSION
---------|---------
21/tcp   | FileZilla 
ftpd     | 53/tcp Simple DNS Plus 
80/tcp   | Microsoft IIS httpd 10.0 
135/tcp  | Microsoft Windows RPC 
3389/tcp | Microsoft Terminal Services

