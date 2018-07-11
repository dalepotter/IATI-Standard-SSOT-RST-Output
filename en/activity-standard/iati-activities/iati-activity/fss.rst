fss
===

``iati-activities/iati-activity/fss``

This is the reference page for the XML element ``fss``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: fss

Definition
~~~~~~~~~~


This section allows entry of data required for the OECD DAC Forward Spending Survey at an activity level.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/fss/.extraction-date:

@extraction-date
  The exact date when the information was collected or extracted from donors' aid management systems.

  This attribute is required.



  This value must be of type xsd:date.



  
.. _iati-activities/iati-activity/fss/.priority:

@priority
  True if the partner country is a priority partner country.


  This value must be of type xsd:boolean.



  
.. _iati-activities/iati-activity/fss/.phaseout-year:

@phaseout-year
  If there are plans to phase out operations from the partner country, this column shows the projected year of last disbursements.


  This value must be of type xsd:decimal.



  



Example Usage
~~~~~~~~~~~~~
Example of ``fss`` of an ``iati-activity``.

| An example date is declared in the ``@extraction-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

| This example declares the attribute ``@phaseout-year`` as *2016*.
| A ``@priority`` boolean *1* declares that this is a partner country priority.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--fss starts-->
	:end-before: <!--fss ends-->


Changelog
~~~~~~~~~

1.03
^^^^

| New in 1.03
| Added the optional ``fss`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2405>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/fss.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   fss/forecast

