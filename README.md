#  Oficina - Banco de Dados Relacional

Descrição
Este projeto implementa o modelo lógico de um sistema de oficina mecânica, baseado em um modelo ER/EER.  
A oficina registra clientes, veículos, equipes, mecânicos, ordens de serviço, serviços prestados e peças utilizadas.  

O objetivo é praticar o mapeamento do modelo conceitual para o relacional, implementar o schema em SQL e criar consultas SQL complexas.

---

Estrutura do Projeto
- `schema.sql` → Script de criação do banco de dados oficina, com tabelas, chaves primárias, estrangeiras e constraints.
- `queries.sql` → Conjunto de consultas SQL cobrindo:
  - `SELECT`  
  - `WHERE`  
  - Atributos derivados  
  - `ORDER BY`  
  - `HAVING`  
  - `JOIN`  

---

Modelo Lógico (resumido)

- Cliente (idCliente, nome, endereço, telefone)  
- Veículo (idVeiculo, placa, marca, modelo, ano, Cliente_idCliente)  
- Equipe (idEquipe, nome)  
- Mecânico (idMecanico, nome, endereço, especialidade)  
- Mecânico_Equipe (N:N entre mecânicos e equipes)  
- OrdemServico (idOrdemServico, status, valor_total, observações, Cliente, Veículo, Equipe)  
- Serviço (idServico, descrição, valor_mao_de_obra)  
- Servico_Escolhido (N:N entre ordem e serviços)  
- Peça (idPeca, descrição, valor_unitario)  
- Peca_Especifica (N:N entre ordem e peças, com quantidade)  

---

Como executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/oficina-database.git
   cd oficina-database
