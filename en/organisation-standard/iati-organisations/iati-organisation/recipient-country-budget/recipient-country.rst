recipient-country
=================

``iati-organisations/iati-organisation/recipient-country-budget/recipient-country``

This is the reference page for the XML element ``recipient-country``. See also the relevant overview page: :doc:`/organisation-standard/overview/budgets` 

.. index::
  single: recipient-country

Definition
~~~~~~~~~~


The recipient country.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-country-budget/recipient-country/.code:

@code
  ISO 3166-1 alpha-2 code for the country.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`Country codelist </codelists/Country>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``recipient-country`` in context of ``recipient-country-budget`` element:

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--recipient-country-budget starts-->
	:end-before: <!--recipient-country-budget ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element, but only in particular use-cases.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L540>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget/recipient-country.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country/narrative

