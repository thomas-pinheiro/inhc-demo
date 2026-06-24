# Gestão de Espaços e Infraestrutura

## Visão Geral

Sistema para gerenciamento de espaços e infraestrutura do campus, permitindo:

- Consulta da disponibilidade de salas;
- Registro de problemas de infraestrutura;
- Acompanhamento de chamados;
- Centralização das informações para coordenação, professores e alunos.

---

# Análise de Viabilidade

## Produto (PM)

### Pontos Positivos

- Beneficia diretamente a gestão do campus.
- Reduz conflitos de sala e problemas sem reporte formal.

### Problemas e Soluções

| Problema | Solução |
|-----------|----------|
| Quem atualiza a disponibilidade das salas? | Coordenação juntamente com a portaria do curso, se necessário. |
| O setor de manutenção precisa estar comprometido para responder aos chamados. | Não existe solução técnica; depende da gestão. |
| Salas vagas podem ser ocupadas sem aviso no sistema. | Uso das salas condicionado à consulta e atualização no sistema. |

---

## Capacidade (DEV)

### Pontos Positivos

- Formulário de chamado é tecnicamente simples.
- Calendário de salas é um CRUD básico.
- Pode ser desenvolvido pelo time com as tecnologias que já conhecem.

### Problemas e Soluções

| Problema | Solução |
|-----------|----------|
| Integração com grade horária real é complexa. | V1 com inserção manual das salas e horários pela coordenação. |
| Atualização em tempo real exige mais infraestrutura. | Implementar em versões futuras, se necessário. |
| Algoritmo ingessado pode dificultar mais do que ajudar. | Não há solução definida no material. |

---

## Desejabilidade (UX)

### Pontos Positivos

- Professores e alunos sofrem com salas ocupadas sem aviso.
- Problemas de infraestrutura sem registro pioram com o tempo.
- Centraliza informação hoje fragmentada.
- Acompanhar o status do problema reportado gera confiança de que foi registrado e não ignorado.

### Problemas e Soluções

| Problema | Solução |
|-----------|----------|
| Professores e alunos podem ter resistência ao cadastro. | Ver salas estará disponível na portaria sem login; reportar problemas exige matrícula. |
| Alunos podem não confiar que o problema será resolvido. | Mostrar status do chamado (aberto, em andamento, resolvido ou em espera). |
| Pode cair em desuso sem resposta rápida da manutenção. | Gerar relatório para gestão de problemas não solucionados e prazos atrasados |

---

# Personas

## Marcos Andrade Silva

### Quem é?

- Trabalhador
- Organizado
- Frustrado com imprevistos

### Informações Demográficas

- 45 anos
- Professor substituto da disciplina de Introdução a Redes
- Trabalha em mais dois campi do IFAL (Centro e Benedito Bentes)
- Atua há 10 anos na instituição

### Comportamentos

- Chega ao campus com antecedência para preparar a aula.
- Procura por salas disponíveis manualmente.
- Já precisou perder tempo de aula para procurar sala desocupada.
- Reclama com a coordenação, mas o problema nem sempre é resolvido.

### Necessidades e Objetivos

- Saber, antes de se deslocar, se a sala está disponível e em condições de uso.
- Reportar rapidamente um problema (projetor quebrado, ar-condicionado etc.) sem burocracia.
- Encontrar rapidamente uma sala disponível sem precisar ir até ela para verificar.

---

## Camila Ferreira Souza

### Quem é?

- Atenta
- Comunicativa
- Desconfiada de processos lentos

### Informações Demográficas

- 21 anos
- Estudante do 4º semestre de BSI
- Turno noturno
- Trabalha durante o dia em uma loja de informática
- Utiliza o campus principalmente à noite, com pouco contato com a coordenação

### Comportamentos

- Percebe problemas estruturais durante as aulas.
- Comenta com colegas da turma, mas raramente reporta formalmente.
- Já desistiu de avisar a coordenação por achar que não vai resolver.
- Utiliza o celular para se manter atualizada.

### Necessidades e Objetivos

- Reportar um problema de infraestrutura de forma simples.
- Não precisar de cadastro complexo ou burocrático.
- Ter certeza de que o chamado foi registrado e não ignorado.
- Acompanhar o status do chamado (aberto, em andamento ou resolvido).

---

## Roberta Lima Costa

### Quem é?

- Sobrecarregada
- Pragmática
- Resistente a mudanças complexas

### Informações Demográficas

- 45 anos
- Coordenadora do curso de BSI
- Acumula funções administrativas e atendimento a alunos e professores
- Trabalha com apoio da portaria para controle de salas

### Comportamentos

- Mantém planilhas e registros manuais para controlar horários e disponibilidade.
- Prioriza soluções simples por falta de tempo para aprender ferramentas complexas.
- Depende do setor de manutenção, que nem sempre responde rapidamente.

### Necessidades e Objetivos

- Ter uma visão centralizada da disponibilidade das salas.
- Visualizar e gerenciar os chamados de manutenção recebidos.
- Acompanhar status atualizados dos chamados.
- Reduzir o volume de solicitações informais e dispersas (e-mail, WhatsApp e atendimento presencial).

---

# Funcionalidades do MVP

## Gestão de Salas

- Cadastro de salas.
- Cadastro de horários.
- Consulta de disponibilidade.
- Calendário de ocupação.
- Controle básico de utilização.

## Gestão de Infraestrutura

- Abertura de chamados.
- Registro de problemas estruturais.
- Acompanhamento do andamento da solicitação.

## Status de Chamados

- Aberto
- Em andamento
- Resolvido
- Em espera

## Administração

- Atualização manual de salas e horários pela coordenação.
- Apoio da portaria na manutenção das informações.
- Visualização centralizada dos dados.

---

# Evoluções Futuras

- Integração com a grade horária oficial.
- Atualização em tempo real da ocupação das salas.
- Notificações para usuários.
- Automatização de processos de reserva e ocupação.