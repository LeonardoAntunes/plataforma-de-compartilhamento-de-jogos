# 🛠️ Especificação Técnica (Tech Spec) - Roubank

Este documento detalha a arquitetura técnica, o modelo de dados e os contratos de API (via JSON Server) necessários para o funcionamento do sistema bancário Roubank.

## 1. Modelo de Dados (Diagrama ER)

Abaixo está o Diagrama Entidade-Relacionamento (DER) que representa a estrutura do nosso "banco de dados" (`db.json`) e como as informações se conectam.

```mermaid
erDiagram
    USER ||--o{ GAME : registers
    USER ||--o{ REVIEW : writes
    USER ||--o{ PROFILE : has
    GAME ||--o{ REVIEW : "receives"
    ADMIN ||--o{ REVIEW : moderates
    ADMIN ||--o{ USER : manages

    USER {
        int userId PK
        string username UK "unique"
        string email UK "unique, valid"
        string passwordHash
        datetime createdAt
        string role "player, admin"
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
        decimal rating "1-10"
        string status "published, flagged, removed"
        datetime createdAt
        datetime updatedAt
    }

    USER_GAME_STATUS {
        int statusId PK
        int userId FK
        int gameId FK
        string status "playing completed abandoned"
        datetime startDate
        datetime completionDate
    }

    ADMIN {
        int adminId PK
        int userId FK
        string permissions
        datetime assignedAt
