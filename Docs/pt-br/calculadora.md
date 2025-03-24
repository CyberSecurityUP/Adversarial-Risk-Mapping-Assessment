# 🛡️ **Risk Score A.R.M.A. - Estrutura de Cálculo**

---

## 🎯 **Fórmula Base (Escalável e Modular)**
```
Risk Score Final = [(Técnica x Peso_Técnica) + (Profundidade x Peso_Profundidade) + (Impacto x Peso_Impacto) + (Compliance x Peso_Compliance) + (Detecção x Peso_Detecção)] x Fator Acelerador de Cadeia
```

Onde:
- **Peso_Técnica**: A complexidade da técnica usada
- **Peso_Profundidade**: O quão fundo o ataque chegou
- **Peso_Impacto**: Quanto de dano financeiro ou reputacional causaria
- **Peso_Compliance**: Quantas regulações o ataque impacta
- **Peso_Detecção**: O quanto o ataque passou despercebido
- **Fator de Cadeia**: Multiplicador caso o ataque tenha gerado pivotagens e dominado múltiplos sistemas

---

## 🔎 **Breakdown das Categorias (com exemplos e pontuação sugerida):**

| Categoria        | Descrição                                                                 | Exemplo                                                        | Pontuação |
|------------------|--------------------------------------------------------------------------|---------------------------------------------------------------|----------|
| **Técnica**         | Complexidade das técnicas / MITRE ATT&CK utilizadas                      | SQLi Básico (2), Living Off the Land (7), Kernel Exploit (10) | 1 - 10   |
| **Profundidade**    | Quão longe o ataque chegou                                              | Acesso user (3), root (7), domínio e dados (10)                | 1 - 10   |
| **Impacto**         | Potencial de dano real ao negócio                                       | Deface (2), Vazar 1TB de dados (9), Parar operação (10)        | 1 - 10   |
| **Compliance**      | Quantidade e criticidade das normas quebradas                          | 0 (0), Violação leve LGPD (5), Violação PCI full (10)          | 0 - 10   |
| **Detecção**        | O quanto o ataque foi ou não detectado                                  | Detectado na hora (2), Passou por SIEM e EDR (10)              | 1 - 10   |
| **Cadeia de ataque**| Quantidade de pivotagens bem-sucedidas **(multiplicador do score final)**| Sem pivô (1x), 2 pivôs (1.5x), Movimento completo (2x)          | 1x - 2x  |

---

## 🔥 **Exemplo Prático de Cálculo**
### 🎯 **Cenário:**
- SQL Injection + Pivotagem para AD
- Exfiltração de 500GB de dados financeiros
- Passou por firewall e SIEM
- Violou PCI DSS e LGPD

| **Categoria**  | **Valor** | **Peso** | **Subtotal** |
|---------------|----------|--------|-------------|
| Técnica       | 8        | 1.5    | 12          |
| Profundidade  | 9        | 2      | 18          |
| Impacto       | 9        | 3      | 27          |
| Compliance    | 9        | 2      | 18          |
| Detecção      | 10       | 1.5    | 15          |
| **Subtotal Geral** |      |        | **90**       |
| Cadeia de Ataque | -      | x2     | **180 (Final)** |

### ✅ **Resultado: Risco Extremo (180 pontos)**

---

## 🎨 **Visualização do Score (Escala de Severidade)**
```
0 - 30   → Baixo (Recomenda-se correção gradual)
31 - 60  → Médio (Prioridade moderada)
61 - 120 → Alto (Risco relevante - ações rápidas)
121+     → Extremo (Risco de quebra operacional e regulatória)
```

---

## 🧠 **Qualitativo Vinculado ao Score:**
- **Acima de 120** → Recomenda-se reunião de crise com o board;
- Todo score acima de **90** gera uma **matriz de impacto financeiro / compliance**;
- **Pivotagens automáticas** elevam o score por risco real de cadeia de impacto.

---

## 📈 **Extras que podemos modular:**
- **Customização de pesos** por vertical (ex: fintech tem peso maior em compliance)
- Adicionar "Velocidade de ataque" como métrica (tempo entre o acesso e o impacto)
- Exportação desse score para gerar **dashboards executivos** ou alimentar GRC.

---

## ⚠️ **Resumo - O que o Score resolve:**
✅ Calcula o risco real e não só a falha  
✅ Força o pentester a pensar **o que de fato causa impacto**  
✅ Permite ao board **entender o perigo sem linguagem técnica**  
✅ Conecta **pivotagens, stealth, impacto financeiro e compliance** numa conta clara
