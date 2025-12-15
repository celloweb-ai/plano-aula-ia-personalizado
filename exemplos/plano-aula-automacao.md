# ⚙️ Plano de Aula: Automação Industrial - Sistemas SCADA

## 📊 Informações Gerais

| Item | Detalhes |
|------|----------|
| **Disciplina** | Automação Industrial / Controle de Processos |
| **Título** | Introdução a Sistemas SCADA: Supervisão e Controle |
| **Duração** | 120 minutos (2 horas) |
| **Nível** | Técnico / Graduação |
| **Público-Alvo** | Estudantes de Engenharia/Técnico em Automação |
| **Modalidade** | Presencial com laboratório |
| **Pré-requisitos** | Conhecimentos de CLP, redes industriais, lógica de programação |

## 🎯 Objetivos de Aprendizagem

### Objetivos Gerais
- Compreender a arquitetura e função de sistemas SCADA
- Aplicar conceitos de supervisão e controle industrial
- Desenvolver competências para projeto de sistemas supervisorios

### Objetivos Específicos
Ao final desta aula, o aluno será capaz de:

1. Definir SCADA e explicar seus componentes principais
2. Diferenciar SCADA de DCS e PLC
3. Identificar aplicações industriais de sistemas SCADA
4. Compreender protocolos de comunicação industrial (Modbus, OPC, etc.)
5. Criar telas básicas de supervisão
6. Configurar tags e comunicação com PLCs
7. Implementar alarmes e históricos de dados
8. Analisar critérios de segurança cibernética em SCADA

### Competências Desenvolvidas
- Análise de sistemas industriais complexos
- Projeto de interfaces homem-máquina (IHM)
- Integração de sistemas de automação
- Troubleshooting de redes industriais
- Consciência de segurança cibernética

## 📚 Conteúdo Programático

### 1. Fundamentos de SCADA
- Definição e histórico
- Sigla: Supervisory Control And Data Acquisition
- Evolução dos sistemas supervisorios
- Arquiteturas: monolítica, distribuída, em rede

### 2. Componentes de um Sistema SCADA
- **MTU** (Master Terminal Unit): Estação mestra
- **RTU** (Remote Terminal Unit): Unidades remotas
- **PLCs**: Controladores programáveis
- **IHM/HMI**: Interface humano-máquina
- **Rede de comunicação**: Protocolos e topologias
- **Sensores e atuadores**: Dispositivos de campo

### 3. Protocolos de Comunicação
- Modbus RTU/TCP
- OPC (OLE for Process Control)
- Profibus/Profinet
- DeviceNet
- Ethernet/IP
- DNP3

### 4. Funcionalidades de SCADA
- Aquisição de dados em tempo real
- Supervisão e monitoramento
- Controle remoto
- Alarmes e eventos
- Tendências e históricos
- Relatórios

### 5. Projeto de Telas Supervisorias
- Princípios de usabilidade
- Hierarquia de telas
- Sinóticos e fluxogramas
- Animações e cores
- Navegação e ergonomia

### 6. Segurança Cibernética
- Vulnerabilidades em SCADA
- Ataques conhecidos (Stuxnet)
- Boas práticas de segurança
- Normas: IEC 62443

## 🛠️ Metodologia

### Estratégias de Ensino
- **Aula expositiva dialógica**: Apresentação com discussão
- **Demonstração prática**: Live demo de software SCADA
- **Aprendizagem baseada em projetos**: Desenvolvimento de aplicativo supervisorio
- **Estudo de caso**: Análise de sistemas reais
- **Laboratório hands-on**: Prática com equipamentos

### Recursos Didáticos
- Apresentação em slides
- Software SCADA (Elipse E3, InduSoft, ScadaBR, ou similar)
- CLP (Siemens S7-1200, Allen-Bradley, ou similar)
- Bancada didática com sensores e atuadores
- Simulador de processos industriais
- Vídeos de plantas industriais
- Diagramas P&ID (Piping and Instrumentation Diagram)

## ⏱️ Desenvolvimento da Aula

### 1ª Etapa: Introdução e Contextualização (20 min)

**Abertura Motivacional**
- Vídeo: Tour virtual por sala de controle industrial
- Discussão: "O que vocês observaram no vídeo?"
- Exemplos de aplicações: energia, saneamento, petróleo & gás, mineração

**Problematização**
> "Como supervisionar e controlar uma planta industrial distribuída geograficamente com milhares de pontos de medida?"

**Contextualização Histórica**
- Anos 1960: Sistemas telemetria rudimentares
- Anos 1980: Primeiros SCADA computadorizados
- Anos 1990-2000: Migração para Windows e redes
- Atualidade: SCADA na nuvem, IIoT, Indústria 4.0

### 2ª Etapa: Fundamentos Teóricos (30 min)

**Definição de SCADA**

SCADA = **S**upervisory **C**ontrol **A**nd **D**ata **A**cquisition

É um sistema computadorizado que permite:
- **Supervisionar**: Monitorar variáveis de processo
- **Controlar**: Atuar sobre equipamentos remotamente
- **Adquirir dados**: Coletar e armazenar informações

**Arquitetura Típica de SCADA**

```
                [Estação Central - MTU]
                         |
                    (Rede Industrial)
                         |
        +----------------+----------------+
        |                |                |
      [RTU 1]          [PLC 1]          [RTU 2]
        |                |                |
   Sensores/         Sensores/       Sensores/
   Atuadores         Atuadores       Atuadores
```

**Comparação: SCADA vs DCS vs PLC**

| Característica | SCADA | DCS | PLC |
|----------------|-------|-----|-----|
| **Área de aplicação** | Grandes distâncias | Processo contínuo | Automação discreta |
| **Arquitetura** | Centralizada | Distribuída | Local |
| **Tempo de resposta** | Segundos | Milissegundos | Milissegundos |
| **Exemplos** | Distribuição de água | Refinaria | Linha de montagem |

**Protocolos de Comunicação**

**Modbus RTU/TCP**
- Protocolo aberto e simples
- Amplamente utilizado
- Master-Slave

**OPC (OPC-UA)**
- Padrão de interoperabilidade
- Cliente-servidor
- Plataforma independente

**Demonstração Prática**
Mostrar captura de pacotes Modbus no Wireshark.

### 3ª Etapa: Demonstração de Software SCADA (25 min)

**Tour pelo Software**

Utilizando plataforma SCADA (ex: Elipse E3, InduSoft):

1. **Interface de Desenvolvimento**
   - Área de trabalho
   - Biblioteca de objetos
   - Propriedades
   - Scripts

2. **Configuração de Comunicação**
   ```
   Driver: Modbus TCP
   IP: 192.168.1.100
   Porta: 502
   Slave ID: 1
   ```

3. **Criação de Tags**
   - Tag: `TK101_Nivel`
   - Tipo: Analógico (Real)
   - Endereço: 40001
   - Escala: 0-100%
   - Unidade: %
   - Alarme: >90% (Alto), <10% (Baixo)

4. **Desenvolvimento de Tela Supervisoria**
   - Adicionar tanque (biblioteca gráfica)
   - Animação de nível (link com tag)
   - Display numérico
   - Tendência (gráfico histórico)
   - Botões de comando

5. **Sistema de Alarmes**
   - Configuração de limites
   - Cores e prioridades
   - Reconhecimento de alarmes
   - Log de eventos

### 4ª Etapa: Atividade Prática em Laboratório (35 min)

**Projeto: Sistema de Controle de Tanque**

**Descrição do Sistema**
- Tanque de armazenamento de água
- Sensor de nível (0-10V = 0-100%)
- Válvula de entrada (ON/OFF)
- Bomba de saída (ON/OFF)

**Objetivo**
Manter nível entre 30% e 70%

**Tarefas dos Alunos** (grupos de 2-3)

1. **Configuração de Comunicação**
   - Conectar SCADA ao CLP via Modbus TCP
   - Testar conectividade

2. **Criar Tags**
   ```
   - TK_Nivel (Leitura analógica)
   - VLV_Entrada (Comando digital)
   - BOMBA_Saida (Comando digital)
   - TK_Nivel_SP (Setpoint)
   ```

3. **Desenvolver Tela Supervisoria**
   - Desenhar sinótico do processo
   - Adicionar indicações de nível
   - Criar botões de comando manual
   - Implementar modo AUTO/MANUAL

4. **Configurar Alarmes**
   - Alarme de nível alto (>80%)
   - Alarme de nível baixo (<20%)
   - Alarme de falha de comunicação

5. **Implementar Histórico**
   - Armazenar dados a cada 1 segundo
   - Criar gráfico de tendência

6. **Testar o Sistema**
   - Simular variações de nível
   - Acionar comandos
   - Verificar alarmes

**Acompanhamento do Professor**
- Circular entre os grupos
- Tirar dúvidas
- Orientar sobre boas práticas
- Registrar dificuldades comuns

### 5ª Etapa: Segurança Cibernética em SCADA (10 min)

**Vulnerabilidades Comuns**

1. **Senhas padrão** (admin/admin)
2. **Protocolos sem autenticação** (Modbus)
3. **Sistemas desatualizados** (Windows XP)
4. **Redes não segregadas** (SCADA na internet)
5. **Falta de monitoramento** de acessos

**Caso Real: Stuxnet (2010)**
- Worm que atacou centrífugas nucleares iranianas
- Explorou vulnerabilidades do Windows
- Modificou código de PLCs Siemens
- Primeiro ataque cibernético a infraestrutura crítica

**Boas Práticas de Segurança**

✅ Segmentar redes (Purdue Model)

✅ Implementar firewalls industriais

✅ Atualizar sistemas regularmente

✅ Usar autenticação forte

✅ Monitorar logs de acesso

✅ Realizar auditorias de segurança

✅ Treinar equipe em conscientização

**Norma IEC 62443**
- Padrão internacional para segurança de sistemas de automação
- 4 pilares: Políticas, Procedimentos, Sistema, Componentes

## 🎯 Avaliação

### Avaliação Prática (60%)

**Critérios do Projeto em Laboratório:**

| Critério | Peso | Descrição |
|----------|------|-------------|
| Comunicação | 15% | Conexão SCADA-PLC funcionando |
| Tags | 15% | Tags criados e vinculados corretamente |
| Interface | 25% | Tela intuitiva e funcional |
| Alarmes | 15% | Alarmes configurados adequadamente |
| Histórico | 10% | Armazenamento e visualização de dados |
| Funcionalidade | 20% | Sistema completo operando |

### Avaliação Teórica (40%)

**Questões Conceituais:**

1. Defina SCADA e explique suas principais funções.
2. Diferencie SCADA de DCS, citando exemplos de aplicação.
3. Explique o funcionamento do protocolo Modbus TCP.
4. Liste 5 vulnerabilidades comuns em sistemas SCADA.
5. Descreva os componentes de uma arquitetura SCADA típica.

**Questão Prática:**
Projetar a arquitetura SCADA para uma estação de tratamento de água com 5 poços distribuídos em 10 km, incluindo:
- Diagrama de arquitetura
- Protocolos de comunicação
- Principais telas supervisorias
- Pontos críticos de segurança

## 📚 Recursos Complementares

### Bibliografia
- **Stuart A. Boyer** - "SCADA: Supervisory Control and Data Acquisition"
- **Gordon Clarke, Deon Reynders** - "Practical Modern SCADA Protocols"
- **ISA-95** - Padrão de integração empresa-controle

### Vídeos e Tutoriais
- [ISA - Introduction to SCADA](https://www.isa.org/)
- [RealPars - SCADA Tutorials](https://realpars.com/)
- [Automation.com - SCADA Fundamentals](https://www.automation.com/)

### Software para Estudo
- **ScadaBR** (Open Source)
- **OpenSCADA** (Open Source)
- **Ignition by Inductive Automation** (Trial 2h reset)
- **Factory I/O** (Simulador 3D de processos)

### Sites e Comunidades
- [PLCTalk Forum](https://plctalk.net/)
- [Automation Forum](https://control.com/)
- [ICS-CERT](https://www.cisa.gov/ics) - Segurança cibernética

## 🔄 Próximos Passos

### Continuidade do Aprendizado

**Próxima Aula:**
- Programação de scripts em SCADA (VBScript, Python)
- Integração com bancos de dados (SQL)
- Relatórios automatizados

**Projeto Integrador:**
Desenvolver sistema SCADA completo para miniplanta industrial didática.

### Certificações Recomendadas
- **ISA Certified Control Systems Technician (CCST)**
- **Rockwell Automation ControlLogix Specialist**
- **Siemens SIMATIC Certification**

## 📝 Observações do Professor

### Pontos de Atenção
- Garantir que todos os softwares estejam instalados e licenciados
- Verificar conectividade de rede antes da aula
- Ter plano B caso equipamento falhe (usar simulador)
- Enfatizar aspectos de segurança desde o início

### Adaptações Sugeridas

**Para turmas iniciantes:**
- Reduzir complexidade do projeto prático
- Fornecer templates prontos de telas
- Focar em um único protocolo (Modbus)

**Para turmas avançadas:**
- Incluir OPC-UA e comunicação com ERP
- Abordar redundância e alta disponibilidade
- Projeto com múltiplos processos integrados

### Conteúdo de Marcus Vasconcellos
Como profissional com mais de 20 anos em automação industrial e cibersegurança, este plano de aula reflete experiência prática em sistemas como **ABB 800xA**, **Autronica Autrosafe 4** e integração de protocolos industriais (Modbus, OPC). A ênfase em segurança cibernética é fundamental no contexto atual da Indústria 4.0.

## ✅ Checklist Final

**Preparação (1 dia antes)**
- [ ] Testar todos os equipamentos
- [ ] Verificar licenças de software
- [ ] Preparar bancadas de laboratório
- [ ] Configurar rede e endereçamento IP
- [ ] Carregar programas nos PLCs

**Material Didático**
- [ ] Slides da apresentação
- [ ] Roteiros de prática impressos
- [ ] Lista de exercícios teóricos
- [ ] Diagramas P&ID do processo

**Durante a Aula**
- [ ] Registrar presença
- [ ] Documentar dúvidas frequentes
- [ ] Fotografar projetos dos alunos
- [ ] Anotar sugestões de melhoria

**Pós-Aula**
- [ ] Disponibilizar materiais no AVA
- [ ] Enviar exercícios complementares
- [ ] Agendar atendimento para dúvidas
- [ ] Preparar feedback individualizado

---

📌 **Nota**: Este plano de aula foi desenvolvido com base em experiência prática em automação industrial e utilizando técnicas de ensino ativo para maximizar o aprendizado prático dos alunos.

👨‍💻 **Desenvolvido por**: Marcus Vasconcellos - Engenheiro de Automação Industrial