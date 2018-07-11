Activity Standard Summary Table
===============================

.. list-table::
    :header-rows: 1

    * - Section
      - Item
      - Description
      - Type
      - Codelist
      - XML
      - Occur
      - Rules


    * - :doc:`iati-activities </activity-standard/iati-activities>`
      - 
      - Top-level list of one or more IATI activity records.
      - 
      - 
      - iati-activities
      - ..
      - 

    * - 
      - version
      - A number indicating the IATI specification version in use.
        This is mandatory and must be a valid version.
      - xsd:string
      - :doc:`/codelists/Version`
      - iati-activities/\@version
      - 1..1
      - 

    * - 
      - generated-datetime
      - A date/time stamp for when this file was generated. This
        is not necessarily the last-updated date for the
        individual activity records in it. Use of this attribute
        is highly recommended, to allow recipients to know when a
        file has been updated.
      - xsd:dateTime
      - 
      - iati-activities/\@generated-datetime
      - 0..1
      - 

    * - 
      - linked-data-default
      - If a publisher chooses to publish linked data about their
        IATI activities then allowing them to declare where this
        data is published would support discovery of it, and any
        additional information they may choose to publish as
        Linked Data alongside it.
        
        This attribute is a URI path upon which an activity
        identifier can be appended to get a differentiable URI
        for any activity contained within a file.
        
        Where a publisher declares using one of these properties
        that authoritative linked data is accessible for an
        activity then consuming applications that are generating
        Linked Data from an IATI XML file should assert an
        owl:sameAs relationship to the relevant URI.
      - xsd:anyURI
      - 
      - iati-activities/\@linked-data-default
      - 0..1
      - 

    * - :doc:`iati-activity </activity-standard/iati-activities/iati-activity>`
      - 
      - Top-level element for a single IATI activity report.
      - 
      - 
      - iati-activities/iati-activity
      - 1..*
      - 

    * - 
      - last-updated-datetime
      - The last date/time that the data for this specific
        activity was updated.  This date must change whenever the
        value of any field changes.
      - xsd:dateTime
      - 
      - iati-activities/iati-activity/\@last-updated-datetime
      - 0..1
      - 

    * - 
      - xml:lang
      - A code specifying the default language of text in this activity. It is recommended that wherever possible only codes from ISO 639-1 are used.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/\@xml:lang
      - 0..1
      - 

    * - 
      - default-currency
      - Default ISO 4217 alphabetic currency code for all
        financial values in this activity report. If this is not
        declared then the currency attribute MUST be specified for
        all monetary values.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/\@default-currency
      - 0..1
      - 

    * - 
      - humanitarian
      - A process flag to indicate that this activity relates entirely
        or partially to humanitarian aid.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/\@humanitarian
      - 0..1
      - 

    * - 
      - hierarchy
      - The hierarchical level within the reporting organisation's
        subdivision of its units of aid. (eg activity = 1;
        sub-activity = 2; sub-sub-activity = 3). If hierarchy is
        not reported then 1 is assumed. If multiple levels are
        reported then, to avoid double counting, financial
        transactions should only be reported at the lowest
        hierarchical level.
      - xsd:int
      - 
      - iati-activities/iati-activity/\@hierarchy
      - 0..1
      - 

    * - 
      - linked-data-uri
      - A Linked Data URI for a given activity (overrides
        iati-activities/\@linked-data-default if set)
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/\@linked-data-uri
      - 0..1
      - 

    * - 
      - budget-not-provided
      - A code indicating the reason why this activity does not contain any iati-activity/budget elements. The value must exist in the BudgetNotProvided codelist.
      - xsd:string
      - :doc:`/codelists/BudgetNotProvided`
      - iati-activities/iati-activity/\@budget-not-provided
      - 0..1
      - 

    * - :doc:`iati-identifier </activity-standard/iati-activities/iati-activity/iati-identifier>`
      - 
      - A globally unique identifier for the activity.
        
        This MUST be prefixed with EITHER the current IATI
        organisation identifier for the reporting organisation
        (reporting-org/\@ref) OR a previous identifier reported in
        other-identifier, and suffixed with the organisation’s own
        activity identifier. The prefix and the suffix should be
        separated by a hyphen "-".
        
        Once an activity has been reported to IATI its identifier MUST
        NOT be changed in subsequent updates.
      - 
      - 
      - iati-activities/iati-activity/iati-identifier
      - 1..1
      - ``iati-identifier`` should match the regex ``[^\/\&\|\?]+``

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/iati-identifier/text()
      - 
      - 

    * - :doc:`reporting-org </activity-standard/iati-activities/iati-activity/reporting-org>`
      - 
      - The organisation issuing the report.
        May be a primary source (reporting on its own activity as
        donor, implementing agency, etc) or a secondary source
        (reporting on the activities of another organisation).
        
        Specifying the @ref attribute is mandatory.
        May contain the organisation name as content.
        
        All activities in an activity xml file must contain the same
        @ref AND this @ref must be the same as the iati-identifier
        recorded in the registry publisher record of the account under
        which this file is published.
      - 
      - 
      - iati-activities/iati-activity/reporting-org
      - 1..1
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}.
      - xsd:string
      - 
      - iati-activities/iati-activity/reporting-org/\@ref
      - 1..1
      - ``reporting-org/@ref`` should match the regex ``[^\/\&\|\?]+``

    * - 
      - type
      - The type of organisation issuing the report. See IATI codelist for values.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/reporting-org/\@type
      - 1..1
      - 

    * - 
      - secondary-reporter
      - A flag indicating that the reporting organisation of this activity is acting as a secondary reporter. A secondary reporter is one that reproduces data on the activities of an organisation for which it is not directly responsible. This does not include a publisher officially assigned as a proxy to report on behalf of another.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/reporting-org/\@secondary-reporter
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/reporting-org/narrative>`
      - The name of the organisation. May be repeated for
        different languages.
      - 
      - 
      - iati-activities/iati-activity/reporting-org/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/reporting-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/reporting-org/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`title </activity-standard/iati-activities/iati-activity/title>`
      - 
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/title/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`description </activity-standard/iati-activities/iati-activity/description>`
      - 
      - A longer, human-readable description containing a
        meaningful description of the activity. May be repeated
        for different languages.
      - 
      - 
      - iati-activities/iati-activity/description
      - 1..*
      - 

    * - 
      - type
      - The type of description being provided. This is not
        required if only one general description of the activity
        is reported.
      - xsd:string
      - :doc:`/codelists/DescriptionType`
      - iati-activities/iati-activity/description/\@type
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/description/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`participating-org </activity-standard/iati-activities/iati-activity/participating-org>`
      - 
      - An organisation involved with the activity. May be a donor, fund, agency, etc. Specifying the @ref identifier is strongly recommended. May contain the organisation name as narrative.
        
        If the reporting organisation plays a role in the activity it should be repeated here. One organisation may play more than one role (eg, funding and implementing): in such a case each role should be reported and the name of the organisation repeated.
      - 
      - 
      - iati-activities/iati-activity/participating-org
      - 1..*
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.
      - xsd:string
      - 
      - iati-activities/iati-activity/participating-org/\@ref
      - 0..1
      - ``participating-org/@ref`` should match the regex ``[^\/\&\|\?]+``
        Either ``@ref`` or ``narrative`` must be present.

    * - 
      - type
      - The type of organisation issuing the report. See IATI codelist for values.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/participating-org/\@type
      - 0..1
      - 

    * - 
      - role
      - An IATI code describing the organisation's role in the activity (donor, agency, etc.).
      - xsd:string
      - :doc:`/codelists/OrganisationRole`
      - iati-activities/iati-activity/participating-org/\@role
      - 1..1
      - 

    * - 
      - activity-id
      - A valid activity identifier published by the participating organisation which points to the activity that it has published to IATI that describes its role in this activity.
      - xsd:string
      - 
      - iati-activities/iati-activity/participating-org/\@activity-id
      - 0..1
      - 

    * - 
      - crs-channel-code
      - Under CRS++ Reporting Directives this code identifies the implementing agency. Codes ending in '00' are generic and are similar to the OrganisationType code.
      - xsd:string
      - :doc:`/codelists/CRSChannelCode`
      - iati-activities/iati-activity/participating-org/\@crs-channel-code
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/participating-org/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/participating-org/narrative
      - 0..*
      - Either ``narrative`` or ``@ref`` must be present.

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/participating-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/participating-org/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`other-identifier </activity-standard/iati-activities/iati-activity/other-identifier>`
      - 
      - An other identifier for the activity. This may be a publishers
        own identifier that it wishes to record with the activity.
        This element is also used to trace changes to activity
        identifiers, for example when and organisation has changed
        it's organisation identifier.
      - 
      - 
      - iati-activities/iati-activity/other-identifier
      - 0..*
      - 

    * - 
      - ref
      - The identifier you wish to report.
        This can be used to report a number of different types
        of identifiers. See the OtherIdentifierType codelist
        for details and options.
      - xsd:string
      - 
      - iati-activities/iati-activity/other-identifier/\@ref
      - 1..1
      - 

    * - 
      - type
      - The type of identifier being reported, taken from
        the OtherIdentifierType codelist.
      - xsd:string
      - :doc:`/codelists/OtherIdentifierType`
      - iati-activities/iati-activity/other-identifier/\@type
      - 1..1
      - 

    * - 
      - :doc:`owner-org </activity-standard/iati-activities/iati-activity/other-identifier/owner-org>`
      - Where applicable, the organisation that owns the other
        identifier being reported. When used, then either
        other-identifier/owner-org/\@ref or
        other-identifier/owner-org/narrative/text() MUST be
        present.
      - 
      - 
      - iati-activities/iati-activity/other-identifier/owner-org
      - 0..1
      - 

    * - 
      - ref
      - An organisation identifier. This is NOT MANDATORY
        but when used MUST contain a valid organisation
        identifier.
      - xsd:string
      - 
      - iati-activities/iati-activity/other-identifier/owner-org/\@ref
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/other-identifier/owner-org/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/other-identifier/owner-org/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/other-identifier/owner-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/other-identifier/owner-org/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`activity-status </activity-standard/iati-activities/iati-activity/activity-status>`
      - 
      - The current status of the activity. See codelist for values.
      - 
      - 
      - iati-activities/iati-activity/activity-status
      - 1..1
      - 

    * - 
      - code
      - An IATI code defining the current status of the activity.
      - xsd:string
      - :doc:`/codelists/ActivityStatus`
      - iati-activities/iati-activity/activity-status/\@code
      - 1..1
      - 

    * - :doc:`activity-date </activity-standard/iati-activities/iati-activity/activity-date>`
      - 
      - The planned and actual start and completion dates of the
        activity. Start dates may reflect either the commencement of
        funding, planning or physical activity. End dates should,
        wherever possible, reflect the ending of physical activity.
        
        The narrative content may contain text (e.g. 2011Q1) for
        accurately recording less specific dates such as month,
        quarter, or year.
      - 
      - 
      - iati-activities/iati-activity/activity-date
      - 1..*
      - ``activity-date[@type='1' or @type='2']`` must be present.

    * - 
      - type
      - An IATI code defining the type of activity date being reported.
      - xsd:string
      - :doc:`/codelists/ActivityDateType`
      - iati-activities/iati-activity/activity-date/\@type
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/activity-date/\@iso-date
      - 1..1
      - ``activity-date[@type='1']/@iso-date`` must be before or the same as ``activity-date[@type='3']/@iso-date``
        ``activity-date[@type='2']/@iso-date`` must be before or the same as ``activity-date[@type='4']/@iso-date``
        ``activity-date[@type='2']/@iso-date`` must not be in the future.
        ``activity-date[@type='4']/@iso-date`` must not be in the future.

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/activity-date/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/activity-date/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/activity-date/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/activity-date/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`contact-info </activity-standard/iati-activities/iati-activity/contact-info>`
      - 
      - Contact information for the activity.  Specify whatever is
        available.  You may repeat this element for each contact
        person.
      - 
      - 
      - iati-activities/iati-activity/contact-info
      - 0..*
      - 

    * - 
      - type
      - The type of contact. See IATI codelist for values.
      - xsd:string
      - :doc:`/codelists/ContactType`
      - iati-activities/iati-activity/contact-info/\@type
      - 0..1
      - 

    * - 
      - :doc:`organisation </activity-standard/iati-activities/iati-activity/contact-info/organisation>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/organisation
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/contact-info/organisation/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/organisation/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/organisation/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/contact-info/organisation/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`department </activity-standard/iati-activities/iati-activity/contact-info/department>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/department
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/contact-info/department/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/department/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/department/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/contact-info/department/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`person-name </activity-standard/iati-activities/iati-activity/contact-info/person-name>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/person-name
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/contact-info/person-name/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/person-name/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/person-name/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/contact-info/person-name/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`job-title </activity-standard/iati-activities/iati-activity/contact-info/job-title>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/job-title
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/contact-info/job-title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/job-title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/job-title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/contact-info/job-title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`telephone </activity-standard/iati-activities/iati-activity/contact-info/telephone>`
      - The contact telephone number. May be repeated for
        multiple numbers.
      - 
      - 
      - iati-activities/iati-activity/contact-info/telephone
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/telephone/text()
      - 
      - 

    * - 
      - :doc:`email </activity-standard/iati-activities/iati-activity/contact-info/email>`
      - The contact email address. May be repeated for multiple
        addresses.
      - 
      - 
      - iati-activities/iati-activity/contact-info/email
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/email/text()
      - 
      - 

    * - 
      - :doc:`website </activity-standard/iati-activities/iati-activity/contact-info/website>`
      - The contact web address. May be repeated for multiple sites.
      - 
      - 
      - iati-activities/iati-activity/contact-info/website
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/contact-info/website/text()
      - 
      - 

    * - 
      - :doc:`mailing-address </activity-standard/iati-activities/iati-activity/contact-info/mailing-address>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/mailing-address
      - 0..*
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/contact-info/mailing-address/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/contact-info/mailing-address/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/contact-info/mailing-address/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/contact-info/mailing-address/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`activity-scope </activity-standard/iati-activities/iati-activity/activity-scope>`
      - 
      - The geographical scope of the activity: regional, national,
        sub-national, etc.
      - 
      - 
      - iati-activities/iati-activity/activity-scope
      - 0..1
      - 

    * - 
      - code
      - The geographical scope. See IATI codelist for values.
      - xsd:string
      - :doc:`/codelists/ActivityScope`
      - iati-activities/iati-activity/activity-scope/\@code
      - 1..1
      - 

    * - :doc:`recipient-country </activity-standard/iati-activities/iati-activity/recipient-country>`
      - 
      - A country that will benefit from this activity. If a specific
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
      - 
      - 
      - iati-activities/iati-activity/recipient-country
      - 0..*
      - 

    * - 
      - code
      - ISO 3166-1 alpha-2 code for the country.
      - xsd:string
      - :doc:`/codelists/Country`
      - iati-activities/iati-activity/recipient-country/\@code
      - 1..1
      - 

    * - 
      - percentage
      - The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. Percentages for all reported countries and regions MUST add up to 100.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/recipient-country/\@percentage
      - 0..1
      - The sum of values matched at ``recipient-country/@percentage`` and ``recipient-region/@percentage`` must be ``100``.

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/recipient-country/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/recipient-country/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/recipient-country/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/recipient-country/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`recipient-region </activity-standard/iati-activities/iati-activity/recipient-region>`
      - 
      - A supranational geopolitical region that will benefit from
        this activity. For sub-national geographical location, use the
        location element.
        
        Multiple countries and regions can be reported, in which case
        the percentage attribute MUST be used to specify the share of
        total commitments across all reported countries and regions.
        Recipient-region must not be used merely to describe the
        region of a country reported in recipient-country, but ONLY if
        the region is a recipient IN ADDITION to the country.
        
        Region can also be reported at transaction rather than
        activity level. If transaction/recipient-country AND/OR
        transaction/recipient-region are used THEN ALL transaction
        elements MUST contain a recipient-country and/or
        recipient-region element AND iati-activity/recipient-region
        and iati-activity/recipient-region MUST NOT be used AND each
        transaction MUST only contain one recipient-country or
        recipient-region.
      - 
      - 
      - iati-activities/iati-activity/recipient-region
      - 0..*
      - 

    * - 
      - code
      - Either an OECD DAC or UN region code. Codelist is
        determined by vocabulary attribute.
      - xsd:string
      - (:doc:`/codelists/Region`)
      - iati-activities/iati-activity/recipient-region/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - An IATI code for the vocabulary from which the region code
        is drawn. If it is not present 1 - 'OECD DAC' is assumed.
      - xsd:string
      - :doc:`/codelists/RegionVocabulary`
      - iati-activities/iati-activity/recipient-region/\@vocabulary
      - 0..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/recipient-region/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - percentage
      - The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. Percentages for all reported countries and regions MUST add up to 100.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/recipient-region/\@percentage
      - 0..1
      - The sum of values matched at ``recipient-region/@percentage`` and ``recipient-country/@percentage`` must be ``100``.

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/recipient-region/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/recipient-region/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/recipient-region/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/recipient-region/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`location </activity-standard/iati-activities/iati-activity/location>`
      - 
      - The sub-national geographical identification of the target locations of an activity. These can be described by gazetteer reference, coordinates, administrative areas or a textual description. Any number of locations may be reported.
      - 
      - 
      - iati-activities/iati-activity/location
      - 0..*
      - 

    * - 
      - ref
      - An internal reference that describes the location in the reporting organisation’s own system.
      - xsd:string
      - 
      - iati-activities/iati-activity/location/\@ref
      - 0..1
      - 

    * - 
      - :doc:`location-reach </activity-standard/iati-activities/iati-activity/location/location-reach>`
      - Does this location describe where the activity takes place or where the intended beneficiaries reside?
      - 
      - 
      - iati-activities/iati-activity/location/location-reach
      - 0..1
      - 

    * - 
      - code
      - An IATI code for the geographic scope of the activity.
      - xsd:string
      - :doc:`/codelists/GeographicLocationReach`
      - iati-activities/iati-activity/location/location-reach/\@code
      - 1..1
      - 

    * - 
      - :doc:`location-id </activity-standard/iati-activities/iati-activity/location/location-id>`
      - A unique code describing the location according to a recognised gazetteer or administrative boundary repository. Administrative areas should only be reported here if the location being defined is the administrative area itself. For describing the administrative area/s within which a more specific location falls the location/administrative element should be used.
      - 
      - 
      - iati-activities/iati-activity/location/location-id
      - 0..*
      - 

    * - 
      - code
      - A code from the gazetteer or administrative boundary repository specified by the vocabulary
      - xsd:string
      - 
      - iati-activities/iati-activity/location/location-id/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - An IATI code for a recognised gazetteer or administrative boundary repository.
      - xsd:string
      - :doc:`/codelists/GeographicVocabulary`
      - iati-activities/iati-activity/location/location-id/\@vocabulary
      - 1..1
      - 

    * - 
      - :doc:`name </activity-standard/iati-activities/iati-activity/location/name>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/location/name
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/location/name/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/location/name/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/location/name/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/location/name/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/location/description>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/location/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/location/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/location/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/location/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/location/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`activity-description </activity-standard/iati-activities/iati-activity/location/activity-description>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/location/activity-description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/location/activity-description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/location/activity-description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/location/activity-description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/location/activity-description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`administrative </activity-standard/iati-activities/iati-activity/location/administrative>`
      - Coded identification of national and sub-national divisions according to recognised administrative boundary repositories. Multiple levels may be reported.
      - 
      - 
      - iati-activities/iati-activity/location/administrative
      - 0..*
      - 

    * - 
      - code
      - The code for the administrative area being reported from the vocabulary specified.
      - xsd:string
      - 
      - iati-activities/iati-activity/location/administrative/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - An IATI code for a recognised administrative boundary repository.
      - xsd:string
      - :doc:`/codelists/GeographicVocabulary`
      - iati-activities/iati-activity/location/administrative/\@vocabulary
      - 1..1
      - 

    * - 
      - level
      - A number defining a subdivision within a hierarchical system of administrative areas. The precise system for defining the particular meaning of each @level value is determined by the @vocabulary being used.
      - xsd:nonNegativeInteger
      - 
      - iati-activities/iati-activity/location/administrative/\@level
      - 0..1
      - 

    * - 
      - :doc:`point </activity-standard/iati-activities/iati-activity/location/point>`
      - The point element is based on a subset of the GML 3.3 Point element.
      - 
      - 
      - iati-activities/iati-activity/location/point
      - 0..1
      - 

    * - 
      - srsName
      - The name of the spatial reference system used by the coordinates.
        
        Always: http://www.opengis.net/def/crs/EPSG/0/4326
      - xsd:string
      - 
      - iati-activities/iati-activity/location/point/\@srsName
      - 1..1
      - 

    * - 
      - :doc:`pos </activity-standard/iati-activities/iati-activity/location/point/pos>`
      - The latitude and longitude coordinates in the format "lat lng"
      - xsd:string
      - 
      - iati-activities/iati-activity/location/point/pos
      - 1..1
      - 

    * - 
      - :doc:`exactness </activity-standard/iati-activities/iati-activity/location/exactness>`
      - Defines whether the location represents the most distinct point reasonably possible for this type of activity or is an approximation due to lack of more detailed information.
      - 
      - 
      - iati-activities/iati-activity/location/exactness
      - 0..1
      - 

    * - 
      - code
      - A code from the Geographic Exactness Codelist.
      - xsd:string
      - :doc:`/codelists/GeographicExactness`
      - iati-activities/iati-activity/location/exactness/\@code
      - 1..1
      - 

    * - 
      - :doc:`location-class </activity-standard/iati-activities/iati-activity/location/location-class>`
      - Whether the location refers to a structure, a populated place (e.g. city or village), an administrative division, or another topological feature (e.g. river, nature reserve).
      - 
      - 
      - iati-activities/iati-activity/location/location-class
      - 0..1
      - 

    * - 
      - code
      - A code from the Location Class codelist
      - xsd:string
      - :doc:`/codelists/GeographicLocationClass`
      - iati-activities/iati-activity/location/location-class/\@code
      - 1..1
      - 

    * - 
      - :doc:`feature-designation </activity-standard/iati-activities/iati-activity/location/feature-designation>`
      - A more refined coded classification of the type of feature referred to by this location.
      - 
      - 
      - iati-activities/iati-activity/location/feature-designation
      - 0..1
      - 

    * - 
      - code
      - A feature designation code form the authorised list (maintained by the US National Geospatial-Intelligence Agency)
      - xsd:string
      - :doc:`/codelists/LocationType`
      - iati-activities/iati-activity/location/feature-designation/\@code
      - 1..1
      - 

    * - :doc:`sector </activity-standard/iati-activities/iati-activity/sector>`
      - 
      - A recognised code, from a recognised vocabulary, classifying
        the purpose of the activity. Sector MUST EITHER be reported
        here OR at transaction level for ALL transactions
      - 
      - 
      - iati-activities/iati-activity/sector
      - 0..*
      - Either ``sector`` or ``transaction/sector`` must be present.

    * - 
      - vocabulary
      - An IATI code for the vocabulary (see codelist) used for sector classifications. If omitted, OECD DAC 5-digit Purpose Codes are assumed.
        
        It is recommended that OECD DAC 5-digit Purpose Codes are used wherever possible. It is also recommended that if a publisher has its own classification system or systems then the vocabularies 99 or 98 (Reporting Organisation's own vocabularies) should be used in addition to DAC codes.
        
        Publishers using 98 or 99 must also include a narrative in the narrative element.
        
        Note that if multiple sector codes are used in multiple vocabularies, then each vocabulary’s percentages should add up to 100.
        
        Sector can also be reported at the transaction level rather than the activity level. Sector must only be reported at EITHER transaction level OR activity level.
      - xsd:string
      - :doc:`/codelists/SectorVocabulary`
      - iati-activities/iati-activity/sector/\@vocabulary
      - 0..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/sector/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - code
      - The code for the sector.
      - xsd:string
      - (:doc:`/codelists/Sector`)
      - iati-activities/iati-activity/sector/\@code
      - 1..1
      - 

    * - 
      - percentage
      - The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. All reported sectors from the same vocabulary MUST add up to 100.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/sector/\@percentage
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/sector/narrative>`
      - The description of a sector defined by the reporting
        organisation. (Only to be used when the reporting
        organisation's own vocabulary is being used).
      - 
      - 
      - iati-activities/iati-activity/sector/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/sector/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/sector/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`tag </activity-standard/iati-activities/iati-activity/tag>`
      - 
      - Categorisations from established taxonomies that enrich the classification of the activity but that, unlike those reported in the sector element, cannot be associated with percentage splits on finances.
      - 
      - 
      - iati-activities/iati-activity/tag
      - 0..*
      - 

    * - 
      - code
      - The code for the tag as defined in the specified vocabulary.
      - xsd:string
      - 
      - iati-activities/iati-activity/tag/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - An IATI code for the vocabulary or taxonomy (see non-embedded codelist) used for tag classifications.
      - xsd:string
      - :doc:`/codelists/TagVocabulary`
      - iati-activities/iati-activity/tag/\@vocabulary
      - 1..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/tag/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/tag/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/tag/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/tag/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/tag/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`country-budget-items </activity-standard/iati-activities/iati-activity/country-budget-items>`
      - 
      - This item encodes the alignment of activities with both the functional and administrative classifications used in the recipient country's Chart of Accounts. This applies to both on- and off-budget activities.
      - 
      - 
      - iati-activities/iati-activity/country-budget-items
      - 0..1
      - 

    * - 
      - vocabulary
      - An IATI code for the common functional classification or country system (This allows for common codes, country-specific, or any other classification agreed between countries and donors).
      - xsd:string
      - :doc:`/codelists/BudgetIdentifierVocabulary`
      - iati-activities/iati-activity/country-budget-items/\@vocabulary
      - 1..1
      - 

    * - 
      - :doc:`budget-item </activity-standard/iati-activities/iati-activity/country-budget-items/budget-item>`
      - Identifier for a single item in the recipient-country budget. If more than one identifier is reported the percentage share must be reported and all percentages should add up to 100 percent.
      - 
      - 
      - iati-activities/iati-activity/country-budget-items/budget-item
      - 1..*
      - 

    * - 
      - code
      - A code for the budget-item from the vocabulary specified.
      - xsd:string
      - (:doc:`/codelists/BudgetIdentifier`)
      - iati-activities/iati-activity/country-budget-items/budget-item/\@code
      - 1..1
      - 

    * - 
      - percentage
      - When multiple budget-item elements are declared within a single country-budget-items element, then, for each vocabulary used, the percentage values should sum 100%.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/country-budget-items/budget-item/\@percentage
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/country-budget-items/budget-item/description>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/country-budget-items/budget-item/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/country-budget-items/budget-item/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/country-budget-items/budget-item/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/country-budget-items/budget-item/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/country-budget-items/budget-item/description/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`humanitarian-scope </activity-standard/iati-activities/iati-activity/humanitarian-scope>`
      - 
      - Classification of emergencies, appeals and other humanitarian
        events and actions.
      - 
      - 
      - iati-activities/iati-activity/humanitarian-scope
      - 0..*
      - 

    * - 
      - type
      - A code for the type of event or action being classified.
      - xsd:string
      - :doc:`/codelists/HumanitarianScopeType`
      - iati-activities/iati-activity/humanitarian-scope/\@type
      - 1..1
      - 

    * - 
      - vocabulary
      - A code for a recognised vocabulary of terms classifying the
        event or action.
      - xsd:string
      - :doc:`/codelists/HumanitarianScopeVocabulary`
      - iati-activities/iati-activity/humanitarian-scope/\@vocabulary
      - 1..1
      - 

    * - 
      - vocabulary-uri
      - A u.r.i. for the vocabulary specified which provides access to
        the list of codes and descriptions.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/humanitarian-scope/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - code
      - A code for the event or action from the vocabulary specified.
      - xsd:string
      - 
      - iati-activities/iati-activity/humanitarian-scope/\@code
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/humanitarian-scope/narrative>`
      - The description of the code specified.
      - 
      - 
      - iati-activities/iati-activity/humanitarian-scope/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/humanitarian-scope/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/humanitarian-scope/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`policy-marker </activity-standard/iati-activities/iati-activity/policy-marker>`
      - 
      - A policy or theme addressed by the activity. This element was
        designed for the reporting of OECD DAC CRS policy markers
        (columns 20-23 and 28-31 of the CRS++ reporting format) but
        the vocabulary attribute allows it use by other (including
        local) systems. This element can be repeated for each policy
        marker.
      - 
      - 
      - iati-activities/iati-activity/policy-marker
      - 0..*
      - 

    * - 
      - vocabulary
      - An IATI code for the vocabulary to be used to define
        policy markers. If omitted then the OECD DAC vocabulary is
        assumed.
      - xsd:string
      - :doc:`/codelists/PolicyMarkerVocabulary`
      - iati-activities/iati-activity/policy-marker/\@vocabulary
      - 0..1
      - 

    * - 
      - vocabulary-uri
      - If the vocabulary is 99 (reporting organisation), the URI
        where this internal vocabulary is defined.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/policy-marker/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - code
      - A policy marker code from the codelist specified in the
        vocabulary.
      - xsd:string
      - (:doc:`/codelists/PolicyMarker`)
      - iati-activities/iati-activity/policy-marker/\@code
      - 1..1
      - 

    * - 
      - significance
      - An OECD DAC CRS code indicating the significance of the policy marker
        for this activity. This attribute MUST be used for all OECD DAC CRS
        vocabularies.
      - xsd:string
      - :doc:`/codelists/PolicySignificance`
      - iati-activities/iati-activity/policy-marker/\@significance
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/policy-marker/narrative>`
      - A description of the policy marker. This MUST ONLY be
        used where vocabulary = "99 - RO" (the reporting
        organisation's own marker vocabulary). May be repeated
        for multiple languages.
      - 
      - 
      - iati-activities/iati-activity/policy-marker/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/policy-marker/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/policy-marker/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`collaboration-type </activity-standard/iati-activities/iati-activity/collaboration-type>`
      - 
      - The type of collaboration involved in the activity's
        disbursements, e.g. "bilateral" or "multilateral".
      - 
      - 
      - iati-activities/iati-activity/collaboration-type
      - 0..1
      - 

    * - 
      - code
      - A code from the OECD DAC CRS "Bi_Multi" codelist.
      - xsd:string
      - :doc:`/codelists/CollaborationType`
      - iati-activities/iati-activity/collaboration-type/\@code
      - 1..1
      - 

    * - :doc:`default-flow-type </activity-standard/iati-activities/iati-activity/default-flow-type>`
      - 
      - Whether the activity is funded by Official Development
        Assistance (ODA), Other Official Flows (OOF), etc
      - 
      - 
      - iati-activities/iati-activity/default-flow-type
      - 0..1
      - 

    * - 
      - code
      - A code from the OECD DAC CRS "Type of flow" codelist
      - xsd:string
      - :doc:`/codelists/FlowType`
      - iati-activities/iati-activity/default-flow-type/\@code
      - 1..1
      - 

    * - :doc:`default-finance-type </activity-standard/iati-activities/iati-activity/default-finance-type>`
      - 
      - The type of finance (e.g. grant, loan, debt relief, etc). This
        the default value for all transactions in the activity report;
        it can be overridden by individual transactions.
      - 
      - 
      - iati-activities/iati-activity/default-finance-type
      - 0..1
      - 

    * - 
      - code
      - A code from the OECD DAC CRS "Type of finance" codelist
      - xsd:string
      - :doc:`/codelists/FinanceType`
      - iati-activities/iati-activity/default-finance-type/\@code
      - 1..1
      - 

    * - :doc:`default-aid-type </activity-standard/iati-activities/iati-activity/default-aid-type>`
      - 
      - The type of aid being supplied (project-type intervention,
        budget support, debt relief, etc.). This element specifies a
        default for all the activity's financial transactions; it can
        be overridden at the individual transaction level.
      - 
      - 
      - iati-activities/iati-activity/default-aid-type
      - 0..*
      - 

    * - 
      - code
      - A code from the specified vocabulary.
      - xsd:string
      - :doc:`/codelists/AidType`
      - iati-activities/iati-activity/default-aid-type/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.
      - xsd:string
      - :doc:`/codelists/AidTypeVocabulary`
      - iati-activities/iati-activity/default-aid-type/\@vocabulary
      - 0..1
      - 

    * - :doc:`default-tied-status </activity-standard/iati-activities/iati-activity/default-tied-status>`
      - 
      - Whether the aid is untied, tied, or partially tied. This
        element specifies a default for all the activity's financial
        transactions; it can be overridden at the individual
        transaction level.
        
        If an activity is partially tied it is recommended that tied
        and untied commitments are reported as separate transactions
        and that transaction/tied-status is used to classify them.
      - 
      - 
      - iati-activities/iati-activity/default-tied-status
      - 0..1
      - 

    * - 
      - code
      - An IATI code interpreting the usage of Columns 36-38 of the
        CRS++ reporting format. (Amount tied, Amount partially
        untied, Amount tied)
      - xsd:string
      - :doc:`/codelists/TiedStatus`
      - iati-activities/iati-activity/default-tied-status/\@code
      - 1..1
      - 

    * - :doc:`budget </activity-standard/iati-activities/iati-activity/budget>`
      - 
      - The value of the activity's budget for each financial quarter or year over the lifetime of the activity. The purpose of this element is to provide predictability for recipient planning on an annual basis. The status explains whether the budget being reported is indicative or has been formally committed. The value should appear within the BudgetStatus codelist. If the @status attribute is not present, the budget is assumed to be indicative. The sum of budgets may or may not match the sum of commitments, depending on a publisher’s business model and legal frameworks.
      - 
      - 
      - iati-activities/iati-activity/budget
      - 0..*
      - 

    * - 
      - type
      - Whether this is the original budget (prepared when the original commitment was made) or has subsequently been revised
      - xsd:string
      - :doc:`/codelists/BudgetType`
      - iati-activities/iati-activity/budget/\@type
      - 0..1
      - 

    * - 
      - status
      - The status explains whether the budget being reported is indicative or has been formally committed. The value should appear within the BudgetStatus codelist. If the @status attribute is not present, the budget is assumed to be indicative.
      - xsd:string
      - :doc:`/codelists/BudgetStatus`
      - iati-activities/iati-activity/budget/\@status
      - 0..1
      - 

    * - 
      - :doc:`period-start </activity-standard/iati-activities/iati-activity/budget/period-start>`
      - The start of the budget period.
      - 
      - 
      - iati-activities/iati-activity/budget/period-start
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/budget/period-start/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`period-end </activity-standard/iati-activities/iati-activity/budget/period-end>`
      - The end of the period (which must not be greater than one year)
      - 
      - 
      - iati-activities/iati-activity/budget/period-end
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/budget/period-end/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`value </activity-standard/iati-activities/iati-activity/budget/value>`
      - Data type for an element containing a currency value.
      - 
      - 
      - iati-activities/iati-activity/budget/value
      - 1..1
      - 

    * - 
      - currency
      - The ISO 4217 alphabetic currency code of the value reported.
        This is required unless the iati-activity/\@default-currency is present and applies.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/budget/value/\@currency
      - 0..1
      - 

    * - 
      - value-date
      - The date to be used for determining the exchange rate for
        currency conversions.
      - xsd:date
      - 
      - iati-activities/iati-activity/budget/value/\@value-date
      - 0..1
      - 

    * - :doc:`planned-disbursement </activity-standard/iati-activities/iati-activity/planned-disbursement>`
      - 
      - The planned disbursement element should only be used to report specific planned cash transfers. These should be reported for a specific date or a meaningfully predictable period. These transactions should be reported in addition to budgets - which are typically annual breakdowns of the total activity commitment.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement
      - 0..*
      - 

    * - 
      - type
      - Whether this is an original plan (prepared when the original commitment was made) or has subsequently been revised.
      - xsd:string
      - :doc:`/codelists/BudgetType`
      - iati-activities/iati-activity/planned-disbursement/\@type
      - 0..1
      - 

    * - 
      - :doc:`period-start </activity-standard/iati-activities/iati-activity/planned-disbursement/period-start>`
      - The exact date of the planned disbursement OR the starting date of the period in which this specific disbursement will be made.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/period-start
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/planned-disbursement/period-start/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`period-end </activity-standard/iati-activities/iati-activity/planned-disbursement/period-end>`
      - The ending date for the period in which this specific disbursement will be made.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/period-end
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/planned-disbursement/period-end/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`value </activity-standard/iati-activities/iati-activity/planned-disbursement/value>`
      - Data type for an element containing a currency value.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/value
      - 1..1
      - 

    * - 
      - currency
      - The ISO 4217 alphabetic currency code of the value reported.
        This is required unless the iati-activity/\@default-currency is present and applies.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/planned-disbursement/value/\@currency
      - 0..1
      - 

    * - 
      - value-date
      - The date to be used for determining the exchange rate for
        currency conversions.
      - xsd:date
      - 
      - iati-activities/iati-activity/planned-disbursement/value/\@value-date
      - 0..1
      - 

    * - 
      - :doc:`provider-org </activity-standard/iati-activities/iati-activity/planned-disbursement/provider-org>`
      - The organisation from which the planned disbursement will originate.
        If omitted the reporting-org is assumed.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/provider-org
      - 0..1
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/provider-org/\@ref
      - 0..1
      - 

    * - 
      - provider-activity-id
      - The identifier for the activity in which the planned disbursement will be reported. If omitted the current activity is assumed.
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/provider-org/\@provider-activity-id
      - 0..1
      - 

    * - 
      - type
      - The type of organisation providing the funds.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/planned-disbursement/provider-org/\@type
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/planned-disbursement/provider-org/narrative>`
      - The name of the organisation. This can be repeated in multiple languages
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/provider-org/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/provider-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/planned-disbursement/provider-org/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`receiver-org </activity-standard/iati-activities/iati-activity/planned-disbursement/receiver-org>`
      - The organisation receiving the money from the planned disbursement.
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/receiver-org
      - 0..1
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/receiver-org/\@ref
      - 0..1
      - 

    * - 
      - receiver-activity-id
      - If outgoing funds are being provided to another activity that is reported to IATI, this may, if possible, record the unique IATI activity identifier for that activity.
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/receiver-org/\@receiver-activity-id
      - 0..1
      - 

    * - 
      - type
      - The type of organisation receiving the funds.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/planned-disbursement/receiver-org/\@type
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/planned-disbursement/receiver-org/narrative>`
      - The name of the organisation. This can be repeated in multiple languages
      - 
      - 
      - iati-activities/iati-activity/planned-disbursement/receiver-org/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/planned-disbursement/receiver-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/planned-disbursement/receiver-org/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`capital-spend </activity-standard/iati-activities/iati-activity/capital-spend>`
      - 
      - The percentage of the total commitment that is for capital
        spending
      - 
      - 
      - iati-activities/iati-activity/capital-spend
      - 0..1
      - 

    * - 
      - percentage
      - The percentage of the total commitment allocated to or planned for capital expenditure. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/capital-spend/\@percentage
      - 1..1
      - 

    * - :doc:`transaction </activity-standard/iati-activities/iati-activity/transaction>`
      - 
      - Transactions recording committed or actual funds flowing in or
        out of an aid activity.
      - 
      - 
      - iati-activities/iati-activity/transaction
      - 0..*
      - 

    * - 
      - ref
      - An internal reference linking this transaction back to the publisher's financial management system.
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/\@ref
      - 0..1
      - 

    * - 
      - humanitarian
      - A process flag to indicate that this transaction relates entirely or partially to humanitarian aid. If the entire activity relates to humanitarian aid this should be reported using iati-activity/\@humanitarian, rather than for each transaction.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/transaction/\@humanitarian
      - 0..1
      - 

    * - 
      - :doc:`transaction-type </activity-standard/iati-activities/iati-activity/transaction/transaction-type>`
      - The type of the transaction (e.g. commitment,
        disbursement, expenditure, etc.).
      - 
      - 
      - iati-activities/iati-activity/transaction/transaction-type
      - 1..1
      - 

    * - 
      - code
      - A code from the specified vocabulary.
      - xsd:string
      - :doc:`/codelists/TransactionType`
      - iati-activities/iati-activity/transaction/transaction-type/\@code
      - 1..1
      - 

    * - 
      - :doc:`transaction-date </activity-standard/iati-activities/iati-activity/transaction/transaction-date>`
      - The date on which the transaction was made or (in the
        case of commitments) agreed. The narrative content may
        contain text (e.g. 2011Q1) for accurately recording less
        specific dates such as month, quarter, or year.
      - 
      - 
      - iati-activities/iati-activity/transaction/transaction-date
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/transaction/transaction-date/\@iso-date
      - 1..1
      - ``transaction-date/@iso-date`` must not be in the future.

    * - 
      - :doc:`value </activity-standard/iati-activities/iati-activity/transaction/value>`
      - Data type for an element containing a currency value.
      - 
      - 
      - iati-activities/iati-activity/transaction/value
      - 1..1
      - 

    * - 
      - currency
      - The ISO 4217 alphabetic currency code of the value reported.
        This is required unless the iati-activity/\@default-currency is present and applies.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/transaction/value/\@currency
      - 0..1
      - 

    * - 
      - value-date
      - The date to be used for determining the exchange rate for
        currency conversions.
      - xsd:date
      - 
      - iati-activities/iati-activity/transaction/value/\@value-date
      - 0..1
      - ``value/@value-date`` must not be in the future.

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/transaction/description>`
      - Data type for an element that must contain human-readable text.
        The information may be repeated in different languages.
      - 
      - 
      - iati-activities/iati-activity/transaction/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/transaction/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`provider-org </activity-standard/iati-activities/iati-activity/transaction/provider-org>`
      - For incoming funds this is the organisation from which
        the transaction originated. If omitted on outgoing funds
        the reporting-org is assumed.
      - 
      - 
      - iati-activities/iati-activity/transaction/provider-org
      - 0..1
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/provider-org/\@ref
      - 0..1
      - ``transaction/provider-org/@ref`` should match the regex ``[^\/\&\|\?]+``

    * - 
      - provider-activity-id
      - If incoming funds are being provided from the budget
        of another activity that is reported to IATI, it if
        STRONGLY RECOMMENDED that this should record the
        provider's unique IATI activity identifier for that
        activity.
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/provider-org/\@provider-activity-id
      - 0..1
      - 

    * - 
      - type
      - The type of organisation providing the funds.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/transaction/provider-org/\@type
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/provider-org/narrative>`
      - The name of the organisation. This can be repeated
        in multiple languages
      - 
      - 
      - iati-activities/iati-activity/transaction/provider-org/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/provider-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/provider-org/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`receiver-org </activity-standard/iati-activities/iati-activity/transaction/receiver-org>`
      - The organisation receiving the money from the transaction (if omitted on incoming funds then the receiver organisation is assumed to be the reporting organisation).
      - 
      - 
      - iati-activities/iati-activity/transaction/receiver-org
      - 0..1
      - 

    * - 
      - ref
      - Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/receiver-org/\@ref
      - 0..1
      - ``transaction/receiver-org/@ref`` should match the regex ``[^\/\&\|\?]+``

    * - 
      - receiver-activity-id
      - If outgoing funds are being provided to another activity that is reported to IATI, this may, if possible, record the unique IATI activity identifier for that activity.
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/receiver-org/\@receiver-activity-id
      - 0..1
      - 

    * - 
      - type
      - The type of organisation receiving the funds.
      - xsd:string
      - :doc:`/codelists/OrganisationType`
      - iati-activities/iati-activity/transaction/receiver-org/\@type
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/receiver-org/narrative>`
      - The name of the organisation. This can be repeated in multiple languages
      - 
      - 
      - iati-activities/iati-activity/transaction/receiver-org/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/receiver-org/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/receiver-org/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`disbursement-channel </activity-standard/iati-activities/iati-activity/transaction/disbursement-channel>`
      - The channel through which the funds will flow for this transaction, from an IATI codelist.
      - 
      - 
      - iati-activities/iati-activity/transaction/disbursement-channel
      - 0..1
      - 

    * - 
      - code
      - An IATI code defining channels of disbursement
      - xsd:string
      - :doc:`/codelists/DisbursementChannel`
      - iati-activities/iati-activity/transaction/disbursement-channel/\@code
      - 1..1
      - 

    * - 
      - :doc:`sector </activity-standard/iati-activities/iati-activity/transaction/sector>`
      - A recognised code, from a recognised vocabulary, classifying the purpose of this transaction.
        
        If this element is used then ALL transaction elements should contain a transaction/sector element and iati-activity/sector should NOT be used.
        
        This element can be used multiple times, but only one sector can be reported per vocabulary.
      - 
      - 
      - iati-activities/iati-activity/transaction/sector
      - 0..*
      - Either ``transaction/sector`` or ``sector`` must be present.

    * - 
      - vocabulary
      - An IATI code for the vocabulary (codelist) used for sector classifications. If omitted, OECD DAC 5-digit Purpose Codes are assumed.
        
        It is recommended that OECD DAC 5-digit Purpose Codes are used wherever possible. It is also recommended that if a publisher has its own classification system or systems, then the vocabularies 99 or 98 (Reporting Organisation's own vocabularies) should be used in addition to the DAC codes.
        
        Note that at transaction level, only one sector per vocabulary can be reported.
      - xsd:string
      - :doc:`/codelists/SectorVocabulary`
      - iati-activities/iati-activity/transaction/sector/\@vocabulary
      - 0..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/transaction/sector/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - code
      - The code for the sector.
      - xsd:string
      - (:doc:`/codelists/Sector`)
      - iati-activities/iati-activity/transaction/sector/\@code
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/sector/narrative>`
      - The free text description of the reporting organisation's own sector definition. This can be repeated in multiple languages
      - 
      - 
      - iati-activities/iati-activity/transaction/sector/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/sector/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/sector/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`recipient-country </activity-standard/iati-activities/iati-activity/transaction/recipient-country>`
      - A country that will benefit from this transaction.
        If a specific country is not known the recipient-region element should be used instead.
        
        If transaction/recipient-country AND/OR transaction/recipient-region are used THEN ALL transaction elements MUST contain a recipient-country or recipient-region element AND (iati-activity/recipient-country AND iati-activity/recipient-region MUST NOT be used)
      - 
      - 
      - iati-activities/iati-activity/transaction/recipient-country
      - 0..1
      - 

    * - 
      - code
      - ISO 3166-1 alpha-2 code for the country.
      - xsd:string
      - :doc:`/codelists/Country`
      - iati-activities/iati-activity/transaction/recipient-country/\@code
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/recipient-country/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/transaction/recipient-country/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/recipient-country/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/recipient-country/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`recipient-region </activity-standard/iati-activities/iati-activity/transaction/recipient-region>`
      - A supranational geopolitical region that will benefit from this transaction. If a specific country is not known, then this element MUST be used.
        
        If transaction/recipient-country AND/OR transaction/recipient-region are used THEN ALL transaction elements MUST contain a recipient-country or recipient-region element AND (iati-activity/recipient-country AND iati-activity/recipient-region MUST NOT be used)
      - 
      - 
      - iati-activities/iati-activity/transaction/recipient-region
      - 0..1
      - 

    * - 
      - code
      - Either an OECD DAC or UN region code. Codelist i determined by vocabulary attribute.
      - xsd:string
      - (:doc:`/codelists/Region`)
      - iati-activities/iati-activity/transaction/recipient-region/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - An IATI code for the vocabulary from which the region code is drawn. If it is not present 1 - 'OECD DAC' is assumed.
      - xsd:string
      - :doc:`/codelists/RegionVocabulary`
      - iati-activities/iati-activity/transaction/recipient-region/\@vocabulary
      - 0..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/transaction/recipient-region/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/transaction/recipient-region/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/transaction/recipient-region/narrative
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/transaction/recipient-region/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/transaction/recipient-region/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`flow-type </activity-standard/iati-activities/iati-activity/transaction/flow-type>`
      - Optional element to override the top-level default-flow-type element.
      - 
      - 
      - iati-activities/iati-activity/transaction/flow-type
      - 0..1
      - 

    * - 
      - code
      - A code from the OECD DAC CRS "Type of flow" codelist
      - xsd:string
      - :doc:`/codelists/FlowType`
      - iati-activities/iati-activity/transaction/flow-type/\@code
      - 1..1
      - 

    * - 
      - :doc:`finance-type </activity-standard/iati-activities/iati-activity/transaction/finance-type>`
      - Optional element to override the top-level default-finance-type element on a transaction-by-transaction basis, if needed.
      - 
      - 
      - iati-activities/iati-activity/transaction/finance-type
      - 0..1
      - 

    * - 
      - code
      - A code from the OECD DAC CRS "Type of finance" codelist
      - xsd:string
      - :doc:`/codelists/FinanceType`
      - iati-activities/iati-activity/transaction/finance-type/\@code
      - 1..1
      - 

    * - 
      - :doc:`aid-type </activity-standard/iati-activities/iati-activity/transaction/aid-type>`
      - A code from the specified vocabulary.
      - 
      - 
      - iati-activities/iati-activity/transaction/aid-type
      - 0..*
      - 

    * - 
      - code
      - A code from the specified vocabulary.
      - xsd:string
      - :doc:`/codelists/AidType`
      - iati-activities/iati-activity/transaction/aid-type/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.
      - xsd:string
      - :doc:`/codelists/AidTypeVocabulary`
      - iati-activities/iati-activity/transaction/aid-type/\@vocabulary
      - 0..1
      - 

    * - 
      - :doc:`tied-status </activity-standard/iati-activities/iati-activity/transaction/tied-status>`
      - Optional element to override the top-level default-tied-status element on a transaction-by-transaction basis if needed.
      - 
      - 
      - iati-activities/iati-activity/transaction/tied-status
      - 0..1
      - 

    * - 
      - code
      - An IATI code interpreting the usage of Columns 36-38 of the CRS++ reporting format. (Amount tied, Amount partially untied, Amount tied)
      - xsd:string
      - :doc:`/codelists/TiedStatus`
      - iati-activities/iati-activity/transaction/tied-status/\@code
      - 1..1
      - 

    * - :doc:`document-link </activity-standard/iati-activities/iati-activity/document-link>`
      - 
      - A link to an online, publicly accessible web page or document.
      - 
      - 
      - iati-activities/iati-activity/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - :doc:`related-activity </activity-standard/iati-activities/iati-activity/related-activity>`
      - 
      - Another separately reported IATI activity that is related to this one. The ‘type’ attribute describes the type of relationship: (eg. parent, child, multifunded). It is strongly recommended that linkage between activities in a hierarchical group should always be managed by use of this element with @type of 1 (parent) or 2 (child).
      - 
      - 
      - iati-activities/iati-activity/related-activity
      - 0..*
      - 

    * - 
      - ref
      - A valid activity identifier (as defined in iati-activity/iati-identifier).
      - xsd:string
      - 
      - iati-activities/iati-activity/related-activity/\@ref
      - 1..1
      - 

    * - 
      - type
      - An IATI code for the type of relationship
      - xsd:string
      - :doc:`/codelists/RelatedActivityType`
      - iati-activities/iati-activity/related-activity/\@type
      - 1..1
      - 

    * - :doc:`legacy-data </activity-standard/iati-activities/iati-activity/legacy-data>`
      - 
      - The legacy data element allows for the reporting of values held in a field in the reporting organisation's system which is similar, but not identical to an IATI element.
      - 
      - 
      - iati-activities/iati-activity/legacy-data
      - 0..*
      - 

    * - 
      - name
      - The original field name in the reporting organisation's system
      - xsd:string
      - 
      - iati-activities/iati-activity/legacy-data/\@name
      - 1..1
      - 

    * - 
      - value
      - The original field value in the reporting organisation's system
      - xsd:string
      - 
      - iati-activities/iati-activity/legacy-data/\@value
      - 1..1
      - 

    * - 
      - iati-equivalent
      - The name of the equivalent IATI element.
      - xsd:NMTOKEN
      - 
      - iati-activities/iati-activity/legacy-data/\@iati-equivalent
      - 0..1
      - 

    * - :doc:`conditions </activity-standard/iati-activities/iati-activity/conditions>`
      - 
      - Specific terms and conditions attached to the activity that, if not met, may influence the delivery of commitments made by participating organisations.
      - 
      - 
      - iati-activities/iati-activity/conditions
      - 0..1
      - 

    * - 
      - attached
      - A yes/no (1/0) value stating whether there are conditions attached to the activity. It is strongly recommended that this attribute is reported, even if there are no conditions attached (i.e. attached="0")
      - xsd:boolean
      - 
      - iati-activities/iati-activity/conditions/\@attached
      - 1..1
      - 

    * - 
      - :doc:`condition </activity-standard/iati-activities/iati-activity/conditions/condition>`
      - The text of a specific condition attached to the activity. Organisation-wide terms and conditions that apply to all activities should not be reported here, but in either iati-organisation/document-link or iati-activity-document-link
      - 
      - 
      - iati-activities/iati-activity/conditions/condition
      - 0..*
      - 

    * - 
      - type
      - An IATI code defining the type of condition.
      - xsd:string
      - :doc:`/codelists/ConditionType`
      - iati-activities/iati-activity/conditions/condition/\@type
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/conditions/condition/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/conditions/condition/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/conditions/condition/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/conditions/condition/narrative/\@xml:lang
      - 0..1
      - 

    * - :doc:`result </activity-standard/iati-activities/iati-activity/result>`
      - 
      - A container for reporting outputs, outcomes, impacts and other results that stem directly from the activity. This may be repeated for each type of result reported.
      - 
      - 
      - iati-activities/iati-activity/result
      - 0..*
      - 

    * - 
      - type
      - An IATI code for the type of result being reported.
      - xsd:string
      - :doc:`/codelists/ResultType`
      - iati-activities/iati-activity/result/\@type
      - 1..1
      - 

    * - 
      - aggregation-status
      - Boolean flag indicating whether the data in the result set are suitable for aggregation.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/result/\@aggregation-status
      - 0..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/description>`
      - A longer, human-readable description.
      - 
      - 
      - iati-activities/iati-activity/result/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`document-link </activity-standard/iati-activities/iati-activity/result/document-link>`
      - A link to an online, publicly accessible web page or document expanding on the result.
      - 
      - 
      - iati-activities/iati-activity/result/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/result/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/result/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/result/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/result/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/result/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/result/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/result/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`reference </activity-standard/iati-activities/iati-activity/result/reference>`
      - A reference element to allow for the coded identification of a results framework.
      - 
      - 
      - iati-activities/iati-activity/result/reference
      - 0..*
      - 

    * - 
      - code
      - A code from the codelist identified in vocabulary that identifies a results framework.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/reference/\@code
      - 1..1
      - 

    * - 
      - vocabulary
      - A code for the results framework vocabulary. The code must be a valid value in the ResultVocabulary codelist.
      - xsd:string
      - :doc:`/codelists/ResultVocabulary`
      - iati-activities/iati-activity/result/reference/\@vocabulary
      - 1..1
      - 

    * - 
      - vocabulary-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/reference/\@vocabulary-uri
      - 0..1
      - 

    * - 
      - :doc:`indicator </activity-standard/iati-activities/iati-activity/result/indicator>`
      - The indicator(s) that meet the results. There can be multiple indicators for each result.
      - 
      - 
      - iati-activities/iati-activity/result/indicator
      - 1..*
      - 

    * - 
      - measure
      - An IATI code defining the unit of measure in which the value is reported.
      - xsd:string
      - :doc:`/codelists/IndicatorMeasure`
      - iati-activities/iati-activity/result/indicator/\@measure
      - 1..1
      - 

    * - 
      - ascending
      - A boolean describing the behaviour of the indicator.
        It is "true" if the indicator improves from small to large (e.g. clinics built); false if it improves from large to small (e.g. cases of a disease).
      - xsd:boolean
      - 
      - iati-activities/iati-activity/result/indicator/\@ascending
      - 0..1
      - 

    * - 
      - aggregation-status
      - Boolean flag indicating whether the data in the result set are suitable for aggregation.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/result/indicator/\@aggregation-status
      - 0..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/indicator/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/indicator/description>`
      - A longer, human-readable description.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`document-link </activity-standard/iati-activities/iati-activity/result/indicator/document-link>`
      - A link to an online, publicly accessible web page or document expanding on the result.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/indicator/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/result/indicator/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/indicator/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/indicator/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/result/indicator/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/result/indicator/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/result/indicator/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/result/indicator/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`reference </activity-standard/iati-activities/iati-activity/result/indicator/reference>`
      - A standardised means of identifying the indicator from a code in a recognised vocabulary. Multiple vocabularies may be specified, but each vocabulary may be specified only once for each indicator.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/reference
      - 0..*
      - There must be no more than one element or attribute matched at ``reference[1]`` or ``../reference[1]``.

    * - 
      - vocabulary
      - A code for a recognised vocabulary of indicators. The value for this field should appear in the IndicatorVocabulary codelist.
      - xsd:string
      - :doc:`/codelists/IndicatorVocabulary`
      - iati-activities/iati-activity/result/indicator/reference/\@vocabulary
      - 1..1
      - 

    * - 
      - code
      - A code for an indicator defined in the specified vocabulary specified.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/reference/\@code
      - 1..1
      - 

    * - 
      - indicator-uri
      - The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/indicator/reference/\@indicator-uri
      - 0..1
      - 

    * - 
      - :doc:`baseline </activity-standard/iati-activities/iati-activity/result/indicator/baseline>`
      - The baseline value for the indicator
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline
      - 0..*
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/baseline/\@iso-date
      - 0..1
      - 

    * - 
      - year
      - The year the baseline value was taken (yyyy)
      - xsd:positiveInteger
      - 
      - iati-activities/iati-activity/result/indicator/baseline/\@year
      - 1..1
      - 

    * - 
      - value
      - The baseline value.
        
        This should be a numeric value if the measure is quantitative.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/\@value
      - 0..1
      - 

    * - 
      - :doc:`location </activity-standard/iati-activities/iati-activity/result/indicator/baseline/location>`
      - A location already defined and described in the iati-activity/location element.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/location
      - 0..*
      - 

    * - 
      - ref
      - A cross-reference to the internal reference assigned to a defined location: iati-activity/location/\@ref.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/location/\@ref
      - 0..1
      - 

    * - 
      - :doc:`dimension </activity-standard/iati-activities/iati-activity/result/indicator/baseline/dimension>`
      - A category used for disaggregating the result by gender, age, etc.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/dimension
      - 0..*
      - 

    * - 
      - name
      - Freetext description of a category being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/dimension/\@name
      - 0..1
      - 

    * - 
      - value
      - Description of the value being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/dimension/\@value
      - 0..1
      - 

    * - 
      - :doc:`document-link </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link>`
      - A link to an online, publicly accessible web page or document expanding on the result.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/result/indicator/baseline/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/baseline/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/result/indicator/baseline/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/baseline/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/baseline/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`comment </activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment>`
      - A human-readable comment associated with a piece of aid information.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/comment
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/baseline/comment/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/baseline/comment/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/baseline/comment/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/baseline/comment/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`period </activity-standard/iati-activities/iati-activity/result/indicator/period>`
      - The period covered for the results reported. Multiple periods can be reported for a single indicator.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period
      - 0..*
      - 

    * - 
      - :doc:`period-start </activity-standard/iati-activities/iati-activity/result/indicator/period/period-start>`
      - The start of the reporting period.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/period-start
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/period/period-start/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`period-end </activity-standard/iati-activities/iati-activity/result/indicator/period/period-end>`
      - The end of the reporting period.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/period-end
      - 1..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/period/period-end/\@iso-date
      - 1..1
      - ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``

    * - 
      - :doc:`target </activity-standard/iati-activities/iati-activity/result/indicator/period/target>`
      - The target milestone for this period
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target
      - 0..*
      - 

    * - 
      - value
      - The target value.
        
        This should be a numeric value if the measure is quantitative.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/\@value
      - 0..1
      - 

    * - 
      - :doc:`location </activity-standard/iati-activities/iati-activity/result/indicator/period/target/location>`
      - A location already defined and described in the iati-activity/location element.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/location
      - 0..*
      - 

    * - 
      - ref
      - A cross-reference to the internal reference assigned to a defined location: iati-activity/location/\@ref.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/location/\@ref
      - 0..1
      - 

    * - 
      - :doc:`dimension </activity-standard/iati-activities/iati-activity/result/indicator/period/target/dimension>`
      - A category used for disaggregating the result by gender, age, etc.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/dimension
      - 0..*
      - 

    * - 
      - name
      - Freetext description of a category being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/dimension/\@name
      - 0..1
      - 

    * - 
      - value
      - Description of the value being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/dimension/\@value
      - 0..1
      - 

    * - 
      - :doc:`comment </activity-standard/iati-activities/iati-activity/result/indicator/period/target/comment>`
      - A human-readable comment associated with a piece of aid information.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/comment
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/target/comment/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/comment/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/comment/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/target/comment/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`document-link </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link>`
      - A link to an online, publicly accessible web page or document expanding on the result.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/result/indicator/period/target/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/target/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/target/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/result/indicator/period/target/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/target/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/result/indicator/period/target/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/period/target/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`actual </activity-standard/iati-activities/iati-activity/result/indicator/period/actual>`
      - A record of the achieved result for this period.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual
      - 0..*
      - 

    * - 
      - value
      - The actual measure.
        
        This should be a numeric value if the measure is quantitative.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/\@value
      - 0..1
      - 

    * - 
      - :doc:`location </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/location>`
      - A location already defined and described in the iati-activity/location element.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/location
      - 0..*
      - 

    * - 
      - ref
      - A cross-reference to the internal reference assigned to a defined location: iati-activity/location/\@ref.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/location/\@ref
      - 0..1
      - 

    * - 
      - :doc:`dimension </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/dimension>`
      - A category used for disaggregating the result by gender, age, etc.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/dimension
      - 0..*
      - 

    * - 
      - name
      - Freetext description of a category being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/dimension/\@name
      - 0..1
      - 

    * - 
      - value
      - Description of the value being disaggregated.
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/dimension/\@value
      - 0..1
      - 

    * - 
      - :doc:`comment </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/comment>`
      - A human-readable comment associated with a piece of aid information.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/comment
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/comment/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/comment/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/comment/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/actual/comment/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`document-link </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link>`
      - A link to an online, publicly accessible web page or document expanding on the result.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link
      - 0..*
      - 

    * - 
      - url
      - The target URL of the external document, e.g. "http://www.example.org/doc.odt".
      - xsd:anyURI
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/\@url
      - 1..1
      - 

    * - 
      - format
      - An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".
      - xsd:string
      - :doc:`/codelists/FileFormat`
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/\@format
      - 1..1
      - 

    * - 
      - :doc:`title </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/title>`
      - A short, human-readable title.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/title
      - 1..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/title/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/title/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/title/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/title/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`description </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/description>`
      - A description of the document contents, or guidance on where to access the relevant information in the document.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/description
      - 0..1
      - 

    * - 
      - :doc:`narrative </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/description/narrative>`
      - The free text name or description of the item being described. This can
        be repeated in multiple languages.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/description/narrative
      - 1..*
      - 

    * - 
      - 
      - 
      - xsd:string
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/description/narrative/text()
      - 
      - 

    * - 
      - xml:lang
      - A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.
      - 
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/description/narrative/\@xml:lang
      - 0..1
      - 

    * - 
      - :doc:`category </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/category>`
      - IATI Document Category Code
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/category
      - 1..*
      - 

    * - 
      - code
      - An IATI code defining the category of the document.
      - xsd:string
      - :doc:`/codelists/DocumentCategory`
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/category/\@code
      - 1..1
      - 

    * - 
      - :doc:`language </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/language>`
      - The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/language
      - 0..*
      - 

    * - 
      - code
      - ISO 639-1 language code
      - xsd:string
      - :doc:`/codelists/Language`
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/language/\@code
      - 1..1
      - 

    * - 
      - :doc:`document-date </activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date>`
      - The date of publication of the document that is being linked to.
      - 
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date/\@iso-date
      - 1..1
      - 

    * - :doc:`crs-add </activity-standard/iati-activities/iati-activity/crs-add>`
      - 
      - Additional items specific to CRS++ reporting.
      - 
      - 
      - iati-activities/iati-activity/crs-add
      - 0..1
      - 

    * - 
      - :doc:`other-flags </activity-standard/iati-activities/iati-activity/crs-add/other-flags>`
      - This covers the four CRS++ columns titled:
        "Free standing technical cooperation";
        "Programme-based approach";
        "Investment project";
        "Associated financing"
      - 
      - 
      - iati-activities/iati-activity/crs-add/other-flags
      - 0..*
      - 

    * - 
      - code
      - An IATI code describing the equivalent CRS++ columns
      - xsd:string
      - :doc:`/codelists/CRSAddOtherFlags`
      - iati-activities/iati-activity/crs-add/other-flags/\@code
      - 1..1
      - 

    * - 
      - significance
      - A boolean indicating whether the flag applies. If 'false' do not report the flag
      - xsd:boolean
      - 
      - iati-activities/iati-activity/crs-add/other-flags/\@significance
      - 1..1
      - 

    * - 
      - :doc:`loan-terms </activity-standard/iati-activities/iati-activity/crs-add/loan-terms>`
      - Loan repayment terms and interest rates
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms
      - 0..1
      - 

    * - 
      - rate-1
      - Interest Rate. If an ODA loan with variable interest rate, report the variable rate here and the reference fixed rate as rate-2
        
        Enter the rate without the percentage sign.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/\@rate-1
      - 0..1
      - 

    * - 
      - rate-2
      - Second Interest Rate.  If an ODA loan with variable interest rate, report the variable rate as rate-1 and the reference fixed rate here
        
        Enter the rate without the percentage sign.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/\@rate-2
      - 0..1
      - 

    * - 
      - :doc:`repayment-type </activity-standard/iati-activities/iati-activity/crs-add/loan-terms/repayment-type>`
      - The type of loan repayment
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-type
      - 0..1
      - 

    * - 
      - code
      - An IATI codelist tabulating CRS-specified values for the type of Repayment.
      - xsd:string
      - :doc:`/codelists/LoanRepaymentType`
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-type/\@code
      - 1..1
      - 

    * - 
      - :doc:`repayment-plan </activity-standard/iati-activities/iati-activity/crs-add/loan-terms/repayment-plan>`
      - Number of repayments per annum.
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-plan
      - 0..1
      - 

    * - 
      - code
      - An IATI codelist tabulating CRS-specified values for the number of repayments per annum.
      - xsd:string
      - :doc:`/codelists/LoanRepaymentPeriod`
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-plan/\@code
      - 1..1
      - 

    * - 
      - :doc:`commitment-date </activity-standard/iati-activities/iati-activity/crs-add/loan-terms/commitment-date>`
      - The CRS++ reported commitment date
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/commitment-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/commitment-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`repayment-first-date </activity-standard/iati-activities/iati-activity/crs-add/loan-terms/repayment-first-date>`
      - First Repayment Date.
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-first-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-first-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`repayment-final-date </activity-standard/iati-activities/iati-activity/crs-add/loan-terms/repayment-final-date>`
      - Final Repayment Date.
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-final-date
      - 0..1
      - 

    * - 
      - iso-date
      - 
      - xsd:date
      - 
      - iati-activities/iati-activity/crs-add/loan-terms/repayment-final-date/\@iso-date
      - 1..1
      - 

    * - 
      - :doc:`loan-status </activity-standard/iati-activities/iati-activity/crs-add/loan-status>`
      - The status of loan and interest repayments for the most recently reported financial year
      - 
      - 
      - iati-activities/iati-activity/crs-add/loan-status
      - 0..1
      - 

    * - 
      - year
      - CRS Reporting Year (CRS++ Column 1)
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-status/\@year
      - 1..1
      - 

    * - 
      - currency
      - The ISO 4217 alphabetic currency code of the value reported.
        This is required unless the iati-activity/\@default-currency is present and applies.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/crs-add/loan-status/\@currency
      - 0..1
      - 

    * - 
      - value-date
      - The date to be used for determining the exchange rate for
        currency conversions.
      - xsd:date
      - 
      - iati-activities/iati-activity/crs-add/loan-status/\@value-date
      - 0..1
      - 

    * - 
      - :doc:`interest-received </activity-standard/iati-activities/iati-activity/crs-add/loan-status/interest-received>`
      - Interest received during the reporting year
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-status/interest-received
      - 0..1
      - 

    * - 
      - :doc:`principal-outstanding </activity-standard/iati-activities/iati-activity/crs-add/loan-status/principal-outstanding>`
      - The amount of principal owed on the loan at the end of the reporting year.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-status/principal-outstanding
      - 0..1
      - 

    * - 
      - :doc:`principal-arrears </activity-standard/iati-activities/iati-activity/crs-add/loan-status/principal-arrears>`
      - Arrears of principal at the end of the year. Included in principal-outstanding
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-status/principal-arrears
      - 0..1
      - 

    * - 
      - :doc:`interest-arrears </activity-standard/iati-activities/iati-activity/crs-add/loan-status/interest-arrears>`
      - Arrears of interest at the end of the year
      - xsd:decimal
      - 
      - iati-activities/iati-activity/crs-add/loan-status/interest-arrears
      - 0..1
      - 

    * - 
      - :doc:`channel-code </activity-standard/iati-activities/iati-activity/crs-add/channel-code>`
      - The CRS channel code for this activity. This should only be used for reporting to CRS. The code list contains both organisation types and names of organisations. For non-CRS purposes these should be reported using the participating-org element.
      - xsd:string
      - 
      - iati-activities/iati-activity/crs-add/channel-code
      - 0..1
      - 

    * - :doc:`fss </activity-standard/iati-activities/iati-activity/fss>`
      - 
      - This section allows entry of data required for the OECD DAC Forward Spending Survey at an activity level.
      - 
      - 
      - iati-activities/iati-activity/fss
      - 0..1
      - 

    * - 
      - extraction-date
      - The exact date when the information was collected or extracted from donors' aid management systems.
      - xsd:date
      - 
      - iati-activities/iati-activity/fss/\@extraction-date
      - 1..1
      - 

    * - 
      - priority
      - True if the partner country is a priority partner country.
      - xsd:boolean
      - 
      - iati-activities/iati-activity/fss/\@priority
      - 0..1
      - 

    * - 
      - phaseout-year
      - If there are plans to phase out operations from the partner country, this column shows the projected year of last disbursements.
      - xsd:decimal
      - 
      - iati-activities/iati-activity/fss/\@phaseout-year
      - 0..1
      - 

    * - 
      - :doc:`forecast </activity-standard/iati-activities/iati-activity/fss/forecast>`
      - A container to hold separate forecasts for each of the years specified Text() holds the forecast value for each year.
      - 
      - 
      - iati-activities/iati-activity/fss/forecast
      - 0..*
      - 

    * - 
      - 
      - 
      - xsd:decimal
      - 
      - iati-activities/iati-activity/fss/forecast/text()
      - 
      - 

    * - 
      - year
      - The calendar year that the forward spend covers
      - xsd:decimal
      - 
      - iati-activities/iati-activity/fss/forecast/\@year
      - 1..1
      - 

    * - 
      - currency
      - The ISO 4217 alphabetic currency code of the value reported.
        This is required unless the iati-activity/\@default-currency is present and applies.
      - xsd:string
      - :doc:`/codelists/Currency`
      - iati-activities/iati-activity/fss/forecast/\@currency
      - 0..1
      - 

    * - 
      - value-date
      - The date to be used for determining the exchange rate for
        currency conversions.
      - xsd:date
      - 
      - iati-activities/iati-activity/fss/forecast/\@value-date
      - 0..1
      - 


::

  
        International Aid Transparency Initiative: Activity-Information Schema
  
        Release 2.03, 2018-02-19
  
        NOTE: the xml.xsd and iati-common.xsd schemas must be in the
        same directory as this one.
  
        This W3C XML Schema defines an XML document type for information
        about one or more aid-related activities, following the standard
        published at http://iatistandard.org/
  
        This document type may be extended with additional elements and
        attributes, but they must belong to an explicit XML namespace.
      