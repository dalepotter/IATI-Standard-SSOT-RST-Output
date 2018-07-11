period-end
==========

``iati-activities/iati-activity/planned-disbursement/period-end``

This is the reference page for the XML element ``period-end``. 

.. index::
  single: period-end

Definition
~~~~~~~~~~


The ending date for the period in which this specific disbursement will be made.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/planned-disbursement/period-end/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2073>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/planned-disbursement/period-end.rst>`_

