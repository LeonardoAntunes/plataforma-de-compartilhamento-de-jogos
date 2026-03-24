# 🛠️ Especificação Técnica (Tech Spec) - Roubank

Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do sistema bancário Roubank.

## 1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do nosso "banco de dados" (`db.json`) e como as informações se conectam.

```mermaid
erDiagram
    USUARIO ||--o{ JOGO : registra
    USUARIO ||--o{ REVIEW : escreve
    USUARIO ||--o{ COMENTARIO : faz
    USUARIO ||--o{ AMIZADE : cria
    REVIEW ||--o{ COMENTARIO : contem
    JOGO ||--o{ REVIEW : recebe
    USUARIO ||--o{ PERFIL : possui
    USUARIO ||--o{ FOTO_PERFIL : tem
    USUARIO ||--o{ REDE_SOCIAL : conecta
    JOGO ||--o{ GENERO : pertence
    REVIEW ||--o{ NOTA : tem
    COMENTARIO ||--o{ RESPOSTA : gera

    USUARIO {
        int usuarioId PK
        string nomeUsuario UK
        string email UK
        string senha
        datetime dataCriacao
        datetime dataUltimaAtualizacao
        boolean ativo
        string tipoUsuario "admin ou jogador"
    }

    PERFIL {
        int perfilId PK
        int usuarioId FK
        string biografia
        string localizacao
        datetime dataAtualizacao
    }

    FOTO_PERFIL {
        int fotoId PK
        int usuarioId FK
        string caminhoFoto
        datetime dataUpload
    }

    REDE_SOCIAL {
        int redeSocialId PK
        int usuarioId FK
        string plataforma
        string url
        datetime dataConexao
    }

    JOGO {
        int jogoId PK
        string titulo UK
        string descricao
        string desenvolvedora
        datetime dataLancamento
        string plataforma
    }

    GENERO {
        int generoId PK
        string nomeGenero UK
    }

    USUARIO_JOGO {
        int usuarioJogoId PK
        int usuarioId FK
        int jogoId FK
        string status "em progresso, finalizado, parado"
        float progressoPercentual
        datetime dataInicio
        datetime dataFinalizacao
    }

    REVIEW {
        int reviewId PK
        int usuarioId FK
        int jogoId FK
        string titulo
        string conteudo
        float nota "1 a 5"
        int pontosPozitivos
        int pontosNegativos
        datetime dataCriacao
        datetime dataUltimaEdicao
        boolean deletada
    }

    NOTA {
        int notaId PK
        int reviewId FK
        float valor
    }

    COMENTARIO {
        int comentarioId PK
        int usuarioId FK
        int reviewId FK
        string conteudo
        datetime dataCriacao
        datetime dataUltimaEdicao
        boolean deletado
    }

    RESPOSTA {
        int respostaId PK
        int comentarioId FK
        int usuarioId FK
        string conteudo
        datetime dataCriacao
        datetime dataUltimaEdicao
        boolean deletada
    }

    AMIZADE {
        int amizadeId PK
        int usuarioId1 FK
        int usuarioId2 FK
        string status "pendente, aceita, recusada"
        datetime dataSolicitacao
        datetime dataAceitacao
    }
