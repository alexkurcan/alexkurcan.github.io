# Nike ERD
```mermaid
erDiagram
PRODUCT ||--o{SALE: "in sold in"
PRODUCT ||--|| INVENTORY: "is tracked"
CUSTOMER ||--o{SALE: makes
PRODUCT {
    string productid PK "123548AKL4"
    string model "Black and Green Curry"
    float price "130.00"
    string size "10.5"
}
CUSTOMER {
    string customerid PK "459045ASL4"
    string name "David Stone"
    string email "davidthecatlover35@gmail.com"
}
SALE {
    string id PK "159044123L5"
    date date "10-18-2024"
    string customerid FK "123548AKL4"
    string prodcutid FK "159044123L5"
    int quantity "2 SOLD"
}
INVENTORY {
    string productid FK "123548AKL4"
    int stock "Currently in stock"
}
```
## Documentation Section
