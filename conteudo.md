**Sistemas de Informação - IFAL, Maceió - Interação Humano Computador (INHC)**

---

## 1 INTRODUÇÃO

A gestão eficiente dos espaços físicos em instituições de ensino superior é um fator crítico para o bom andamento das atividades acadêmicas e administrativas. No entanto, é comum observar processos manuais e descentralizados para a reserva de salas e laboratórios, o que gera retrabalho, conflitos de horários, perda de tempo e insatisfação entre alunos, professores e servidores. Ademais, a comunicação sobre problemas estruturais – como defeitos em equipamentos de climatização, iluminação ou mobiliário – frequentemente ocorre por canais informais (mensagens de texto, e-mails ou contato pessoal), dificultando o rastreamento, a priorização e a resolução ágil dessas demandas.

No Instituto Federal de Alagoas – Campus Maceió, essa realidade se manifesta na rotina diária da comunidade acadêmica. Atualmente, a reserva de salas depende, em grande parte, do deslocamento até a secretaria ou do preenchimento de planilhas, o que sobrecarrega os servidores e limita a transparência sobre a real disponibilidade dos espaços. Paralelamente, o reporte de problemas de infraestrutura carece de um canal único e padronizado, o que muitas vezes leva à demora na solução ou até mesmo ao esquecimento da solicitação.

Diante desse cenário, este projeto propõe o desenvolvimento de um protótipo de sistema integrado para reserva de salas e reporte de problemas estruturais no IFAL – Campus Maceió. A solução visa oferecer uma experiência digital intuitiva, acessível e eficiente, permitindo que alunos, professores, coordenadores e equipe de manutenção interajam com os espaços de forma transparente e ágil. Ao adotar os princípios da Interação Humano-Computador (IHC) e a metodologia Design Thinking, busca-se colocar o usuário no centro do processo de design, compreendendo suas dores, necessidades e expectativas para construir uma ferramenta que realmente transforme a gestão dos espaços acadêmicos.

**Objetivo Geral:** Desenvolver um protótipo de sistema integrado para reserva de salas e reporte de problemas estruturais no IFAL – Campus Maceió, alinhado aos princípios da Interação Humano-Computador e da metodologia Design Thinking.

**Objetivos Específicos:**

- Realizar levantamento de requisitos e necessidades dos usuários por meio de Pesquisa Documental (Desk Research), com base em trabalhos acadêmicos correlatos.
- Construir proto-personas representativas dos principais perfis de usuários do sistema (alunos, professores, coordenadores e equipe de manutenção).
- Avaliar a viabilidade, desejabilidade e capacidade técnica da solução por meio do framework Triângulo de Ouro.
- Priorizar funcionalidades essenciais por meio de User Stories, considerando impacto, dificuldade de implementação e esforço aparente.
- Elaborar um protótipo de baixa fidelidade (wireframes) que represente a arquitetura da informação e os fluxos de navegação do sistema.

O presente estudo de caso, elaborado pela equipe composta por Roque, Eduardo, Thomas e Maryane, disciplina de IHC do curso de Sistemas de Informação, documenta as etapas iniciais do projeto: empatia, definição, ideação e prototipação, servindo como base para a construção de uma solução centrada no ser humano e alinhada às demandas reais da instituição.

---

## 2 METODOLOGIA

A presente pesquisa e o desenvolvimento do protótipo fundamentam-se na metodologia Design Thinking, uma abordagem centrada no ser humano que visa solucionar problemas complexos por meio de um processo colaborativo e iterativo. Conforme proposto por Brown (2008), o Design Thinking estimula a imersão no contexto do usuário para gerar soluções inovadoras que equilibrem desejabilidade (necessidades humanas), viabilidade técnica e sustentabilidade organizacional.

Para este estudo de caso, foram percorridas as etapas de Empatia, Definição, Ideação e Prototipação, de acordo com a metodologia proposta por Vianna et al. (2012). A etapa de Testes, embora fundamental, será executada em momento posterior ao escopo deste trabalho, permanecendo como perspectiva futura. Ressalta-se que, em virtude do cronograma reduzido e da indisponibilidade para contato com os usuários reais neste momento, não foram realizadas entrevistas ou observações sistemáticas. Desta forma, as análises e constructos apresentados baseiam-se em pesquisa documental e na inferência contextual realizada pela equipe.

---

### 2.1 Empatia

A etapa de Empatia teve como objetivo principal a imersão no cotidiano dos usuários para mapear suas necessidades explícitas e implícitas. Para tanto, considerando as limitações de tempo, optou-se por uma abordagem baseada em três técnicas: Pesquisa Documental (Desk Research), construção de Proto-Personas com seus respectivos Mapas de Empatia, e User Stories.

---

### 2.1.1 Pesquisa Documental (Desk Research) – Análise de Trabalhos Relacionados

Para embasar a etapa de Empatia, foram analisados três trabalhos acadêmicos que abordam sistemas de reserva de salas e gestão de espaços em instituições de ensino. A escolha desses trabalhos justifica-se pela similaridade dos contextos (ambientes universitários e técnicos) e pela diversidade de abordagens, que vão desde a integração entre sistemas até o desenvolvimento de soluções web com módulo de reporte de problemas.

O primeiro trabalho, de Costa et al. (2025), descreve a implementação de uma integração entre uma planilha e o Sistema de Reserva de Salas (SRS) da UFERSA, automatizando um processo que antes era realizado manualmente. Os autores demonstram que a automação reduziu o tempo de cadastro de uma semana para segundos, eliminando retrabalho e erros humanos. Este estudo foi fundamental para compreender os ganhos operacionais que uma solução digital pode proporcionar.

O segundo trabalho, de Freire & Fortes (2003), apresenta o manual de uso do Sistema de Reserva de Salas da intranet do ICMC-USP, detalhando funcionalidades para diferentes perfis de usuários (acesso público, usuários cadastrados, usuários com domínio e administradores). O sistema contempla reservas fixas e eventuais, busca por horários livres e funções gerenciais. Este trabalho contribuiu para a identificação de requisitos funcionais comuns em sistemas de reserva, como a distinção entre diferentes níveis de permissão e a necessidade de calendários interativos.

O terceiro trabalho, de Silva et al. (2017), descreve o desenvolvimento de um sistema online para reservas de salas e laboratórios em uma ETEC, com funcionalidade adicional de relato de erros estruturais. Os autores destacam a importância de um canal unificado para comunicação de defeitos, com status de acompanhamento para o solicitante. Este estudo foi particularmente relevante para o presente projeto, pois incorpora o módulo de reporte de problemas, funcionalidade central da solução proposta para o IFAL.

| Fonte | Objetivo | Público-alvo | Escolaridade | Resultados/Notas Principais | Conclusões |
| --- | --- | --- | --- | --- | --- |
| Costa et al. (2025) – Revista de Sistemas e Computação – UFERSA | Automatizar o cadastro de reservas de salas, eliminando retrabalho e reduzindo erros humanos. | Funcionários da coordenadoria acadêmica e desenvolvedor do SRS. | Ensino Superior (servidores técnico-administrativos e docente). | O processo manual de reserva levava cerca de uma semana; com a integração, passou a ser concluído em segundos. Redução de horas de trabalho e eliminação de dados imprecisos. | A integração entre sistemas é essencial para otimizar processos organizacionais, reduzir sobrecarga e melhorar a confiabilidade dos dados. |
| Freire & Fortes (2003) – Relatório Técnico ICMC-USP | Descrever as funcionalidades do sistema de reservas de salas da intranet do ICMC, atendendo diferentes perfis de usuários. | Alunos, professores, secretárias, administradores e público externo. | Ensino Superior (graduação, pós-graduação e corpo técnico-administrativo). | Sistema com níveis de acesso (público, cadastrado, com domínio, administrador) permite reservas fixas e eventuais, busca por horários livres, e funções de gerenciamento de salas e usuários. | A agenda colaborativa demonstrou ser uma ferramenta útil para o planejamento acadêmico, reduzindo conflitos e melhorando a comunicação entre os envolvidos. |
| Silva et al. (2017) – TCC ETEC Prof. Massuyuki Kawano | Desenvolver um sistema online para reservas de salas/laboratórios e relato de problemas estruturais na instituição. | Alunos e professores da ETEC. | Ensino Médio/Técnico. | Sistema com login, visualização de ambientes por período, reserva com data/horário, relato de erros com status, e painel administrativo para gerenciar usuários, reservas e problemas. | A digitalização do processo de reserva e a possibilidade de reportar falhas facilitam a organização e a manutenção, evitando o uso de papel e agilizando a comunicação com os responsáveis. |

---

### 2.1.2 Proto-Personas

Para representar os principais perfis de usuários do sistema, foram construídas quatro proto-personas, que sintetizam características demográficas, comportamentos, necessidades e objetivos extraídos da literatura analisada e da vivência acadêmica da equipe no campus.

---

### Marcos Andrade Silva – Professor

**Quem é?**
Trabalhador, organizado e frequentemente frustrado com imprevistos de infraestrutura.

**Informações Demográficas**
Marcos Andrade Silva tem 45 anos e atua como professor substituto da disciplina de Introdução a Redes no IFAL. Leciona em três campi diferentes (Maceió, Centro e Benedito B.) e, por isso, sua rotina é marcada por deslocamentos e pela necessidade de otimizar o tempo. Há 10 anos na instituição, é uma pessoa organizada, mas frequentemente frustrada com imprevistos relacionados à infraestrutura.

**Comportamentos**
Seu comportamento típico inclui chegar ao campus com antecedência para preparar a aula e, em seguida, percorrer os corredores em busca de salas disponíveis de forma manual. Já perdeu tempo valioso de aula simplesmente para encontrar um espaço desocupado, e reclama com a coordenação, mas sente que o problema não é resolvido.

**Necessidades e Objetivos**
Marcos precisa saber, antes de se deslocar, se a sala está disponível e em condições de uso. Deseja reportar rapidamente problemas como projetor quebrado ou ar-condicionado defeituoso, sem burocracia. Além disso, almeja encontrar uma sala livre de forma ágil, sem precisar ir até o local para verificar pessoalmente.

---

**Mapa de Empatia – Marcos (Professor)**

| Dimensão | Conteúdo |
| --- | --- |
| **Pensa e Sente** | Sente que seu tempo é desperdiçado em tarefas que deveriam ser simples. Pensa que a instituição poderia ser mais organizada. Fica ansioso quando não sabe se a sala estará disponível antes de se deslocar. |
| **Ouve** | Colegas reclamando dos mesmos problemas. Coordenação pedindo que “aguarde” ou “mande e-mail”. Alunos perguntando onde será a aula. |
| **Vê** | Salas ocupadas sem aviso. Projetores quebrados sem data de conserto. Planilhas desatualizadas na secretaria. |
| **Diz e Faz** | Reclama com a coordenação, mas desiste com o tempo. Chega mais cedo para “garantir” uma sala. Manda mensagens no WhatsApp para descobrir disponibilidade. |
| **Dores** | Perda de tempo de aula. Falta de previsibilidade. Sensação de descaso institucional. |
| **Necessidades** | Consultar disponibilidade de qualquer lugar, antes de se deslocar. Reportar problemas com rapidez e ter retorno sobre a resolução. |

---

### Roberto Lima Costa – Coordenador

**Quem é?**
Sobrecarregado, pragmático e resistente a mudanças complexas.

**Informações Demográficas**
Roberto Lima Costa, 45 anos, é o coordenador do curso de Bacharelado em Sistemas de Informação (BSI). Acumula funções administrativas, atendimento a alunos e professores, e ainda precisa gerenciar o controle de salas com o apoio da portaria. Sente-se sobrecarregado, é pragmático e demonstra certa resistência a mudanças complexas, pois já tem uma rotina intensa.

**Comportamentos**
Seu comportamento reflete essa sobrecarga: mantém planilhas e papéis manuais para controlar horários e disponibilidade. Prioriza soluções simples por falta de tempo para aprender ferramentas complexas. Depende do setor de manutenção, que nem sempre responde com rapidez. Lida com solicitações informais por e-mail, WhatsApp e contato presencial, o que dificulta o rastreamento e a priorização das demandas.

**Necessidades e Objetivos**
Roberto almeja ter uma visão centralizada da disponibilidade das salas, de modo a planejar a alocação com mais segurança. Precisa visualizar e gerenciar todos os chamados de manutenção recebidos, com status atualizado, para poder acompanhar as soluções. Seu objetivo principal é reduzir o volume de solicitações informais e eliminar a dependência de canais dispersos (e-mail, WhatsApp, atendimento presencial), tornando o processo mais organizado e mensurável.

---

**Mapa de Empatia – Roberto (Coordenador)**

| Dimensão | Conteúdo |
| --- | --- |
| **Pensa e Sente** | Sente que está sempre “apagando incêndio”. Pensa que precisaria de mais tempo e de uma ferramenta que centralize tudo. Preocupa-se com conflitos de sala que passam despercebidos. |
| **Ouve** | Professores reclamando de salas ocupadas. Alunos reclamando de problemas não resolvidos. Equipe de manutenção dizendo que “não foi avisada”. |
| **Vê** | Planilhas desatualizadas. Mensagens de WhatsApp em vários grupos diferentes. Salas sendo usadas sem reserva formal. |
| **Diz e Faz** | Anota pedidos em papel. Encaminha demandas manualmente por e-mail. Tenta coordenar horários via planilhas compartilhadas. |
| **Dores** | Falta de visibilidade sobre a ocupação real das salas. Dificuldade de rastrear chamados de manutenção. Volume excessivo de solicitações informais. |
| **Necessidades** | Painel centralizado com todas as reservas e chamados. Reduzir comunicação informal e fragmentada. Ter histórico de reservas e manutenções. |

---

### Camila Ferreira Souza – Aluna

**Quem é?**
Atenta, comunicativa e desconfiada de processos lentos.

**Informações Demográficas**
Camila Ferreira Souza tem 21 anos e cursa o 4º semestre de BSI no turno noturno. Durante o dia, trabalha em uma loja de informática, o que limita seu contato com a coordenação e com os serviços administrativos do campus. É atenta e comunicativa, mas desconfia de processos lentos, pois já presenciou diversas situações em que problemas estruturais demoraram a ser resolvidos.

**Comportamentos**
Seu comportamento é marcado pela percepção constante de defeitos durante as aulas – cadeiras quebradas, lâmpadas queimadas, ar-condicionado com mau funcionamento. Comenta esses problemas com os colegas, mas raramente reporta formalmente, pois já desistiu de avisar a coordenação por acreditar que “não vai resolver mesmo”. Utiliza o celular para se manter atualizada e espera que o sistema seja acessível pelo dispositivo móvel.

**Necessidades e Objetivos**
Camila deseja reportar um problema de infraestrutura de forma simples e rápida, preferencialmente sem a necessidade de cadastro ou login complicado. Quer ter certeza de que seu chamado foi registrado e não será ignorado, e por isso valoriza a possibilidade de acompanhar o status da solicitação (aberto, em andamento, resolvido) de maneira transparente e acessível.

---

**Mapa de Empatia – Camila (Aluna)**

| Dimensão | Conteúdo |
| --- | --- |
| **Pensa e Sente** | Sente que reclamar é inútil porque nada muda. Pensa que seria mais fácil se houvesse um jeito simples de registrar o problema pelo celular. Espera que alguém tome iniciativa, mas geralmente ninguém o faz. |
| **Ouve** | Colegas reclamando dos mesmos problemas. “Vai lá na coordenação falar.” “Manda mensagem pro professor.” |
| **Vê** | Salas com equipamentos quebrados há semanas. Nenhum retorno visível após reclamações informais. Colegas desistindo de reportar. |
| **Diz e Faz** | Comenta com colegas, mas não formaliza a reclamação. Usa o celular para praticamente tudo. Prefere canais rápidos como WhatsApp. |
| **Dores** | Sensação de que sua reclamação não será vista nem resolvida. Processo de reporte atual é lento e burocrático. Falta de retorno sobre o andamento. |
| **Necessidades** | Reportar um problema pelo celular em menos de 1 minuto, sem login complexo. Acompanhar o status do chamado para saber se foi registrado e está sendo tratado. |

---

### Carlos Mendes da Silva – Técnico de Manutenção

**Quem é?**
Proativo, pragmático e frustrado com a desorganização das demandas que recebe.

**Informações Demográficas**
Carlos Mendes da Silva, 38 anos, é técnico de manutenção do IFAL Campus Maceió. Atua na instituição há 6 anos e é responsável por atender chamados de reparo em salas, laboratórios e áreas comuns. Recebe solicitações por canais informais (WhatsApp pessoal, recados verbais, bilhetes) e não dispõe de nenhuma ferramenta centralizada para organizar e priorizar seu trabalho.

**Comportamentos**
Carlos começa o dia sem uma lista clara do que precisa ser feito. Recebe mensagens de WhatsApp de professores, coordenadores e funcionários com diferentes graus de urgência, sem nenhum padrão. Frequentemente descobre que um problema “resolvido” voltou a ocorrer, mas não há histórico formal. Quando conclui um reparo, não tem como notificar o solicitante de forma oficial — precisa mandar mensagem individualmente.

**Necessidades e Objetivos**
Carlos precisa de uma lista organizada de todos os chamados abertos, com informações sobre local, tipo de problema e data de abertura. Deseja poder atualizar o status de cada chamado (em análise, resolvido) para que o solicitante seja notificado automaticamente, sem depender de contato individual. Almeja ter um histórico dos problemas resolvidos por sala, o que facilitaria a identificação de defeitos recorrentes e a justificativa para solicitações de verba de manutenção.

---

**Mapa de Empatia – Carlos (Técnico de Manutenção)**

| Dimensão | Conteúdo |
| --- | --- |
| **Pensa e Sente** | Sente que está sempre correndo atrás de informações dispersas. Pensa que seria muito mais fácil se houvesse uma lista organizada de problemas. Preocupa-se em não deixar chamados urgentes passarem despercebidos. |
| **Ouve** | “Carlos, o ar-condicionado da sala 3 quebrou de novo.” “Ninguém veio olhar aqui ainda.” “Você recebeu meu recado?” |
| **Vê** | Mensagens de WhatsApp em diferentes grupos. Bilhetes colados em portas. Problemas antigos que voltam a aparecer sem histórico. |
| **Diz e Faz** | Tenta organizar as demandas em anotações pessoais. Avisa sobre a resolução por WhatsApp individual. Prioriza por memória e urgência percebida. |
| **Dores** | Falta de padronização nos chamados recebidos. Impossibilidade de priorizar sem informação clara. Ausência de histórico para identificar problemas recorrentes. |
| **Necessidades** | Lista centralizada de chamados com local, categoria e urgência. Poder atualizar o status e notificar o solicitante automaticamente. Histórico por sala para suportar decisões de manutenção preventiva. |

---

### 2.1.3 User Stories

| Problema | User Story | Persona de Origem | Impacto (Qtd. Usuários) | Dificuldade (Resolução) | Prioridade |
| --- | --- | --- | --- | --- | --- |
| Os alunos e professores não têm visibilidade em tempo real sobre quais salas estão disponíveis, precisando ir à secretaria ou perguntar a terceiros, o que gera incerteza e perda de tempo. | Como aluno ou professor, quero visualizar um calendário interativo com a ocupação de todas as salas em tempo real, para que eu possa identificar rapidamente os horários livres sem precisar me deslocar até a secretaria. | Marcos / Camila | Alto (afeta a maioria dos alunos e professores) | Baixa (implementação de calendário com consulta ao banco de dados) | **Alta** |
| O processo de reserva é manual, burocrático e sujeito a conflitos de horário, causando retrabalho para os servidores e frustração para os solicitantes. | Como aluno ou professor, quero fazer uma reserva de sala diretamente pelo sistema, selecionando data, horário e finalidade, para que o processo seja automatizado, rápido e livre de duplicidade de agendamentos. | Marcos / Camila | Alto (todos os que precisam reservar espaços) | Média (regras de negócio para validar conflitos e integrar com a base de salas) | **Alta** |
| Os usuários não conseguem cancelar ou alterar reservas de forma autônoma, dependendo de contato com a secretaria, o que gera transtornos e ocupação desnecessária de espaços. | Como aluno ou professor, quero editar ou cancelar minhas próprias reservas dentro de um prazo estipulado, para que eu possa ajustar minha programação e liberar a sala para outros usuários sem passar por intermediários. | Marcos | Médio (usuários que precisam de flexibilidade) | Baixa (operações simples de CRUD com validação de prazo) | **Média** |
| O reporte de problemas estruturais é feito de forma descentralizada (WhatsApp, e-mail, presencial), o que dificulta o rastreamento, a priorização e a comunicação com a equipe de manutenção. | Como aluno, professor ou servidor, quero relatar um problema em uma sala ou laboratório através de um formulário padronizado (com local, categoria, descrição e foto), para que minha solicitação chegue de forma organizada ao responsável e eu possa acompanhar seu status. | Camila / Marcos | Alto (toda a comunidade pode se deparar com problemas) | Média (formulário com upload de imagem e categorização) | **Alta** |
| O solicitante de um reparo não tem retorno sobre o andamento da sua solicitação, gerando sensação de descaso e necessidade de reclamar novamente. | Como usuário que reportou um problema, quero visualizar uma lista com todos os meus relatos e seus respectivos status (pendente, em análise, resolvido), para que eu saiba se minha demanda está sendo tratada e evite refazer a solicitação. | Camila | Médio (usuários que reportam problemas com frequência) | Baixa (consulta simples ao banco de dados) | **Média** |
| Os coordenadores e administradores não possuem uma visão consolidada de todas as reservas, dificultando a aprovação de eventos especiais e a identificação de conflitos. | Como coordenador ou administrador, quero visualizar todas as reservas realizadas (com filtros por sala, data e curso) e ter a permissão para aprovar ou excluir reservas conflitantes, para que eu possa gerenciar a ocupação de forma estratégica e garantir a prioridade das atividades acadêmicas. | Roberto | Baixo (apenas coordenadores e administradores) | Média (painel com filtros e ações administrativas) | **Média** |
| A equipe de manutenção recebe demandas sem padronização e sem critério de prioridade, o que atrasa a solução dos casos mais urgentes. | Como membro da equipe de manutenção, quero visualizar todos os problemas reportados em uma lista ordenável por data, local e urgência, e poder atualizar o status de cada um, para que eu possa planejar minhas ações e comunicar o progresso aos solicitantes. | Carlos | Baixo em número, mas crítico para o funcionamento do módulo de problemas | Média (interface de gestão com atualização de status) | **Alta** *(fechamento do ciclo de chamados depende desta funcionalidade)* |
| Não há um cadastro centralizado e dinâmico das salas, impossibilitando a adição ou remoção de novos espaços conforme a necessidade da instituição. | Como administrador do sistema, quero cadastrar, editar e remover salas (com informações como nome, capacidade, localização e recursos), para que o sistema reflita com precisão a infraestrutura real do campus e se adapte a mudanças. | Roberto | Baixo (apenas administradores) | Baixa (CRUD básico) | **Alta** *(pré-requisito para que o calendário e as reservas funcionem)* |
| Os usuários não possuem acesso controlado ao sistema conforme seu perfil (aluno, professor, coordenador, manutenção, administrador). | Como usuário do sistema, quero realizar login com minhas credenciais institucionais e ter acesso apenas às funcionalidades correspondentes ao meu perfil, para que o sistema seja seguro e cada pessoa veja somente o que é relevante para ela. | Todos | Alto (todos os usuários) | Média (autenticação com controle de papéis/permissões) | **Alta** *(pré-requisito de segurança para todo o sistema)* |

---

### 2.2 Definição

Nesta fase, consolidaram-se as informações levantadas na etapa anterior para estabelecer um ponto de vista claro sobre o problema central. A partir da síntese das dores e necessidades mapeadas nas quatro proto-personas, foram elaboradas questões norteadoras (perguntas “Como Poderíamos?”) específicas para cada perfil de usuário:

- **Como poderíamos** ajudar professores como Marcos a saberem, antes mesmo de sair de casa, se uma sala está disponível e em boas condições de uso, sem precisar se deslocar ou ligar para a secretaria?
- **Como poderíamos** tornar o reporte de problemas tão simples e transparente que alunos como Camila deixem de desistir de reportar, por terem a certeza de que o chamado será visto e tratado?
- **Como poderíamos** oferecer ao coordenador Roberto uma visão centralizada de todas as reservas e chamados, reduzindo drasticamente o volume de solicitações informais por WhatsApp e e-mail?
- **Como poderíamos** garantir que o técnico Carlos receba chamados organizados, com informação suficiente para priorizar seu trabalho e comunicar o progresso ao solicitante sem esforço adicional?

Com base nessas perguntas norteadoras e nas necessidades levantadas pelas proto-personas, foram elencados os seguintes requisitos funcionais e não funcionais para o sistema:

**Requisitos Funcionais:**

| Código | Descrição | Persona de Origem |
| --- | --- | --- |
| RF001 | **Visualizar calendário de disponibilidade:** O sistema deve exibir a ocupação das salas em formato de calendário semanal ou mensal, com indicação visual (cores) para salas livres (verde), ocupadas (vermelho) ou com problemas reportados (amarelo). | Marcos / Camila |
| RF002 | **Realizar reserva de sala:** O sistema deve permitir que usuários autenticados façam reservas selecionando sala, data, horário de início e fim, além de finalidade. O sistema deve validar conflitos de horário automaticamente. | Marcos / Camila |
| RF003 | **Gerenciar reservas próprias:** O sistema deve listar todas as reservas ativas do usuário e permitir edição ou cancelamento dentro de um prazo estipulado. | Marcos |
| RF004 | **Reportar problemas estruturais:** O sistema deve oferecer um formulário com campos para local (sala/laboratório), categoria do problema, descrição detalhada e opção de anexar foto. O reporte de visualização de salas na portaria deve ser possível sem login; o envio de chamados deve exigir matrícula, sem necessidade de senha complexa. | Camila / Marcos |
| RF005 | **Acompanhar status dos relatos:** O sistema deve exibir ao solicitante uma lista com todos os seus relatos e seus respectivos status (pendente, em análise, resolvido). | Camila |
| RF006 | **Gerenciar salas (administrador):** O sistema deve permitir o cadastro, edição e remoção de salas, com informações como nome, capacidade, localização e recursos disponíveis. *Pré-requisito para o funcionamento do calendário e das reservas.* | Roberto |
| RF007 | **Gerenciar usuários (administrador):** O sistema deve permitir o cadastro, edição de permissões e remoção de usuários. | Roberto |
| RF008 | **Visualizar e gerenciar todos os problemas (administrador/manutenção):** O sistema deve exibir uma lista consolidada de todos os problemas reportados, com filtros por local, categoria e status, e permitir a atualização do status de cada solicitação. O histórico por sala deve ser acessível para consulta. | Carlos / Roberto |
| RF009 | **Autenticação e controle de perfis:** O sistema deve permitir login com credenciais institucionais (matrícula/e-mail e senha) e controlar o acesso às funcionalidades conforme o perfil do usuário (aluno, professor, coordenador, manutenção, administrador). | Todos |

**Requisitos Não Funcionais:**

- **RNF001 – Interface responsiva:** O sistema deve ser acessível e navegável em dispositivos móveis (smartphones e tablets), adaptando-se a diferentes tamanhos de tela.
- **RNF002 – Tempo de resposta:** As operações de consulta e reserva devem ser concluídas em até 5 segundos, em condições normais de uso.
- **RNF003 – Notificações automáticas:** O sistema deve enviar notificações por e-mail para confirmação de reservas, alterações, cancelamentos e atualizações de status de problemas.
- **RNF004 – Segurança e autenticação:** O acesso às funcionalidades deve ser controlado por login, com diferentes níveis de permissão conforme o perfil do usuário.

---

### 2.3 Ideação

A etapa de Ideação foi conduzida por meio de uma sessão de brainstorming com os quatro membros da equipe (Roque, Eduardo, Thomas e Maryane), estimulando o pensamento divergente para gerar o maior número possível de soluções criativas para os problemas identificados. As principais contribuições individuais foram:

**Roque** sugeriu a implementação de um painel visual no estilo Kanban para o módulo de manutenção, onde os problemas reportados pudessem ser organizados por status (Pendente, Em Análise, Resolvido), facilitando a priorização do serviço.

**Eduardo** propôs a integração de um mapa interativo do campus, permitindo que os usuários localizem rapidamente as salas disponíveis e visualizem seu estado (livre, ocupada ou com problema) de forma geoespacial.

**Thomas** enfatizou a necessidade de um sistema automatizado de notificações, garantindo que os usuários recebam e-mails ou alertas sobre a confirmação, alteração ou cancelamento de reservas, bem como sobre atualizações no status de seus relatos de problema.

**Maryane** direcionou o foco para a acessibilidade e usabilidade, sugerindo uma interface com botões grandes, cores contrastantes, formulários enxutos e navegação intuitiva, atendendo aos princípios de Interação Humano-Computador para públicos diversos.

---

### 2.3.1 Avaliação da Solução pelo Triângulo de Ouro

Para avaliar a viabilidade da solução proposta antes de definir o escopo do MVP, a equipe aplicou o framework Triângulo de Ouro, que analisa a solução sob três perspectivas complementares: **Desejabilidade (UX)**, **Capacidade Técnica (DEV)** e **Viabilidade (PM)**. O objetivo é identificar pontos de tensão entre o que os usuários querem, o que a equipe consegue construir e o que a organização consegue sustentar.

**Desejabilidade (UX)**

| Positivos | Negativos | Solução Proposta |
| --- | --- | --- |
| Professores e alunos sofrem com salas ocupadas sem aviso e desejam uma solução. | Professores e alunos podem ter resistência a criar cadastro. | Visualização de salas disponível sem login; reporte de problemas exige apenas matrícula, sem senha. |
| Problemas de infraestrutura sem registro pioram com o tempo, gerando custo e insatisfação. | Alunos podem não confiar que o problema será resolvido, e podem abandonar o sistema. | Exibir o status do chamado (pendente / em análise / resolvido) de forma visível para o solicitante. |
| Há demanda real por um canal que feche o ciclo: reporte → análise → resolução → confirmação. | Pode cair em desuso se a equipe de manutenção não responder com agilidade. | Mostrar histórico de chamados resolvidos para demonstrar que o sistema funciona e gera resultados. |

**Capacidade Técnica (DEV)**

| Positivos | Negativos | Solução Proposta |
| --- | --- | --- |
| Formulário de chamado é tecnicamente simples e pode ser implementado com as tecnologias que o time já conhece. | Integração com a grade horária real do campus é complexa e depende de dados externos. | V1 com inserção manual das salas e horários pela coordenação; integração com grade horária fica para versões futuras. |
| Calendário de disponibilidade é essencialmente um CRUD básico com visualização. | Atualização em tempo real da disponibilidade das salas exige mais infraestrutura (ex: WebSockets). | Implementar atualização em tempo real em versões futuras; na V1, adotar atualização por polling simples. |
| A equipe pode convidar colaboradores externos (colegas, professores) para apoiar no desenvolvimento. | A equipe tem pouca experiência com deploy e infraestrutura de aplicações web. | Buscar apoio de professores ou monitores para viabilizar o deploy institucional. |

**Viabilidade (PM)**

| Positivos | Negativos | Solução Proposta |
| --- | --- | --- |
| A solução beneficia diretamente a gestão do campus, com potencial de apoio institucional. | Quem será responsável por manter as informações de salas e horários atualizadas no sistema? | A coordenação, em parceria com a portaria, assume a responsabilidade de atualização. |
| Reduz conflitos de agenda e centraliza informações hoje fragmentadas em e-mails, WhatsApp e papéis. | O setor de manutenção precisa estar comprometido para responder aos chamados; sem isso, o módulo perde sentido. | **Sem solução técnica:** este é um risco organizacional. O sucesso do módulo de problemas depende de gestão e engajamento institucional, não de tecnologia. |
| O uso de salas vagas pode ser potencializado com um sistema que mostre disponibilidade em tempo real. | O sistema pode cair em desuso se não houver atualização constante e resposta ágil da manutenção. | Definir responsáveis claros (coordenação, portaria, manutenção) antes do lançamento do sistema. |

> **Nota:** A principal ameaça à viabilidade do projeto não é técnica, mas organizacional. O módulo de reporte de problemas só entregará valor se o setor de manutenção estiver comprometido com o uso do sistema e com a atualização dos status dos chamados. Este risco deve ser gerenciado pela coordenação como condição prévia ao lançamento.
> 

---

### 2.3.2 Definição do MVP

A partir das ideias geradas na sessão de brainstorming e da análise pelo Triângulo de Ouro, a equipe priorizou as seguintes funcionalidades para compor o Produto Mínimo Viável (MVP), considerando o equilíbrio entre valor entregue ao usuário e esforço de desenvolvimento e desenvolveu um site map:

- **Dashboard inicial:** com atalhos para “Ver salas”, “Minhas reservas”, “Reportar problema” e “Status dos meus relatos”.
- **Calendário de disponibilidade:** visualização semanal das reservas com cores indicativas (verde = livre, vermelho = ocupado, amarelo = com problema).
- **Reserva de sala:** seleção de sala, data, horário de início e fim, com validação automática de conflitos.
- **Gerenciamento de reservas próprias:** listagem com opções de editar e cancelar reservas (dentro do prazo permitido).
- **Reporte de problemas:** formulário com local, categoria, descrição e anexo de foto (opcional), acessível com matrícula (sem senha).
- **Acompanhamento de relatos:** lista dos problemas reportados pelo usuário com status atualizado.
- **Painel de manutenção:** visão consolidada de todos os chamados abertos, com filtros por local, categoria e urgência, e permissão para atualizar status de cada chamado.
- **Painel administrativo:** para coordenadores, com visão de todas as reservas e problemas, permissão para gerenciar salas e usuários.
- **Sistema de autenticação:** login com diferentes níveis de permissão (aluno, professor, coordenador, administrador, manutenção).

https://www.figma.com/board/aX1G4a29VE78MP0ET6kUCT/SiteMap---Reserva-de-Salas---INHC---SI?node-id=0-1&t=60AGUDby7moEQDkb-1

Funcionalidades como mapa interativo do campus, integração com QR Code, atualização em tempo real e relatórios gerenciais foram mantidas como “desejáveis” para versões futuras, por demandarem maior complexidade técnica e não serem essenciais para a validação inicial do conceito.

---

### 2.4 Prototipação

Com base nas funcionalidades definidas, procedeu-se à criação de um protótipo de alta fidelidade, utilizando ferramentas de wireframing digital. O objetivo foi materializar as ideias de forma tangível, permitindo uma visualização inicial da arquitetura da informação e dos fluxos de navegação.

Foram desenhadas as principais telas do sistema:

- **Tela de Login e Dashboard:** com atalhos para as ações principais (Ver Salas, Minhas Reservas, Relatar Problema).
- **Tela de Calendário de Salas:** exibindo a ocupação semanal com indicação por cores (verde para livre, vermelho para ocupado, amarelo para com problema).
- **Tela de Nova Reserva e Gerenciamento:** contendo formulários simplificados e listagem das reservas ativas com opções de edição/cancelamento.
- **Tela de Relato de Problemas:** com campos para local, categoria, descrição e anexo de imagem, além da consulta ao status dos relatos realizados.
- **Painel Administrativo/Coordenação:** com visões consolidadas para gerenciamento de salas, usuários e visualização de todos os problemas e reservas.
- **Painel de Manutenção:** com listagem de todos os chamados abertos, filtros por local e urgência, e opção de atualização de status.

---

O fluxo de navegação principal do sistema foi definido da seguinte forma:

**Fluxo do usuário comum (aluno/professor):**

1. O usuário acessa a página inicial e realiza o login com suas credenciais (matrícula/e-mail e senha).
2. Após autenticado, é direcionado ao Dashboard, onde visualiza um resumo das próximas reservas e atalhos para as principais ações.
3. Ao clicar em “Ver salas”, o usuário tem acesso a uma lista de todos os espaços disponíveis. Selecionando uma sala, é exibido um calendário semanal com os horários ocupados (em vermelho) e livres (em verde).
4. Para reservar, o usuário clica em um horário livre e é direcionado ao formulário de reserva, onde preenche a data, horário de início e fim, e a finalidade. Ao confirmar, o sistema valida se não há conflitos e registra a reserva.
5. O usuário pode acessar “Minhas reservas” para visualizar todas as suas reservas ativas e, se desejar, editar ou cancelar cada uma delas (desde que respeitado o prazo mínimo de antecedência).
6. Para reportar um problema, o usuário acessa “Reportar problema”, preenche o local, a categoria, descreve o defeito e pode anexar uma foto. Ao enviar, o sistema registra o chamado com status “pendente” e exibe uma confirmação de que o chamado foi recebido.
7. Em “Meus relatos”, o usuário acompanha a evolução de cada solicitação, visualizando quando o status muda para “em análise” ou “resolvido”.

**Fluxo do técnico de manutenção:**

1. O técnico realiza login com perfil de manutenção e acessa diretamente o Painel de Manutenção.
2. O painel exibe a lista de todos os chamados abertos, com informações de local, categoria, descrição, data de abertura e prioridade. O técnico pode ordenar e filtrar por qualquer um desses critérios.
3. Ao selecionar um chamado, o técnico visualiza os detalhes completos (incluindo foto, se houver) e pode alterar o status para “em análise” ao iniciar o atendimento.
4. Após concluir o reparo, o técnico atualiza o status para “resolvido” e pode adicionar um comentário descrevendo o que foi feito. O solicitante é notificado automaticamente por e-mail.
5. O técnico pode consultar o histórico de chamados resolvidos por sala para identificar problemas recorrentes.

**Fluxo do administrador/coordenador:**

1. Após login com perfil administrativo, o usuário tem acesso a um menu adicional com opções como “Gerenciar salas”, “Gerenciar usuários”, “Todos os problemas” e “Todas as reservas”.
2. Em “Todos os problemas”, o administrador visualiza uma tabela com todos os chamados abertos, podendo aplicar filtros por local, categoria ou status.
3. Em “Todas as reservas”, é possível visualizar a ocupação consolidada de todas as salas e, se necessário, excluir reservas conflitantes ou não autorizadas.
4. Em “Gerenciar salas”, o administrador pode cadastrar novas salas, editar informações existentes (nome, capacidade, localização) ou remover salas que não estejam mais em uso.
5. Em “Gerenciar usuários”, o administrador pode cadastrar novos usuários, definir ou alterar seus perfis (aluno, professor, coordenador, manutenção) e remover usuários inativos.

---

## 3 CONSIDERAÇÕES FINAIS

### Limitações do trabalho

Embora o estudo de caso tenha proporcionado uma base sólida para o desenvolvimento do sistema, algumas limitações devem ser reconhecidas. A principal delas é a ausência de validação empírica com usuários reais, uma vez que não foram realizadas entrevistas ou observações sistemáticas, devido ao cronograma reduzido do projeto. As proto-personas, embora baseadas em literatura e conhecimento contextual, são constructos hipotéticos que não substituem a compreensão aprofundada das necessidades específicas da comunidade do IFAL – Campus Maceió. Além disso, o protótipo desenvolvido é de baixa fidelidade, o que limita a avaliação de aspectos como usabilidade, experiência do usuário e adequação às tarefas cotidianas.

Uma limitação adicional, identificada durante a análise pelo Triângulo de Ouro, é de natureza **organizacional**: o módulo de reporte de problemas estruturais só cumprirá sua função se o setor de manutenção estiver comprometido com o uso do sistema e com a atualização ágil dos chamados. Trata-se de uma dependência que nenhuma solução técnica resolve por si só — sem o engajamento institucional da equipe responsável, o módulo tende ao desuso, minando a confiança dos demais usuários no sistema como um todo. Recomenda-se que, antes do lançamento, a coordenação defina formalmente os responsáveis pelo atendimento dos chamados e estabeleça indicadores mínimos de tempo de resposta.

### Trabalhos futuros

Como desdobramento natural deste estudo, sugerem-se as seguintes atividades:

- **Testes de usabilidade com usuários reais:** Realizar sessões de teste com alunos, professores, coordenadores e equipe de manutenção, utilizando o protótipo de baixa fidelidade para coletar feedback sobre a navegação, clareza das telas e utilidade das funcionalidades.
- **Desenvolvimento de protótipo de alta fidelidade:** Com base nos ajustes realizados na etapa de testes, evoluir o protótipo para uma versão interativa e visualmente mais próxima do produto final, utilizando ferramentas como Figma ou Adobe XD.
- **Implementação do sistema completo:** Desenvolver o sistema em produção, com as tecnologias adequadas (ex.: React ou Angular para front-end, Node.js ou Django para back-end, banco de dados relacional), garantindo escalabilidade e segurança.
- **Integração com sistemas institucionais:** Conectar o sistema ao portal acadêmico do IFAL, permitindo login único (SSO) e, futuramente, integração com a grade de horários fixos dos cursos.
- **Expansão para outros campi:** Avaliar a viabilidade de replicar a solução para os demais campi do IFAL, padronizando a gestão de espaços em toda a instituição.
- **Validação do compromisso organizacional:** Antes de qualquer implementação em produção, realizar reuniões com a gestão do campus para formalizar o comprometimento da equipe de manutenção com o uso do sistema.

---

## REFERÊNCIAS

COSTA, Francisco Renan Leite da; MAIA, David Candeia Medeiros; MILANEZ, Alysson Filgueira. Transformando a Gestão de Espaços: Integração de Sistemas para Reservas de Salas na UFERSA. *Revista de Sistemas e Computação*, Salvador, v. 15, n. 3, p. 34-46, set./dez. 2025.

FREIRE, André Pimenta; FORTES, Renata Pontin de M. Manual de Uso: Sistema de Reserva de Salas da Intranet do ICMC-USP. São Carlos: ICMC-USP, 2003. (Relatórios Técnicos do ICMC, n. 213).

SILVA, Giovana da; FIGUEIREDO, Italo Bruno Oliveira; SILVA, João Victor Rodrigues Ferreira da; GABINE, Jordana Santos. Sistema Online para Reservas de Salas e Laboratórios. Tupã: ETEC Prof. Massuyuki Kawano, 2017. Trabalho de Conclusão de Curso.

BROWN, Tim. Design Thinking. *Harvard Business Review*, v. 86, n. 6, p. 84-92, 2008.

VIANNA, Maurício et al. *Design Thinking: Inovação em Negócios*. Rio de Janeiro: MJV Press, 2012.