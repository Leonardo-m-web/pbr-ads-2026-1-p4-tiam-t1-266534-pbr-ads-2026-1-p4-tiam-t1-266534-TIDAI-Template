
# 3. Especificações do Projeto

📌 **Pré-requisito:** Planejamento do Projeto (Cronograma e Sprints definidos).

Nesta seção serão detalhados:

- ✅ Requisitos Funcionais  
- ✅ Histórias de Usuário  
- ✅ Requisitos Não Funcionais  
- ✅ Restrições do Projeto  

O objetivo é organizar claramente as funcionalidades, qualidades e limites da solução.

---

# 3.1 Requisitos Funcionais

Os **Requisitos Funcionais (RF)** descrevem o que o sistema deve fazer.

📌 Cada requisito deve:
- Representar uma funcionalidade única
- Ser claro e objetivo
- Orientar diretamente o desenvolvimento

---

## Tabela de Requisitos Funcionais

| ID | Descrição Resumida | Dificuldade (B/M/A)* | Prioridade (B/M/A)* |
| -- | ------------------ | -------------------- | ------------------- |
| RF01 | Autenticação: o sistema deve permitir cadastro e login exclusivo do funcionário da farmácia. | B | A |
| RF02 | Busca Rápida: o sistema deve permitir pesquisar clientes por nome, CPF ou telefone. | M | A |
| RF03 | Cadastro Direto: o sistema deve permitir a inclusão simples de novos clientes no balcão. | B | A |
| RF04 | Registro de Pressão: o sistema deve permitir a entrada dos valores de pressão sistólica, diastólica e pulso. | B | A |
| RF05 | Histórico Cronológico: o sistema deve exibir as medições anteriores com data e hora. | M | M |
| RF06 | Exportação: o sistema deve permitir a expostação dos registros através de wpp. | B | A |


---

# 3.2 Histórias de Usuário

Cada história deve seguir o padrão ensinado na disciplina:

> **Como** [persona],  
> **eu quero** [funcionalidade],  
> **para que** [benefício].

⚠️ **ATENÇÃO:**  
Cada História de Usuário deve estar associada a um Requisito Funcional específico (RF-XX).

---

## Histórias do Projeto

---

### História 1 (relacionada ao RF-01)

Como funcionário da farmácia,  
Eu quero realizar meu cadastro e acessar o sistema com credenciais próprias,  
Para que somente pessoas autorizadas possam consultar e registrar dados dos clientes.

---

### História 2 (relacionada ao RF-02)

Como atendente de balcão,  
Eu quero pesquisar um cliente por nome, CPF ou telefone,  
Para que eu localize sua ficha rapidamente durante o atendimento.

---

### História 3 (relacionada ao RF-03)

Como atendente de balcão,  
Eu quero cadastrar um novo cliente diretamente no sistema,  
Para que a medição possa ser registrada mesmo quando ele ainda não possuir ficha.

---

### História 4 (relacionada ao RF-04)

Como farmacêutico ou atendente autorizado,  
Eu quero informar os valores de pressão sistólica, diastólica e pulso obtidos na medição,  
Para que o resultado do atendimento fique registrado de forma organizada.

---

### História 5 (relacionada ao RF-05)

Como farmacêutico ou atendente autorizado,  
Eu quero visualizar as medições anteriores do cliente em ordem cronológica,  
Para que eu possa acompanhar a variação dos registros ao longo do tempo.

---

### História 6 (relacionada ao RF-06)

Como funcionário da farmácia,  
Eu quero exportar os registros de pressão pelo WhatsApp,  
Para que o cliente possa receber e guardar seu histórico de medições.

---

> 💡 Dica: Agrupe as histórias por módulo (Cadastro, Relatórios, Pagamentos, etc.) para melhor organização.

---

# 3.3 Requisitos Não Funcionais

Os **Requisitos Não Funcionais (RNF)** definem características de qualidade do sistema, como:

- ⚡ Desempenho  
- 🔒 Segurança  
- 🎨 Usabilidade  
- 📈 Escalabilidade  
- 🌐 Compatibilidade  

Eles garantem a qualidade da solução.

---

## Tabela de Requisitos Não Funcionais

| ID | Descrição Resumida | Prioridade (B/M/A)* |
| -- | ------------------ | ------------------- |
| RNF01 | Agilidade: o fluxo completo de registro deve ser finalizado em até 40 segundos. | A |
| RNF02 | Usabilidade: a interface deve ser clara e adaptada para telas de balcão e tablets. | A |
| RNF03 | Segurança: o sistema deve restringir o acesso e proteger os dados de saúde. | A |

---

# 3.4 Restrições do Projeto

📌 **Restrições** são limitações externas impostas ao projeto.

Elas podem envolver:
- 📅 Prazo
- 🖥️ Tecnologia obrigatória ou proibida
- 🌐 Ambiente de execução
- 📜 Normas legais
- 🏢 Políticas institucionais

⚠️ Diferente dos RNFs, as restrições impõem **limites fixos** ao projeto.

---

## Tabela de Restrições

| ID  | Restrição |
|-----|-----------|
| R-01 | O projeto deverá ser entregue até o final do semestre. |
| R-02 | O sistema será de uso interno da Drogaria Cruz e deverá ser acessado somente por funcionários autorizados. |
| R-03 | A solução deverá ser compatível com os computadores e tablets disponíveis no balcão da farmácia. |
| R-04 | O cliente não deverá criar conta, instalar aplicativo ou efetuar login para ter sua medição registrada. |
| R-05 | Os dados pessoais e de saúde dos clientes deverão ser tratados conforme a Lei Geral de Proteção de Dados Pessoais (LGPD — Lei nº 13.709/2018). |
| R-06 | O sistema deverá registrar medições inseridas manualmente pelos funcionários; não faz parte do escopo a integração direta com aparelhos de pressão. |
| R-07 | O FarmaPress Desk servirá para registro e consulta de medições e não realizará diagnóstico, prescrição ou orientação médica. |
| R-08 | O envio de registros pelo WhatsApp dependerá da disponibilidade do serviço e de um canal de contato informado pelo cliente. |

---

# ✅ Checklist de Validação

Antes de entregar, confirme:

- [x] Todos os RFs estão claros e numerados corretamente  
- [x] Todas as Histórias estão associadas a um RF  
- [x] RNFs estão mensuráveis  
- [x] Restrições são realmente limitações externas  
- [x] O documento está atualizado no GitHub  

---



> **Links Úteis**:
> - [O que são Requisitos Funcionais e Requisitos Não Funcionais?](https://codificar.com.br/requisitos-funcionais-nao-funcionais/)
> - [O que são requisitos funcionais e requisitos não funcionais?](https://analisederequisitos.com.br/requisitos-funcionais-e-requisitos-nao-funcionais-o-que-sao/)
