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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L102>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/description.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   description/narrative

