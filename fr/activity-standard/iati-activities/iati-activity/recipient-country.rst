recipient-country
=================

``iati-activities/iati-activity/recipient-country``

This is the reference page for the XML element ``recipient-country``. 

.. index::
  single: recipient-country

Definition
~~~~~~~~~~


A country that will benefit from this activity. If a specific
country is not known the recipient-region element should be
used instead. For geographical location, use the location
element.

Multiple countries and regions can be reported, in which case
the percentage attribute MUST be used to specify the share of
total commitments across all reported countries and regions.

The country can also be specified at transaction rather than
activity level. If recipient-country OR recipient-region are
reported at the transaction level, ALL transactions MUST
contain a recipient-country or recipient-region element and
iati-activity/recipient-country
and iati-activity/recipient-region MUST NOT be used.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/recipient-country/.code:

@code
  ISO 3166-1 alpha-2 code for the country.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`Country codelist </codelists/Country>`.



  
.. _iati-activities/iati-activity/recipient-country/.percentage:

@percentage
  The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. Percentages for all reported countries and regions MUST add up to 100.


  This value must be of type xsd:decimal.



  The sum of values matched at ``recipient-country/@percentage`` and ``recipient-region/@percentage`` must be ``100``.





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L324>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/recipient-country.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country/narrative

