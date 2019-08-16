Creation
========

Draw
----

Show Partial
***************
.. autoclass:: manimlib.animation.creation.ShowPartial
    :members:

Show Creation
***************
.. autoclass:: manimlib.animation.creation.ShowCreation
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ShowCreationExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ShowCreationExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[ShowCreation(mob) for mob in mobjects]
          )
  
          self.wait()

Uncreate
*********
.. autoclass:: manimlib.animation.creation.Uncreate
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/UncreateExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class UncreateExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.add(mobjects)
  
          self.wait(0.3)
  
          self.play(
              *[Uncreate(mob) for mob in mobjects]
          )
  
          self.wait()

Draw Border Then Fill
**********************
.. autoclass:: manimlib.animation.creation.DrawBorderThenFill
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/DrawBorderThenFillExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class DrawBorderThenFillExample(Scene):
      def construct(self):
          vmobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          vmobjects.scale(1.5)
          vmobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[DrawBorderThenFill(mob) for mob in vmobjects]
          )
  
          self.wait()

Write
*****************
.. autoclass:: manimlib.animation.creation.Write
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/WriteExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class WriteExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[Write(mob) for mob in mobjects]
          )
  
          self.wait()

Fade
----

Fade Out
*****************
.. autoclass:: manimlib.animation.creation.FadeOut
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeOutExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeOutExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.add(mobjects)
          self.wait(0.3)
  
          self.play(
              *[FadeOut(mob) for mob in mobjects]
          )
  
          self.wait()

Fade In
*****************
.. autoclass:: manimlib.animation.creation.FadeIn
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeInExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeInExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[FadeIn(mob) for mob in mobjects]
          )
  
          self.wait()

Fade In From
***************************
.. autoclass:: manimlib.animation.creation.FadeInFrom
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeInFromExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeInFromExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          directions=[UP,LEFT,DOWN,RIGHT]
  
          for direction in directions:
              self.play(
                  *[FadeInFrom(mob,direction) for mob in mobjects]
              )
  
          self.wait()

Fade In From Down
*****************
.. autoclass:: manimlib.animation.creation.FadeInFromDown
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeInFromDownExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeInFromDownExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[FadeInFromDown(mob) for mob in mobjects]
          )
  
          self.wait()

Fade Out And Shift
**********************
.. autoclass:: manimlib.animation.creation.FadeOutAndShift
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeOutAndShiftExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeOutAndShiftExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          directions=[UP,LEFT,DOWN,RIGHT]
  
          self.add(mobjects)
          self.wait(0.3)
  
          for direction in directions:
              self.play(
                  *[FadeOutAndShift(mob,direction) for mob in mobjects]
              )
  
          self.wait()

Fade Out And Shift Down
****************************
.. autoclass:: manimlib.animation.creation.FadeOutAndShiftDown
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeOutAndShiftDownExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeOutAndShiftDownExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[FadeOutAndShiftDown(mob) for mob in mobjects]
          )
  
          self.wait()

Fade In From Large
*********************
.. autoclass:: manimlib.animation.creation.FadeInFromLarge
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeInFromLargeExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeInFromLargeExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          scale_factors=[0.3,0.8,1,1.3,1.8]
  
          for scale_factor in scale_factors:
              t_scale_factor = TextMobject(f"\\tt scale\\_factor = {scale_factor}")
              t_scale_factor.to_edge(UP)
  
              self.add(t_scale_factor)
  
              self.play(
                  *[FadeInFromLarge(mob,scale_factor) for mob in mobjects]
              )
  
              self.remove(t_scale_factor)
  
          self.wait(0.3)

VFade In
*****************
.. autoclass:: manimlib.animation.creation.VFadeIn
    :members:

VFade Out
*****************
.. autoclass:: manimlib.animation.creation.VFadeOut
    :members:

Grow
----

Grow From Point
********************
.. autoclass:: manimlib.animation.creation.GrowFromPoint
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/GrowFromPointExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class GrowFromPointExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          directions=[UP,LEFT,DOWN,RIGHT]
  
          for direction in directions:
              self.play(
                  *[GrowFromPoint(mob,mob.get_center()+direction*3) for mob in mobjects]
              )
  
          self.wait()

Grow From Center
*****************
.. autoclass:: manimlib.animation.creation.GrowFromCenter
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/GrowFromCenterExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class GrowFromCenterExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[GrowFromCenter(mob) for mob in mobjects]
          )
  
          self.wait()

Grow From Edge
*****************
.. autoclass:: manimlib.animation.creation.GrowFromEdge
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/GrowFromEdgeExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class GrowFromEdgeExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Circle(),
                  Circle(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          directions=[UP,LEFT,DOWN,RIGHT]
  
          for direction in directions:
              self.play(
                  *[GrowFromEdge(mob,direction) for mob in mobjects]
              )
  
          self.wait()

Grow Arrow
***************
.. autoclass:: manimlib.animation.creation.GrowArrow
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/GrowArrowExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class GrowArrowExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Arrow(LEFT,RIGHT),
                  Vector(RIGHT*2)
              )
          mobjects.scale(3)
          mobjects.arrange_submobjects(DOWN,buff=2)
  
          self.play(
              *[GrowArrow(mob)for mob in mobjects]
          )
  
          self.wait()

Spin In From Nothing
***********************
.. autoclass:: manimlib.animation.creation.SpinInFromNothing
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/SpinInFromNothingExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class SpinInFromNothingExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Square(),
                  RegularPolygon(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[SpinInFromNothing(mob) for mob in mobjects]
          )
  
          self.wait()

Shrink To Center
*****************
.. autoclass:: manimlib.animation.creation.ShrinkToCenter
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ShrinkToCenterExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ShrinkToCenterExample(Scene):
      def construct(self):
          mobjects = VGroup(
                  Square(),
                  RegularPolygon(fill_opacity=1),
                  TextMobject("Text").scale(2)
              )
          mobjects.scale(1.5)
          mobjects.arrange_submobjects(RIGHT,buff=2)
  
          self.play(
              *[ShrinkToCenter(mob) for mob in mobjects]
          )
  
          self.wait()