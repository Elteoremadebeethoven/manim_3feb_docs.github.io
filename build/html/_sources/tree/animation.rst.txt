Animations
==========

.. autoclass:: manimlib.animation.animation.Animation

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   animations/creation.rst
   animations/indication.rst
   animations/transform.rst
   animations/movement.rst

Rate functions
--------------

See

::

    manimlib/utils/rate_functions.py

.. literalinclude:: ../manimlib/utils/rate_functions.py
    :lines: 7-77

Submobject modes
----------------

::

    "lagged_start"
    "smoothed_lagged_start"
    "one_at_a_time"
    "all_at_once"

See ``get_sub_alpha`` from:

::

    manimlib/animation/animation.py

.. literalinclude:: ../manimlib/animation/animation.py
    :lines: 94-107
    :lineno-start: 107

Tree
----

::

    .
    ├── AnimationGroup
    │   ├── AnimationOnSurroundingRectangle
    │   │   ├── ShowCreationThenDestructionAround
    │   │   ├── ShowCreationThenFadeAround
    │   │   └── ShowPassingFlashAround
    │   └── Flash
    ├── ApplyToCenters
    ├── ChangingDecimal
    │   └── ChangeDecimalToValue
    ├── DrawBorderThenFill
    │   └── Write
    ├── EmptyAnimation
    ├── Homotopy
    │   ├── ApplyWave
    │   ├── ComplexHomotopy
    │   └── SmoothedVectorizedHomotopy
    ├── LaggedStart
    ├── MaintainPositionRelativeTo
    ├── MoveAlongPath
    ├── PhaseFlow
    ├── Rotating
    ├── ShowIncreasingSubsets
    ├── ShowPartial
    │   ├── ShowCreation
    │   │   └── Uncreate
    │   └── ShowPassingFlash
    │       └── ShowCreationThenDestruction
    ├── Succession
    │   └── ShowCreationThenFadeOut
    ├── Transform
    │   ├── FadeIn
    │   ├── FadeInAndShiftFromDirection
    │   │   └── FadeInFromDown
    │   ├── FadeInFromLarge
    │   ├── FadeOut
    │   │   └── FadeOutAndShift
    │   │       └── FadeOutAndShiftDown
    │   ├── FocusOn
    │   ├── GrowFromPoint
    │   │   ├── GrowArrow
    │   │   ├── GrowFromCenter
    │   │   │   └── SpinInFromNothing
    │   │   └── GrowFromEdge
    │   ├── Indicate
    │   │   └── CircleIndicate
    │   ├── Rotate
    │   ├── ShrinkToCenter
    │   └── TurnInsideOut
    ├── UpdateFromAlphaFunc
    ├── UpdateFromFunc
    ├── VFadeIn
    ├── Vibrate
    └── WiggleOutThenIn
