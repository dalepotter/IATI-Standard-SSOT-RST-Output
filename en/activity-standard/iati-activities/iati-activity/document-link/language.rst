language
========

``iati-activities/iati-activity/document-link/language``

This is the reference page for the XML element ``language``. See also the relevant overview page: :doc:`/activity-standard/overview/linked-documents` 

.. index::
  single: language

Definition
~~~~~~~~~~


The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/document-link/language/.code:

@code
  ISO 639-1 language code

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
| Example usage of ``language`` of a ``document-link`` in an ``iati-activity``.

| The ``@language`` attribute declares a valid code (*en*) from the *Language* codelist.
| Note: This specifies the language of the document being linked to.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--document-link starts-->
	:end-before: <!--document-link ends-->

| In some cases, a ``document-link`` may be in multiple languages.  This is expressed by repeating the ``language`` element.

.. code-block:: xml

	<document-link format="application/vnd.oasis.opendocument.text" url="http:www.example.org/docs/report.odt">
		<title>
			<narrative>Project Report 2013</narrative>
			<narrative xml:lang="fr">Rapport de projet 2013</narrative>
		</title>
		<category code="A01" />
		<language code="en" />
		<language code="fr" />
	</document-link>

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.

| In 2.01 this element usage rules were changed, to allow it to be repeated.

1.02
^^^^
Addition of a ``@language`` element as a child of the ``document-link`` element:
document-link/language/text() (0..1) - The ISO 639 code for the language
of the document



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L217>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/document-link/language.rst>`_

