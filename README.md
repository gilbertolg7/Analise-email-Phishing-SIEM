# Análise de alerta Phishing URL no SIEM da  LetsDefend 
## SOC 141 - Phishing URL Detected
![Tela do Alerta de Caso](/images/1.png)<br>
__Quando foi acessado?__ Mar, 22, 2021, 09:23 PM<br>
__Qual é o endereço de origem?__ 172.16.17.49<br>
__Qual é o endereço de destino?__ 91.189.114.8<br>
__Qual usuário tentou acessar?__ EmilyComp <br>
__O que é o User Agent?__ Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36<br>
__O pedido foi bloqueado?__ Allowed<br>

## Análise do URL Suspeito.
![Analise de URL Suspeito VirusToral ](/images/2.png)<br>
Como o URL Request foi constatado como permitido (Allowed) na análise do alerta primário e logs é necessário uma melhor investigação no Endpoint da possível vítima.

## Análise do Endpoint.
![Analise do Endpoint processo suspeito ](/images/3.png)<br>
Em análise dos processos do Endpoint  da possível vítima podemos identificar um processo suspeito.

## Análise do hash do Processo encontrado no Endpoint.
![Analise Hash processo ](/images/4.png)<br>
Ao analisar o hash MD5 do processo suspeito, o VirusTotal confirmou que se tratava de um malware/trojan, o que justificou as ações de isolamento.<br>

## Ações de Resposta ao Incidente
__Confinamento:__ O endpoint (EmilyComp) foi isolado da rede para mitigar a propagação do ataque.<br>
__Erradicação:__ A máquina será desinfectada para remover a ameaça.<br>
__Comunicação:__ O incidente foi reportado à gestão e à equipe de segurança.<br>
__Ações Pós-Incidente:__ Será providenciado treinamento de segurança para os colaboradores, com foco em conscientização sobre ataques de engenharia social.<br>
__Recomendação para aprimoramento de firewall:__ Devemos revisar as regras de bloqueios de URLs no Firewall da empresa e aprimorá-las com base no resultado dessa análise.<br>


