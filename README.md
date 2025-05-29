# Task 2 Starter Repo
Contains Everything you need to get started on task 2 of Forage's Wells Fargo software engineering program


New ERD
```
erDiagram
    ADVISOR {
        long advisorId PK
        string firstName
        string lastName
        string address
        string phone
        string email
    }

    CLIENT {
        long clientId PK
        string name
        string email
        string phone
        datetime createdAt
        long advisor_id FK
    }

    PORTFOLIO {
        long portfolioId PK
        datetime createdAt
        long client_id FK
    }

    SECURITY {
        long securityId PK
        string name
        string category
        date purchaseDate
        double purchasePrice
        int quantity
        long portfolio_id FK
    }

    %% Relationships
    ADVISOR ||--o{ CLIENT : manages
    CLIENT ||--|| PORTFOLIO : owns
    PORTFOLIO ||--o{ SECURITY : contains
```
