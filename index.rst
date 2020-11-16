..
  Technote content.

  See https://developer.lsst.io/restructuredtext/style.html
  for a guide to reStructuredText writing.

  Do not put the title, authors or other metadata in this document;
  those are automatically added.

  Use the following syntax for sections:

  Sections
  ========

  and

  Subsections
  -----------

  and

  Subsubsections
  ^^^^^^^^^^^^^^

  To add images, add the image file (png, svg or jpeg preferred) to the
  _static/ directory. The reST syntax for adding the image is

  .. figure:: /_static/filename.ext
     :name: fig-label

     Caption text.

   Run: ``make html`` and ``open _build/html/index.html`` to preview your work.
   See the README at https://github.com/lsst-sqre/lsst-technote-bootstrap or
   this repo's README for more info.

   Feel free to delete this instructional comment.

:tocdepth: 1

.. Please do not modify tocdepth; will be fixed when a new Sphinx theme is shipped.

.. sectnum::

.. TODO: Delete the note below before merging new content to the master branch.

.. note::

   **This technote is not yet published.**

   This technote will describe metrics to evaluate the LSST survey strategy performance for detecting galactic microlensing and Tidal Disruption Events.

.. Add content here.
.. Do not include the document title (it's automatically added from metadata.yaml).

Introduction
============

In this tech note we discuss science metrics for two types of transient objects, fast microlensing events and tidal disruption events (TDEs).

Code for running these metrics and generating the plots in this note are in a jupyter notebook microlensing_and_tde_metrics.ipynb xxx-link to github.

xxx-are we applying dust to TDEs?

For both of these metrics, we will compare their performance on two different simulatied surveys, `baseline_nexp2_v1_6` and `combo_dust_nexp2_v1_6`. The main diffference between these simulations is `combo_dust_nexp2_v1_6` avoids dusty regions of the galactic plane and covers the bulge as part of the wide-fast-deep survey.

.. image:: /_static/thumb.baseline_nexp2_v1_6_10yrs_CoaddM5_r_and_note_not_like_DD_HEAL_SkyMap.png
   :width: 49%
.. image:: /_static/thumb.combo_dust_nexp2_v1_6_10yrs_CoaddM5_r_and_note_not_like_DD_HEAL_SkyMap.png
   :width: 49%



Tidal Disruption Events
=======================




.. figure:: /_static/tde_lc.png
   :name: fig-tde_lc

   Example light curve shapes used for TDEs. 




Microlensing
============

Microlensing events are generated with a crossing times drawn uniformly from 1 to 10 days, and impact parameters drawn from 0 to 1, and distributed on the sky 



xxx---the criteria for detecting a microlensing event:  
2 points detected before maximum, and 2 points detected post maximum. By default, we assume the lensed object is an r=20 point source (flat SED) and demand that the amplification be detected at the 3-sigma level, e.g., a point on the light curve must have sufficient SNR to be detected at the catalog level as amplified from a previous observation at the 3-sigma level. 


.. figure:: /_static/microlensing_lc.png
   :name: fig-microlensing_lc

   Example light curve shape used for fast microlensing events. This is a 4.37 day crossing time with impact parameter of 0.73. 



.. image:: /_static/micro_input.png
   :width: 33%
.. image:: /_static/thumb.baseline_nexp2_v1_6_10yrs_Fast_Microlensing_USER_SkyMap.png
   :width: 33%
.. image:: /_static/thumb.combo_dust_nexp2_v1_6_10yrs_Fast_Microlensing_USER_SkyMap.png
   :width: 33%

The images above show the input microlensing events along with the recovered events for the two simulations. The baseline recovers 15% of the input events, while combo_dust recovers 37% of the input. The extra bulge coverage in the combo_dust simulation results in many more microlensing events being discovered.


Extending to Other Populations
==============================

These transient metrics can be used as a templates for writing metrics for other transient populations. The basic steps for any transient metric are to 1) Generate a population of transients, 2) Define a criteria for a transient to be "detected" (and/or well-detected), 3) Use MAF to generate the expected observed light curves and check to see what fraction meet the detection criteria.








.. .. rubric:: References

.. Make in-text citations with: :cite:`bibkey`.

.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
