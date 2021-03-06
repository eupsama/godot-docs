.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the CollisionObject2D.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_CollisionObject2D:

CollisionObject2D
=================

**Inherits:** :ref:`Node2D<class_node2d>` **<** :ref:`CanvasItem<class_canvasitem>` **<** :ref:`Node<class_node>` **<** :ref:`Object<class_object>`

**Inherited By:** :ref:`Area2D<class_area2d>`, :ref:`PhysicsBody2D<class_physicsbody2d>`

**Category:** Core

Brief Description
-----------------

Base node for 2D collision objects.

Member Functions
----------------

+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`_input_event<class_CollisionObject2D__input_event>` **(** :ref:`Object<class_object>` viewport, :ref:`InputEvent<class_inputevent>` event, :ref:`int<class_int>` shape_idx **)** virtual |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                  | :ref:`create_shape_owner<class_CollisionObject2D_create_shape_owner>` **(** :ref:`Object<class_object>` owner **)**                                                                            |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`RID<class_rid>`                  | :ref:`get_rid<class_CollisionObject2D_get_rid>` **(** **)** const                                                                                                                              |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_array>`              | :ref:`get_shape_owners<class_CollisionObject2D_get_shape_owners>` **(** **)**                                                                                                                  |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                | :ref:`is_shape_owner_disabled<class_CollisionObject2D_is_shape_owner_disabled>` **(** :ref:`int<class_int>` owner_id **)** const                                                               |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                | :ref:`is_shape_owner_one_way_collision_enabled<class_CollisionObject2D_is_shape_owner_one_way_collision_enabled>` **(** :ref:`int<class_int>` owner_id **)** const                             |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`remove_shape_owner<class_CollisionObject2D_remove_shape_owner>` **(** :ref:`int<class_int>` owner_id **)**                                                                               |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                  | :ref:`shape_find_owner<class_CollisionObject2D_shape_find_owner>` **(** :ref:`int<class_int>` shape_index **)** const                                                                          |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_add_shape<class_CollisionObject2D_shape_owner_add_shape>` **(** :ref:`int<class_int>` owner_id, :ref:`Shape2D<class_shape2d>` shape **)**                                    |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_clear_shapes<class_CollisionObject2D_shape_owner_clear_shapes>` **(** :ref:`int<class_int>` owner_id **)**                                                                   |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Object<class_object>`            | :ref:`shape_owner_get_owner<class_CollisionObject2D_shape_owner_get_owner>` **(** :ref:`int<class_int>` owner_id **)** const                                                                   |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Shape2D<class_shape2d>`          | :ref:`shape_owner_get_shape<class_CollisionObject2D_shape_owner_get_shape>` **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)** const                                   |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                  | :ref:`shape_owner_get_shape_count<class_CollisionObject2D_shape_owner_get_shape_count>` **(** :ref:`int<class_int>` owner_id **)** const                                                       |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                  | :ref:`shape_owner_get_shape_index<class_CollisionObject2D_shape_owner_get_shape_index>` **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)** const                       |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Transform2D<class_transform2d>`  | :ref:`shape_owner_get_transform<class_CollisionObject2D_shape_owner_get_transform>` **(** :ref:`int<class_int>` owner_id **)** const                                                           |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_remove_shape<class_CollisionObject2D_shape_owner_remove_shape>` **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)**                                   |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_set_disabled<class_CollisionObject2D_shape_owner_set_disabled>` **(** :ref:`int<class_int>` owner_id, :ref:`bool<class_bool>` disabled **)**                                 |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_set_one_way_collision<class_CollisionObject2D_shape_owner_set_one_way_collision>` **(** :ref:`int<class_int>` owner_id, :ref:`bool<class_bool>` enable **)**                 |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                   | :ref:`shape_owner_set_transform<class_CollisionObject2D_shape_owner_set_transform>` **(** :ref:`int<class_int>` owner_id, :ref:`Transform2D<class_transform2d>` transform **)**                |
+----------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Signals
-------

.. _class_CollisionObject2D_input_event:

- **input_event** **(** :ref:`Object<class_object>` viewport, :ref:`Object<class_object>` event, :ref:`int<class_int>` shape_idx **)**

Emitted when an input event occurs and ``input_pickable`` is ``true``. See :ref:`_input_event<class_CollisionObject2D__input_event>` for details.

.. _class_CollisionObject2D_mouse_entered:

- **mouse_entered** **(** **)**

Emitted when the mouse pointer enters any of this object's shapes.

.. _class_CollisionObject2D_mouse_exited:

- **mouse_exited** **(** **)**

Emitted when the mouse pointer exits all this object's shapes.


Member Variables
----------------

  .. _class_CollisionObject2D_input_pickable:

- :ref:`bool<class_bool>` **input_pickable** - If ``true`` this object is pickable. A pickable object can detect the mouse pointer entering/leaving, and if the mouse is inside it, report input events.


Description
-----------

CollisionObject2D is the base class for 2D physics objects. It can hold any number of 2D collision :ref:`Shape2D<class_shape2d>`\ s. Each shape must be assigned to a *shape owner*. The CollisionObject2D can have any number of shape owners. Shape owners are not nodes and do not appear in the editor, but are accessible through code using the ``shape_owner_*`` methods.

Member Function Description
---------------------------

.. _class_CollisionObject2D__input_event:

- void **_input_event** **(** :ref:`Object<class_object>` viewport, :ref:`InputEvent<class_inputevent>` event, :ref:`int<class_int>` shape_idx **)** virtual

Accepts unhandled :ref:`InputEvent<class_inputevent>`\ s. ``shape_idx`` is the child index of the clicked :ref:`Shape2D<class_shape2d>`. Connect to the ``input_event`` signal to easily pick up these events.

.. _class_CollisionObject2D_create_shape_owner:

- :ref:`int<class_int>` **create_shape_owner** **(** :ref:`Object<class_object>` owner **)**

Creates a new shape owner for the given object. Returns ``owner_id`` of the new owner for future reference.

.. _class_CollisionObject2D_get_rid:

- :ref:`RID<class_rid>` **get_rid** **(** **)** const

Returns the object's :ref:`RID<class_rid>`.

.. _class_CollisionObject2D_get_shape_owners:

- :ref:`Array<class_array>` **get_shape_owners** **(** **)**

Returns an :ref:`Array<class_array>` of ``owner_id`` identifiers. You can use these ids in other methods that take ``owner_id`` as an argument.

.. _class_CollisionObject2D_is_shape_owner_disabled:

- :ref:`bool<class_bool>` **is_shape_owner_disabled** **(** :ref:`int<class_int>` owner_id **)** const

If ``true`` the shape owner and its shapes are disabled.

.. _class_CollisionObject2D_is_shape_owner_one_way_collision_enabled:

- :ref:`bool<class_bool>` **is_shape_owner_one_way_collision_enabled** **(** :ref:`int<class_int>` owner_id **)** const

Returns ``true`` if collisions for the shape owner originating from this ``CollisionObject2D`` will not be reported to collided with ``CollisionObject2D``\ s.

.. _class_CollisionObject2D_remove_shape_owner:

- void **remove_shape_owner** **(** :ref:`int<class_int>` owner_id **)**

Removes the given shape owner.

.. _class_CollisionObject2D_shape_find_owner:

- :ref:`int<class_int>` **shape_find_owner** **(** :ref:`int<class_int>` shape_index **)** const

Returns the ``owner_id`` of the given shape.

.. _class_CollisionObject2D_shape_owner_add_shape:

- void **shape_owner_add_shape** **(** :ref:`int<class_int>` owner_id, :ref:`Shape2D<class_shape2d>` shape **)**

Adds a :ref:`Shape2D<class_shape2d>` to the shape owner.

.. _class_CollisionObject2D_shape_owner_clear_shapes:

- void **shape_owner_clear_shapes** **(** :ref:`int<class_int>` owner_id **)**

Removes all shapes from the shape owner.

.. _class_CollisionObject2D_shape_owner_get_owner:

- :ref:`Object<class_object>` **shape_owner_get_owner** **(** :ref:`int<class_int>` owner_id **)** const

Returns the parent object of the given shape owner.

.. _class_CollisionObject2D_shape_owner_get_shape:

- :ref:`Shape2D<class_shape2d>` **shape_owner_get_shape** **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)** const

Returns the :ref:`Shape2D<class_shape2d>` with the given id from the given shape owner.

.. _class_CollisionObject2D_shape_owner_get_shape_count:

- :ref:`int<class_int>` **shape_owner_get_shape_count** **(** :ref:`int<class_int>` owner_id **)** const

Returns the number of shapes the given shape owner contains.

.. _class_CollisionObject2D_shape_owner_get_shape_index:

- :ref:`int<class_int>` **shape_owner_get_shape_index** **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)** const

Returns the child index of the :ref:`Shape2D<class_shape2d>` with the given id from the given shape owner.

.. _class_CollisionObject2D_shape_owner_get_transform:

- :ref:`Transform2D<class_transform2d>` **shape_owner_get_transform** **(** :ref:`int<class_int>` owner_id **)** const

Returns the shape owner's :ref:`Transform2D<class_transform2d>`.

.. _class_CollisionObject2D_shape_owner_remove_shape:

- void **shape_owner_remove_shape** **(** :ref:`int<class_int>` owner_id, :ref:`int<class_int>` shape_id **)**

Removes a shape from the given shape owner.

.. _class_CollisionObject2D_shape_owner_set_disabled:

- void **shape_owner_set_disabled** **(** :ref:`int<class_int>` owner_id, :ref:`bool<class_bool>` disabled **)**

If ``true`` disables the given shape owner.

.. _class_CollisionObject2D_shape_owner_set_one_way_collision:

- void **shape_owner_set_one_way_collision** **(** :ref:`int<class_int>` owner_id, :ref:`bool<class_bool>` enable **)**

If ``enable`` is ``true``, collisions for the shape owner originating from this ``CollisionObject2D`` will not be reported to collided with ``CollisionObject2D``\ s.

.. _class_CollisionObject2D_shape_owner_set_transform:

- void **shape_owner_set_transform** **(** :ref:`int<class_int>` owner_id, :ref:`Transform2D<class_transform2d>` transform **)**

Sets the :ref:`Transform2D<class_transform2d>` of the given shape owner.


