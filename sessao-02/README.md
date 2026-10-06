<h1> Laboratório — Sessão 2 </h1>

<h2> Auditoria de Sistemas Linux e Análise Avançada de Logs </h2>

Curso       | Reskilling
---------   | ----------
Modulo      | Linux e Cibersegurança
Formador    | Péricles Borges
Formando    | Mauro Nobre
Laboratório | Sessão 02

<h2> Contexto </h2>

> Um servidor da infraestrutura foi alvo de conexões anómalas. Atuará como analista forense para determinar a origem e o sucesso do ataque, com base na análise de logs de autenticação.

<h3> Ambiente Virtual </h3>

+ > TryHackMe — Intro to Logs (gratuito): https://tryhackme.com/room/introtologs 

+ > TryHackMe — Linux Server Forensics (gratuito): https://tryhackme.com/room/ linuxserverforensics

<h3> tarefas a executar </h3>

+ > Aceder ao laboratório Intro to Logs para compreender a mecânica dos registos do sistema 

+ > No lab Linux Server Forensics, navegar até à diretoria de logs do servidor comprometido: 
`cd /var/log/`

+ > Isolar tentativas falhadas de login: 
`grep "Failed password" auth.log`

+ > Extrair e contar quais os IPs que mais tentaram autenticar-se no sistema: 
`grep "Failed password" auth.log | awk '{print $11}' | sort | uniq -c | sort -nr`

+ > Identificar se o atacante obteve sucesso: 
`grep -E "Accepted password | Accepted publickey" auth.log`

<h3> Critérios de Entrega </h3>

1. O IP do atacante identificado

2. A hora exata do comprometimento (timestamp) 

3. O utilizador afetado Breve linha temporal do ataque (tentativas falhadas → sucesso