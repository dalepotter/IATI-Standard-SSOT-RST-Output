activity-status
===============

``iati-activities/iati-activity/activity-status``

This is the reference page for the XML element ``activity-status``. See also the relevant overview page: :doc:`/activity-standard/overview/dates` 

.. index::
  single: activity-status

Definition
~~~~~~~~~~


The current status of the activity. See codelist for values.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/activity-status/.code:

@code
  An IATI code defining the current status of the activity.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ActivityStatus codelist </codelists/ActivityStatus>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``activity-status`` of an ``iati-activity``

| The ``@code`` attribute declares a valid code (*2*) from the *ActivityStatus* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--activity-status starts-->
	:end-before: <!--activity-status ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L662>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/activity-status.rst>`_

