<p align="center">
<img class="mark" src="https://laravel.com//img/logomark.min.svg" alt="Laravel">
<img class="type" src="https://laravel.com//img/logotype.min.svg" alt="Laravel">
</p>


##Eloquent ORM

<p class="default">
<a href="https://laravel.ru/docs/v5/eloquent" >Eloquent</a> — это стандартное <abbr title="Объектно-реляционное отображение (Object-relational mapping) - приём для связывания баз данных с концепциями объектно-ориентированного программирования, как бы создающий &quot;виртуальную объектную базу данных&quot;.">ORM</abbr> для Laravel (объектно-реляционное отображение). Eloquent делает безболезненным получение и хранение данных в вашей базе данных, используя чётко определённые <span class="quotes quotes-0">«модели»</span>. Обычно, каждая Eloquent модель однозначно соответствует одной таблице базы данных.<a name="модели-1" href="https://laravel.ru/docs/v5/quickstart#модели-1" title="#модели-1" class="anchor"></a>
</p>
<p class="default">
Давайте определим модель <kbd>Task</kbd>, которая будет соответствовать только что созданной нами таблице <kbd>tasks</kbd>. Мы снова можем использовать команду Artisan, чтобы сгенерировать эту модель. В этом случае мы будем использовать команду <code class="format format-sh"><span class="format-name"></span>make:model</code>:<a name="модели-2" href="https://laravel.ru/docs/v5/quickstart#модели-2" title="#модели-2" class="anchor"></a>
</p>
<pre>
php artisan make:model Task
</pre>
<p>Модель будет помещена в каталог app вашего приложения.</p>
