Utilities
-------------------------

.. currentmodule:: scm.plams.tools.utils

Presented here is a small set of useful utility tools that can come handy in various contexts in your scripts. They are simple, standalone objects always present in the main namespace.

What is characteristic for objects described below is that they are meant to be used in a bit different way than all other PLAMS classes. Usually one takes a class (like |DiracJob|), creates an instance of it (``myjob = DiracJob(...)``) and executes some of its methods (``r = myjob.run()``). In contrast, utility classes are designed in a way similar to so called singleton design pattern. That means it is not possible to create any instances of these classes. The class itself serves for "one and only instance" and all methods should be called using the class as the calling object::

    >>> x = PeriodicTable()
    PTError: Instances of PeriodicTable cannot be created
    >>> s = PeriodicTable.get_symbol(20)
    >>> print(s)
    20

Periodic Table
~~~~~~~~~~~~~~~~~~~~~~~~~

.. autoclass:: PeriodicTable
    :exclude-members: __weakref__

Units
~~~~~~~~~~~~~~~~~~~~~~~~~

.. autoclass:: Units
    :exclude-members: __weakref__
