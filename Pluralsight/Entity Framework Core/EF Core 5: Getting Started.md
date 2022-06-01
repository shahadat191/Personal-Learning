<h2> DbContext </h2>
<ul>
  <li> DbContext provides logic for EF Core to interact with your database </li>
</ul>
<h3> DbSet </h3>
Wrapper

In DbContext file
```C#
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
{
    var connectionString = "Data Source= (localdb)\\MSSQLLocalDB; Initial Catalog=SamuraiAppData";
    optionsBuilder.UseSqlServer(connectionString);
}

```


<h1> Controlling Database Creation and Schema Changes with Migrations </h1>

<h3> EF Core Basic Migrations Workflow </h3>
Define/Change Model => Create a Migration File => Apply Migration to DB or Script

<h3> EF Core Migrations are source-control friendly </h3>
1. Migrations in Team Environments.
2. 


<h3> Tooling and APIs for EF Core Migrations </h3>
                      At the Command Line
Migration Commands      Install dotnet -ef tools on your dev machine

Migration APIs   Design Package

* > dotnet tool install --global dotnet-ef

        Add-Migration               Adds a new migration.
        Update-Database             Updates the database to a specified migration.
script-migration for production
Update-Database for development


<h3> Reverse Enginnering </h3>

<h4> How EF Core Determines Mappings to DB </h4>

Convention => Default Assumptions => proprty name = column name
Override with Fluent Mappings => modelBuilder.Entity<Quotes>().Property(q => q.Text).HasColumnName("Line")
Override wiht Data Annotations [Column("Line")]
  
  <h1> Defining Relationship in Your Model </h1>
  
