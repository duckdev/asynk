# Asynk - Drupal Asynchronous Tasks
Run asynchronous tasks in Drupal easily.

### Sample Usage:
Register asynchronous task for a heavy function.
```php
// Execute the heavy task asynchronously.
asynk('sample_heavy_task', $key, $lan);
```
Heavy resource task for execution
```php
// Send email to 10 people.
function sample_heavy_task($key, $lan) {

  for ($i = 0; $i < 10; $i ++) {
    drupal_mail('my_module', $key, 'sample@sample.com', $lan);
  }
}
```
