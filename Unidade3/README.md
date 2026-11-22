# Unidade 3 — Estudo de caso: Clínica Vida+ Saúde

**Tema:** atendimento e agendamento de consultas  
**Disciplina:** Engenharia de Requisitos  
**Curso:** Engenharia de Software

---

## 📑 Sumário

1. [Processo analisado](#1-processo-analisado)
2. [Pessoas envolvidas](#2-pessoas-envolvidas)
3. [Como o processo funciona hoje](#3-como-o-processo-funciona-hoje)
4. [Atividades e requisitos](#4-atividades-e-requisitos)
5. [Regras e dificuldades](#5-regras-e-dificuldades)
6. [Modelo atual e melhorias](#6-modelo-atual-e-melhorias)

## 1. Processo analisado

**1. Qual é o nome do processo?**

R: Atendimento e agendamento de consultas médicas.

**2. Qual é o objetivo do processo?**

R: Organizar o atendimento e reduzir a fragmentação das informações da Clínica Vida+ Saúde.

**3. Quem é o cliente do processo?**

R: Pacientes e equipe administrativa.

**4. Quem executa as atividades?**

R: Principalmente a equipe administrativa; o médico participa da consulta e do registro do atendimento.

**5. Quem gerencia o processo?**

R: A gestão da clínica.

**6. Qual evento inicia o processo?**

R: Quando o paciente entra em contato para pedir uma consulta.

**7. Qual evento encerra o processo?**

R: Quando a consulta fica agendada, é cancelada ou acontece.

**8. Qual valor é entregue ao cliente?**

R: Uma forma mais simples de marcar e acompanhar a consulta.

## 2. Pessoas envolvidas

| Pessoa ou grupo | O que busca | Como participa | Necessidade principal |
|---|---|---|---|
| Paciente | Marcar uma consulta sem confusão de horários nem repetição de dados. | Pede o agendamento presencialmente ou por um canal online. | Cadastro fácil de localizar, agilidade e lembretes. |
| Recepcionista | Organizar os horários e evitar retrabalho com planilhas. | Consulta a agenda, cadastra pacientes e confirma consultas. | Agenda atualizada, busca rápida e remarcação simples. |
| Médico | Consultar uma agenda organizada e atender no horário. | Realiza as consultas e registra os atendimentos. | Evitar horários duplicados e acessar o histórico necessário. |
| Gerência | Acompanhar a rotina e identificar o que precisa melhorar. | Analisa a agenda e os resultados do atendimento. | Indicadores e visão geral do processo. |
| Direção | Melhorar o atendimento e reduzir problemas da clínica. | Acompanha os resultados e toma decisões. | Informações para orientar decisões e controlar custos. |
| Equipe de TI | Manter o sistema funcionando e prestar suporte. | Desenvolve, atualiza e dá suporte à solução. | Requisitos claros, proteção dos dados e facilidade de manutenção. |

---

## 3. Como o processo funciona hoje

### Quem participa?

**Quem é o cliente?**

O paciente é quem solicita o atendimento.

**Quem executa as atividades?**

A recepção cuida dos cadastros, agendamentos, confirmações e cancelamentos. O médico atende o paciente e registra as informações da consulta.

**Quem gerencia?**

A direção e as pessoas responsáveis pela operação da clínica.

**Quem fornece informações?**

O paciente informa seus dados e o médico mantém sua disponibilidade atualizada.

**Quem participa das decisões?**

A equipe de recepção, os médicos e a gestão.

### O que é usado e produzido?

**Entradas:** dados do paciente, pedido de consulta e horários dos médicos.

**Saídas:** consulta marcada, confirmada, cancelada ou concluída.

**Recursos:** computadores, celulares, conexão com a internet e equipe da clínica.

**Ferramentas:** planilhas, WhatsApp, telefone e sistema usado pelo médico.

**Dificuldades:** horários duplicados, dados desatualizados, cadastros repetidos, retrabalho e falhas de comunicação.

**Ponto positivo:** os pacientes já conseguem entrar em contato por diferentes canais, e há uma equipe dedicada ao atendimento.

**O que pode ser acompanhado:** consultas realizadas, cancelamentos, faltas, remarcações e ocupação da agenda.

### Em que momento?

**Começa:** quando o paciente pede um horário.

**Acontece:** na busca por um horário e, depois, no atendimento.

**Termina:** quando a consulta ocorre ou é cancelada.

### Onde acontece?

**Início:** telefone, WhatsApp ou recepção.

**Atendimento:** na recepção e nos consultórios.

**Informações:** os horários são controlados em planilhas, enquanto os registros médicos ficam em outro sistema.

### Para que serve?

**Por que existe?**

Para marcar consultas e manter os horários dos profissionais organizados.

**Valor para o paciente:** permite encontrar um horário e acompanhar o agendamento.

**Valor para a clínica:** ajuda a clínica a controlar a agenda e o atendimento.

### Como pode funcionar com um sistema?

Um sistema web pode reunir os agendamentos em uma agenda única, acessada com login. A recepção teria as permissões necessárias para administrar os horários e os cadastros.

Na agenda, a recepção poderia consultar os horários livres, marcar consultas, confirmar, cancelar ou remarcar atendimentos. Como as alterações ficariam registradas no mesmo lugar, haveria menos risco de trabalhar com uma planilha desatualizada ou reservar duas consultas no mesmo horário.

Se um médico alterasse sua disponibilidade, a equipe atualizaria a agenda e poderia avisar os pacientes afetados.

As permissões dependeriam do perfil de cada pessoa. Por exemplo, a recepção administraria os agendamentos, enquanto outros usuários teriam acesso apenas às funções necessárias para seu trabalho.

## 4. Atividades e requisitos

| Atividade | Responsável | Entrada | Saída | Regra |
|---|---|---|---|---|
| Solicitar consulta | Paciente | Necessidade de atendimento | solicitação de consulta | O paciente deve informar os dados necessários para solicitar a consulta. |
| Localizar paciente | Recepção | Pedido de consulta | Cadastro localizado | O cadastro deve ser conferido antes de marcar. |
| Consultar agenda | Recepção | Dados do paciente e pedido | Horários do médico | A agenda deve ser verificada antes da escolha do horário. |
| Verificar horário | Recepção | Agenda do médico | Horário livre ou ocupado | A consulta só pode ser marcada em horário livre. |
| Registrar consulta | Recepção | Paciente e horário escolhido | Agendamento criado | O registro deve conter paciente, médico, data e horário. |

---

## Requisitos Funcionais

1. O sistema deve receber pedidos de consulta feitos pelos pacientes.
2. A equipe deve conseguir localizar um paciente pelo nome, CPF ou telefone.
3. A recepção deve visualizar os horários livres e ocupados de cada médico.
4. Antes de salvar uma consulta, o sistema deve conferir se o horário continua disponível.
5. O agendamento deve relacionar paciente, médico, data e horário.
6. A recepção deve poder confirmar, cancelar ou remarcar uma consulta e enviar a confirmação ao paciente pelo canal disponível.
7. O médico deve consultar as informações necessárias para atender o paciente e registrar a consulta.
8. O sistema deve apresentar relatórios de consultas e faltas por período.

## Requisitos Não Funcionais

1. Somente usuários autorizados devem acessar dados pessoais e informações médicas.
2. O acesso às funções deve respeitar as permissões definidas para cada perfil.
3. A agenda deve ser atualizada para reduzir o risco de horários duplicados.
4. As consultas de disponibilidade devem responder sem atrasar o trabalho da recepção.
5. As telas e mensagens devem ser claras para que a equipe consiga realizar as tarefas do dia a dia.
6. O sistema deve estar disponível durante o expediente da clínica.

---

## 5. Regras e dificuldades

| Código | Regra de Negócio | Origem |
|---|---|---|
| RN01 | O paciente deve possuir cadastro para realizar um agendamento. | Processo da clínica |
| RN02 | Um médico não pode ter dois pacientes no mesmo horário. | Agenda médica |
| RN03 | A consulta só pode ser marcada em um horário disponível. | Agenda médica |
| RN04 | O cancelamento deve liberar o horário do médico. | Processo de agendamento |
| RN05 | Os dados do paciente devem ser conferidos antes do agendamento. | Recepção |
| RN06 | Alterações na agenda do médico devem ser informadas aos pacientes afetados. | Gestão da clínica |
| RN07 | O agendamento deve conter data, horário, paciente e médico. | Processo de agendamento |
| RN08 | O atendimento deve ser registrado após a consulta. | Médico |
| RN09 | Uma consulta cancelada pode ser remarcada para outro horário disponível. | Recepção |
| RN10 | Cada usuário deve acessar somente as funções permitidas pelo seu perfil. | Gestão/TI |

---

### Problemas observados

| Problema | Causa provável | Impacto | Prioridade |
|---|---|---|---|
| Conflito de horários | Uso de planilhas diferentes | Agendamentos duplicados | 🔴 Alta |
| Retrabalho | Informações espalhadas | Perda de tempo | 🔴 Alta |
| Cadastro repetido | Falta de cadastro centralizado | Demora no atendimento | 🟡 Média |
| Informações desatualizadas | Planilhas não atualizadas ao mesmo tempo | Erros nos agendamentos | 🔴 Alta |
| Falta de lembretes | Processo feito manualmente | Aumento das faltas | 🟡 Média |
| Cancelamentos manuais | Falta de controle centralizado | Dificuldade para liberar horários | 🟡 Média |
| Alteração da agenda do médico | Comunicação individual | Retrabalho da recepção | 🔴 Alta |
| Falha na confirmação | WhatsApp e planilha separados | Paciente pode ficar sem atendimento | 🔴 Alta |

---

## 6. Modelo atual e melhorias

### Fluxo atual (AS-IS)

O fluxograma do processo atual deve mostrar:

- início e fim do processo;
- atividades e responsáveis;
- decisões e caminhos alternativos;
- entradas, saídas e regras envolvidas.

### Melhorias sugeridas

| Problema | Melhoria proposta | Benefício esperado |
|---|---|---|
| Conflito de horários | Agenda centralizada | Redução de conflitos e agendamentos duplicados |
| Cadastro duplicado | Cadastro único de pacientes | Redução de retrabalho e maior organização das informações |
| Falta de lembretes | Envio automático de lembretes | Redução de faltas e maior pontualidade dos pacientes |
| Cancelamentos feitos manualmente | Cancelamento e remarcação pelo sistema | Maior agilidade e atualização automática da agenda |
| Alterações na agenda do médico | Atualização da agenda em tempo real | Evita informações desatualizadas e reduz erros |
| Controle de acesso limitado | Login com diferentes níveis de permissão | Maior segurança das informações e controle das operações |
| Dificuldade para consultar horários | Visualização dos horários disponíveis no sistema | Agendamentos mais rápidos e facilidade para encontrar horários |
| Comunicação de alterações aos pacientes | Notificações automáticas | Melhoria na comunicação e redução de esquecimentos e desencontros |

---

*Trabalho acadêmico da disciplina de Engenharia de Requisitos.*
