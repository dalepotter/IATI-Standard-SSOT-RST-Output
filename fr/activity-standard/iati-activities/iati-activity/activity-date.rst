activity-date
=============

``iati-activities/iati-activity/activity-date``

This is the reference page for the XML element ``activity-date``. 

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





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L632>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/activity-date.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   activity-date/narrative

