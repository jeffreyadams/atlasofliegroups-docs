Basic Functions
===================

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`flex_add, flex_sub <flex>`
     - ``(vec,vec->vec)``
   * - :ref:`convolve`
     - ``(vec,vec->vec)``
   * - :ref:`stack_rows`
     - ``([vec]->mat)``
   * - :ref:`error`
     - ``(*,...->*)``
   * - :ref:`int_format`
     - ``(int->string)``
   * - :ref:`to_string`
     - ``(*,...->string)``
   * - :ref:`print`
     - ``(T->T)``
   * - :ref:`prints`
     - ``(*,...->)``
   * - :ref:`ascii`
     - ``(string->int)``
   * - :ref:`ascii2`
     - ``(int->string)``
   * - :ref:`null`
     - ``(int->vec)``
   * - :ref:`null2`
     - ``(int,int->mat)``


.. _flex:

flex
+++++

    ``flex_add`` and ``flex_sub`` are variants of ``+``, ``-`` adding/removing trailing 0's.

.. _convolve:

convolve
+++++++++

    ``convolve`` produce convolution product of vectors, removing trailing 0's.

.. _stack_rows:

stack_rows
++++++++++++

    ``stack_rows`` combine ragged rows into matrix, zero-extend shorts.

.. _error:

error
+++++++

    ``error`` print values and abort computation; report a runtime error.

.. _int_format:

int_format
++++++++++++

    ``(int->string)``: representation of integer as digit string.

.. _to_string:

to_string
++++++++++

    ``(*,...->string)``: string representation of arguments (concatenated).

.. _print:

print
+++++++

    ``(T->T)``: print value, followed by newline; return same value.

.. _prints:

prints
++++++++

    ``(*,...->)``: print values raw (no quotes or commas) followed by newline.

.. _ascii:

ascii
++++++

    ``(string->int)``: ASCII code of initial character, or -1 if string empty

.. _ascii2:

ascii
+++++++

    ``(int->string)``: string of length 1 with given ASCII code (if safe value).

.. _null:

null
+++++

    ``(int->vec)``: null vector of given length.

.. _null2:

null
+++++

    ``(int,int->mat)``: null matrix with given number of rows and columns.