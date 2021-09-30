Labelling
=========

Though all your measurement data is organised by :doc:`../Services` and Incident, 
some log files require some further attention before you can start :doc:`Training` models:

- Long :ref:`ref-automated-diagnostics` logs (>5s)
- :ref:`ref-predictive-maintenance` logs for degradation curves

.. image:: ../images/labelling.PNG
  :width: 600
  :alt: Amplo

Labelling Automated Diagnostics Logs
---------------------------------------------
When Automated Diagnostics logs are above 5 seconds, it's often helpfull to mark the interval where the failure 
patterns are most obvious in the data. When you mark the failure, all unmarked data will be disregarded when 
you train the corresponding model. 
You can open the label interface shown in the picture below from the :doc:`Data` or from a :ref:`ref-labeljobs`. 

- Use the select bar above the graph to (de)select the columns shown in the graph. 
- Use the brush to scroll through the timeline of the log. 
- Double click on the graph to show the entire timeline. 
- Hold shift and drag from left to right to mark a faulty interval. 
- With the top left 

Labelling Predictive Maintenance Logs
-------------------------------------




.. _ref-labeljobs:

Label Jobs
----------
