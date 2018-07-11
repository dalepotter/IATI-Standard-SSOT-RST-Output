contact-info
============

``iati-activities/iati-activity/contact-info``

This is the reference page for the XML element ``contact-info``. See also the relevant overview page: :doc:`/activity-standard/overview/contact-info` 

.. index::
  single: contact-info

Definition
~~~~~~~~~~


Contact information for the activity.  Specify whatever is
available.  You may repeat this element for each contact
person.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/contact-info/.type:

@type
  The type of contact. See IATI codelist for values.


  This value must be of type xsd:string.


  This value must be on the :doc:`ContactType codelist </codelists/ContactType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``contact-info`` for an ``iati-activity``.

| This element is a parent for other child elements.

| The ``@type`` attribute declares a valid code (*1*) from the *ContactType* codelist.

.. code-block:: xml

	<contact-info type="1">
	...
	</contact-info>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--contact-info starts-->
	:end-before: <!--contact-info ends-->

Changelog
~~~~~~~~~

2.01
^^^^
The optional ``contact-info/department`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#contact-info-department-new-element>`__.

1.03
^^^^
Added the optional ``contact-info/website`` element.

| Added the optional ``contact-info/@type`` attribute.

| Changed the following subelements of contact-info to allow multiple-language versions explicitly (no change to parsing; purely semantic):

-  organisation
-  person-name
-  job-title
-  mailing-address


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L683>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/contact-info.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   contact-info/organisation
   contact-info/department
   contact-info/person-name
   contact-info/job-title
   contact-info/telephone
   contact-info/email
   contact-info/website
   contact-info/mailing-address

