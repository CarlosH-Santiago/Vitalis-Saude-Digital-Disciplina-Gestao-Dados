
# **Entrega 1 — Data Architecture (Visão Macro)**
*Responsável: Carlos Henrique De Souza Santana Santiago*

## **1.A. Sistemas**
- Qual é o papel principal deste sistema na operação?
- Quem é o usuário direto dele (médico, paciente, equipe financeira, diretoria)?
- Ele é um sistema de entrada de dados, de processamento ou de análise?

* **Aplicativo Mobile/Web do Paciente**
  * **Papel:** Agendamento de consultas, acesso à sala virtual de telemedicina e consulta de receitas e exames.
  * **Usuário Direto:** Pacientes (B2C).
  * **Tipo:** Entrada e consulta de dados.

* **Sistema Administrativo (VitalisConnect)**
  * **Papel:** Gestão de agendas, preenchimento do Prontuário Eletrônico do Paciente (PEP) e emissão de prescrições.
  * **Usuário Direto:** Médicos, enfermeiros e recepcionistas (B2B).
  * **Tipo:** Entrada e processamento operacional.

* **Sistema de Pagamentos (Gateway)**
  * **Papel:** Processamento de pagamentos de consultas e cobrança das assinaturas das clínicas.
  * **Usuário Direto:** Pacientes, gestores de clínicas e equipe financeira.
  * **Tipo:** Processamento transacional financeiro.

* **CRM de Suporte**
  * **Papel:** Registro e acompanhamento de chamados técnicos e dúvidas operacionais.
  * **Usuário Direto:** Equipe de atendimento, clínicas parceiras e pacientes.
  * **Tipo:** Gestão de atendimento.

* **Banco Operacional (OLTP - PostgreSQL)**
  * **Papel:** Armazenamento relacional de dados transacionais com garantia de consistência e baixa latência.
  * **Usuário Direto:** Serviços de backend da aplicação e administradores de banco de dados.
  * **Tipo:** Armazenamento transacional (OLTP).

* **Data Warehouse (OLAP - Redshift)**
  * **Papel:** Armazenamento consolidado do histórico operacional para análise de dados e geração de relatórios.
  * **Usuário Direto:** Engenheiros de dados e analistas de BI.
  * **Tipo:** Armazenamento e processamento analítico (OLAP).

* **Sistema de BI (Metabase / Power BI)**
  * **Papel:** Exibição de painéis gerenciais e indicadores de desempenho da operação.
  * **Usuário Direto:** Diretoria executiva e gestores de clínicas.
  * **Tipo:** Visualização e análise de dados.

* **Servidor de Mídia (WebRTC)**
  * **Papel:** Transmissão de áudio e vídeo em tempo real durante as teleconsultas.
  * **Usuário Direto:** Médicos e pacientes em atendimento.
  * **Tipo:** Infraestrutura de comunicação em tempo real.

* **Repositório de Arquivos (AWS S3)**
  * **Papel:** Armazenamento de arquivos pesados, como exames em PDF, laudos e imagens no padrão DICOM.
  * **Usuário Direto:** Aplicação backend, médicos e pacientes.
  * **Tipo:** Armazenamento não estruturado (Object Storage).







