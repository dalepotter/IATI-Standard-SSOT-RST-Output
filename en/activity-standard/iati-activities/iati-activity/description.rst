description
===========

``iati-activities/iati-activity/description``

This is the reference page for the XML element ``description``. 

.. index::
  single: description

Definition
~~~~~~~~~~


A longer, human-readable description containing a
meaningful description of the activity. May be repeated
for different languages.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/description/.type:

@type
  The type of description being provided. This is not
  required if only one general description of the activity
  is reported.


  This value must be of type xsd:string.


  This value must be on the :doc:`DescriptionType codelist </codelists/DescriptionType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``description`` of an ``iati-activity``.

| The ``@type`` attribute declares a valid code (*en*) from the *DescriptionType* codelist.

.. code-block:: xml

    <description type="1">
       <narrative>General activity description text.  Long description of the activity with no particular structure.</narrative>
    </description>

| The ``description`` element can be repeated in any ``iati-activity``.
| In this example, three different ``description`` are declared.
| Note - it is optional to include all ``DescriptionType``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--description starts-->
	:end-before: <!--description ends-->

Changelog
~~~~~~~~~
2.01
^^^^
| Freetext is no longer allowed with this element.  It should now be declared with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L102>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/description.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   description/narrative

