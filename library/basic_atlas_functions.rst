

Built-In **atlas** Functions
==============================

Built-in functions are those functions that are available before you load any ``.at`` files.

Basic Functions
------------------

.. list-table::
   :widths: 10 20
   :header-rows: 1
   
   * - Function
     - Argument(s) -> Result(s)
   * - :ref:`flex_add, flex_sub <flex>`
     - ``(vec,vec->vec)``
   * - :ref:`convolve`
     - ``(vec,vec->vec)``


.. _flex:

flex
+++++

``flex_add`` and ``flex_sub`` are variants of ``+``, ``-`` adding/removing trailing 0's.

.. _convolve:

convolve
+++++++++

``convolve`` produce convolution product of vectors, removing trailing 0's.

.. raw:: html

    <div data-role="main" class="ui-content">
      <div data-role="collapsible">
        <h1>Click me - I'm collapsible!</h1>
        <p>I'm the expanded content.</p>
      </div>
    </div>