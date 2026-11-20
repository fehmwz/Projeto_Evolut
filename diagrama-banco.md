# Estrutura do banco de dados — Evolut

## Objetivo
O banco de dados foi planejado para centralizar informações de usuários, colaboradores e processos de Recursos Humanos: metas, avaliações, feedbacks, treinamentos, plano de carreira, férias e registro de ponto.

> **Atenção:** este é o modelo lógico proposto para documentar a Sprint 2. Os nomes e campos devem corresponder ao banco realmente implementado pelo grupo. Se o código de vocês usar nomes diferentes, ajustem o diagrama para manter a documentação fiel ao sistema.

## Diagrama entidade-relacionamento (DER)

```mermaid
erDiagram
    SETOR ||--o{ COLABORADOR : possui
    CARGO ||--o{ COLABORADOR : ocupa
    COLABORADOR ||--o| USUARIO : acessa
    COLABORADOR ||--o{ META : possui
    COLABORADOR ||--o{ FEEDBACK : recebe
    USUARIO ||--o{ FEEDBACK : registra
    COLABORADOR ||--o{ AVALIACAO : recebe
    USUARIO ||--o{ AVALIACAO : realiza
    COLABORADOR ||--o{ FERIAS : solicita
    COLABORADOR ||--o{ REGISTRO_PONTO : registra
    COLABORADOR ||--o{ PLANO_CARREIRA : possui
    COLABORADOR ||--o{ COLABORADOR_TREINAMENTO : participa
    TREINAMENTO ||--o{ COLABORADOR_TREINAMENTO : inclui

    SETOR {
        int id_setor PK
        string nome
        string descricao
    }

    CARGO {
        int id_cargo PK
        string nome
        string descricao
    }

    COLABORADOR {
        int id_colaborador PK
        int id_setor FK
        int id_cargo FK
        string nome
        string cpf
        string email
        date data_admissao
        string status
    }

    USUARIO {
        int id_usuario PK
        int id_colaborador FK
        string login
        string senha_hash
        string tipo_acesso
        boolean ativo
    }

    META {
        int id_meta PK
        int id_colaborador FK
        string titulo
        string descricao
        date prazo
        string status
        decimal progresso
    }

    FEEDBACK {
        int id_feedback PK
        int id_colaborador FK
        int id_usuario FK
        string descricao
        date data_feedback
        string tipo
    }

    AVALIACAO {
        int id_avaliacao PK
        int id_colaborador FK
        int id_usuario FK
        date data_avaliacao
        decimal nota
        string observacoes
    }

    TREINAMENTO {
        int id_treinamento PK
        string titulo
        string descricao
        date data_inicio
        date data_fim
    }

    COLABORADOR_TREINAMENTO {
        int id_colaborador_treinamento PK
        int id_colaborador FK
        int id_treinamento FK
        string status
        date data_conclusao
    }

    FERIAS {
        int id_ferias PK
        int id_colaborador FK
        date data_inicio
        date data_fim
        string status
        date data_solicitacao
    }

    REGISTRO_PONTO {
        int id_registro PK
        int id_colaborador FK
        date data
        time horario_entrada
        time horario_saida
        string observacao
    }

    PLANO_CARREIRA {
        int id_plano PK
        int id_colaborador FK
        string cargo_atual
        string cargo_desejado
        string competencias
        string etapas_desenvolvimento
        string status
    }
```

## Descrição das entidades

| Entidade | Finalidade |
|---|---|
| `USUARIO` | Armazena as credenciais e o tipo de acesso ao sistema. |
| `COLABORADOR` | Guarda os dados cadastrais dos funcionários. |
| `SETOR` | Organiza os colaboradores por departamento. |
| `CARGO` | Registra os cargos existentes na empresa. |
| `META` | Permite cadastrar e acompanhar objetivos dos colaboradores. |
| `FEEDBACK` | Registra comentários e orientações recebidos pelos colaboradores. |
| `AVALIACAO` | Armazena avaliações de desempenho. |
| `TREINAMENTO` | Mantém o catálogo de treinamentos disponíveis. |
| `COLABORADOR_TREINAMENTO` | Relaciona colaboradores aos treinamentos e acompanha sua participação. |
| `FERIAS` | Registra solicitações e períodos de férias. |
| `REGISTRO_PONTO` | Armazena horários de entrada e saída. |
| `PLANO_CARREIRA` | Registra objetivos e etapas de desenvolvimento profissional. |

## Relacionamentos principais
- Um setor pode possuir vários colaboradores; cada colaborador está associado a um setor.
- Um cargo pode ser ocupado por vários colaboradores.
- Um colaborador pode ter uma conta de usuário para acessar o sistema.
- Um colaborador pode possuir várias metas, avaliações, solicitações de férias e registros de ponto.
- Um feedback é associado ao colaborador que o recebe e ao usuário que o registra.
- Um treinamento pode ter vários colaboradores, e um colaborador pode participar de vários treinamentos. A tabela `COLABORADOR_TREINAMENTO` representa essa relação.
- Um colaborador pode possuir um ou mais registros de plano de carreira.

## Regras e cuidados
- As chaves `PK` identificam exclusivamente cada registro.
- As chaves `FK` conectam registros de tabelas diferentes.
- A senha deve ser armazenada como hash, nunca em texto puro.
- O tipo de acesso deve controlar quais funcionalidades cada usuário pode utilizar.
- Campos obrigatórios, validações e regras de exclusão devem ser definidos na implementação do banco.
