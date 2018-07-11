recipient-country
=================

``iati-activities/iati-activity/transaction/recipient-country``

This is the reference page for the XML element ``recipient-country``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: recipient-country

Definition
~~~~~~~~~~


A country that will benefit from this transaction.
If a specific country is not known the recipient-region element should be used instead.

If transaction/recipient-country AND/OR transaction/recipient-region are used THEN ALL transaction elements MUST contain a recipient-country or recipient-region element AND (iati-activity/recipient-country AND iati-activity/recipient-region MUST NOT be used)


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/recipient-country/.code:

@code
  ISO 3166-1 alpha-2 code for the country.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`Country codelist </codelists/Country>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``recipient-country`` of ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*AF*) from the *Country* codelist.

.. code-block:: xml

        <recipient-country code="AF" />

Full example:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->


Changelog
~~~~~~~~~

2.01
^^^^
The ``sector`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#transaction-new-child-elements>`__ as a child element of ``transaction``.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1173>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/recipient-country.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country/narrative

