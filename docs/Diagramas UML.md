## 📐 Diagramas UML

O projeto conta com diferentes diagramas UML que representam os principais aspectos da modelagem:

- **Diagrama de Casos de Uso**  
  - **Atores:** Morador, Síndico, Administrador  
  - **Ações:**  
    - Morador → [Reservar Área Comum], [Abrir Ocorrência]  
    - Síndico → [Enviar Comunicado], [Atualizar Ocorrência]  
    - Administrador → [Gerar Relatório Financeiro]  

- **Diagrama de Classe (Entidades principais)**  
  - **Morador:**  
    - Atributos: id, nome, cpf, apartamento, inadimplente (boolean)  
    - Métodos: `solicitarReserva()`, `abrirOcorrencia()`  
  - **Reserva:**  
    - Atributos: id, idMorador, idArea, data, status  
    - Métodos: `verificarDisponibilidade()`, `confirmar()`  
  - **Ocorrência:**  
    - Atributos: id, idMorador, descricao, status, dataAbertura  

- **Diagrama de Atividade (Fluxo de Reserva)**  
  - [Início] → Selecionar "Reservas" → Escolher Ambiente → Escolher Data  
  - [Decisão: Disponível?] → (Não) Mostrar Erro → Fim  
  - (Sim) [Decisão: Inadimplente?] → (Sim) Bloquear → Fim  
  - (Não) Efetivar Reserva → Fim  

- **Diagrama de Máquina de Estado (Status da Ocorrência)**  
  - [Aberta] → (Síndico visualiza e atua) → [Em Andamento] → (Problema solucionado) → [Resolvida]  

- **Diagrama de Sequência (Reserva)**  
  - Morador → Interface: `solicitarReserva()`  
  - Interface → Backend: `verificarDisponibilidade()`  
  - Backend → Banco de Dados: Retorna livre  
  - Backend → Banco de Dados: `inserirReserva()`  
  - Banco de Dados → Backend: sucesso  
  - Backend → Interface: Mostrar confirmação  

---
