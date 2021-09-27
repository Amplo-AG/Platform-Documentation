Machine Learning Services
=========================

This section describes in more detail the requirements for data, setup & integration.


Automated Diagnostics
---------------------
Automated Diagnostics is a service dedicated to reduce Time To Diagnose & Time To Resolve. Instead of hours of data
analyses and field inspections, Machine Learning models can accurately determine the root cause of incidents and
directly instruct the optimal resolution.
This service is often the first to be implemented as it can be done manually, and therefore without intrusive
infrastructural setup. However, the manual approach is more time consuming than the automatic setup, as will become
obvious from the explanation below.

**Training Data**

To detect the root cause of a malfunctioning machine, machine learning models are trained on snapshots of data. These
snapshots are ideally short (~5 seconds) during which the failure occurred or its consequences are most noticeable.
If you are unable to extract the exact time interval of the occurred incident, try and limit the window of the snapshot
to 1 day. For longer logs, we internally analyse where in the snapshot the failure patterns are most present and filter
the rest.
The training data may contain as many sensor measurements and flags / status' as is available. See
:doc:`Custom Flags <Processing/Custom Flags>` to find out how to extract additional information such as Serial Numbers.
If possible, having a timestamp to every data point is extremely useful. This allows for additional resampling
strategies.
Though it slightly depends on the complexity of the incident, a rule of thumb is that we need a minimum of 20-30
faulty snapshots per incident and 100+ snapshots of healthy data.

**Automatic Setup**

blabla

**Manual Setup**

blabla

**Integration**

blabla


Anomaly Detection
-----------------

**Training Data**

blabla

**Setup**

blabla

**Integration**

blabla


Condition Monitoring
--------------------

**Training Data**

blabla

**Setup**

blabla

**Integration**

blabla


Predictive Maintenance
----------------------

**Training Data**

blabla

**Setup**

blabla

**Integration**

blabla
