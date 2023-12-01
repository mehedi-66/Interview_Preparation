# Entity Framework Interview Questions

1. **What is Entity Framework (EF)?**
   - Entity Framework is an Object-Relational Mapping (ORM) framework provided by Microsoft. It simplifies database interactions in .NET applications by allowing developers to work with database entities as objects.

2. **Explain the key components of Entity Framework.**
   - Entity Framework includes the ObjectContext or DbContext, Entity Data Model, LINQ to Entities, and Entity SQL. DbContext is more commonly used in recent versions.

3. **What is Code First in Entity Framework?**
   - Code First is an approach in Entity Framework where you define your model classes first and then generate the database from these classes. It allows developers to focus on the domain model rather than the database schema.

4. **What is Database First in Entity Framework?**
   - Database First is an approach in Entity Framework where the entity data model is generated from an existing database. It involves reverse engineering the database schema to create the corresponding model classes.

5. **Explain the difference between DbSet and IQueryable in Entity Framework.**
   - `DbSet` represents an entity set that can be queried from the database, while `IQueryable` is an interface that allows for building complex LINQ queries that are translated to SQL.

6. **What is Lazy Loading in Entity Framework?**
   - Lazy Loading is a feature in Entity Framework where related entities are loaded from the database only when they are accessed for the first time. This can help improve performance by loading data on-demand.

7. **What is Eager Loading in Entity Framework?**
   - Eager Loading is the opposite of Lazy Loading. It involves loading related entities along with the main entity in a single query. This can reduce the number of database queries but may load more data than necessary.

8. **Explain the differences between EntityState.Added, EntityState.Modified, and EntityState.Deleted.**
   - These are states of an entity being tracked by the DbContext. `Added` means the entity is marked for insertion, `Modified` means it has been changed and needs an update, and `Deleted` means it should be removed from the database.

9. **What is the purpose of migrations in Entity Framework?**
   - Migrations in Entity Framework enable developers to evolve the database schema over time as the application's model changes. It provides a way to update the database schema without losing data.

10. **Explain the role of the Fluent API in Entity Framework.**
    - Fluent API is an alternative way to configure the model in Entity Framework. It provides a more fluent and code-based approach for configuring entities, relationships, and other aspects of the model.

Remember to provide practical examples and discuss your experiences with Entity Framework during the interview. Good luck!
