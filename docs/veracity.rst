==========
Veracity
==========

Valuehorizon has developed a data quality assurance manual that governs the storage, documentation and testing of its datasets. The following is a basic overview of the steps outlined in the manual to boost the accuracy of its datasets.

Procurement
===================

In order to prevent human error, the acquisition of data is executed as an automated process where possible. In general data is found via a scheduled task that checks online sources and downloads data via a RESTful API, pdf file sheets or websites with POST or GET variables. This task is executed twice every business day. Historical data are obtained either through official historical quotes (from the web or newspapers of record) or from the fund manager.

Storage
===================

All raw and processed data points are stored in a relational database. Data is extracted using a object relational mapper. In general, the use of spreadsheets are avoided to prevent data corruption, human error and memory limitations. See section 7.1 for more information.

Data Scrubbing
===================

All data are screened for anomalies using vectorised rule-based checks. These include (but are not limited to) the following checks:
* Are NAVs observed on non-business days?
* Are NAVs not observed on business days?
* Are the correct currencies used for NAVs, distributions and financial statement time-series?
* Have the intra-series missing data points been forward-filled according to the stated methodology?
* Are there any abnormally large jumps or dips in the observed time-series?

Duplicate data are rejected via unique constraints at the database level. Outlier data points are found using an elliptical envelope algorithm. These flagged outliers are temporarily removed from the dataset and verified with the fund manager and/or alternative source documentation.

Source Documentation
=====================

The Valuehorizon Document Engine™ was built to support the sources of its datasets. Each raw data point is linked to a source document which is stored in pdf format and has a unique identification code. Valuehorizon allows subscribers to inspect all non-confidential source documents.

Data Auditing
===================

Valuehorizon audits its data time series on the first day of every month. A 0.5% sample is selected and verified by humans. The sample is chosen algorithmically so that it is  spread equally over the life of the time-series. The audit samples in subsequent months are selected to exclude the prior verified data points.

Return Verification
====================

Most funds publish their annual or quarterly returns. Valuehorizon uses these returns as a cross check to see whether the computed returns are accurate. Furthermore, Valuehorizon owns roughly 90% of the funds tracked. Thus, actual account statement returns may be used in lieu of published returns for the purpose of return verification.
















