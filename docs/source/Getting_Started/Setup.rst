Platform Setup
==============
This page describes how you can get started as quick as possible!

Login & Team Environment
------------------------
You can easily sign up at https://portal.amplo.ch. Make sure you use your business email,
as this will be used to recognize your colleagues. After verifying your account, the first
colleague to register enters the setup screen. Here he/she sets up the machines and incidents.


Machines & Incidents
--------------------
Within the Smart Maintenance Platform, you have separated environments for each machine,
with their own data connectors, processors, incidents and models.
Every machine you add will have its own list of incidents. Note that these incidents will
have their all have their own model, and therefore define what is being predicted.

.. note::
    When your machines have many custom elements or models, the level of segregation may be
    difficult to determine. Try to segregate machines that have different sensor measurements,
    data processing steps, incidents or key indicators for root cause while limiting the total
    number of machines. Every added machine requires its own set of training data, integration
    and setup.

.. note::
    The level of segregation for incidents may also not be straight forward. In general,
    we advise to define the incidents as per resolution. So if two different incidents are
    solved by the same resolution, it is smart to combine the two into one resolution, e.g.
    full sub-system replacement.

.. _`ref-data-integration`:

Data Integration
----------------

Though all functionality of the platform is available without integrating a single element,
the true power only becomes apparent when integrated deeply into your existing workflows
and IT landscape. It automates manual steps, saving time while gaining robustness and consistency.
We have three types of data integrations, `Storage Connections`, `Event Driven` and `Data Streams`. Event Driven data
connectors only send measurement data when a specific event is triggered, such as the creation
of a service ticket or a specific alarm. Data Streams is a continuous connection, where measurement
data is send at a fixed interval (often once a second to once a minute).

Storage Connections
^^^^^^^^^^^^^^^^^^^
With the purpose of creating the initial training data and getting a maximum amount of
operational data for anomaly detection, we have off the shelf data connectors for:
* Google Cloud Storage
* Amazon Web Services S3
* Azure Blob Storage

.. note::
    If your cloud vendor or storage service is not listed, we're more than happy to add a few names on our list!

Google Cloud Storage
~~~~~~~~~~~~~~~~~~~~
Google Cloud Storage requires a few items for setting up. To set this up, click on `Machine Data` in the `Integrations`
section of the menu. On the left, you see a card for Storage Connections with a Google Cloud Storage inside. When you
click on the plus icon, the setup screen will open.

**1. Authentication**
First, you need to attach a Service Key as a file or as a raw JSON. The Service Account for this Service Key needs the
`storage.objects.get` and `storage.buckets.get` permissions.

**2. Bucket Name**
The Service Key already contains your `Project ID`, so we only need the `Bucket Name` (or names in case of multiple) to
identify the location of your measurement data.

**3. Timestamp & Serial Identification**
In order to link the data to the ticket system to determine whether it's incident or healthy data, we need to establish
a a timestamp and serial number per file / sample. This can be done either by filename with regular expressions or by
column inside the data.

**4. Convert**
In case you use a specific data format (such as Avro or CAN), you have the option to add a small data processor.
Standard, we support CSV, JSON, XML, Feather, Parquet and Stata. In case you use these file formats, you don't need to
use specify this.

Event Driven
^^^^^^^^^^^^
Event Driven integration goes through APIs. Head over `Machine Data` under `Integrations`.
Here you find

.. _`ref-data-streams`:

Data Streams
^^^^^^^^^^^^

bla bla

.. _`ref-ticket-integration`:

Ticket System Integration
-------------------------

blabla

