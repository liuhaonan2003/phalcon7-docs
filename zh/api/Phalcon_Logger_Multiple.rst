Class **Phalcon\\Logger\\Multiple**
===================================

.. role:: raw-html(raw)
   :format: html

:raw-html:`<a href="https://github.com/dreamsxin/cphalcon7/blob/master/ext/logger/multiple.c" class="btn btn-default btn-sm">Source on GitHub</a>`

Handles multiples logger handlers


Methods
-------

public  **push** (:doc:`Phalcon\\Logger\\AdapterInterface <Phalcon_Logger_AdapterInterface>` $logger)

Pushes a logger to the logger tail



public :doc:`Phalcon\\Logger\\AdapterInterface <Phalcon_Logger_AdapterInterface>` [] **getLoggers** ()

Returns the registered loggers



public  **setFormatter** (:doc:`Phalcon\\Logger\\FormatterInterface <Phalcon_Logger_FormatterInterface>` $formatter)

Sets a global formatter



public :doc:`Phalcon\\Logger\\FormatterInterface <Phalcon_Logger_FormatterInterface>`  **getFormatter** ()

Returns a formatter



public  **log** (*int* $type, *string* $message, [*array* $context])

Sends a message to each registered logger



public  **emergency** (*string* $message, [*array* $context])

Sends/Writes an emergency message to the log



public  **emergence** (*unknown* $message, [*array* $context])

...


public  **debug** (*string* $message, [*array* $context])

Sends/Writes a debug message to the log



public  **error** (*string* $message, [*array* $context])

Sends/Writes an error message to the log



public  **info** (*string* $message, [*array* $context])

Sends/Writes an info message to the log



public  **notice** (*string* $message, [*array* $context])

Sends/Writes a notice message to the log



public  **warning** (*string* $message, [*array* $context])

Sends/Writes a warning message to the log



public  **alert** (*string* $message, [*array* $context])

Sends/Writes an alert message to the log



