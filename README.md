# restful-api-laravel

## Create new table

-   Tạo bảng mới : `php artisan make:migration name_database`
-   File database/migrations/...(file mới) => `function up(){Schema::create('posts', function (Blueprint $table) {
          $table->id();
          $table->string("name");
          ...
          $table->timestamps();
      });}` => khởi tạo table mới
-   Tạo bảng mới `php artisan migrate`

- Tạo Model `php artisan  make:model Post`
- Tạo biến mới `protected $fillable = [
        "name",
        ...
    ];`
- Tạo controller : `php artisan make:controller API/PostController --api` : --resource(CRUD) , --api(API) => tạo controller đầy đủ các hàm
- Tạo routes mới : `Route::apiResource("/posts",PostController::class)`
# Auto create 

- Create factory : `php artisan make:factory PostFactory`
- `php artisan tinker`
- `App\Models\Post::factory(20)->create()`