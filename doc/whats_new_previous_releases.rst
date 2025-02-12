:orphan:

.. _whats_new_in_previous_releases:

.. currentmodule:: mne_icalabel

What was new in previous releases?
==================================

Version 0.3 (08/10/2022)
------------------------

This new version adds an experimental GUI for annotating ICA components. Please test it out if you find
it useful in your workflow! Moreover, we consolidated our testing suite and improved overall coverage
and added some bug fixes. We also created a function to extract topomap features from fitted ICA instances.

Enhancements
~~~~~~~~~~~~

- Adding a GUI to facilitate the labeling of ICA components by `Adam Li`_ and `Mathieu Scheltienne`_ (:pr:`66`)
- Improve test coverage and documentation by `Mathieu Scheltienne`_ (:pr:`94`)

Bug
~~~

- Ignore the ``RuntimeWarning`` issued by the grid inteprolation for ICLabel topographic feature by `Mathieu Scheltienne`_ (:pr:`69`)

API
~~~

- Add topographic feature using MNE with `~mne_icalabel.features.get_topomaps` by `Anand Saini`_ and `Mathieu Scheltienne`_ (:pr:`71`)

Authors
~~~~~~~

* `Mathieu Scheltienne`_
* `Anand Saini`_
* `Adam Li`_

Version 0.2 (06/30/2022)
------------------------

This includes series of bug fixes to the ICLabel ported model. In addition, we have
added an experimental feature for helping add ICA component annotations to BIDS-derivative for EEG format.

Enhancements
~~~~~~~~~~~~

- Add functions for annotating and labeling ICA components in BIDS format :func:`mne_icalabel.annotation.write_components_tsv`, :func:`mne_icalabel.annotation.mark_component` by `Adam Li`_ (:pr:`60`)

Bug
~~~

- Fix shape of ``'y_pred_proba'`` output from :func:`mne_icalabel.label_components` by `Mathieu Scheltienne`_ (:pr:`36`)
- Add a warning if the ICA decomposition provided does not match the expected decomposition by ``ICLabel``  by `Mathieu Scheltienne`_ (:pr:`42`)
- Fix extraction of PSD feature from ``ICLabel`` model on epochs by `Mathieu Scheltienne`_ (:pr:`64`)
- Fix ICLabel topographic features on ICA fitted with a channel selection performed by ``picks`` by `Mathieu Scheltienne`_ (:pr:`68`)

API
~~~

-

Authors
~~~~~~~

* `Mathieu Scheltienne`_
* `Adam Li`_

Version 0.1 (2022-05-03)
------------------------

This is the first version of mne-icalabel that is released. This package
consists of a replica of the ICLabel network and pipeline present in EEGLAB
for automatically predicting the label of an ICA component and whether it
is brain signal, or noise.

We integrated our API on top of MNE-Python and provide a lightweight example
demonstrating how to use the ICLabel network.

Authors
~~~~~~~

People who contributed to this release (in alphabetical order):

* `Adam Li`_
* `Jacob Feitelberg`_
* `Anand Saini`_
* `Mathieu Scheltienne`_

.. include:: authors.inc
