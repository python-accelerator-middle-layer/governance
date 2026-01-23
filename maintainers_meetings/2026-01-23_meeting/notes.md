## pyaml maintainers meeting 23 Jan 2026


#### Present:

S.Liuzzo  
T.Olsson  
K.Paraschou  
W. Sulaiman Kail  
Y.Hidaka  
JL Pons  
G.Pichon  
Gayane Ayatuni  
Julian Gethmann  


agenda: in governance github

#### Discussion:

TO  
release strategy.
We need a stable version for the workshop. Need to fix a version for the workshop and then run test and put everything together.
What to do if there is a bug next week?

Restriction policy before the workshop?
What would be the best way to do?

JLP  
just need to tag and a release will appear in pip.

TO  
In case of issue new release

JLP  
stop development now and concentrate on examples. minor fix only. no refurbishment. nothing that could brake the interface.

TO  
only fixes that are required for the tests to run
People can continue working but PR not merged.

JLP  
PR on doc can be merged?

TO: yes, ready after review.

JLP  
Bessy Virtual machine is working for JLP, KP and SL
last OA binding release is on pip
Also pyaml latest is on pip

Anyone can tag and the release will deploy on pip

JLP  
for examples should be ok, unless a few bugs are discovered

TO  
version is then fixed to 0.2.3.
we make a new relase with bug fixes if needed next week
documentation can evolve without releases.


TO  

in the morning all WP will have the same task (see description online)
list of workshop afternoon session topics:

1) implement use cases: ex BBA. for people with experience
2) set/wait. looking at MML for example
3) metadata
4) unit conversion: A-K strength-integrated strength
5) (remote) standardized ways to perform measurement: flows, measurement execution engines, etc..

No details in indico:
6) CI/CD automated testing
7) doc
8) ecosystem development (several packages) WP could discuss how to separate tuning tools in separate repositories.
9) optics switch
10) convergence strategy accml-pyaml WS: call in people from labs that are not active. give through repo and evaluate. what can be taken from repoA and repoB of best. Expert go through repo and tell what policy can be taken to converge. could also say take one discard the other.

TO  
5) is likely a no hope topic. we will likely not converge. labs have tools that they will want to keep. we could instead replace it by ecosystem solution.

JLP  
ecosystem is possible in pyaml. orbit correction for example has a default implementation but there can be several.
Sextupole is for example a separate package.
Still discussion to do to give more flexibility.
TO  
what should be flexible what should not be. what could be already moved to external repo, what would stay in core.

TO  
new use cases are may be not high priority.
JLP  
BBA could be tricky, needs to work with BPM offsets correctly. For example Besdy Va has BPM offsets? in pyaml Vadim implemented BPM offsets but to be tested. Could be challenging to implement BBA during the workshop.

GP  
convergence stategy group will take place during workshop

YH  
need to start discussing the divergence of each facility
sometimes need to write code before PR is approved.
How do we keep synchronized?

TO  
with ecosystem is good idea, but not eash to realize. rely on relase and organization.
need to tell people how to keep packages up to date and maintain them.

YH  
customizable part could be defined for the code.
A lot will be common, but some will be fully facility specific.

TO  
will merge proposal of YH to ecosystem

WS  
could just put priority and let Vadim decide.

TO  
need to choose topic for WG remote. YH has a preference?

TO  
YH has experience with pint? unit conversion for remote group?

YH  
do we have to come out with code at the hackathon?

TO  
the ambission level for the hachatohon has to be feasible.


List of topics is prioritized with numbers and remote session.

Vadim will assign people to WG.

JLP  
How Soleil will make test with apptainer?

TO  
there was a meeting this morning. Soleil has now an aptainer container. Will test as soon as release is done (now). Will then add to container registry.
It will then require to have aptainer. Sometimes need root permission.
Will send out instructions on how to get apptainer.
During preparation session we will help people to get code installed.
Vadim will make a meeting with remote so that also remote people will have a working set up.

Soleil colleague need more time.

JLP  
Bessy VA will remain as it is?

TO + WS  
PSchnizer will look at BPM. But may be will not finish before workshop. Need to test before releasing.
New PVs for tune will also be included.
Naming issues also fixed in BPMs.

JLP  
would require that PV that are available will remain.

TO  
some PV will change name

WS  
anyway the old container will remain

TO  
problem with apptainer, need linux. But there are instructions available.

JLP  
observed strange behaviour on MAC-OS. if linux env can see all set point. in macos not visible, but it works.


GP  
PAtrick medela confirms that apptainer will be available next week. will include Jive in the apptainer.

TO  
for epics two containers: one for twin and one for jive.

GP  
can make a reminder about the version?

TO: accelerator-middle-layer 0.2.3
only for critical bugs, we do PR and release.
