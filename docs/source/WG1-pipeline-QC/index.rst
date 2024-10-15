.. _WG1_QC-docs:

WG1-pipeline-QC
===============

.. _issue: https://github.com/sc-eQTLgen-consortium/WG1-pipeline-QC/issues

.. figure:: https://user-images.githubusercontent.com/44268007/89252548-35b96f80-d659-11ea-97e9-4b4176df5f08.png
  :width: 300

The purpose of this repository is to provide references and instructions for preparation of data for the sceQTL-Gen Consortium. 
Please note that you can run this pipeline in parallel to the `Working Group 2 (Cell Classification) <https://github.com/sc-eQTLgen-consortium/WG2-pipeline-classification>`__ pipeline both of which will be used for `Working Group 3 (eQTL Detection) <https://github.com/sc-eQTLgen-consortium/WG3-pipeline-QTL>`__.
Upon completion of the WG1 pipelines, please contact Drew Neavin (d.neavin @ garvan.org.au) so a meeting can be set up to discuss the best QC thresholds for the dataset that are consistent with thresholds for other datasets in the consortium.

We ask that you upload the results from each of these pipelines (except the SNP genotype data) when completed to a shared own cloud.
To get a link to upload the data please email Marc Jan Bonder at bondermj @ gmail.com and provide the dataset name as well as the PI name associated to the dataset.
The link will be the same for the WG2 data upload. 
Please note you can't change filenames after uploading!


There are four major steps that this group is addressing with data preprocessing:

#. The first step is to :ref:`impute the SNP genotypes <Imputation_Background-docs>`. This will be used for demultiplexing and for eQTL detection.

#. The second step is to :ref:`demultiplex and identify doublets<Demultiplexing_Introduction-docs>`. This will allow droplets containing single cells to be assigned to an individual and droplets that contain two cells to be removed.

#. The third step is to :ref:`analyze the quality metrics<QC_Filtering-docs>` of the data. These data and results should be fully discussed with members of WG1 too choose effective thresholds for each dataset

#. The last step is the :ref:`final data preparation<QC_Filtering-docs>` to fileter out doublets.


If you have any questions or issues, feel free to open an issue_ or directly email Drew Neavin (d.neavin @ garvan.org.au)

.. toctree::
   :hidden:

   Imputation/index
   Demultiplexing/index
   QC/index
   SubmissionExamples/index
