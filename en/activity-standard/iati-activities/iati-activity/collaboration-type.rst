collaboration-type
==================

``iati-activities/iati-activity/collaboration-type``

This is the reference page for the XML element ``collaboration-type``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: collaboration-type

Definition
~~~~~~~~~~


The type of collaboration involved in the activity's
disbursements, e.g. "bilateral" or "multilateral".


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/collaboration-type/.code:

@code
  A code from the OECD DAC CRS "Bi_Multi" codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`CollaborationType codelist </codelists/CollaborationType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``collaboration-type``  for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *CollaborationType* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--collaboration-type starts-->
	:end-before: <!--collaboration-type ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L430>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/collaboration-type.rst>`_

