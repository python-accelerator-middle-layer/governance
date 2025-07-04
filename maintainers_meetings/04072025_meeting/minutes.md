# PyAML maintainers weekly meeting minutes (04/07/2025)

## On going developement

* Branch of Yoshi was merged into the branch of Jean-Luc Pons
* Now the branch of Jean-Luc is using Pydantic but there are some unresolved issues concerning MetaConfigurator schema generation
* Guillaume Pichon have implemented first attemp at Tango bindings and Jean-Luc verified that it is working
* Guillaume and Jean-Luc discuss TANGO bindings (quality factor and time stamps and whether this should be inside the core)
* Jean-Luc notes that pyAML core must be system independent (no EPICS or TANGO dependency)
* Jean-Luc emphasises that the branches should not diverge because it will cause problems for development
* Guillaume agreed to come back to Jean-Luc with his proposal for modifications
* Combined function magnet discussion between Alexis and Jean-Luc
* Alexis proposed that there should be a range for all values (normal magnets and combined function magnet), including a dynamic range if necessary
This is optional and not mandatory

## Code documentation

*Docstring is decided to be in numpy format*

## GitHub/CI-CD discussion

* Git workflow is fixed to the one proposed by Alexis (except we will use main instead of master)
    - main/develop
    - stable (used for releases)
* Copier template was discussed but no decision yet. Martin (DIAMOND) will prepare some demonstration in a few weeks to make a decision
* Discussion on free GitHub runners (performance limited) vs setting up a paid runner (better performance). GitLab vs GitHub for hosting the project. In DIAMOND, no issues were seen with GitHub runners




