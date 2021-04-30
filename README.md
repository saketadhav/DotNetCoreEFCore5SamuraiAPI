> Wiring up ASP.NET CORE with EF CORE

**Web API Project**

    1. Add references to project with Entities and DBContext 
      (Add project references of Data and Domain into API project)

    2. Build

    3. Add controller (EF and API Actions)
        <!-- For adding Samurai Controller -->
        ```
        Add new controller -> Add API Controller with Actions using Entity FRamework.
        ModelClass == Samurai
        DBContextClass == SamuraiContext
        Controller Name == SamuraisController
        Click Add button
        This will add EF and other packeges to csproj
        ```

**Startup**

    4. Add services.DBContext with UseSqlServer to startup Configure()
    <!-- services.AddDbContext -->

**applicationsettings.json**

    5. Add connection string config
    <!-- ConnectionStrings -> SamuraiConnex -->

    6. Add EF core logging config
    <!-- Logging -> LogLevel -> Microsoft.EntityFrameworkCore.Database.Command -->

**DBContext**

    7. Add constructor that takes in DbContextOptions

    //CleanUp:- Not mandatory

    8. Remove optionsBuilder from OnConfiguring

    9. Clean up using statements