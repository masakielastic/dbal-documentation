Supporting Other Databases
==========================

To support a database which is not currently shipped with Doctrine
you have to implement the following interfaces and abstract
classes:


-  ``\Doctrine\DBAL\Driver\Driver``
-  ``\Doctrine\DBAL\Driver\Statement``
-  ``\Doctrine\DBAL\Platforms\AbstractPlatform``
-  ``\Doctrine\DBAL\Schema\AbstractSchemaManager``

For an already supported platform but unsupported driver you only
need to implement the first two interfaces, since the SQL
Generation and Schema Management is already supported by the
respective platform and schema instances. You can also make use of
several Abstract Unittests in the ``\Doctrine\Tests\DBAL`` package
to check if your platform behaves like all the others which is
necessary for SchemaTool support, namely:


-  ``\Doctrine\Tests\DBAL\Platforms\AbstractPlatformTestCase``
-  ``\Doctrine\Tests\DBAL\Functional\Schema\AbstractSchemaManagerTestCase``

We would be very happy if any support for new databases would be
contributed back to Doctrine to make it an even better product.


