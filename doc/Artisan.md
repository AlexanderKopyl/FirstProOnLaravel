##Artisan 
<p>Added in 5.1.11:<a href="http://laravel.com/docs/5.1/authorization#creating-policies">http://laravel.com/</a></p>
<pre>
php artisan make:policy PostPolicy
</pre>

##Displays help for a given command
<pre>
php artisan --help OR -h
</pre>

##Do not output any message
<pre>
php artisan --quiet OR -q
</pre>

## Display this application version
<pre>
phh5p artisan --version OR -V
</pre>

##Do not ask any interactive question
<pre>
php artisan --no-interaction OR -n
</pre>

##Force ANSI output
<pre>
php artisan --ansi
</pre>

##Disable ANSI output
<pre>
php artisan --no-ansi
</pre>

##The environment the command should run under
<pre>
php artisan --env
</pre>

##-v|vv|vvv Increase the verbosity of messages: 
<ul>
<li>1 for normal output</li>
<li>2 for more verbose output</li>
<li>3 for debug</li>
</ul>

<pre>
php artisan --verbose
</pre>

##Remove the compiled class file
<pre>
php artisan clear-compiled
</pre>

##Display the current framework environment
<pre>
php artisan env
</pre>

##Displays help for a command
<pre>
php artisan help
</pre>

##Lists commands
<pre>
php artisan list
</pre>

##Interact with your application
<pre>
php artisan tinker
</pre>

##Put the application into maintenance mode
<pre>
php artisan down
</pre>

##Bring the application out of maintenance mode
<pre>
php artisan up
</pre>

##Optimize the framework for better performance
  <ul>
   <li>--force    Force the compiled class file to be written.</li>
  <li>--psr      Do not optimize Composer dump-autoload.</li>
  </ul>
  <pre>
php artisan optimize [--force] [--psr]
</pre>

##Serve the application on the PHP development server
<pre>
php artisan serve
</pre>

##Change the default port
<pre>
php artisan serve --port 8080
</pre>

##Get it to work outside localhost
<pre>
php artisan serve --host 0.0.0.0
</pre>

##Set the application namespace
<pre>
php artisan app:name namespace
</pre>

##Flush expired password reset tokens
<pre>
php artisan auth:clear-resets
</pre>

##Flush the application cache
<pre>
php artisan cache:clear
</pre>

##Create a migration for the cache database table
<pre>
php artisan cache:table
</pre>

##Create a cache file for faster configuration loading
<pre>
php artisan config:cache
</pre>

##Remove the configuration cache file
<pre>
php artisan config:clear
</pre>

##In program
<p>$exitCode = Artisan::call('config:cache');
</p>
<p>Seed the database with records</p>
<ul>
<li> --class      The class name of the root seeder (default: "DatabaseSeeder")
</li>
<li>  --database   The database connection to seed
</li>
<li> --force      Force the operation to run when in production.
</li>

</ul>
<pre>
php artisan db:seed [--class[="..."]] [--database[="..."]] [--force]
</pre>

##Generate the missing events and handlers based on registration
<pre>
php artisan event:generate
</pre>

##Create a new command handler class
<ul>
<li>--command      The command class the handler handles.</li>
</ul>
<pre>
php artisan handler:command [--command="..."] name
</pre>

##Create a new event handler class
 <ul>
 <li>--event        The event class the handler handles.</li>
 <li>--queued       Indicates the event handler should be queued.</li>
 </ul>
<pre>
php artisan handler:event [--event="..."] [--queued] name
</pre>
##Set the application key
<pre>
php artisan key:generate
</pre>

##By default, this creates a self-handling command that isn't pushed to the queue.
<ul>
<li>
 Pass this the --handler flag to generate a handler, and the --queued flag to make it queued.

</li>
</ul>

<pre>
php artisan make:command [--handler] [--queued] name
</pre>

##Create a new Artisan command
<ul>
<li> --command     The terminal command that should be assigned. (default: "command:name")
</li>
</ul>
<pre>
make:console [--command[="..."]] name
</pre>
##Create a new resourceful controller
<ul>
<li>
--plain      Generate an empty controller class.
</li>
</ul>
<pre>
php artisan make:controller [--plain] name
php artisan make:controller App\\Admin\\Http\\Controllers\\DashboardController
</pre>

##Create a new event class
<pre>
php artisan make:event name
</pre>
##Create a new middleware class
<pre>
php artisan make:middleware name
</pre>
##Create a new migration file
<ul>
<li>--create     The table to be created.</li>
<li> --table      The table to migrate.</li>
</ul>
<pre>
php artisan make:migration [--create[="..."]] [--table[="..."]] name
</pre>
##Create a new Eloquent model class
<pre>
php artisan make:model name
</pre>
##Create a new service provider class
<pre>
php artisan make:provider name
</pre>
##Create a new form request class
<pre>
php artisan make:request name
</pre>
##Database migrations
<ul>
 <li>--database   The database connection to use.</li>
 <li>--force      Force the operation to run when in production.</li>
<li>--path       The path of migrations files to be executed.</li>
<li> --pretend    Dump the SQL queries that would be run.</li>
 <li>--seed       Indicates if the seed task should be re-run.</li>
</ul>
<pre>
php artisan migrate [--database[="..."]] [--force] [--path[="..."]] [--pretend] [--seed]
</pre>

## Create the migration repository
<pre>
php artisan migrate:install [--database[="..."]]
</pre>
##Create a new migration file
 <ul>
 <li>--seeder     The class name of the root seeder.</li>
 </ul>
<pre>
php artisan migrate:refresh [--database[="..."]] [--force] [--seed] [--seeder[="..."]]
</pre>
##Rollback all database migrations
<ul>
<li>--pretend    Dump the SQL queries that would be run.</li>
</ul>
<pre>
php artisan migrate:reset [--database[="..."]] [--force] [--pretend]
</pre>
##Rollback the last database migration
<pre>
php artisan migrate:rollback [--database[="..."]] [--force] [--pretend]
</pre>
##Show a list of migrations up/down
<pre>
php artisan migrate:status
</pre>
##Create a migration for the queue jobs database table
<pre>
php artisan queue:table
</pre>
##Listen to a given queue
<ul>
<li>--queue      The queue to listen on</li>
<li>--delay      Amount of time to delay failed jobs (default: 0)</li>
<li>--memory     The memory limit in megabytes (default: 128)</li>
<li>--timeout    Seconds a job may run before timing out (default: 60)</li>
<li>--sleep      Seconds to wait before checking queue for jobs (default: 3)</li>
<li>--tries      Number of times to attempt a job before logging it failed (default: 0)</li>
</ul>
<pre>
php artisan queue:listen [--queue[="..."]] [--delay[="..."]] [--memory[="..."]] [--timeout[="..."]] [--sleep[="..."]] [--tries[="..."]] [connection]
</pre>

##List all of the failed queue jobs
<pre>
php artisan queue:failed
</pre>
##Create a migration for the failed queue jobs database table
<pre>
php artisan queue:failed-table
</pre>
##Flush all of the failed queue jobs
<pre>
php artisan queue:flush
</pre>
##Delete a failed queue job
<pre>
php artisan queue:forget
</pre>
##Restart queue worker daemons after their current job
<pre>
php artisan queue:restart
</pre>
##Retry a failed queue job(id: The ID of the failed job)
<pre>
php artisan queue:retry id
</pre>
##Subscribe a URL to an Iron.io push queue
<ul>
<li>queue: The name of Iron.io queue.</li>
<li>url: The URL to be subscribed.</li>
<li>--type       The push type for the queue.</li>
</ul>
 <pre>
php artisan queue:subscribe [--type[="..."]] queue url
</pre>

##Process the next job on a queue
<ul>
<li>--queue      The queue to listen on</li>
<li>--daemon     Run the worker in daemon mode</li>
<li>--delay      Amount of time to delay failed jobs (default: 0)</li>
<li>--force      Force the worker to run even in maintenance mode</li>
<li>--memory     The memory limit in megabytes (default: 128)</li>
<li>--sleep      Number of seconds to sleep when no job is available (default: 3)</li>
<li>--tries      Number of times to attempt a job before logging it failed (default: 0)</li>
</ul>
<pre>
php artisan queue:work [--queue[="..."]] [--daemon] [--delay[="..."]] [--force] [--memory[="..."]] [--sleep[="..."]] [--tries[="..."]] [connection]
</pre>

##Create a route cache file for faster route registration
<pre>
php artisan route:cache
</pre>

##Remove the route cache file
<pre>
php artisan route:clear
</pre>

##List all registered routes
<pre>
php artisan route:list
</pre>

##Run the scheduled commands
<pre>
php artisan schedule:run
</pre>

##Create a migration for the session database table
<pre>
php artisan session:table
</pre>

##Publish any publishable assets from vendor packages
<ul>
<li>--force        Overwrite any existing files.</li>
<li>--provider     The service provider that has assets you want to publish.</li>
<li>--tag          The tag that has assets you want to publish.</li>
</ul>
<pre>
php artisan vendor:publish [--force] [--provider[="..."]] [--tag[="..."]]
php artisan tail [--path[="..."]] [--lines[="..."]] [connection]
</pre>
