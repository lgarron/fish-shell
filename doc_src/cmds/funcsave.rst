.. _cmd-funcsave:

funcsave - save the definition of a function to the user's autoload directory
=============================================================================

Synopsis
--------

::

    funcsave FUNCTION_NAME
    funcsave [-q] [(-d | --directory) DIR ] FUNCTION_NAME


Description
-----------

``funcsave`` saves a function to a file in the fish configuration directory. This function will be :ref:`automatically loaded <syntax-function-autoloading>` by current and future fish sessions. This can be useful to commit functions created interactively for permanent use.

Because fish loads functions on-demand, saved functions cannot serve as :ref:`event handlers <event>` until they are run or otherwise sourced. To activate an event handler for every new shell, add the function to the :ref:`configuration file <configuration>` instead of using ``funcsave``.

This is often used after :ref:`funced <cmd-funced>`, which opens the function in ``$EDITOR`` or ``$VISUAL`` and loads it into the current session afterwards.
