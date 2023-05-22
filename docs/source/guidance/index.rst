.. _guidance:

Guidance
============

This page contains general guidance about minting DOIs that is not directly relevant to any particular metadata field.

Datasets that will be available in the future
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If a dataset is not yet available for sharing but will be in the future (i.e. 'under embargo') then it can still be included in the HeSANDA catalogue. This may include if
data collection is still being completed or if the main results are still being prepared for publication. To indicate your dataset will be available in the future:

* In DataCite 5 PublicationYear, indicate the year that the data will be available for sharing
* In the ANZCTR Data Sharing Statement, include the date that the dataset will be available for sharing as part of your response to the questions "When will data be available (start and end dates)?". An approximate date (e.g. July 2024) is acceptable.

**Optional:** you may also include the date in DataCite 8 Date. If you do this, you must specify the value "Available" for the associated field DataCite 8.a dateType

As per the `DataCite v.4.4 schema documentation <https://schema.datacite.org/meta/kernel-4.4/doc/DataCite-MetadataKernel_v4.4.pdf>`_ (Page 16), the definition of PublicationYear
is: "The year when the data was or will be made publicly available". Furthermore:

"If an embargo period has been in effect, use the date when the embargo period ends. In the case of datasets, "publish" is understood to mean making the data available on a specific
date to the community of researchers. If there is no standard publication year value, use the date that would be preferred from a citation perspective."

DOI state and workflow
~~~~~~~~~~~~~~~~~~~~~~

The "state" of a DOI refers to the stage of the minting workflow it is in

**Draft:** The unique DOI has been reserved but not registered in the DOI system. Draft DOIs can be deleted.
**Registered:** The unique DOI has been registered in the DOI system, but hidden in search results. The DOI can no longer be deleted.
**Findable:** The unique DOI can now be found in searches. It cannot be deleted, but it can be hidden from searches by being reverted back to the Registered state.

DOIs can be freely swapped between Registered and Findable. Once a DOI leaves Draft state, it can never revert to Draft state.

Landing pages
~~~~~~~~~~~~~

A landing page is a human-readable web page that describes the object that you are minting a DOI for. For example, a dataset's
landing page will provide the "who what when where why how" such as who created it, what it covers, when and where it was created,
and so on. DataCite provides `information on best practice for landing pages <https://support.datacite.org/docs/landing-pages>`_.
A landing page should be hosted on your own systems, such as in a data repository or on a website.

For each landing page link, a full stop (.) will need to be included in the url, or www.
For example, the link to the landing page cannot be https://trog.com.au//landingpage .
Instead, it must to be https://www.trog.com.au/landingpage

Metadata format - XML or JSON
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

DataCite metadata can be fully expressed in either XML or JSON formats. There is no advantage to one over the other
beyond the technical requirements of your systems and workflows.

The metadata must conform to both the DataCite metadata standard 4.4 as well as this HeSANDA metadata profile.

`DataCite's Fabrica service can be used to validate metadata <https://support.datacite.org/docs/how-do-i-validate-doi-metadata>`_ against the DataCite metadata schema.

What needs to have a DOI?
~~~~~~~~~~~~~~~~~~~~~~~~~

The most important thing in HeSANDA is the Individual Participant Data (IPD) - the DOI created for this artifact is essential for having a dataset appear in the
HeSANDA catalogue.

Other artifacts of the study, such as a data dictionary or study protocol, can also have DOIs minted for them, with fewer required metadata fields than for the IPD:

* Landing page URL
* Creator
* Title
* Publisher
* Publication year
* Resource type general - "Text" for a data dictionary, "Workflow" for a study protocol

How can I remove a dataset from the portal?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If a dataset needs to be withdrawn, the DOI needs to be edited so that it points to a "Tombstone" page, but left Findable state.
If a DOI was created in error, its "state" needs to be to be changed from a Findable to a Registered state. This will stop the dataset from appearing in the portal.

