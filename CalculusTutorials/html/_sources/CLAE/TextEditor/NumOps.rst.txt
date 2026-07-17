Number Conversion Options
=========================

This submenu contains options for numeric base conversions and numeric formatting.  Most of these were originally created for conversion that are common in cryptography but some users may have a use for them.

Decimal -> Binary
-----------------

Converts decimal numbers to binary. For example,

.. code-block:: console

    1234567890

is converted to

.. code-block:: console

    1001001100101100000001011010010

Decimal -> Octal
----------------

Converts decimal numbers to octal. For example,

.. code-block:: console

    1234567890

is converted to

.. code-block:: console

    11145401322



Decimal -> Hexadecimal
----------------------

Converts decimal numbers to hexadecimal. For example,

.. code-block:: console

    1234567890

is converted to

.. code-block:: console

    499602D2


Binary -> Decimal
-----------------

Converts binary numbers to decimal.  For example,

.. code-block:: console

    111101111001000000001000001100

is converted to

.. code-block:: console

    1038352908

Binary -> Octal
---------------

Converts binary numbers to octal. For example,

.. code-block:: console

    111101111001000000001000001100

is converted to

.. code-block:: console

    7571001014

Binary -> Hexadecimal
---------------------

Converts binary numbers to hexadecimal. For example,

.. code-block:: console

    111101111001000000001000001100

is converted to

.. code-block:: console

    3DE4020C

Octal -> Decimal
----------------

Converts octal numbers to decimal.  For example,

.. code-block:: console

    7263551734432

is converted to

.. code-block:: console

    505156188442


Octal -> Binary
---------------

Converts octal numbers to binary. For example,

.. code-block:: console

    7263551734432

is converted to

.. code-block:: console

    111010110011101101001111011100100011010

Octal -> Hexadecimal
--------------------

Converts octal numbers to hexadecimal. For example,

.. code-block:: console

    7263551734432

is converted to

.. code-block:: console

    759DA7B91A


Hexadecimal -> Decimal
----------------------

Converts hexadecimal numbers to decimal. For example,

.. code-block:: console

    A34BC09AD

is converted to

.. code-block:: console

    43834411437

Hexadecimal -> Binary
---------------------

Converts hexadecimal numbers to binary. For example,

.. code-block:: console

    A34BC09AD

is converted to

.. code-block:: console

    101000110100101111000000100110101101

Hexadecimal -> Octal
--------------------

Converts hexadecimal numbers to octal. For example,

.. code-block:: console

    A34BC09AD

is converted to

.. code-block:: console

    506457004655

General Base Conversion
-----------------------

Allows the user to select the base conversion by inputting the original and target bases. Bases are restricted to be between 2 and 36, as with hexadecimal representation the a, b, c, d, e, f, sequence is continued with g, h, i, ... for bases that exceed 16.

For example,

.. code-block:: console

    43834411437

converting from base 10 to base 3 gives,

.. code-block:: console

    11012010220011211010220

and converting the original number from base 9 to base 7 gives,

.. code-block:: console

    1055242002223

Remove Leading Zeros
--------------------

Removes leading zeros from numbers.

Remove Leading Zeros with Minimum Length
----------------------------------------

Removes leading zeros from numbers but allows the user to select a minimum length of the resulting number. For example, with the value

.. code-block:: console

    00001101

if the user selects a minimum length of 5 the result will be

.. code-block:: console

    01101

Pad with Zeros
--------------

Pads the beginning of each number with zeros up to a maximum length that is specified by the user. For example, if the number is 42 and the user selects a length of 5 the result will be

.. code-block:: console

    00042

Likewise, if the user selects a length of 2 (or 0 or 1) the result will be 42.


