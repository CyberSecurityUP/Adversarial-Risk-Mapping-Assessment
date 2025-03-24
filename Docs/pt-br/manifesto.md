# 🛡️ **Manifesto da Metodologia A.R.M.A. - Adversarial Risk Mapping & Assessment**


## **Princípio 1 - Não somos operadores de ferramenta, somos comandantes de uma operação adversarial**
Pentest deixou de ser um checklist técnico. Nós conduzimos simulações adversariais com a mentalidade de um atacante real. Cada ação, cada exploração, cada movimento é pensado como um agente malicioso faria, visando o **impacto real** no negócio.

### 🔎 **Tópicos-Chave:**
- O mindset parte da estratégia, não da ferramenta.
- A execução só começa depois de entender **“quem eu seria se eu fosse o atacante”**.
- Nenhum ataque é feito sem uma narrativa: *“qual é meu objetivo e qual o plano para alcançá-lo?”*

### 💣 **Exemplos Práticos:**
- Antes de rodar um Burp ou Nmap, o pentester define: "Se eu fosse um grupo APT visando vazar dados financeiros para extorsão, o que eu faria primeiro?"
- Escolhe-se o vetor mais promissor para exploração, mesmo que exija **pivotagens complexas**.

---

## **Princípio 2 - Mapear o risco, não só encontrar a falha**
Nosso objetivo final não é apenas apontar vulnerabilidades ou coletar CVEs, mas **construir a cadeia de risco** que demonstra:
- **Onde** está a falha;
- **Como** ela é explorada;
- **Qual** o efeito dominó;
- **Quanto custa** ao negócio;
- **Quais compliance** estão expostos.

### 🔎 **Tópicos-Chave:**
- A vulnerabilidade só importa se **conecta à cadeia de risco**.
- Sempre questionar: “O que isso me permite atingir?”
- Cada finding precisa ter um *Risk Impact Score* atribuído.

### 💣 **Exemplos Práticos:**
- Um XSS simples é classificado como **baixo**? Não no A.R.M.A.: se isso dá acesso ao painel financeiro via cookie hijacking, o risco vira **crítico**.
- Relacionar vulnerabilidades em cadeia: *"Esse RCE junto com o credential stuffing me dá domínio total do ambiente."*


---

## **Princípio 3 - O Pentest é um ciclo vivo, não um laudo morto**
Na A.R.M.A., a entrega não é só um relatório. **É um mapa vivo do risco**, que cresce, evolui e se adapta conforme o ambiente muda e novas ameaças surgem.

### 🔎 **Tópicos-Chave:**
- O laudo é o **ponto de partida** para o ciclo seguinte.
- Criar um **Mapa de Superfície de Ataque** atualizado e vivo.
- Gerar recomendações em **ciclos de melhoria contínua**.

### 💣 **Exemplos Práticos:**
- Cliente corrige a falha X, mas a metodologia obriga a reavaliar: "Que nova janela de ataque se abriu após esse patch?"
- Um painel visual vivo, onde cada ativo vulnerável é um **nó dinâmico da rede de risco**.

---

## **Princípio 4 - A decisão do atacante é a nossa bússola**
- Cada etapa contém checkpoints que nos forçam a **simular o pensamento adversarial**;
- Não seguimos um fluxo linear — adaptamos o ataque conforme **oportunidades reais** surgem;
- Nosso objetivo é **aprender com o ataque**, e não só executá-lo.

### 🔎 **Tópicos-Chave:**
- Em todo momento, o pentester para e se pergunta: *“Se eu fosse o atacante, o que faria com essa brecha?”*
- A exploração nunca segue linear, ela se adapta.

### 💣 **Exemplos Práticos:**
- Ao invadir uma VPN, o pentester decide **não** continuar atacando o AD. Ele avalia: *“E se eu explorar o e-mail e fazer um ataque de Business Email Compromise?”*
- A escolha dos alvos muda com o que o ambiente apresenta.

---

## **Princípio 5 - Compliances não são obstáculos, são indicadores**
A metodologia A.R.M.A. se alinha com regulatórios e compliance como:
- **PCI DSS, HIPAA, LGPD, DORA, NIS2, NIST, ISO 27001**;
- Para cada risco mapeado, associamos o impacto **regulatório**;
- Geramos entregáveis que **facilitam auditorias** e ajudam empresas a se manterem **em conformidade**.

### 🔎 **Tópicos-Chave:**
- Cada risco mapeado é **automaticamente linkado** a um compliance.
- Gera-se uma tabela clara: *“Este risco quebra esta norma, por este motivo”*.

### 💣 **Exemplos Práticos:**
- Um vazamento de dados médicos é linkado direto ao HIPAA;
- Um endpoint com PCI é rastreado até o ponto de não conformidade;
- Na hora do board meeting, o CEO já sabe *qual multa pode cair* e *por qual falha*.

---

## **Princípio 6 - Resultados entregues em três linguagens**
1. **Técnica** — Para o time de TI e Segurança;
2. **Negócios** — Traduzido em impacto financeiro;
3. **Compliance** — Pontos de falha frente às obrigações legais.

### 🔎 **Tópicos-Chave:**
- **Técnica:** Descrição detalhada dos ataques e ferramentas;
- **Negócios:** Impacto financeiro estimado da exploração;
- **Compliance:** Relatório modular para cada framework (PCI, DORA, NIS2).

### 💣 **Exemplos Práticos:**
| Camada | Exemplo |
|-------|---------|
| Técnica | *SQLi no endpoint /api/user* permitiu extração da tabela “users” |
| Negócios | *Prejuízo estimado de R$ 5 milhões por vazamento de credenciais* |
| Compliance | *Violação direta à cláusula X do LGPD – tratamento inadequado de dados* |

---

## **Princípio 7 - Superação de limites e evolução contínua**
Cada ciclo da A.R.M.A. **não termina, evolui**:
- O time ofensivo aprende;
- O cliente entende suas fraquezas;
- As defesas são testadas de verdade;
- **Próxima execução começa mais forte e mais inteligente**.

### 🔎 **Tópicos-Chave:**
- O objetivo do pentester é **se superar** a cada ciclo;
- Incentivo a técnicas novas, exploração de vetores negligenciados, estudo de APTs.

### 💣 **Exemplos Práticos:**
- Time de Red Team é forçado a tentar **lateral movement via protocolo legacy** nunca testado;
- Após sucesso, cria-se um **repositório interno de “lições aprendidas”**;
- O próximo ciclo parte **mais profundo**: se antes o acesso foi só até user, agora o alvo é impactar negócio ou reputação.

---

## **Princípio 8 - A única forma de defender é pensar como quem ataca**
O A.R.M.A. não é uma metodologia para empresas que querem um papel bonito no final. É para quem entende que o verdadeiro **escudo nasce de uma mente ofensiva**.

### 🔎 **Tópicos-Chave:**
- Defender significa prever os próximos passos de quem quer causar o caos;
- Toda defesa implementada deve nascer de uma **tentativa real de ataque**.

### 💣 **Exemplos Práticos:**
- Ao invés de só fechar uma porta, o time de defesa aprende:
   - **Por onde entrei?**
   - **Por onde eu sairia se o ataque continuasse?**
   - **Onde posso deixar uma backdoor que ninguém vê?**
- Defesa proativa nasce da visão ofensiva: *“O que eu faria se eu fosse o grupo X do MITRE ATT&CK?”*

---

## **O Nosso Compromisso:**
🚀 **Gerar clareza, não confusão**;  
💣 **Criar impacto real, não ruído técnico**;  
🧠 **Ensinar o time a pensar como o inimigo, não como um operador de scanner**;  
📈 **Fortalecer o negócio e não apenas cumprir tabela.**

---

## **Resumo Visual do Espírito A.R.M.A.**
```
Explorar > Reavaliar > Adaptar > Escalar > Mapear Risco > Impacto Real > Evoluir
```
