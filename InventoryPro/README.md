## Technology Stack

### Backend Services
- **Framework**: ASP.NET Core 9.0
- **Database**: SQL Server 2022
- **ORM**: Entity Framework Core 9.0
- **Authentication**: JWT Bearer Tokens
- **API Gateway**: Ocelot
- **Logging**: Serilog
- **API Documentation**: Swagger/OpenAPI

### Windows Forms Client
- **Framework**: .NET 9.0 Windows Forms
- **HTTP Client**: HttpClient with Polly for resilience
- **Reporting**: Microsoft Reporting Services
- **UI Components**: DevExpress (optional) or standard Windows Forms controls

### Development Tools
- **IDE**: Visual Studio 2022 (17.8+)
- **Version Control**: Git
- **Package Manager**: NuGet
- **Container**: Docker (optional for microservices)

## Database Schema

### AuthDB
- Users (Id, Username, PasswordHash, Email, Role, CreatedAt, UpdatedAt)
- Roles (Id, Name, Permissions)
- RefreshTokens (Id, Token, UserId, ExpiresAt)

### ProductDB
- Products (Id, Name, SKU, Description, Price, Stock, CategoryId, CreatedAt, UpdatedAt)
- Categories (Id, Name, Description)
- StockMovements (Id, ProductId, Quantity, Type, Reason, Date)

### SalesDB
- Customers (Id, Name, Email, Phone, Address, CreatedAt)
- Sales (Id, CustomerId, Date, TotalAmount, Status)
- SaleItems (Id, SaleId, ProductId, Quantity, UnitPrice, Subtotal)

### ReportDB
- ReportTemplates (Id, Name, Type, Query)
- ReportHistory (Id, TemplateId, GeneratedAt, GeneratedBy)