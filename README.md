# EFCore-Relationships

This project showcases various use cases of Entity Framework Core (EF Core) relationships, specifically focusing on one-to-many and one-to-one relationships. EF Core is a popular Object-Relational Mapping (ORM) framework for .NET that simplifies database interactions and management.

## Getting Started

To use this project and explore its EF Core relationship examples, follow the steps below:

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Njuguna-JohnBrian/EFCore-Relationships
   cd EFCore-Relationships
   ```

2. Restore the necessary NuGet packages:

   ```bash
   dotnet restore
   ```

3. Apply the EF Core migrations to create the database structure.

   ```bash
   dotnet ef migrations add Initial
   dotnet ef database update
   ```

## Database Structure

This project demonstrates two main types of relationships using EF Core:

1. **One-to-Many Relationship: User and Character**

   - One User can have many Character(s).
   - One Character can have only one User.

   To illustrate this relationship, the project defines two entities, User and Character, with the following properties:

   - `User` Entity:
     - `UserId`: Unique identifier for each User.
     - `Username`: User's username.
     - `Characters`: A collection of Character entities associated with this user.

   - `Character` Entity:
     - `CharacterId`: Unique identifier for each Character.
     - `Name`: Character's name.
     - `UserId`: Foreign key reference to the User who owns this character.

   This one-to-many relationship is implemented using navigation properties and foreign keys.

2. **One-to-One Relationship: User and UserProfile**

   - One User has exactly one UserProfile.
   - One UserProfile is associated with only one User.

   To demonstrate this one-to-one relationship, the project defines two entities, User and UserProfile, with the following properties:

   - `User` Entity:
     - `UserId`: Unique identifier for each User.
     - `Username`: User's username.
     - `UserProfile`: Navigation property representing the associated UserProfile for the User.

   - `UserProfile` Entity:
     - `UserProfileId`: Unique identifier for each UserProfile.
     - `FullName`: User's full name.
     - `UserId`: Foreign key reference to the User related to this UserProfile.

   This one-to-one relationship is implemented using navigation properties and foreign keys, as well as a unique constraint on the `UserId` property in the UserProfile entity.

## Usage

You can explore and experiment with the different EF Core relationship examples in this project by running and extending the code as needed. The sample code and entity configurations are provided to help you understand how to work with one-to-many and one-to-one relationships using EF Core.

Feel free to modify the code and database to suit your specific use cases and learn how to effectively use EF Core to manage complex relationships in your own projects.

## License

This project is open-source and available under the [MIT License](LICENSE.md). You are free to use, modify, and distribute it as needed.