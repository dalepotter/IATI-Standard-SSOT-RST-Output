activity-date
=============

``iati-activities/iati-activity/activity-date``

This is the reference page for the XML element ``activity-date``. See also the relevant overview page: :doc:`/activity-standard/overview/dates` 

.. index::
  single: activity-date

Definition
~~~~~~~~~~


The planned and actual start and completion dates of the
activity. Start dates may reflect either the commencement of
funding, planning or physical activity. End dates should,
wherever possible, reflect the ending of physical activity.

The narrative content may contain text (e.g. 2011Q1) for
accurately recording less specific dates such as month,
quarter, or year.


Rules
~~~~~








This element must occur at least once (within each parent element).







``activity-date[@type='1' or @type='2']`` must be present.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/activity-date/.type:

@type
  An IATI code defining the type of activity date being reported.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ActivityDateType codelist </codelists/ActivityDateType>`.



  
.. _iati-activities/iati-activity/activity-date/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``activity-date[@type='1']/@iso-date`` must be before or the same as ``activity-date[@type='3']/@iso-date``

  ``activity-date[@type='2']/@iso-date`` must be before or the same as ``activity-date[@type='4']/@iso-date``

  ``activity-date[@type='2']/@iso-date`` must not be in the future.

  ``activity-date[@type='4']/@iso-date`` must not be in the future.



Example Usage
~~~~~~~~~~~~~
Example ``activity-date`` for an``iati-activity``.

| The ``@type`` attribute declares a valid code (*1*) from the *ActivityDateType* codelist.

| An example date is declared in the ``@iso-date`` attribute.
| Example date format conforms to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. code-block:: xml

	<activity-date iso-date="2012-04-28" type="1" />

| The ``activity-date`` element can be repeated in any ``iati-activity``.
| In this example four ``activity-date`` are declared.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--activity-date starts-->
	:end-before: <!--activity-date ends-->

Note: In some cases, not all *ActivityDateType* codes can be declared, depending on the ``activity-status`` of the ``iati-activity``

| Note: All instances of the *ActivityDateType* code *2* & *4* (actual dates) are not expected to be in the *future*.

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.

| The ``ActivityDateType`` codelist was changed to numeric codes




Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L632>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/activity-date.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   activity-date/narrative

