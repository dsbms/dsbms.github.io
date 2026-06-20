---
title: "Goslin: A Grammar of Succinct Lipid Nomenclature"
chip: "Goslin"
area: "Harmonization & nomenclature"
areanum: 1
weight: 1
tag: "Nomenclature"
year: "2020"
venue: "Analytical Chemistry"
authors: "Kopczynski D, Hoffmann N, Peng B, Ahrends R"
doi: "10.1021/acs.analchem.0c01690"
toolurl: "https://lifs-tools.org/tools/goslin.html"
toollabel: "lifs-tools.org/goslin"
idea: "A formal grammar that lets software read lipid names written in many different dialects and normalize them to one standard shorthand."
lead: "Lipid names are written inconsistently across labs, tools and databases — which silently breaks any attempt to compare datasets. Goslin defines lipid shorthand nomenclature as a formal grammar, so a parser can recognise the many name dialects in use and rewrite each one into a single, canonical form."
concepts:
  - "Context-free grammars describe the structure of lipid names precisely, the way a programming language is parsed."
  - "Names are resolved onto the hierarchical shorthand levels, from sum-composition species up to structure-defined."
  - "One shared specification, implemented as libraries in C++, Python, Java and R, so every tool behaves identically."
findings:
  - "The first grammar-based library to parse and normalize multiple lipid-name dialects."
  - "For each parsed name it returns the monoisotopic mass, sum formula and LIPID MAPS category/class."
  - "Became the shared naming foundation reused across the LIFS tool suite, including LipidSpace."
---
