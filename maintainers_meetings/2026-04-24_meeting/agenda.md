## Agenda pyAML maintainers' meeting

**Date:** April 24, 2026  
**Time:** 15:00 (CEST)  

---

- [Integration of ophyd-async devices in pyAML](https://github.com/python-accelerator-middle-layer/pyaml/pull/233) and [the corresponding issue](https://github.com/python-accelerator-middle-layer/pyaml/issues/230)
- [Roadmap](https://github.com/python-accelerator-middle-layer/governance/blob/main/roadmaps/roadmap_2026-2027.pdf)
- Dates and objectives of the online hackathon proposed by the steering committee
- (if time allows it) Additional magnet windings. Especially the case when 2 power supplies can affect one single multipole (i.e. 2 power supplies that can affect a single quad strength) which leads to a non invertible magnet model and the impossibility to handle it in pyaml. Unfortunately there is no correction polynomial in AT to handle correction strength (error polynomial has been added recently but it would not be nice to use it for correction strength). We have to take a decision on how to handle this use case:

    - Add correction strengths in yaml configuration file.

    - Add an extra field in the AT lattice.

    - Add a variable in pyaml and allow to load/save optics correction (with a default to 0 correction).

---

### Topics for future meetings

- [Newest change to the configuration](https://github.com/python-accelerator-middle-layer/pyaml/pull/231) -> already merged

- Tuning tools configuration simplification (response matrices hold observables and variables name, tuning tools should create dynamically corresponding arrays)

