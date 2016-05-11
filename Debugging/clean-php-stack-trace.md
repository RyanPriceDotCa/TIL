#Output a clean stacktrace in PHP

```php
$e = new Exception;
var_dump($e->getTraceAsString());
```
Will Output:

```
#0 /var/www/interdev/modules/node/node.module(1151): drupal_write_record('node', Object(stdClass), 'nid')
#1 /var/www/interdev/sites/all/modules/contrib/webform/includes/webform.conditionals.inc(254): node_save(Object(stdClass))
#2 /var/www/interdev/includes/form.inc(1519): webform_conditionals_form_submit(Array, Array)
#3 /var/www/interdev/includes/form.inc(903): form_execute_handlers('submit', Array, Array)
#4 /var/www/interdev/includes/form.inc(385): drupal_process_form('webform_conditi...', Array, Array)
#5 /var/www/interdev/includes/form.inc(130): drupal_build_form('webform_conditi...', Array)
#6 [internal function]: drupal_get_form('webform_conditi...', Object(stdClass))
#7 /var/www/interdev/includes/menu.inc(527): call_user_func_array('drupal_get_form', Array)
#8 /var/www/interdev/index.php(21): menu_execute_active_handler()
#9 {main}"
```
