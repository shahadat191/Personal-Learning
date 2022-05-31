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
