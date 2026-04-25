# Framework de Análise - Pós-Entrevistas
## ConectaPay - Definição de ICP Baseada em Dados

Este documento contém os frameworks para análise dos dados coletados nas 15-20 entrevistas.

---

## 1. ICP Profile Framework

### Dados Demográficos (Empresa)

**Critérios a Analisar:**
- **Tamanho**: Número de funcionários
- **Volume**: Consultas/leads por mês
- **Localização**: Capital vs interior
- **Modelo**: Negócio próprio vs franquia vs rede
- **Ticket médio**: Valor por consulta/venda

### Dados Psicográficos (Decisor)

**Critérios a Analisar:**
- **Perfil do tomador de decisão**: Idade, formação, experiência anterior
- **Maturidade digital**: Usa automação? SaaS?
- **Sensibilidade a dor**: Como reconhece o problema?
- **Abertura à inovação**: Primeiro adotador vs conservador
- **Orçamento**: Disposição e capacidade de pagar

### Template de ICP (Preencher após entrevistas)

```
## PERFIL DO CLIENTE IDEAL - ConectaPay

### Demográfico
- Tamanho da empresa: ___ funcionários
- Volume mensal: ___ operações
- Nicho: [ ] Clínica [ ] Imobiliária [ ] Outro
- Localização: ___
- Ticket médio: R$ ___
- Tecnologia atual: ___

### Psicográfico
- Cargo do decisor: ___
- Perfil: [ ] Early adopter [ ] Pragmático [ ] Conservador
- Principal motivador: [ ] Crescimento [ ] Eficiência [ ] Redução de custos
- Barreiras: ___

### Dor
- Problema: No-shows / Perda de leads
- Frequência: ___ vezes/mês
- Impacto financeiro: R$ ___/mês
- Urgência: [ ] Alta [ ] Média [ ] Baixa

### Solução
- Funcionalidades prioritárias:
  1. ___
  2. ___
  3. ___
- Willingness-to-pay: R$ ___/mês
- Timeline para implementação: ___ meses

### Exclusões (Não é ICP se:)
- ___
- ___
- ___
```

---

## 2. Pain Severity Matrix

### Matriz de Severidade vs Frequência

| **Frequência \ Severidade** | **Baixa (R$ < 1k/mês)** | **Média (R$ 1k-5k/mês)** | **Alta (R$ 5k+/mês)** |
|-----------------------------|-------------------------|--------------------------|-----------------------|
| **Baixa (< 10 ocorrências/mês)** | Baixa prioridade | Prioridade baixa-média | Prioridade média |
| **Média (10-50 ocorrências/mês)** | Prioridade baixa-média | **ALTA PRIORIDADE** | **PRIORIDADE CRÍTICA** |
| **Alta (50+ ocorrências/mês)** | Prioridade média | **PRIORIDADE CRÍTICA** | **PRIORIDADE MÁXIMA** |

### Preencher com dados reais:

**Clínicas:**
- Severidade média: R$ ___/mês
- Frequência média: ___ no-shows/mês
- Quadrante: [ ] Baixa [ ] Média [ ] Alta [ ] Crítica

**Imobiliárias:**
- Severidade média: R$ ___/mês
- Frequência média: ___ leads perdidos/mês
- Quadrante: [ ] Baixa [ ] Média [ ] Alta [ ] Crítica

### Análise de Causa Raiz

**Principais causas identificadas:**
1. ___ (___% dos entrevistados)
2. ___ (___% dos entrevistados)
3. ___ (___% dos entrevistados)

**Impacto por causa:**
| Causa | % Afetados | Impacto Financeiro Médio | Facilidade de Resolver |
|-------|------------|--------------------------|------------------------|
| Esquecimento | ___% | R$ ___/mês | Alta |
| ___ | ___% | R$ ___/mês | ___ |
| ___ | ___% | R$ ___/mês | ___ |

---

## 3. ROI Calculation Framework

### Cálculo de ROI por Nicho

**Fórmula Base:**
```
ROI = (Ganho - Custo) / Custo × 100%

Ganho = (Redução de no-shows × Ticket médio × 12 meses) + (Recuperação de vendas)
Custo = Assinatura mensal × 12 meses + Implementação
```

### Template por Nicho

#### Para Clínicas:

| Variável | Valor (Mín) | Valor (Médio) | Valor (Máx) |
|----------|-------------|---------------|-------------|
| Volume de consultas/mês | 50 | 150 | 500 |
| Taxa atual de no-show | 20% | 35% | 50% |
| Taxa projetada com ConectaPay | 10% | 17.5% | 25% |
| Redução de no-shows | 10% | 17.5% | 25% |
| Ticket médio por consulta | R$ 150 | R$ 300 | R$ 600 |
| Ganho mensal estimado | R$ 750 | R$ 2.625 | R$ 7.500 |
| Ganho anual estimado | R$ 9.000 | R$ 31.500 | R$ 90.000 |
| Custo ConectaPay/mês | R$ 200 | R$ 400 | R$ 800 |
| ROI (primeiro ano) | 375% | 656% | 937% |
| Payback period | 3.2 meses | 1.8 meses | 1.3 meses |

#### Para Imobiliárias:

| Variável | Valor (Mín) | Valor (Médio) | Valor (Máx) |
|----------|-------------|---------------|-------------|
| Leads/mês | 30 | 100 | 300 |
| Taxa atual de conversão | 5% | 10% | 15% |
| Taxa projetada com ConectaPay | 7.5% | 15% | 22.5% |
| Aumento de conversão | 2.5% | 5% | 7.5% |
| Ticket médio por venda | R$ 5.000 | R$ 15.000 | R$ 50.000 |
| Ganho mensal estimado | R$ 1.125 | R$ 7.500 | R$ 33.750 |
| Ganho anual estimado | R$ 13.500 | R$ 90.000 | R$ 405.000 |
| Custo ConectaPay/mês | R$ 300 | R$ 500 | R$ 1.000 |
| ROI (primeiro ano) | 450% | 1.500% | 4.050% |
| Payback period | 2.7 meses | 0.7 meses | 0.3 meses |

### Cálculo de Custo de Oportunidade

**Sem ConectaPay:**
- No-shows/perdas: R$ ___/mês
- Tempo gasto em follow-up manual: ___ horas/mês
- Custo de mão de obra: R$ ___/mês
- **Custo total de oportunidade: R$ ___/mês**

**Com ConectaPay:**
- Redução de perdas: ___%
- Tempo economizado: ___%
- **Economia total: R$ ___/mês**

---

## 4. Competitive Landscape

### Soluções Atuais (Mencionadas nas Entrevistas)

| Solução | % Que Usa | Principal Limitação | Satisfação (1-10) |
|---------|-----------|---------------------|-------------------|
| WhatsApp manual | ___% | Consome tempo | ___ |
| Telefone | ___% | Baixa resposta | ___ |
| Email | ___% | Não é lido | ___ |
| Sistema X | ___% | ___ | ___ |
| Não tem processo | ___% | N/A | N/A |

### Gaps Identificados no Mercado

1. **Gap 1**: ___
   - ___% dos entrevistados mencionaram
   - Impacto: ___
   - Como ConectaPay resolve: ___

2. **Gap 2**: ___
   - ___% dos entrevistados mencionaram
   - Impacto: ___
   - Como ConectaPay resolve: ___

3. **Gap 3**: ___
   - ___% dos entrevistados mencionaram
   - Impacto: ___
   - Como ConectaPay resolve: ___

---

## 5. Pricing Validation

### Willingness-to-Pay (WTP) por Segmento

**Clínicas:**
- WTP médio: R$ ___/mês
- WTP mediano: R$ ___/mês
- WTP mínimo: R$ ___/mês
- WTP máximo: R$ ___/mês
- Distribuição:
  - R$ 200-300: ___%
  - R$ 300-500: ___%
  - R$ 500-1000: ___%
  - R$ 1000+: ___%

**Imobiliárias:**
- WTP médio: R$ ___/mês
- WTP mediano: R$ ___/mês
- WTP mínimo: R$ ___/mês
- WTP máximo: R$ ___/mês
- Distribuição:
  - R$ 200-300: ___%
  - R$ 300-500: ___%
  - R$ 500-1000: ___%
  - R$ 1000+: ___%

### Correlação WTP × Tamanho da Empresa

| Tamanho (funcionários) | WTP Médio | Justificativa Principal |
|------------------------|-----------|-------------------------|
| 1-10 | R$ ___ | ___ |
| 11-50 | R$ ___ | ___ |
| 51-200 | R$ ___ | ___ |
| 200+ | R$ ___ | ___ |

### Correlação WTP × Impacto Financeiro

| Impacto da Dor (R$/mês) | WTP Médio | % do Impacto |
|-------------------------|-----------|--------------|
| < R$ 1.000 | R$ ___ | ___% |
| R$ 1.000 - R$ 5.000 | R$ ___ | ___% |
| R$ 5.000 - R$ 10.000 | R$ ___ | ___% |
| > R$ 10.000 | R$ ___ | ___% |

**Insight de Pricing:**
- Empresas estão dispostas a pagar cerca de ___% do impacto da dor
- Sweet spot pricing: R$ ___/mês
- Estrutura sugerida:
  - Starter: R$ ___ (até ___ operações/mês)
  - Pro: R$ ___ (até ___ operações/mês)
  - Enterprise: R$ ___+ (ilimitado)

---

## 6. Mensagem e Copywriting Insights

### Palavras e Frases que Resonaram

**Durante as entrevistas, anotar:**
- "O que mais me dóle é..." → ___
- "Se eu pudesse resolver uma coisa..." → ___
- "Eu pagaria por..." → ___

### Framework de Mensagem (Para Smoke Test)

**Headline Base:**
"Recupere R$ [VALOR MÉDIO]/mês em [VENDAS/CONSULTAS] perdidas com automação via WhatsApp"

**Sub-headline:**
"[NICHOS] perdem [TAXA]% de receita por [NO-SHOWS/LEADS FRIOS]. O ConectaPay automatiza confirmações, follow-ups e pagamentos via Pix em um único lugar."

**Bullet Points (benefícios validados):**
- ✓ Reduz [no-shows/leads perdidos] em [REDUÇÃO]% em média
- ✓ Economize [HORAS]h/semana em follow-ups manuais
- ✓ Receba pagamentos via Pix instantaneamente no WhatsApp
- ✓ ROI de [ROI]% no primeiro mês
- ✓ Setup em 10 minutos, sem integração complexa

**Social Proof (após beta):**
"[NOME] de [EMPRESA] recuperou R$ [VALOR] no primeiro mês"

---

## 7. Next Steps Após Análise

### Com base nos dados das entrevistas:

1. **Definir nicho prioritário**: [ ] Clínicas [ ] Imobiliárias [ ] Ambos
2. **Refinar ICP**: Criar perfil detalhado
3. **Ajustar pricing**: Baseado em WTP e ROI
4. **Criar smoke test**: Landing page + ads
5. **Validar com tráfego pago**: Testar messaging

### KPIs para Smoke Test:

- Visitantes: ___
- Taxa de conversão para waitlist: ___%
- Custo por lead (CPL): R$ ___
- Qualidade dos leads (fit com ICP): ___%

### Decisão Go/No-Go:

**GO se:**
- ___%+ reconhecem o problema
- WTP médio ≥ R$ ___/mês
- ROI ≥ ___%
- ___%+ interessados em beta

**NO-GO se:**
- < ___% reconhecem o problema
- WTP médio < R$ ___/mês
- ROI < ___%
- Diferentes problemas que o esperado

---

## 8. Documentos a Serem Gerados

Após completar as 15-20 entrevistas:

- [ ] **ICP Profile**: Documento detalhado do cliente ideal
- [ ] **Pain Severity Matrix**: Visualização da severidade vs frequência
- [ ] **ROI Calculator**: Planilha de cálculo de ROI por nicho
- [ ] **Competitive Analysis**: O que existe hoje e gaps
- [ ] **Pricing Strategy**: Estrutura de preços validada
- [ ] **Messaging Framework**: Copy para smoke test
- [ ] **Smoke Test Plan**: Landing page, ads, critérios de sucesso
- [ ] **Final Report**: Apresentação para board com recomendações
