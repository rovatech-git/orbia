<div align="center">

<br/>

```
 ██████╗ ██████╗ ██████╗ ██╗ █████╗ 
██╔═══██╗██╔══██╗██╔══██╗██║██╔══██╗
██║   ██║██████╔╝██████╔╝██║███████║
██║   ██║██╔══██╗██╔══██╗██║██╔══██║
╚██████╔╝██║  ██║██████╔╝██║██║  ██║
 ╚═════╝ ╚═╝  ╚═╝╚═════╝ ╚═╝╚═╝  ╚═╝
```

### Sistemas embarcados com propósito. Da borda ao painel, em tempo real.

*Um projeto [RovaTech](https://github.com/rovatech)*

[![Status](https://img.shields.io/badge/status-em_desenvolvimento-orange?style=flat-square)]()
[![Licença](https://img.shields.io/badge/licença-MIT-blue?style=flat-square)]()
[![ESP+Lua](https://img.shields.io/badge/ESP-Lua-darkgreen?style=flat-square)]()
[![Tasmota](https://img.shields.io/badge/Tasmota-firmware-red?style=flat-square)]()
[![TouchDesigner](https://img.shields.io/badge/TouchDesigner-visual_engine-purple?style=flat-square)]()

</div>

---

## O que é o Orbia

**Orbia** é uma suíte de sistemas embarcados modulares desenvolvida pela RovaTech, com foco em quatro domínios de impacto social: **casa, acessibilidade, indústria e educação**.

Cada sistema combina firmware em ESP com Lua, controle de cargas via Tasmota e visualização em tempo real no TouchDesigner — formando uma arquitetura de baixo custo, open source e replicável por qualquer pessoa ou organização.

---

## Stack

| Camada | Tecnologia | Função |
|---|---|---|
| **Edge / Firmware** | ESP8266 / ESP32 + Lua | Processamento local, lógica embarcada |
| **Controle de cargas** | Tasmota | Relés, interruptores, automação via MQTT |
| **Visualização** | TouchDesigner | Dashboards, interfaces visuais e audiovisual em tempo real |
| **Comunicação** | MQTT, HTTP REST, WebSocket | Integração entre camadas |
| **Sensores** | DHT22, HC-SR04, MPU6050, PIR, MQ-series | Coleta de dados ambientais e de movimento |

---

## Módulos

### 🏠 Casa — Automação Residencial Avançada

#### Sistema de Adaptação Ambiental
Sensores de movimento, temperatura, umidade e luminosidade espalhados pela residência. O ESP com Lua processa os dados localmente, o Tasmota controla as cargas e o TouchDesigner gera um painel visual que **aprende os hábitos da família** e ajusta iluminação, ventilação e segurança automaticamente.
- Detecção de movimento suspeito com alerta noturno
- Ajuste automático de ambiente por horário e perfil de uso
- Interface visual em tempo real para monitoramento

#### Sistema de Cuidados com Idosos
Combina sensor de movimento, sensor de queda, monitoramento de porta e câmera simples. Detecta se o idoso ficou muito tempo parado, caiu ou deixou a porta aberta — projeta **alertas visuais na TV da sala** e envia notificação para o celular do familiar.
- Detecção de inatividade prolongada e quedas
- Integração com TV e dispositivos móveis
- Histórico de eventos para acompanhamento

---

### ♿ Acessibilidade — Inclusão mais profunda

#### Mapa Sonoro e Visual para Deficientes Visuais
Múltiplos sensores ultrassônicos e de movimento criam um **mapa do ambiente em tempo real**. O TouchDesigner transforma os dados em som direcional (volume proporcional à proximidade do obstáculo) e projeção visual para acompanhantes e educadores.
- Navegação assistida em ambientes fechados
- Suporte a professores em contexto escolar e terapêutico
- Aplicável em casa, escola e transporte público

#### Controle por Movimento para Paralisia Parcial
Sistema que interpreta gestos complexos usando `MPU6050 + Lua` para **controlar luzes, TV, ventilador e acionar emergência**. O TouchDesigner serve como interface visual para familiares acompanharem os comandos executados.
- Controle do ambiente por gestos
- Acionamento de emergência integrado
- Interface legível para familiares e cuidadores

---

### 🔧 Técnico / Profissional

#### Monitoramento Preditivo em Pequenas Indústrias
Sensores de vibração, temperatura e movimento em máquinas. O ESP com Lua faz pré-processamento dos dados, o Tasmota controla relés de segurança e o TouchDesigner gera um painel com **gráficos em tempo real, alertas de falha iminente e histórico de uso**.
- Manutenção preditiva acessível para pequenas fábricas e oficinas
- Redução de manutenção corretiva e paradas não programadas
- Dados exportáveis para análise posterior

#### Sistema de Controle de Qualidade em Laboratórios
Sensor de movimento + temperatura + abertura de porta. Detecta acesso indevido, variação de temperatura fora do padrão e equipamentos ligados por tempo excessivo — **registrando tudo visualmente no TouchDesigner**.
- Conformidade de ambiente para laboratórios e salas técnicas
- Log automatizado de eventos e violações
- Alertas em tempo real por MQTT

---

### 🔬 Científico e Educacional

#### Estação de Monitoramento Ambiental Comunitário
Rede de ESPs com sensores de qualidade do ar, movimento de animais, temperatura, umidade e CO2. Os dados são processados em Lua e enviados para um **dashboard no TouchDesigner com visualizações científicas**. Projetado para escolas, universidades e ONGs.
- Monitoramento de poluição em bairros e áreas de preservação
- Dados abertos e exportáveis para pesquisa
- Instalação de baixo custo com hardware acessível

#### Laboratório Interativo de Física e Biologia
Alunos usam sensores de movimento, força e distância para conduzir experimentos avançados. O TouchDesigner exibe **gráficos, simulações e análises em tempo real** — transformando aulas teóricas em experiências práticas sem equipamentos caros.
- Substitui equipamentos de laboratório de alto custo
- Interface intuitiva para professores e alunos
- Expansível com novos sensores e experimentos

---

## Estrutura do repositório

```
orbia/
├── casa/
│   ├── adaptacao-ambiental/
│   └── cuidados-idosos/
├── acessibilidade/
│   ├── mapa-sonoro-visual/
│   └── controle-por-movimento/
├── tecnico/
│   ├── monitoramento-preditivo/
│   └── controle-qualidade-lab/
├── educacional/
│   ├── estacao-ambiental/
│   └── laboratorio-interativo/
└── shared/
    ├── firmware/           # Base ESP+Lua reutilizável
    ├── tasmota-configs/    # Templates de configuração Tasmota
    └── td-patches/         # Patches TouchDesigner base
```

---

## Como contribuir

```bash
# Clone o repositório
git clone https://github.com/rovatech/orbia.git

# Acesse o módulo desejado
cd orbia/<dominio>/<projeto>
cat README.md
```

1. **Fork** o repositório
2. Crie uma branch: `git checkout -b feat/nome-da-feature`
3. Commit: `git commit -m 'feat: descrição clara'`
4. Push: `git push origin feat/nome-da-feature`
5. Abra um **Pull Request**

---

## Desenvolvido por

**[RovaTech](https://github.com/rovatech)** — [@pedro-juno](https://github.com/pedro-juno) · [@ana-mouca](https://github.com/ana-mouca)

---

<div align="center">

**Orbia · RovaTech** — *Da borda ao painel, em tempo real.*

</div>
