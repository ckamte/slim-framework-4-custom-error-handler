# error-handler-for-slim-framework-4

using twig-view and monolog as container

# usage

```php
<?php
use App\Errors\ViewErrorHandler;
use DI\ContainerBuilder;
use Slim\Factory\AppFactory;

...

// Register Error Middleware
$displayErrorDetails = true; //from your settings
$errorMiddleware = $app->addErrorMiddleware($displayErrorDetails, true, true);

// Create Error Handler
$errorHandler = new ViewErrorHandler($app);
$errorMiddleware->setDefaultErrorHandler($errorHandler);

// Run Application
$app->run();

// ...
```
