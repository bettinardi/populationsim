.. PopulationSim documentation master file
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. |br| raw:: html

   <br />
   
Validation of Results
=====================

One of the most critical steps in the population synthesis procedure is the validation of the synthetic population. Validation can give us clues about inconsistencies among controls, data processing errors or misspecification of settings. This section provides general guidelines on validation procedures

What to validate?
------------------

At a regional level, for each control, total number of records (household/person) specified, the total number of records synthesized, the difference between the synthesized totals and the control totals and the percentage difference are reported automatically by PopulationSim. Most population synthesizers will match each control very well at a regional level; therefore such summaries are useful but not very insightful into the goodness-of-fit of the tool at lower level geographies.

Statistics that inform us of convergence at a more disaggregate level are also computed – please note that these statistics are being computed for the geography at which the controls are specified i.e. MAZ, TAZ or Meta as the case might be. The following three statistics are computed as a part of this exercise: |br| 
(1)	the average percentage difference between the control totals and the synthesized totals, |br|  
(2)	the standard deviation (STDEV) of the percentage difference – this measure informs us of how much dispersion from the average exists, and  |br| 
(3)	the percentage root mean square error (RMSE) - an indicator of the proximity of synthesized and control totals. |br|  
The number of geographies for which the control is non-zero (N) are also reported.

Charts & Plots
--------------

Validation Charts
~~~~~~~~~~~~~~~~~

The validation chart is a visualization of the disaggregate summary statistics – mean percentage difference, STDEV and RMSE of percentage differences. A form of dot and whisker plot is generated for each control where the dots are the mean percentage differences and horizontal bars are twice the STDEV or RMSE centered around zero. An example validation chart is below:



	.. image:: images/validation.jpeg

Frequency Distribution Plots
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These are simply frequency distribution plots of differences between control and synthesized values across the geography at which the controls were specified. An example frequency distribution plot is below:

  .. image:: images/hh_inc_30_60_control.png

Expansion Factor Distributions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

While a synthetic population may match the controls well, it is important to know how uniform the household weights are, and how different they are from the initial weights. The closer the final weights are to the initial PUMS weight, the higher the probability of matching the distribution of uncontrolled variables. An expansion factor is computed for each record in the seed data as total final weight/initial weight. A distribution plot of these expansion factors is created for each Seed geography. A good synthetic population would have most of these expansion factors as close to one as possible. An example expansion factor distribution is shown below:

  .. image:: images/EF-Distribution.png

Resources
---------

Validation R Script
~~~~~~~~~~~~~~~~~~~~


