.. _WG3_QTL-docs:

WG3-pipeline-QTL
================

Part of the sc-eQTLgen consortium pipeline. Step 3, where the QTL mapping and further downstream analyses will be done.

These instructions are not frozen yet and will/can be uppdated as the analyses continue

We exepect for each of the datasets that the pipelines in WG1 and WG2 are ran and QC has be done.

See the :ref:`wiki <QTL_Cookbook-docs>` for more detailed instructions on the steps.

Please find the most recent version of the eQTL mapping software we used `here <https://github.com/single-cell-genetics/limix_qtl/wiki>`_.


General overview of the steps
------------------------------

For each dataset at the contributor site (DS):

- Perfom genotyp conversion and collect meta-data on genotyped samples, and calulcate local LD matrices.

-  perform normalization and harmonization over all cells, (per cell type / overall)

- determine which covariates to include in correction, per celltype, using harmonized dataset (e.g. PCs, sequencing-based covariates, sample quality measures, etc)

- perform an eQTL analysis within each dataset, using `LIMIX pipeline <https://github.com/single-cell-genetics/limix_qtl>`__, including permutations.

- Upload information to the central side for the central analysis.

At the central analysis (CS):

- collect summary statistics for step 3 at central site (per cell type and per dataset maximally 300 million cis-eQTLs sumtats + 40,000 permutation summary statistics, when using 20,000 genes)

- meta-analyze real assocations (+permutations) summary statistics per gene, combine beta distribution parameters from all datasets to adjust top non-permuted p-value per gene

- determine false discovery rate using adjusted p-values per gene.

- downstream analyses

.. toctree::
   :hidden:

   QTL_Cookbook
