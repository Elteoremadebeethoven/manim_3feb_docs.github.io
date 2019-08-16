TeX and Text
============

There are two commands to create text, ``TexMobject`` and ``TextMobject``. In both parameters the text is written in TeX format, but while in ``TextMobject`` you write in normal mode, in ``TexMobject`` you are writing within the ``align*`` environment.


The LaTeX packages that Manim uses are in:
::

    manimlib/tex_template.tex

..

They are the following by default:

.. literalinclude:: ../../manimlib/tex_template.tex
    :lines: 3-18

TexMobject
----------

.. autoclass:: manimlib.mobject.svg.tex_mobject.TexMobject
.. automethod:: manimlib.mobject.svg.tex_mobject.TexMobject.get_tex_string
.. automethod:: manimlib.mobject.svg.tex_mobject.TexMobject.set_color_by_tex

..

TextMobject
-----------

.. autoclass:: manimlib.mobject.svg.tex_mobject.TextMobject
.. automethod:: manimlib.mobject.svg.tex_mobject.TextMobject.get_tex_string
.. automethod:: manimlib.mobject.svg.tex_mobject.TextMobject.set_color_by_tex
