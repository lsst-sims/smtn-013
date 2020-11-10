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



Tidal Disruption Events
=======================

.. figure:: /_static/tde_lc.png
   :name: fig-tde_lc

   Example light curve shapes used for TDEs. 




Microlensing
============


.. figure:: /_static/microlensing_lc.png
   :name: fig-microlensing_lc

   Example light curve shapes used for TDEs. 


Extending to Other Populations
==============================

These can be used as a templates for writing metrics for other transient populations. To write a new transient population

- Write a slicer generator that makes a population of transients with the proper spatial distribution and distribution of transient properties. For example, xxx-add link generateMicrolensingSlicer distributes microlensing events distributed proportionally to 
- 








.. .. rubric:: References

.. Make in-text citations with: :cite:`bibkey`.

.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
