Workflow
========

Before we start using the platform, we want to explain the general workflow. 
This consist of :
* :doc:`Data`
* :doc:`Labelling`
* :doc:`Training`
* :doc:`Models`
* :doc:`Diagnostics`
* **coming soon** Condition Monitoring
* **coming soon** Anomaly Detection
* **coming soon** Predictive Maintenance

Data is at the heart of machine learning, and therefore at the heart of this Smart Maintenance Platform. 
Even when you made the necessary :ref:`ref-data-integration`, the :doc:`Data` keeps track of your training 
data. You can inspect your training data here and see all made changes. 
In order to distinguish between incidents, data needs to be labelled. The :doc:`Labelling` helps you with this. 
It allows you to mark intervals of incident occurance, mark remaining useful lifetimes and the useful features. 
It also closes provides a feedback loop so newly occuring incidents are used to enrich the training data. 
With a labelled and organised training data set, you can start training models in the :doc:`Training`. 
We made this as easy as possible, but it will a bit of time to run! 
Once completed, you can see the results and all other information in the :doc:`Models`. You can directly use the different 
services on the platform and over APIs!

Additionally to this workflow, there are some more advanced topics which you may want to use:
* :doc:`Preprocessor.rst`
* :doc:`Permissions.rst`
* :doc:`APIs.rst`
