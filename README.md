# ⚡ Laravel Advanced Topics

## 🔁 Eloquent ORM & Relationships

### 📘 1. One-to-One Relationship
- Typical use case: `User` ↔ `Profile`
- Follows standard foreign key conventions
- Access and manipulate related models using Eloquent methods

### 📗 2. One-to-Many Relationship
- Example: `Post` → multiple `Comments`
- Use the inverse relationship (`belongsTo`)
- Optimize with `withCount()` and `withSum()`

### 📙 3. Many-to-Many Relationship
- Set up using pivot tables (e.g., `role_user`)
- Use `belongsToMany()` to define the relationship
- Access pivot attributes via `withPivot()`
- Add timestamps with `->withTimestamps()`

### 📒 4. Has-Many-Through Relationship
- Useful for indirect relationships (e.g., `Country` → `Posts` via `User`)
- Understand intermediate table and key alignment

### 📕 5. Polymorphic Relationships
- Use `morphTo`, `morphMany`, and `morphOne`
- Shared relationships for models like `Comment`, `Image`, `Tag`
- Support inverse polymorphic relations
- Support eager loading with polymorphic types

### 📓 6. Polymorphic Many-to-Many
- Use `morphToMany`, `morphedByMany`
- Ideal for tagging multiple model types (e.g., `Post`, `Video`)
- Requires polymorphic pivot table structure

---

## 🚀 Eager Loading vs Lazy Loading

### 💤 Lazy Loading
- Default behavior; loads relations on demand
- Can lead to N+1 query problems

### ⚡ Eager Loading
- Load relations ahead using `with()`
- Supports nested loading: `with('comments.user')`
- Apply constraints within eager loading queries

### 🧠 Lazy Eager Loading
- Load relations after initial fetch using `load()` or `loadMissing()`

### 📊 Eager Loading Aggregates
- Use `withCount()`, `withSum()`, `withAvg()` for efficient aggregate queries

---

## 🔍 Query Scopes

### 📌 Local Scopes
- Reusable logic within models (e.g., `scopePublished()`)
- Can be chained like query builder methods

### 🌐 Global Scopes
- Automatically apply conditions to all queries (e.g., `is_active = true`)
- Use `withoutGlobalScope()` to override when needed

---

## 🛠️ Mutators & Accessors

### 🧾 Accessors
- Customize how attributes are retrieved (e.g., full name concatenation)
- Use `$appends` to include them in model serialization

### 🛡️ Mutators (Laravel 9+)
- Use the `Attribute` class with `get` and `set` closures
- Ideal for formatting or sanitizing input/output
- Legacy support via `getXAttribute` / `setXAttribute` methods

---

## 🧬 Casting & Attribute Customization

### 🧮 Basic Attribute Casting
- Supports built-in types: `boolean`, `array`, `collection`, `datetime`, `decimal`

### 🔧 Custom Casts
- Implement `CastsAttributes` for custom transformation logic
- Useful for types like `Money`, `Coordinates`, etc.

### 🧾 Enum Casting
- Native PHP 8.1 enums supported in Laravel 9+
- Cast attributes to and from backed enums

### 🧱 JSON Column Casting
- Handle JSON attributes as arrays or objects
- Query nested values with `whereJsonContains()`, `whereJsonLength()`

---


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