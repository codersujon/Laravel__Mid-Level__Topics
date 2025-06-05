# ⚡LARAVEL ADVANCED TOPICS

🔁 Eloquent ORM & Relationships
 - One-to-One, One-to-Many, Many-to-Many, Has-Many-Through, Polymorphic relations
    ## One-to-One Relationship
    - Use cases (e.g., User ↔ Profile)
    - Foreign key conventions
    - Retrieving and saving related models

    ## One-to-Many Relationship
    - Use cases (e.g., Post → Comments)
    - Inverse relation (belongsTo)
    - Using withCount() and withSum()

    ## Many-to-Many Relationship
    - Pivot table creation and naming conventions
    - belongsToMany() method
    - Accessing pivot data using withPivot()
    - Timestamps on pivot (->withTimestamps())

    ## Has-Many-Through Relationship
    - Use case (e.g., Country → Posts via User)
    - Understanding intermediate models and key mapping

    ## Polymorphic Relationship
    - morphTo, morphMany, morphOne
    - Use cases: Comments, Tags, Images
    - Eager loading polymorphic relations
    - Inverse polymorphic relationships

    ## Polymorphic Many-to-Many (morphToMany, morphedByMany)
    - Use case: Tags across different models (Posts, Videos, etc.)
    - Pivot table setup with morph types
    
 - Eager Loading vs Lazy Loading
    ## Lazy Loading
    - Default behavior
    - The N+1 problem and its impact

    ## Eager Loading
    - with() and nested eager loading (with('relation.subrelation'))
    - Conditional eager loading with constraints

    ## Lazy Eager Loading
    - When to use load() and loadMissing() on existing collections

    ## Eager Loading Aggregates
    - withCount(), withSum(), withAvg() for optimizing queries

 - Query scopes (local and global)
    ## Local Scopes
    - Creating reusable query logic (e.g., scopePublished)
    - Chaining scopes

    ## Global Scopes
    - Adding default query constraints (e.g., is_active = true)
    - Removing global scopes (withoutGlobalScope())

 - Mutators & Accessors
    ## Custom Accessors
    - Formatting attributes (e.g., full name, formatted date)
    - Appending computed attributes ($appends)

    ## Mutators (Laravel 9+ syntax)
    - Creating Attribute::make() definitions
    - Use cases: auto-hashing passwords, formatting input
    - Legacy Mutators (getXAttribute/setXAttribute)

 - Casting and attribute customization
    ## Basic Attribute Casting
    - Built-in cast types: boolean, array, collection, datetime, decimal

    ## Custom Casts
    - Creating classes implementing CastsAttributes
    - Transforming values into domain-specific types (e.g., Money object)

    ## Enum Casting (Laravel 9+)
    - Using backed enums with attribute casting

    ## JSON Column Casting
    - Working with nested JSON structures
    - Querying and casting JSON fields

 🔐 Authentication & Authorization
 - Laravel Breeze, Jetstream, or Fortify
 - Custom guards
 - Gates & Policies
 - Role-based access control (RBAC)

 📦 Service Container & Dependency Injection
 - Binding interfaces to implementations
 - Singleton vs transient bindings
 - Auto-injection into controllers and services

 🔄 Service Providers & Facades
 - Creating custom service providers
 - When and why to use facades
 - Binding classes to the service container

 📤 Event System
 - Events and Listeners
 - Broadcasting (with Pusher or Laravel Echo)
 - Queued listeners

 📥 API Development
 - Resource controllers
 - API Resource (transformers)
 - Rate limiting and throttling
 - Sanctum or Passport for token authentication

 ⚙️ Testing
 - Feature vs Unit tests
 - HTTP tests with actingAs(), json(), etc.
 - Mocking dependencies
 - Database transactions in testing

 📁 Advanced File Storage
 - Using Laravel Filesystem
 - Working with cloud storage (S3, etc.)
 - File uploads and downloads

 ⏱️ Task Scheduling
 - Defining and running scheduled tasks via Task Scheduling
 - Using cron jobs and php artisan schedule:run