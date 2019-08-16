Manim packages
==============

Ubication
---------

All packages of this version are in::

    big_ol_pile_of_manim_imports.py


.. literalinclude:: ../big_ol_pile_of_manim_imports.py
    :linenos:


Tree
----

The files that we really need are:

* ``big_ol_pile_of_manim_imports.py``
* ``manim.py``
* ``stage_scenes.py``
* ``manimlib/``

The rest files we can delete it.

::

    .
    ├── big_ol_pile_of_manim_imports.py
    ├── manim.py
    ├── stage_scenes.py 
    ├── manimlib
    │   ├── animation
    │   │   ├── animation.py
    │   │   ├── composition.py
    │   │   ├── creation.py
    │   │   ├── indication.py
    │   │   ├── movement.py
    │   │   ├── numbers.py
    │   │   ├── rotation.py
    │   │   ├── specialized.py
    │   │   ├── transform.py
    │   │   └── update.py
    │   ├── camera
    │   │   ├── camera.py
    │   │   ├── mapping_camera.py
    │   │   ├── moving_camera.py
    │   │   ├── multi_camera.py
    │   │   └── three_d_camera.py
    │   ├── config.py
    │   ├── constants.py
    │   ├── container
    │   │   └── container.py
    │   ├── continual_animation
    │   │   ├── continual_animation.py
    │   │   ├── from_animation.py
    │   │   ├── numbers.py
    │   │   └── update.py
    │   ├── ctex_template.tex
    │   ├── extract_scene.py
    │   ├── files
    │   │   ├── Bubbles_speech.svg
    │   │   ├── Bubbles_thought.svg
    │   │   └── PiCreatures_plain.svg
    │   ├── for_3b1b_videos
    │   │   ├── common_scenes.py
    │   │   ├── pi_class.py
    │   │   ├── pi_creature_animations.py
    │   │   ├── pi_creature.py
    │   │   └── pi_creature_scene.py
    │   ├── media_dir.txt
    │   ├── mobject
    │   │   ├── coordinate_systems.py
    │   │   ├── frame.py
    │   │   ├── functions.py
    │   │   ├── geometry.py
    │   │   ├── matrix.py
    │   │   ├── mobject.py
    │   │   ├── number_line.py
    │   │   ├── numbers.py
    │   │   ├── probability.py
    │   │   ├── shape_matchers.py
    │   │   ├── svg
    │   │   │   ├── brace.py
    │   │   │   ├── drawings.py
    │   │   │   ├── svg_mobject.py
    │   │   │   └── tex_mobject.py
    │   │   ├── three_dimensions.py
    │   │   ├── three_d_shading_utils.py
    │   │   ├── three_d_utils.py
    │   │   ├── types
    │   │   │   ├── image_mobject.py
    │   │   │   ├── point_cloud_mobject.py
    │   │   │   └── vectorized_mobject.py
    │   │   ├── updater.py
    │   │   └── value_tracker.py
    │   ├── once_useful_constructs
    │   │   ├── arithmetic.py
    │   │   ├── combinatorics.py
    │   │   ├── complex_transformation_scene.py
    │   │   ├── counting.py
    │   │   ├── fractals.py
    │   │   ├── graph_theory.py
    │   │   ├── light.py
    │   │   ├── matrix_multiplication.py
    │   │   ├── NOTE.md
    │   │   └── region.py
    │   ├── scene
    │   │   ├── graph_scene.py
    │   │   ├── media_dir.txt
    │   │   ├── moving_camera_scene.py
    │   │   ├── reconfigurable_scene.py
    │   │   ├── sample_space_scene.py
    │   │   ├── scene_file_writer.py
    │   │   ├── scene_from_video.py
    │   │   ├── scene.py
    │   │   ├── three_d_scene.py
    │   │   ├── vector_space_scene.py
    │   │   └── zoomed_scene.py
    │   ├── stream_starter.py
    │   ├── tex_template.tex
    │   └── utils
    │       ├── bezier.py
    │       ├── color.py
    │       ├── config_ops.py
    │       ├── file_ops.py
    │       ├── images.py
    │       ├── iterables.py
    │       ├── paths.py
    │       ├── rate_functions.py
    │       ├── simple_functions.py
    │       ├── sounds.py
    │       ├── space_ops.py
    │       ├── strings.py
    │       └── tex_file_writing.py
    ├── README.md          # <- Don't needed
    ├── requirements.txt   # <- Don't needed
    ├── Dockerfile         # <- Don't needed
    ├── example_scenes.py  # <- Don't needed
    └── LICENSE            # <- Don't needed

You can delete ``README.md``, ``requirements.txt``, ``Dockerfile``, ``example_scenes.py`` and ``LICENSE``.

..