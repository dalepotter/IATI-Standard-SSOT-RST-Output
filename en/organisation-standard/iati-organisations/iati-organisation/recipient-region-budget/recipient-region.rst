recipient-region
================

``iati-organisations/iati-organisation/recipient-region-budget/recipient-region``

This is the reference page for the XML element ``recipient-region``. 

.. index::
  single: recipient-region

Definition
~~~~~~~~~~


The supranational geographic region where funds have been allocated.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-region-budget/recipient-region/.vocabulary:

@vocabulary
  An IATI code for the vocabulary from which the region code is
  drawn. If it is not present, code 1 ('OECD DAC') is assumed.


  This value must be of type xsd:string.


  This value must be on the :doc:`RegionVocabulary codelist </codelists/RegionVocabulary>`.



  
.. _iati-organisations/iati-organisation/recipient-region-budget/recipient-region/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  
.. _iati-organisations/iati-organisation/recipient-region-budget/recipient-region/.code:

@code
  Either an OECD DAC, UN region code or (if code ‘99’ Reporting
  organisation is selected for recipient-region/\@vocabulary) a
  code from your internal vocabulary. The codelist is determined
  by vocabulary attribute. The value in recipient-region/\@code
  should appear within the Region codelist, if the vocabulary
  code 1 ('OECD DAC') is used.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``recipient-region`` in context of ``recipient-region-budget`` element:

| The ``@code`` attribute declares a valid code (*489*) from the *Region* codelist.
| The optional ``@vocabulary`` attribute declares a valid code (*1*) from the *RegionVocabulary* codelist.

.. code-block:: xml

	<recipient-region code="489" vocabulary="1" />

If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:
.. code-block:: xml

	<recipient-region code="A1" vocabulary="99" vocabulary-uri="http://example.com/vocab.html" />

Example of ``recipient-region`` in context of a complete ``recipient-region-budget`` element:

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--recipient-region-budget starts-->
	:end-before: <!--recipient-region-budget ends-->

Changelog
~~~~~~~~~

2.03
^^^^
Definition of ``@vocabulary-uri`` attribute `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

2.02
^^^^
The optional ``recipient-region-budget`` element was `added <http://support.iatistandard.org/entries/79323113-Org-Standard-recipient-region-budget>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L391>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/recipient-region-budget/recipient-region.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-region/narrative

