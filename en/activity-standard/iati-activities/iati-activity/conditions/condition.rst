condition
=========

``iati-activities/iati-activity/conditions/condition``

This is the reference page for the XML element ``condition``. See also the relevant overview pages: :doc:`/activity-standard/overview/conditions`,  :doc:`/activity-standard/overview/conditions` 

.. index::
  single: condition

Definition
~~~~~~~~~~


The text of a specific condition attached to the activity. Organisation-wide terms and conditions that apply to all activities should not be reported here, but in either iati-organisation/document-link or iati-activity-document-link


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/conditions/condition/.type:

@type
  An IATI code defining the type of condition.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ConditionType codelist </codelists/ConditionType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``condition`` child element of ``conditions`` of an ``iati-activity``.

| The ``@type`` attribute declares a valid code (*1*) from the *ConditionType* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--conditions starts-->
	:end-before: <!--conditions ends-->

| The ``condition`` element can be repeated in any ``conditions`` of an ``iati-activity``.

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.

1.04
^^^^
| It was always the intention of the standard that a condition could be specified in different languages but the schema has never allowed it.
| This has now been fixed.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1955>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/conditions/condition.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   condition/narrative

