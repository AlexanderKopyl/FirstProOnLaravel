##Мои личные заметки по проекту

<p>
Команда migrate:refresh отменит изменения всех ваших миграций, а затем выполнит команду migrate. Эта команда эффективно создаёт заново всю вашу БД:
</p>
<pre>
php artisan migrate:refresh
</pre>

##Создание БД Миграции
<pre>
CREATE DATABASE 'your-database' CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci 
</pre>

<p>Создаем модел и миграции</p>
<pre>
php artisan make:model Models/BlogCategory -m
php artisan make:model Models/BlogPost -m
</pre> 
<p>Создаем Сиды</p>
<pre>
php artisan make:seeder UsersTableSeeder
php artisan make:seeder BlogCategoriesTableSeeder
</pre>
<p>Запуск сидов</p>
<pre>
php artisan db:seed
php artisan db:seed --classUsersTableSeeder
php artisan migrate:refresh --seed
</pre>
<p class="default">
Конечно, ручное определение признаков для каждой модели начальных данных затруднительно. Вместо этого вы можете использовать 
<a href="https://laravel.ru/docs/v5/database-testing#создание" title="/docs/v5/database-testing#создание" class="round-brackets internal">фабрики моделей</a> для быстрой генерации больших объёмов данных. 
Во-первых, пересмотрите <a href="https://laravel.ru/docs/v5/database-testing#создание" title="/docs/v5/database-testing#создание" class="round-brackets internal">документацию по фабрике моделей</a>, чтобы изучить, как определяются фабрики. 
Как только вы определите свои фабрики, вы можете использовать вспомогательную функцию <code class="format format-php"><span class="format-name">PHP</span><span style="color: #000000"><span style="color: #0000BB">factory</span><span style="color: #007700">()</span></span></code>, чтобы вставлять записи в вашу базу данных.<a name="использование-1" href="https://laravel.ru/docs/v5/seeding#использование-1" title="#использование-1" class="anchor"></a>
</p>
<pre>
/**
 * Загрузка начальных данных.
 *
 * @return void
 */
public function run()
{
  factory(App\User::class, 50)->create()->each(function ($u) {
    $u->posts()->save(factory(App\Post::class)->make());
  });
}
</pre>
<p>Создание реквеста</p>
<pre>
php artisan make:request BlogCategoryUpdateRequest
</pre>
