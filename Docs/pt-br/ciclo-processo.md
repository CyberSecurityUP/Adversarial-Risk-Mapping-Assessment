# 🛡️ **CICLO A.R.M.A. - Adversarial Risk Mapping & Assessment**

## 🚀 **Visão Geral do Ciclo:**
O A.R.M.A. funciona como um **ciclo dinâmico e iterativo** de exploração e aprendizado. Ele força o pentester a pensar, adaptar e gerar um **mapa de risco** sólido que conecte o lado técnico ao impacto de negócio e compliance.

Cada fase é medida **quantitativamente** e **qualitativamente**.

---

## ✅ **Fase 1 - Context Discovery (Descoberta de Contexto)**
**Objetivo:** Entender o ambiente, o negócio, a superfície real de ataque e definir o perfil do adversário.

### **Entregáveis Qualitativos:**
- Contexto do negócio (Ex: banco digital, e-commerce, healthcare)
- Quais ativos são **vitais**
- Definição de **personas adversárias** (APT, insider, hacktivista, ransomware group)

### **Métricas Quantitativas:**
- Número de ativos mapeados
- Número de interfaces externas expostas
- Ranking de criticidade dos ativos

---

## ✅ **Fase 2 - Adversarial Emulation Planning**
**Objetivo:** Traçar a narrativa ofensiva. Construir cenários e estratégias como se fosse o atacante.

### **Entregáveis Qualitativos:**
- Definição da **Kill Chain inicial**
- Escolha de técnicas MITRE ATT&CK e ferramentas
- Construção da “**Adversary Storyline**” – O que queremos atingir? Como?

### **Métricas Quantitativas:**
- Número de vetores planejados
- Score inicial de risco estimado por vetor

---

## ✅ **Fase 3 - Offensive Iterative Loops (Loops Ofensivos Iterativos)**
**Objetivo:** Atacar, pausar, reavaliar, adaptar — nunca seguir o fluxo linear.

### **Entregáveis Qualitativos:**
- Registro da **decisão adversarial**: Por que atacou aquele ponto? O que abandonou e por quê?
- Análise de cada passo: *“O que essa conquista me abriu?”*
- Relato de pivotagens não planejadas

### **Métricas Quantitativas:**
- Nível de profundidade (externo > interno > domínio > dados)
- Número de caminhos percorridos
- Número de técnicas únicas usadas
- Score de cada conquista técnica (com peso por criticidade)

---

## ✅ **Fase 4 - Risk Chain Mapping (Mapeamento da Cadeia de Risco)**
**Objetivo:** Conectar todos os pontos explorados até um **impacto de negócio ou compliance real**.

### **Entregáveis Qualitativos:**
- Mapa visual da cadeia de ataque e suas consequências
- Relação direta: Técnica -> Impacto Negócio -> Impacto Compliance
- Análise de **efeito dominó**

### **Métricas Quantitativas:**
- Quantidade de ativos impactados
- Quantidade de dados sensíveis acessados
- Valor financeiro estimado da cadeia de risco (R$ ou USD)

---

## ✅ **Fase 5 - Business Impact & Compliance Report**
**Objetivo:** Traduzir o ataque em:
- **Perda financeira**
- **Impacto regulatório**
- **Consequências reputacionais**

### **Entregáveis Qualitativos:**
- Laudo técnico com storytelling adversarial
- Relatório executivo com impacto financeiro
- Tabela de violações por compliance (PCI, HIPAA, LGPD, DORA)

### **Métricas Quantitativas:**
- Custo estimado do ataque simulado
- Quantidade de obrigações regulatórias violadas
- Score geral de exposição da empresa

---

## ✅ **Fase 6 - Adversary Driven Learning (Aprendizado Adversarial)**
**Objetivo:** Extrair lições para fortalecer o cliente e o próprio time.

### **Entregáveis Qualitativos:**
- O que o pentester aprendeu?
- O que a empresa precisa melhorar?
- Novos vetores que surgiram e não existiam antes
- Plano de evolução para o próximo ciclo

### **Métricas Quantitativas:**
- Número de recomendações de melhoria
- Quantidade de gaps de detecção ou resposta encontrados
- Novo score de maturidade defensiva do cliente

---

# 🔥 **Exemplo de Como o Ciclo Evolui na Prática (Qualitativo + Quantitativo):**

| **Fase** | **Exemplo Qualitativo** | **Exemplo Quantitativo** |
|--------|------------------------|-------------------------|
| Descoberta | Identificamos que a empresa tem uma fintech integrada ao Open Banking | 3 domínios, 12 APIs expostas, 2 com credenciais hardcoded |
| Planejamento | Adversário: Lapsus$, motivação: vazamento para extorsão | Score de risco estimado: 75/100 |
| Execução | Invadimos via falha de OAuth mal configurado e pivotamos para admin | 5 técnicas MITRE usadas, acesso a 3 bancos de dados sensíveis |
| Cadeia de Risco | Conseguimos gerar transações falsas de R$ 2 milhões | Impacto potencial financeiro: R$ 2M, 2 normas do BACEN violadas |
| Relatório | Exec traduziu: risco de multa e bloqueio do serviço pela regulação | PCI DSS Violated: YES / LGPD Violated: YES |
| Aprendizado | Cliente não detectou o ataque - precisa SIEM e MFA reforçado | 7 gaps de detecção mapeados |

---

# 🎯 **Resumo das Medidas Quantitativas:**
✅ Número de vetores explorados  
✅ Profundidade alcançada (externo > domínio > crown jewels)  
✅ Custo potencial do ataque (R$ ou USD)  
✅ Número de técnicas / táticas MITRE aplicadas  
✅ Quantidade de normas/regulatórios violados  
✅ Gaps defensivos encontrados  
✅ Score de maturidade antes / depois  

---

# 🎯 **Resumo das Entregas Qualitativas:**
✅ Narrativa do atacante — *por que o ataque seguiu aquele caminho*  
✅ Risco conectado ao impacto de negócio  
✅ Tradução para executivos, segurança e compliance  
✅ Lições aprendidas e novo roadmap de defesa

---
