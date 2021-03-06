## Documento de Definição de Requisitos
****Projeto****: Quattuor

****Responsáveis****: Adrielly Rodrigues de Jesus Galeno, John Lynn Rodrigues de Jesus, Keven Cavalcante Galeno

------------


## 1. Introdução

  Este documento apresenta os requisitos de usuário do sistema Quattuor e está organizado da seguinte forma: a Seção 2 contém uma descrição do propósito do sistema; a Seção 3 apresenta uma descrição do minimundo apresentando o problema; e a Seção 4 apresenta as listas de requisitos de usuário levantados junto ao cliente.

## 2. Descrição do Propósito do Sistema

  Sistema de gestão on-line para barbearias que permite agendamentos de horários com diversos serviços previamente cadastrados, organizando a agenda e otimizando os processos do estabelecimento.

## 3. Descrição do Minimundo

|  Descrição do Minimundo |
| ------------|
|  Barbearias costumam fazer uso de agendas (físicas) para controlar os cortes realizados pelos seus funcionários, para ter um controle de quantos clientes foram atendidos no final do dia e quem os atendeu. Este software tratará de um sistema simplificado em sua interface, porém robusta por trás dela, trazendo maior controle dos agendamentos e na geração de relatórios específicos para uma barbearia. A barbearia hipotética para a qual o software deve ser construído atende solicitações, tais como, realizar agendamentos, receber notícias e promoções, lembretes automáticos, entre outros, facilitando e aproximando a barbearia do seu cliente, gestão do estabelecimento, com controle de cada profissional, histórico de clientes, estoque e excelentes relatórios financeiros. |

## 4. Requisitos de Usuário

  Tomando por base o contexto do sistema, foram identificados os seguintes requisitos de usuário:

### Requisitos Funcionais

| Identificador  |  Descrição |  Prioridade | Depende  de  |
| ------------ | ------------ | ------------ | ------------ |
|  RF01 | O sistema deve permitir que os clientes façam Login|  Alta |  --- |
|  RF02 | O sistema deve permitir que os Funcionarios façam Login|  Alta |  --- |
|  RF03 | O sistema deve permitir cadastrar os dados pessoais dos clientes.  | Alta  | RF01  |
|  RF04 | O sistema deve permitir cadastrar os dados pessoais dos funcionarios.  | Alta  | RF02  |
|  RF05 | O sistema deve permitir cadastrar horários disponíveis. |  Alta | ---  |
|  RF06 | O sistema deve permitir cadastrar procedimentos.| Alta  |  --- |
|  RF07 | O sistema deve emitir uma listagem  de horários disponíveis.  | Alta  | RF05  |
|  RF08 | O sistema deve permitir que o usuário/cliente faça marcações de procedimentos de acordo com os horários disponíveis. . | Alta  | RF03, RF05, RF06.  |
|  RF09 | O sistema deve emitir uma listagem de horários preenchidos.   |  Alta | RF08  |
|  RF10 | O sistema deve permitir que o administrador tenha controle de toda a agenda de procedimentos.| Alta  |  --- |
|  RF11 | O sistema deve permitir a consulta da agenda pessoal de cada funcionário.  | Alta  | RF02  |
|  RF12 | O sistema deve permitir o agendamento de reserva.   |Alta   |  RF08 |
|  RF13 | O sistema deve permitir que o usuário/cliente faça o pagamento online dos seus procedimentos. |  Alta |  --- |
|  RF14 | O sistema deve permitir visualizar a duração de cada procedimento.  |  Média | RF06  |
|  RF15 | O sistema deve emitir relatórios gerenciais periódicos ao administrador.. | Alta  | ---  |
|  RF16 | O sistema deve permitir que o usuário/cliente possa gerar feedback ao estabelecimento ou funcionário.|  Média |  --- |
|  RF17 | O sistema deve emitir notificações de lembrete ao usuário/cliente.  |  Média |---   |



### Regras de Negócio 


|  Identificador | Descrição  | Prioridade  | Depende De  |
| ------------ | ------------ | ------------ | ------------ |
| RN01  | O Sistema deve fazer a autenticação de CPF  | Alta  |  --  |
| RN02  | A senha de login deve ter, no maximo, 15 caracteres númericos | Média  |  --  |
| RN03  | Um profissional não poderá ser agendado por dois clientes para o mesmo horário  | Alta  |  --  |
| RN04  | O sistema deve permitir um cadastro por CPF ou Email | Alta  |  --  |
| RN05  | A tabela de horários preenchidos deve ser atualizada sempre após o ultimo agendamento |  Alta  |  --  |
| RN06  | O sistema deve emitir um alerta sempre que um profissional não estiver disponivel para agendamento  |  Média |  --  |
| RN07  | O alerta para os agendamentos de reservas deverá ser feita com antecedencia  | Baixa  | --  |
| RN08  | O sistema deve suportar o tráfego de pelo menos 20 usuarios conectadas simultaneamente | Média  | --  |
| RN09  | Os dados de cadastramento armazenados devem ser criptografados | Média  | --  |
| RN10  | O sistema deve permitir que o cliente desmarque o agendamento até 15 min antes | Alta  |  -- |
| RN11  | A senha do usuario deverá ter, no minimo, 6 caracteres númericos | Média  | --  |
| RN12  | O sistema deve aceitar pagamentos via PIX, cartão de Credito ou no Local | Baixa |  -- |
| RN13  | Ao concluir um agendamento o sistema deve solicitar o modo de pagamento  | Médio  |  -- |
| RN14  | Após conclusão do procedimento o sistema deve gerar uma notificação de feedback ao cliente   | Baixa  |  -- |


### Requisitos Não Funcionais

| Identificador  |  Descrição |Categoria   |Escopo   |Prioridade   | Depende  de  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| RNF01  | O Sistema deve estar disponível para Android, iOS e WEB. | Portabilidade  |  Sistem |  Alta | --  |
| RNF02  | Os horários devem ser atualizados em tempo real para não ocorrer problemas com agendamento.  |  Segurança |  Sistema | Alta  | --  |
| RNF03  | Deve oferecer criptografia para a segurança dos dados de acesso. |  Segurança | Sistema  | Alta  | --  |
| RNF04  | Deve oferecer suporte e manutenção ao sistema sempre que houver algum problema.  |  Manutenção | Sistema  |  Alta | --  |
| RNF05  | O sistema deve estar disponível de 08:00 às 20:00 para agendamentos. |  Eficiência |  Sistema | Média | --  |
| RNF06  | Um relatório geral deve ser entregue toda segunda-feira.  |  Entrega |  Sistema | Baixa  | RNF05.  |
| RNF07  | O Sistema deve atender às normas legais tais como padrões, leis e etc. | Legais  |  Sistema | Alta  | RNF01, RNF03.  |
| RNF08  | O sistema não apresentará aos usuários quaisquer dados de cunho privativo (LGPD).  |  Éticos | Sistema  | Média  |  -- |
| RNF09  | Os usuários terão um tutorial de uso do sistema  | Facilidade de Uso  | Funcionalidades  | Baixa  |  RNF01. |
| RNF10  | Para pagamento online com cartão, deverá exigir o codigo de verificação. | Segurança  | Funcionalidades  | Média  |  RNF01,RNF02,RNF05.  |
| RNF11  | O sistema deverá possuir sincronização com o serviço NTP.  | Interoperabilidade  | Sistema  | Alta  | RNF01,RNF02, RNF05.  |
| RNF12  | Deverá possuir espaço em disco de “ “ para armazenamento de dados. | Desempenho  | Sistema  | Alta   | --  |
| RNF13  | É limitado 1 agendamento por cadastro  | Segurança  | Sistema  | Alta  | --  |
| RNF14  | Ao fazer um agendamento deve ocupar o horário selecionado em no máximo 3 segundos.  | Desempenho  | Sistema  | Média  | RNF02, RNF11.  |
| RNF15  | O sistema deverá emitir uma notificação de confirmação ao cliente 10 minutos antes do horário agendado  | Eficiência  | Sistema  | Baixa  | --  |

## Simulação de Telas

### Cadastramento de usuário

|  Campo | Tamanho  | Tipo |
| ------------ | ------------ |------------ |
| Email  | 255 | Texto
|  CPF  |  11  | Texto
| Senha | 08 | Numérico
| Nome  | 255  | Texto
| Telefone  |  09  | Numérico
| Sexo  |  Inteiro | Texto

### Login

|  Campo | Tamanho  | Tipo |
| ------------ | ------------ |------------ |
| Email  / CPF  | Inteiro | Texto
|  Senha  |  08  | Numérico

### Atualização de Cadastro

|  Campo | Tamanho  | Tipo |
| ------------ | ------------ |------------ |
| Email  | 255 | Texto
|  CPF  |  11  | Texto
| Senha | 08 | Numérico
| Nome  | 255  | Texto
| Telefone  |  09  | Numérico
| Sexo  |  Inteiro | Texto

<div align="right">
<img src="https://user-images.githubusercontent.com/94652912/144938411-2d1dbb6f-267b-4527-81e1-e3ecb3a11100.png" width="100px" />
</div>
