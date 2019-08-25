<p align="center">
<img class="mark" src="https://laravel.com//img/logomark.min.svg" alt="Laravel">
<img class="type" src="https://laravel.com//img/logotype.min.svg" alt="Laravel">
</p>


## Установка

<p>
<strong>Установка Laravel</strong><a name="установка-1" href="https://laravel.ru/docs/v5/quickstart#установка-1" title="#установка-1" class="anchor"></a>
</p>
<p>
Конечно, в первую очередь вам будет нужен свежий фреймворк Laravel. Чтобы запустить его, вы можете использовать <a href="/docs/v5/homestead" title="/docs/v5/homestead" class="round-brackets internal">виртуальную машину Homestead</a> или локальную PHP-среду на ваш выбор. Как только ваше окружение будет готово, вы можете установить фреймворк Laravel, используя Composer:<a name="установка-2" href="https://laravel.ru/docs/v5/quickstart#установка-2" title="#установка-2" class="anchor"></a>
</p>
<pre>
composer create-project laravel/laravel --prefer-dist
</pre>
<p>
<strong>Установка проекта Quickstart (не обязательно)</strong><a name="установка-3" href="https://laravel.ru/docs/v5/quickstart#установка-3" title="#установка-3" class="anchor"></a>
</p>
<p>
Однако, если вы хотите загрузить исходный код для этого руководства и выполнить его на локальной машине, то можете клонировать Git хранилище и установить зависимости:<a name="установка-4" href="https://laravel.ru/docs/v5/quickstart#установка-4" title="#установка-4" class="anchor"></a>
</p>
<pre>
git clone https://github.com/laravel/quickstart-basic quickstart
cd quickstart
composer install
php artisan migrate
</pre>
<p>
Больше информации относительно создания локальной среды разработки Laravel вы сможете найти в документации по <a href="/docs/v5/homestead" title="/docs/v5/homestead" class="round-brackets internal">Homestead</a> и по <a href="/docs/v5/installation" title="/docs/v5/installation" class="round-brackets internal">установке</a>.<a name="установка-5" href="https://laravel.ru/docs/v5/quickstart#установка-5" title="#установка-5" class="anchor"></a>
</p>
