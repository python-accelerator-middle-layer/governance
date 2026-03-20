## Agenda pyAML maintainers' meeting

**Date:** March 20, 2026  
**Time:** 15:00 (CEST)  

---
- Discussion following catalogs suggestion for configuration (https://github.com/python-accelerator-middle-layer/pyaml/pull/192)
       - Backend linking: managing dynamic links (DB) and static links (configuration files). Possibly with a user API for exploration? This might be challenging if the database is not very clean (e.g., contains test devices). That’s what I initially started here, but it ended up diverging a bit too much.
        - Handling link changes for high-level objects, and clarifying the distinction between generic high-level object definitions (modifiable and responsible for propagating changes) and their instantiations across all control systems (not changeable by the user).
        - A catalogue of high-level object definitions, similar to Yellow Pages (with or without control system objects?).
- Teresia will share details of the last steering committee meeting and the proposed project roadmap
- If time allows it, Jean-Luc was ready to share his proposal for the Measurement Class. 



