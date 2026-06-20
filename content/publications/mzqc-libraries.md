---
title: "Communicating MS quality information in mzQC with Python, R and Java"
chip: "mzQC libraries"
area: "Standards & interoperability"
areanum: 4
weight: 3
tag: "Quality control"
year: "2024"
venue: "J. Am. Soc. Mass Spectrometry"
authors: "Bielow C, Hoffmann N, Jimenez-Morales D, Van Den Bossche T, Vizcaíno JA, Tabb DL, Bittremieux W, Walzer M"
doi: "10.1021/jasms.4c00174"
toolurl: "https://github.com/MS-Quality-Hub"
toollabel: "github.com/MS-Quality-Hub"
idea: "Open-source libraries in three languages that let any software read, write and validate mzQC quality-control files."
lead: "A data standard is only as useful as the software that supports it. This work delivers reference libraries for mzQC in Python, R and Java, so quality-control metrics for mass-spectrometry runs can be written, exchanged and validated consistently across the tools a lab already uses."
concepts:
  - "mzQC is a lightweight JSON format from the HUPO-PSI Quality Control working group."
  - "Metrics are grouped in runQuality / setQuality elements with provenance metadata."
  - "Each metric is anchored to a PSI-MS controlled-vocabulary term for unambiguous meaning."
findings:
  - "Parallel, interoperable implementations in Python, R and Java with consistent behaviour."
  - "Reading, writing and validation against the official mzQC specification."
  - "Released as open source under the MS-Quality-Hub organisation to drive adoption."
---
