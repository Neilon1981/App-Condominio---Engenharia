## 🔄 BPMN (Modelagem de Processos)

O projeto conta com modelagens de processos em BPMN que representam os principais fluxos do sistema:

- **Processo de Reserva**  
  - **Raia Morador:** Acessa o app → Escolhe a área e data → Solicita reserva  
  - **Raia Sistema:** Verifica disponibilidade na data → Valida inadimplência → Aprova e bloqueia a data  
  - **Raia Síndico:** Recebe notificação da reserva aprovada  

- **Processo de Ocorrências**  
  - **Raia Morador:** Preenche formulário de reclamação/manutenção → Envia  
  - **Raia Sistema:** Registra status como "Aberta" → Notifica síndico  
  - **Raia Síndico:** Analisa o chamado → Inicia providências → Altera status para "Resolvida"  
  - **Raia Sistema:** Notifica morador da resolução  

---
