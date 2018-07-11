iati-identifier
===============

``iati-activities/iati-activity/iati-identifier``

This is the reference page for the XML element ``iati-identifier``. See also the relevant overview page: :doc:`/activity-standard/overview/iati-identifier` 

.. index::
  single: iati-identifier

Definition
~~~~~~~~~~


A globally unique identifier for the activity.

This MUST be prefixed with EITHER the current IATI
organisation identifier for the reporting organisation
(reporting-org/\@ref) OR a previous identifier reported in
other-identifier, and suffixed with the organisation’s own
activity identifier. The prefix and the suffix should be
separated by a hyphen "-".

Once an activity has been reported to IATI its identifier MUST
NOT be changed in subsequent updates.


Rules
~~~~~

The text in this element must be of type xsd:string.








This element must occur once and only once (within each parent element).







``iati-identifier`` should match the regex ``[^\/\&\|\?]+``





Example Usage
~~~~~~~~~~~~~
Example ``iati-identifier`` of an ``iati-activity``.

| Example uses a concatenation of the ``reporting-org`` identifier *AA-AAA-123456789* and the internal activity identifier *ABC123*.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-identifier starts-->
	:end-before: <!--iati-identifier ends-->


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L225>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/iati-identifier.rst>`_

