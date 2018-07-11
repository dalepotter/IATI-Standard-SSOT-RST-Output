activity-scope
==============

``iati-activities/iati-activity/activity-scope``

This is the reference page for the XML element ``activity-scope``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: activity-scope

Definition
~~~~~~~~~~


The geographical scope of the activity: regional, national,
sub-national, etc.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/activity-scope/.code:

@code
  The geographical scope. See IATI codelist for values.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ActivityScope codelist </codelists/ActivityScope>`.



  



Example Usage
~~~~~~~~~~~~~
Example of an ``activity-scope`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*3*) from the *ActivityScope* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--activity-scope starts-->
	:end-before: <!--activity-scope ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.

1.03
^^^^
This is a new element, introduced in version 1.03 of the standard

1.02
^^^^
This element did not exist

1.01
^^^^
This element did not exist


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L302>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/activity-scope.rst>`_

