# Estrutura das telas — Wireframes do Evolut

## Padrão visual e navegação
As telas internas seguem uma estrutura padrão:
- Cabeçalho com nome do sistema e identificação do usuário.
- Menu lateral para acessar os módulos.
- Área central com título, informações e ações da tela.
- Botões e formulários organizados para facilitar o uso.

Os wireframes abaixo representam a organização planejada dos elementos. Eles não substituem os prints das telas implementadas.

## 1. Login

```text
+------------------------------------------------------+
|                       EVOLUT                         |
|              Gestão de Pessoas                       |
|                                                      |
|                 Acesse sua conta                     |
|                                                      |
|  E-mail / usuário: [________________________]        |
|  Senha:           [________________________]        |
|                                                      |
|                  [ ENTRAR ]                          |
|                                                      |
+------------------------------------------------------+
```

## 2. Menu / Dashboard

```text
+--------------------------------------------------------------+
| EVOLUT                                  Usuário | Sair        |
+----------------------+---------------------------------------+
| MENU                 | Dashboard                             |
|                      |                                       |
| > Início             | [Colaboradores] [Metas] [Treinamentos]|
|   Colaboradores      |                                       |
|   Metas              | Resumo de atividades                  |
|   Avaliações         | +----------------+ +----------------+  |
|   Feedbacks          | | Metas pendentes| | Próximas férias|  |
|   Treinamentos       | +----------------+ +----------------+  |
|   Plano de carreira  |                                       |
|   Estrutura          | Atividades recentes                   |
|   Férias             | [Lista de atualizações................]|
|   Registro de ponto  |                                       |
|   Meu perfil         |                                       |
+----------------------+---------------------------------------+
```

## 3. Cadastro de usuários e colaboradores

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Cadastro de colaborador               |
|                      |                                       |
|                      | Nome:       [____________________]    |
|                      | CPF:        [____________________]    |
|                      | E-mail:     [____________________]    |
|                      | Cargo:      [ Selecionar       v ]    |
|                      | Setor:      [ Selecionar       v ]    |
|                      | Data adm.:  [____/____/______]        |
|                      | Tipo acesso:[ Selecionar       v ]    |
|                      |                                       |
|                      | [CANCELAR]          [SALVAR]          |
+----------------------+---------------------------------------+
```

## 4. Metas

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Metas dos colaboradores               |
|                      |                                       |
|                      | [ + Nova meta ]                       |
|                      |                                       |
|                      | Colaborador | Meta | Prazo | Status   |
|                      | ------------|------|-------|--------- |
|                      | Nome        | ...  | ...   | Pendente |
|                      | Nome        | ...  | ...   | Em andamento
|                      |                                       |
|                      | [Visualizar] [Editar]                 |
+----------------------+---------------------------------------+
```

## 5. Avaliação de desempenho

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Avaliação de desempenho                |
|                      |                                       |
|                      | Colaborador: [Selecionar          v]  |
|                      | Data:        [____/____/______]        |
|                      | Nota:        [________]                |
|                      | Observações:                          |
|                      | [__________________________________]  |
|                      | [__________________________________]  |
|                      |                                       |
|                      | [CANCELAR]       [SALVAR AVALIAÇÃO]   |
+----------------------+---------------------------------------+
```

## 6. Feedback

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Feedback                              |
|                      |                                       |
|                      | [ + Registrar feedback ]              |
|                      | Colaborador: [Selecionar          v]  |
|                      | Tipo:        [Selecionar          v]  |
|                      | Descrição:                            |
|                      | [__________________________________]  |
|                      | [__________________________________]  |
|                      |                                       |
|                      | Histórico de feedbacks                |
|                      | [Data] [Colaborador] [Descrição]      |
|                      |                                       |
|                      | [SALVAR]                              |
+----------------------+---------------------------------------+
```

## 7. Treinamentos

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Treinamentos                          |
|                      |                                       |
|                      | [ + Novo treinamento ]               |
|                      | Nome:       [____________________]    |
|                      | Descrição:  [____________________]    |
|                      | Início:     [____/____/______]        |
|                      | Término:    [____/____/______]        |
|                      |                                       |
|                      | Treinamentos disponíveis              |
|                      | [Nome] [Período] [Participantes]       |
|                      |                                       |
|                      | [SALVAR]                              |
+----------------------+---------------------------------------+
```

## 8. Plano de carreira

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Plano de carreira                     |
|                      |                                       |
|                      | Colaborador: [Selecionar          v]  |
|                      | Cargo atual: [____________________]   |
|                      | Cargo desejado: [_________________]   |
|                      | Competências a desenvolver:           |
|                      | [__________________________________]  |
|                      | Etapas do desenvolvimento:            |
|                      | [__________________________________]  |
|                      | Status: [Selecionar              v]  |
|                      | [SALVAR PLANO]                        |
+----------------------+---------------------------------------+
```

## 9. Estrutura organizacional

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Estrutura organizacional              |
|                      |                                       |
|                      | Empresa                               |
|                      |          |                            |
|                      |     Diretoria                         |
|                      |          |                            |
|                      |    +-----+-----+                      |
|                      |    |           |                      |
|                      |  Financeiro   RH                      |
|                      |                |                      |
|                      |           Colaboradores                |
|                      |                                       |
|                      | [ + Adicionar setor ]                 |
+----------------------+---------------------------------------+
```

## 10. Férias

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Gestão de férias                      |
|                      |                                       |
|                      | [ + Solicitar férias ]                |
|                      | Colaborador: [Selecionar          v]  |
|                      | Início:      [____/____/______]        |
|                      | Término:     [____/____/______]        |
|                      |                                       |
|                      | Solicitações                          |
|                      | [Colaborador] [Período] [Status]      |
|                      | [Aprovar] [Rejeitar]                  |
+----------------------+---------------------------------------+
```

## 11. Registro de ponto

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Registro de ponto                     |
|                      |                                       |
|                      | Colaborador: Nome                     |
|                      | Data: __/__/____                      |
|                      |                                       |
|                      |       [ REGISTRAR ENTRADA ]            |
|                      |       [ REGISTRAR SAÍDA ]              |
|                      |                                       |
|                      | Histórico de registros                |
|                      | [Data] [Entrada] [Saída] [Observação] |
+----------------------+---------------------------------------+
```

## 12. Perfil

```text
+--------------------------------------------------------------+
| EVOLUT | MENU                                      Usuário   |
+----------------------+---------------------------------------+
| Menu lateral         | Meu perfil                            |
|                      |                                       |
|                      | Nome:       [____________________]    |
|                      | E-mail:     [____________________]    |
|                      | Cargo:      [____________________]    |
|                      | Setor:      [____________________]    |
|                      |                                       |
|                      | [ALTERAR DADOS] [SALVAR ALTERAÇÕES]   |
+----------------------+---------------------------------------+
```

## Observação
Os wireframes são propostas de organização. Antes da entrega, confiram se cada campo e botão corresponde às funcionalidades que realmente existem no sistema.
