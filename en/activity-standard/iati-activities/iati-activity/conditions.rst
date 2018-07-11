conditions
==========

``iati-activities/iati-activity/conditions``

This is the reference page for the XML element ``conditions``. See also the relevant overview page: :doc:`/activity-standard/overview/conditions` 

.. index::
  single: conditions

Definition
~~~~~~~~~~


Specific terms and conditions attached to the activity that, if not met, may influence the delivery of commitments made by participating organisations.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/conditions/.attached:

@attached
  A yes/no (1/0) value stating whether there are conditions attached to the activity. It is strongly recommended that this attribute is reported, even if there are no conditions attached (i.e. attached="0")

  This attribute is required.



  This value must be of type xsd:boolean.



  



Example Usage
~~~~~~~~~~~~~
Example ``conditions`` for an ``iati-activity``.

| This element is a parent for ``condition`` child element(s).

| The ``@attached`` *0* boolean is included, for illustration of no conditions.

.. code-block:: xml

     <conditions attached="0"/>

| The ``@attached`` *1* boolean is included, for illustration of conditions.

.. code-block:: xml

     <conditions attached="1">
     ...
     </conditions>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--conditions starts-->
	:end-before: <!--conditions ends-->



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1947>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/conditions.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   conditions/condition

