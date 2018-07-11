disbursement-channel
====================

``iati-activities/iati-activity/transaction/disbursement-channel``

This is the reference page for the XML element ``disbursement-channel``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: disbursement-channel

Definition
~~~~~~~~~~


The channel through which the funds will flow for this transaction, from an IATI codelist.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/disbursement-channel/.code:

@code
  An IATI code defining channels of disbursement

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`DisbursementChannel codelist </codelists/DisbursementChannel>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``disbursement-channel`` of a ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *DisbursementChannel* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1104>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/disbursement-channel.rst>`_

