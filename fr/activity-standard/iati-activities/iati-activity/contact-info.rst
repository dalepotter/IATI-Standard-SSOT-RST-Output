contact-info
============

``iati-activities/iati-activity/contact-info``

This is the reference page for the XML element ``contact-info``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L683>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/contact-info.rst>`_


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

