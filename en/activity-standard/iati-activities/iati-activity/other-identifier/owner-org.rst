owner-org
=========

``iati-activities/iati-activity/other-identifier/owner-org``

This is the reference page for the XML element ``owner-org``. 

.. index::
  single: owner-org

Definition
~~~~~~~~~~


Where applicable, the organisation that owns the other
identifier being reported. When used, then either
other-identifier/owner-org/\@ref or
other-identifier/owner-org/narrative/text() MUST be
present.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/other-identifier/owner-org/.ref:

@ref
  An organisation identifier. This is NOT MANDATORY
  but when used MUST contain a valid organisation
  identifier.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example ``owner-org`` of an ``other-identifier`` of an ``iati-activity``.

| An example organisation ``@ref`` of *AA-AAA-123456789* is declared.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--other-identifier starts-->
	:end-before: <!--other-identifier ends-->

Changelog
~~~~~~~~~

2.01
^^^^
| The ``owner-org`` element was added in version 2.01


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L520>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/other-identifier/owner-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   owner-org/narrative

