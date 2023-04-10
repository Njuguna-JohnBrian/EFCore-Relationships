# EFCore-Relationships

- Add table/update

```bash
dotnet ef migrations add Users
```

## DB STRUCTURE

```sql
One User can have many Character(s)
One Character can only have one User
```