Constants
=========

Directories
-----------

When you run an animation for first time you can see this message::

    Media will be stored in media/. You can change this behavior by writing a different directory to media_dir.txt.

That is because the animation file has been saved in a directory called ``media``, in the manim directory, then you have a new directory and two new files:

::

    .
    ├── big_ol_pile_of_manim_imports.py
    ├── manim.py
    ├── stage_scenes.py 
    ├── media              # <- New directory
    ├── media_dir.txt      # <- New file
    └── manimlib
        └── media_dir.txt  # <- New file

You should have not to see that message again, but, in case that you see it again, then you can change the content of the ``media_dir.txt`` files with ``/`` and change the line 14 of ``manimlib/constants.py``:

.. literalinclude:: ../manimlib/constants.py
    :lines: 4-23
    :lineno-start: 4
    :emphasize-lines: 11

with:

.. code-block:: python
    :lineno-start: 14

            "/"

If you want to learn how change the ``media`` directory see:

.. raw:: html

    <iframe width="560" height="315" src="http://www.youtube.com/embed/I9rHHiKqTWY?rel=0" frameborder="0" allowfullscreen></iframe>

Resolution
----------

.. literalinclude:: ../manimlib/constants.py
    :lines: 86-108
    :lineno-start: 86

Frame dimensions
----------------

.. literalinclude:: ../manimlib/constants.py
    :lines: 110-122
    :lineno-start: 110

Buffs
-----

.. literalinclude:: ../manimlib/constants.py
    :lines: 124-130
    :lineno-start: 124

Vectors
-------

.. literalinclude:: ../manimlib/constants.py
    :lines: 139-159
    :lineno-start: 139

Color palette
-------------

.. raw:: html

    <a href="../_static/colors/colors.html"> Check this page </a> to see the color palette.

.. note::
    
    ``COLOR = COLOR_C``

.. literalinclude:: ../manimlib/constants.py
    :lines: 168-228
    :lineno-start: 168

..