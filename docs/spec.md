# 🛠️ Especificação Técnica (Tech Spec) - Roubank

Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do sistema bancário Roubank.

## 1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do nosso "banco de dados" (`db.json`) e como as informações se conectam.

```mermaid
erDiagram
    USER ||--|| PROFILE : has
    USER ||--o{ REVIEW : writes
    USER ||--o{ USER_GAME_STATUS : tracks
    GAME ||--o{ REVIEW : receives
    GAME ||--o{ USER_GAME_STATUS : has
    ADMIN ||--o{ REVIEW : moderates
    ADMIN ||--|| USER : is

    USER {
        int userId PK
        string username UK
        string email UK
        string passwordHash
        datetime createdAt
        string role
    }

    PROFILE {
        int profileId PK
        int userId FK
        string profilePhoto
        string bio
        string socialMediaLinks
        datetime updatedAt
    }

    GAME {
        int gameId PK
        string title
        string description
        string genre
        datetime releaseDate
    }

    REVIEW {
        int reviewId PK
        int userId FK
        int gameId FK
        string content
        decimal rating
        string status
        datetime createdAt
        datetime updatedAt
    }

    USER_GAME_STATUS {
        int statusId PK
        int userId FK
        int gameId FK
        string status
        datetime startDate
        datetime completionDate
    }

    ADMIN {
        int adminId PK
        int userId FK
        string permissions
        datetime assignedAt
    }
