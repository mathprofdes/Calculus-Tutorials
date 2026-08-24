Character Conversion Options
============================

This submenu contains options for character encoding.  Most of these were originally created for conversion that are common in cryptography but some users may have a use for them.

A-Z -> 1-26
-----------

Codes characters A-Z as 1-26. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    1 2 3 4 5 6 7 8

A-Z -> 01-26
------------

Codes characters A-Z as 01-26. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    01 02 03 04 05 06 07 08

A-Z -> 0-25
-----------

Codes characters A-Z as 1-26. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    0 1 2 3 4 5 6 7

A-Z -> 00-25
------------

Codes characters A-Z as 01-26. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    00 01 02 03 04 05 06 07

A-Z -> 1-26 Binary
------------------

Codes characters A-Z as 1-26 and output is in binary form. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    1 10 11 100 101 110 111 1000

A-Z -> 0-25 Binary
------------------

Codes characters A-Z as 0-25 and output is in binary form. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    0 1 10 11 100 101 110 111

A-Z -> 1-26 8-Bit Binary
------------------------

Codes characters A-Z as 1-26 and output is in 8-bit binary form. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    00000001 00000010 00000011 00000100 00000101 00000110 00000111 00001000

A-Z -> 0-25 8-Bit Binary
------------------------

Codes characters A-Z as 0-25 and output is in 8-bit binary form. Lowercase characters are converted to uppercase before coding and all other characters are ignored. For example,

.. code-block:: console

    abcde, fgh

is coded as

.. code-block:: console

    00000000 00000001 00000010 00000011 00000100 00000101 00000110 00000111

Text -> ASCII
-------------

Codes each character to its ASCII value. The input is assumed to be keyboard characters within the ASCII table. For example,

.. code-block:: console

    Cryptography is cool!

is coded as

.. code-block:: console

    67 114 121 112 116 111 103 114 97 112 104 121 32 105 115 32 99 111 111 108 33


Text -> ASCII: 3 Digits
-----------------------

Codes each character to its ASCII value using 3 digits for each number, padding the beginning with zeros if needed. For example,

.. code-block:: console

    Cryptography is cool!

is coded as

.. code-block:: console

    067 114 121 112 116 111 103 114 097 112 104 121 032 105 115 032 099 111 111 108 033


Text -> ASCII: Binary
---------------------

Codes each character to its ASCII value and returns the binary representation of the number. For example,

.. code-block:: console

    Cryptography is cool!

is coded as

.. code-block:: console

    1000011 1110010 1111001 1110000 1110100 1101111 1100111 1110010
    1100001 1110000 1101000 1111001 100000 1101001 1110011 100000
    1100011 1101111 1101111 1101100 100001


Text -> ASCII: 8-Bit Binary
---------------------------

Codes each character to its ASCII value and returns the 8-Bit binary representation of the number. For example,

.. code-block:: console

    Cryptography is cool!

is coded as

.. code-block:: console

    01000011 01110010 01111001 01110000 01110100 01101111 01100111 01110010
    01100001 01110000 01101000 01111001 00100000 01101001 01110011 00100000
    01100011 01101111 01101111 01101100 00100001

1-26 -> A-Z
-----------

Converts the 1-26 numeric coding back to A-Z. For example,

.. code-block:: console

    1 2 3 4 5 6 7 8

is coded as

.. code-block:: console

    ABCDEFGH

0-25 -> A-Z
-----------

Converts the 0-25 numeric coding back to A-Z. For example,

.. code-block:: console

    0 1 2 3 4 5 6 7

is coded as

.. code-block:: console

    ABCDEFGH

1-26 Binary -> A-Z
------------------

Converts the binary 1-26 numeric coding back to A-Z. For example,

.. code-block:: console

    1 10 11 100 101 110 111 1000

is coded as

.. code-block:: console

    ABCDEFGH

Note that this option also works if there are leading zeros in the input.

0-25 Binary -> A-Z
------------------

Converts the binary 0-25 numeric coding back to A-Z. For example,

.. code-block:: console

    0 1 10 11 100 101 110 111

is coded as

.. code-block:: console

    ABCDEFGH

Note that this option also works if there are leading zeros in the input.

ASCII -> Text
-------------

Converts the ASCII value coding back to text. It assumes that each number is between 0 and 255. For example,

.. code-block:: console

    67 114 121 112 116 111 103 114 97 112 104 121 32 105 115 32 99 111 111 108 33

is coded as

.. code-block:: console

    Cryptography is cool!

Note that this option also works if there are leading zeros in the input.


ASCII Binary -> Text
--------------------

Converts the binary ASCII value coding back to text. It assumes that each number is between 0 and 255. For example,

.. code-block:: console

    1000011 1110010 1111001 1110000 1110100 1101111 1100111 1110010
    1100001 1110000 1101000 1111001 100000 1101001 1110011 100000
    1100011 1101111 1101111 1101100 100001

is coded as

.. code-block:: console

    Cryptography is cool!

Note that this option also works if there are leading zeros in the input.

