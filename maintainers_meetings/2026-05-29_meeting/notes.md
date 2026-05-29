
**Date:** April 24, 2026  
**Time:** 15:00 (CEST)  

#### Present:
Teresia Olsson (HZB)
Patrick Madela (SOLEIL)
Alexis Gamelin (SOLEIL)
Konstantinos Paraschou (DESY)
Jean-Luc Pons (ESRF)
Guillaume Pichon (SOLEIL)
Yoshi Hidaka (BNL)

#### Discussion: 

##### Schema registry

- TO is presenting her suggestion for configuration simplification with Schema registry. 
- Discussion is MagnetSchema should be specific to magnet type or general.
- Some disagreement on the duplication in schema and the actual class and the string representation is also lost.
- Refurbishment is also difficult because of the insuficient code coverage.
- GP do EPICS labs have some list of requirements? If this is a configuration we can try to address this issue.
- Unit tests should cover more use cases 
- GP: it is not clear how the configuration should be simplified
- Ideally this should be reviewed and merged after the catalog change as these two MR are big refurbishments and likely not compatible with each other.

##### Other MRs in the past month

- Catalog update could be merged in the near future
- Not discussed in this meeting

##### Update on the user community meeting the 11 June

- Not discussed this meeting

##### Update on "digital twin" for pyAML CI/CD

- Guillaume recently ran digital twin on CI/CD
- Status is to get an initial version by the end of June
- Some files and links were shared during the meeting

##### Report on IPAC satellite meetings (if anything is useful to us)

- Nothing to report from the satellite meetings

#### Workload distribution

- TO will continue working on the schema registry and configuration refactoring.
- JLP is busy with machine restart and code reviews. 
- GP and JLP will finalise the catalog update.
- GP and SOLEIL colleagues work on the digital twin side. 

#### Topics of the next meetings

- Schema configuration
- Catalogs for configuration
