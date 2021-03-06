调用方法（Calling Methods）
===========================
As seen when calling functions, in Phalcon the methods are called in the PHP userland. Thanks to this, a Phalcon
user can generate a backtrace and know exactly which components are involved in a given task. They also
allows users to replace Phalcon components by PHP classes of their own. Additionally,
like everything else we've seen, the way to make calls is familiar to PHP developers.

调用实例方法（Instance methods）
--------------------------------

.. code-block:: c

	// Define the connection DSN
	ZVAL_STRING(&dsn, "mysql:host=localhost;username=root;password=secret;dbname=some");

	// Get the PDO class entry
	pdo_class_entry = zend_fetch_class(SL("PDO"), ZEND_FETCH_CLASS_AUTO);

	// Create a PDO instance passing the dsn to the constructor
	object_init_ex(&pdo, pdo_class_entry);
	PHALCON_CALL_METHOD(NULL, pdo, "__construct", &dsn);

	// Create a SQL statement
	ZVAL_STRING(&sql_statement, "SELECT * FROM robots");

	// Call the "exec" method in the pdo object passing the sql_statement
	PHALCON_CALL_METHOD(&success, &pdo, "exec", &sql_statement);

调用静态方法（Static methods）
------------------------------

.. code-block:: c

	ZVAL_STRING(&some_variable, "invoices_detail");

	// Calling Phalcon\Text::camelize("invoices_detail")
	PHALCON_CALL_STATIC(camelized, "phalcon\\text::camelize", some_variable);
