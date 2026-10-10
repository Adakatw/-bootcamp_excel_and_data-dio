# Simulador de Investimentos em Fundos Imobiliários (FIIs)

Trata-se de uma ferramenta em Excel que simula o crescimento de uma carteira de fundos imobiliários ao longo do tempo, auxiliando na tomada de decisão de investimentos, como parte do desafio prático do Bootcamp de Excel e dados da DIO.



## As 5 Perguntas de Negócio
A ferramenta responde de forma clara e visual às seguintes perguntas:
1. **Quanto investir por mês?** (Localizado na célula de input `aporte`).
2. **Por quantos anos?** (Localizado na célula de input `anos`).
3. **Qual a taxa de rendimento mensal?** (Localizado na célula de input `taxa_mensal`).
4. **Quanto de patrimônio vai acumular?** (Calculado na célula `patrimonio_acumulado`).
5. **Quanto vai receber de dividendos por mês?** (Calculado na célula `dividendos_mensais`).



##  Como funciona por dentro
*   **Função VF:** Utilizada para calcular o valor futuro do patrimônio. A fórmula base é `=VF(taxa_mensal; anos*12; -aporte; 0; 0)`. Ela considera os aportes mensais e os juros compostos.
*   **PROCV e Chave Composta:** Para dividir o aporte entre os 6 tipos de fundos, foi criada uma chave composta (ex: `Perfil & "-" & "TipoFundo"`). O `PROCV` busca essa chave na aba de apoio para retornar o percentual correto de cada fundo, baseado no perfil do investidor.
*   **Intervalos Nomeados:** Foram criados nomes como `aporte`, `taxa_mensal` e `salario` para facilitar a leitura das fórmulas.



##  Perfis de Investidor
Cada perfil soma 100%.

**Conservador:**

* PAPEL: 30%
* TIJOLO: 50%
* HÍBRIDOS: 10%
* FOFs: 10%
* DESENVOLVIMENTO: 0%
* HOTELARIAS: 0%


**Moderado:**
* PAPEL: 32%
* TIJOLO: 35%
* HÍBRIDOS: 8%
* FOFs: 5%
* DESENVOLVIMENTO: 10%
* HOTELARIAS: 10%

**Agressivo:**
* PAPEL: 50%
* TIJOLO: 10%
* HÍBRIDOS: 5%
* FOFs: 5%
* DESENVOLVIMENTO: 20%
* HOTELARIAS: 10%


## Mudanças em relação à ferramenta do Expert

**Não houveram mudanças relevantes.**
