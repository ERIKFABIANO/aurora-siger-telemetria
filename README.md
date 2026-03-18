# Missão Aurora Siger — Sistema de Verificação de Pré-Decolagem

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![FIAP](https://img.shields.io/badge/FIAP-2026-red)

## Descrição

Este projeto implementa um sistema computacional de verificação de telemetria para a missão fictícia Aurora Siger, uma nave interplanetária com destino a Marte. O objetivo é simular os procedimentos críticos de pré-decolagem realizados por equipes reais da NASA e SpaceX, adaptados como atividade integradora da disciplina de Ciência da Computação — Fase 1.

Os parâmetros de telemetria foram definidos com base em dados reais:

- NASA ISS — temperatura interna dos módulos, nível de energia, integridade estrutural
- SpaceX Falcon 9 — pressão dos tanques de LOX e temperatura do propelente

---

## Funcionalidades

- Organização da telemetria em tabela formatada com pandas, com colorização automática por status
- Algoritmo de verificação que avalia 7 parâmetros e emite a decisão: PRONTO PARA DECOLAR ou DECOLAGEM ABORTADA
- Simulação de anomalia com telemetria de falha para testar a robustez do sistema
- Gráficos com matplotlib comparando valores atuais e faixas seguras
- Análise energética com cálculo de autonomia, perdas e energia residual pós-decolagem
- Análise assistida por IA com classificação, identificação de anomalias e sugestões operacionais
- Reflexão crítica sobre ética, impacto social e sustentabilidade na exploração espacial
- Relatório final consolidado gerado automaticamente pelo próprio notebook

---

## Pré-requisitos

- Python 3.10 ou superior
- pip

---

## Instalação e execução

**1. Clone o repositório**
```bash
git clone https://github.com/ERIKFABIANO/aurora-siger-telemetria.git
cd aurora-siger-telemetria
```

**2. Instale as dependências**
```bash
pip install -r requirements.txt
```

**3. Abra o notebook**
```bash
jupyter notebook aurora_siger_telemetria.ipynb
```

**4. Execute todas as células em ordem**

No menu do Jupyter: `Kernel > Restart & Run All`

---

## Estrutura do projeto

```
aurora-siger-telemetria/
│
├── aurora_siger_telemetria.ipynb          # Notebook principal com todo o código
├── README.md                              # Documentação do projeto
├── requirements.txt                       # Dependências
├── Relatorio_Operacional_Pre_Decolagem.pdf  # Relatório em PDF para entrega
├── telemetria_grafico.png                 # Gerado ao executar o notebook
└── energia_grafico.png                    # Gerado ao executar o notebook
```

---

## Saída esperada

Ao rodar o cenário normal, o resultado deve ser:

```
Verificacao de telemetria — Telemetria Normal — Aurora Siger
-------------------------------------------------------
  OK     | Temperatura Interna: 22 C (faixa: 18 a 27)
  OK     | Temperatura Externa: -85 C (faixa: -120 a 120)
  OK     | Pressao Tanque LOX: 47 psi (faixa: 40 a 55)
  OK     | Temperatura do LOX: -207 C (faixa: -215 a -200)
  OK     | Integridade Estrutural: 1
  OK     | Nivel de Energia: 87 % (faixa: 75 a 100)
  OK     | Status Modulos Criticos: 1
-------------------------------------------------------
RESULTADO: PRONTO PARA DECOLAR — todos os sistemas operacionais.
```

Ao rodar o cenário com falhas:

```
RESULTADO: DECOLAGEM ABORTADA — corrija os alertas antes de prosseguir.
```

---

## Fontes dos dados

| Parâmetro | Fonte | Link |
|-----------|-------|------|
| Temperatura interna | NASA ISS | https://www.nasa.gov/international-space-station/ |
| Temperatura do LOX | SpaceX Falcon 9 | https://www.spacex.com/vehicles/falcon-9 |
| Pressão dos tanques | SpaceX Falcon 9 | https://www.spacex.com/vehicles/falcon-9 |
| Sistema de energia | NASA ISS | https://www.nasa.gov/international-space-station/ |

---

## Autor

Erik Appe
Ciência da Computação — Fase 1 | FIAP 2026
erikfabiano082@gmail.com

---

## Licença

Licença MIT — consulte o arquivo LICENSE para detalhes.

---

*Atividade Integradora — Relatório Operacional de Pré-Decolagem | FIAP 2026*
