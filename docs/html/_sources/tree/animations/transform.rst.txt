Transformations
===============

Transform
***********************
.. autoclass:: manimlib.animation.transform.Transform
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/TransformExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class TransformExample(Scene):
      def construct(self):
          mobject = RegularPolygon(3).scale(2)
  
          self.add(mobject)
  
          for n in range(4,9):
              self.play(
                  Transform(
                      mobject,
                      RegularPolygon(n).scale(2)
                  )
              )
  
          self.wait(0.3)

Replacement Transform
***********************
.. autoclass:: manimlib.animation.transform.ReplacementTransform
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ReplacementTransformExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ReplacementTransformExample(Scene):
      def construct(self):
          polygons = [*[RegularPolygon(n).scale(2) for n in range(3,9)]]
  
          self.add(polygons[0])
  
          for i in range(len(polygons)-1):
              self.play(
                  ReplacementTransform(
                      polygons[i],
                      polygons[i+1]
                  )
              )
  
          self.wait(0.3)

Transform From Copy
***********************
.. autoclass:: manimlib.animation.transform.TransformFromCopy
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/TransformFromCopyExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class TransformFromCopyExample(Scene):
      def construct(self):
          mobject = RegularPolygon(3).scale(2)
  
          self.add(mobject)
  
          for n in range(4,9):
              self.play(
                  TransformFromCopy(
                      mobject,
                      RegularPolygon(n).scale(2)
                  )
              )
  
          self.wait(0.3)

Clockwise Transform
***********************
.. autoclass:: manimlib.animation.transform.ClockwiseTransform
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ClockwiseTransformExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ClockwiseTransformExample(Scene):
      def construct(self):
          polygons = VGroup(
          	*[RegularPolygon(n).scale(0.7) for n in range(3,9)]
          ).arrange_submobjects(RIGHT,buff=1)
  
          self.add(polygons[0])
  
          for i in range(len(polygons)-1):
              self.play(
                  ClockwiseTransform(
                      polygons[0],
                      polygons[i+1]
                  )
              )
  
          self.wait(0.3)

Counterclockwise Transform
**************************
.. autoclass:: manimlib.animation.transform.CounterclockwiseTransform
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/CounterclockwiseTransformExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class CounterclockwiseTransformExample(Scene):
      def construct(self):
          polygons = VGroup(
              *[RegularPolygon(n).scale(0.7) for n in range(3,9)]
          ).arrange_submobjects(RIGHT,buff=1)
  
          self.add(polygons[0])
  
          for i in range(len(polygons)-1):
              self.play(
                  CounterclockwiseTransform(
                      polygons[0],
                      polygons[i+1]
                  )
              )
  
          self.wait(0.3)

Move To Target
***********************
.. autoclass:: manimlib.animation.transform.MoveToTarget
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/MoveToTargetExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class MoveToTargetExample(Scene):
      def construct(self):
          mobject=Square()
          mobject.generate_target()
          VGroup(mobject,mobject.target)\
              .arrange_submobjects(RIGHT,buff=3)
  
          mobject.target.rotate(PI/4)\
                        .scale(2)\
                        .set_stroke(PURPLE,9)\
                        .set_fill(ORANGE,1)
  
          self.add(mobject)
          self.wait(0.3)
  
          self.play(MoveToTarget(mobject))
          self.wait(0.3)

Apply Method
***********************
.. autoclass:: manimlib.animation.transform.ApplyMethod
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ApplyMethodExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ApplyMethodExample(Scene):
      def construct(self):
          dot = Dot()
          text = TextMobject("Text")
  
          dot.next_to(text,LEFT)
  
          self.add(text,dot)
  
          self.play(ApplyMethod(text.scale,3,{"about_point":dot.get_center()}))
          #                                  --------------------------------
          #                                          Optional parameters
  
          self.wait(0.3)

Apply Pointwise Function
*************************
.. autoclass:: manimlib.animation.transform.ApplyPointwiseFunction
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ApplyPointwiseFunctionExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ApplyPointwiseFunctionExample(Scene):
      def construct(self):
          text = TextMobject("Text")
  
          self.add(text)
  
          def spread_out(p):
              p = p + 2*DOWN
              return (FRAME_X_RADIUS+FRAME_Y_RADIUS)*p/get_norm(p)
              #      -------------------------------
              #          See manimlib/constants.py
  
          self.play(
              ApplyPointwiseFunction(spread_out, text)
          )

Fade To Color
***********************
.. autoclass:: manimlib.animation.transform.FadeToColor
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/FadeToColorExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class FadeToColorExample(Scene):
      def construct(self):
          text = TextMobject("Text")\
                 .set_width(FRAME_WIDTH)
  
          colors=[RED,PURPLE,GOLD,TEAL]
  
          self.add(text)
  
          for color in colors:
              self.play(FadeToColor(text,color))
  
          self.wait(0.3)

Scale In Place
***********************
.. autoclass:: manimlib.animation.transform.ScaleInPlace
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ScaleInPlaceExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ScaleInPlaceExample(Scene):
      def construct(self):
          text = TextMobject("Text")\
                 .set_width(FRAME_WIDTH/2)
  
          scale_factors=[2,0.3,0.6,2]
  
          self.add(text)
  
          for scale_factor in scale_factors:
              self.play(ScaleInPlace(text,scale_factor))
  
          self.wait(0.3)

Restore
***********************
.. autoclass:: manimlib.animation.transform.Restore
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/RestoreExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class RestoreExample(Scene):
      def construct(self):
          text = TextMobject("Original")\
                 .set_width(FRAME_WIDTH/2)
  
          text.save_state()
  
          text_2 = TextMobject("Modified")\
                 .set_width(FRAME_WIDTH/1.5)\
                 .set_color(ORANGE)\
                 .to_corner(DL)
  
          self.add(text)
  
          self.play(Transform(text,text_2))
          self.play(
              text.shift,RIGHT,
              text.rotate,PI/4
              )
          self.play(Restore(text))
  
          self.wait(0.7)

Apply Function
***********************
.. autoclass:: manimlib.animation.transform.ApplyFunction
    :members:
.. raw:: html

    <video width="560" height="315" controls>
        <source src="../../_static/ApplyFunctionExample.mp4" type="video/mp4">
    </video>
.. code-block:: python

  class ApplyFunctionExample(Scene):
      def construct(self):
          text = TextMobject("Text")\
                 .to_corner(DL)
  
          self.add(text)
  
          def apply_function(mob):
              mob.scale(2)
              mob.to_corner(UR)
              mob.rotate(PI/4)
              mob.set_color(RED)
              return mob
  
          self.play(
              ApplyFunction(
                  apply_function,
                  text
              )
          )
  
          self.wait(0.3)

Complex Function
***********************
.. autoclass:: manimlib.animation.transform.ComplexFunction
    :members:

Cyclic Replace
***********************
.. autoclass:: manimlib.animation.transform.CyclicReplace
    :members:

Transform Animations
***********************
.. autoclass:: manimlib.animation.transform.TransformAnimations
    :members:

