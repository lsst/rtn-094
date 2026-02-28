# Summit Facility ConOps (DRAFT)

To become RTN-094

[1\. Reference documents	3](#reference-documents)

[2\. Introduction	7](#introduction)

[2.1. Operations organizational chart	8](#operations-organizational-chart)

[3\. Director’s office	10](#director’s-office)

[3.1. The Director’s office teams	10](#the-director’s-office-teams)

[4\. Data management in operations	12](#data-management-in-operations)

[4.1. The DM teams	12](#the-dm-teams)

[4.2. Handling a problem	13](#handling-a-problem)

[4.2.1. Data problem handling	14](#data-problem-handling)

[5\. Summit operations	18](#summit-operations)

[5.1. The RSO teams	18](#the-rso-teams)

[5.2. Planning for eng-ops summit work	19](#planning-for-eng-ops-summit-work)

[5.2.1. Yearly/quarterly planning meeting	22](#yearly/quarterly-planning-meeting)

[5.2.2. Monthly/weekly planning meeting: the Summit Monthly Planning meeting	22](#monthly/weekly-planning-meeting:-the-summit-monthly-planning-meeting)

[5.2.3. Weekly planning meetings	22](#weekly-planning-meetings)

[5.2.3.1. The Daytime Weekly Integration Meeting	23](#the-daytime-weekly-integration-meeting)

[5.2.3.2. The Weekly Summit Performance Status	23](#the-weekly-summit-performance-status)

[5.2.4. Daily planning meeting: Daytime Briefing meeting	23](#daily-planning-meeting:-daytime-briefing-meeting)

[5.2.5. Observatory software and DevOps	24](#observatory-software-and-devops)

[5.2.6. Summary	24](#summary)

[5.3. Planning for obs-ops summit work	26](#planning-for-obs-ops-summit-work)

[5.3.1. Forming the daily observatory operations plan	26](#forming-the-daily-observatory-operations-plan)

[5.3.2. Calibrations	27](#calibrations)

[5.3.3. Meetings	28](#meetings)

[5.3.4. Summary	31](#summary-1)

[5.4. Implementing eng-ops summit work	32](#implementing-eng-ops-summit-work)

[5.4.1. Version control	32](#version-control)

[5.4.2. Output	33](#output)

[5.4.3. Handover	33](#handover)

[5.4.4. Summary	33](#summary-2)

[5.5. Implementing obs-ops summit work	35](#implementing-obs-ops-summit-work)

[5.5.1. Who’s at the summit	35](#who’s-at-the-summit)

[5.5.2. Who’s responsible	35](#who’s-responsible)

[5.5.3. Who’s on call	36](#who’s-on-call)

[5.5.4. Handover	36](#handover-1)

[5.5.5. Summary	37](#summary-3)

[5.6. Handling a problem	37](#handling-a-problem-1)

[5.6.1. System problem handling	37](#system-problem-handling)

[5.6.2. Doing a summit test	37](#doing-a-summit-test)

[6\. Communications	40](#communications)

[6.1. Communication channels and etiquette	40](#communication-channels-and-etiquette)

[6.2. Slack channels	40](#slack-channels)

[6.3. SquadCast	42](#squadcast)

[6.4. Zoom	42](#zoom)

[6.5. Calling for help	42](#calling-for-help)

[7\. Safety	44](#safety)

[8\. Understanding data quality	45](#understanding-data-quality)

[8.1. The different steps of understanding data quality	45](#the-different-steps-of-understanding-data-quality)

[8.2. What to do with quality assessments	45](#what-to-do-with-quality-assessments)

[8.3. Using the tools	46](#using-the-tools)

[A. People in roles	48](#people-in-roles)

(reference-documents)=
1. # Reference documents 

These documents are referred to as RDX in the text where X equals the decimal number of the document here. Ex. RD6 refers to 1.6 *The Nightly digest.*

(RD1)=
1. SIT-Com meeting summary and schedule [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/452395103/SIT-Com+ConOps+Meetings+Summary+-+LSSTCam+On-Sky+Commisioning](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/452395103/SIT-Com+ConOps+Meetings+Summary+-+LSSTCam+On-Sky+Commisioning)  
(RD2)=
2. SIT-Com 24hr script [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/408813569/24hr+Script+-+LSSTCam+On-Sky+Commissioning](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/408813569/24hr+Script+-+LSSTCam+On-Sky+Commissioning)  
(RD3)=
3. Zephyr scale workflows [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741853/BLOCK+Zephyr+Scale+Workflows](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741853/BLOCK+Zephyr+Scale+Workflows)  
(RD4)=
4. The SUMMIT Jira board [https://rubinobs.atlassian.net/jira/software/c/projects/SUMMIT/boards/249](https://rubinobs.atlassian.net/jira/software/c/projects/SUMMIT/boards/249)  
(RD5)=
5. The OBS Jira board [https://rubinobs.atlassian.net/jira/software/c/projects/OBS/summary](https://rubinobs.atlassian.net/jira/software/c/projects/OBS/summary)  
(RD6)=
6. The Nightly Digest   
      [https://usdf-rsp.slac.stanford.edu/nightlydigest/\#](https://usdf-rsp.slac.stanford.edu/nightlydigest/#)  
(RD7)=
7. Nightly monitoring resources [https://rubinobs.atlassian.net/wiki/spaces/DM/pages/48835951/Nightly+Monitoring+Resources](https://rubinobs.atlassian.net/wiki/spaces/DM/pages/48835951/Nightly+Monitoring+Resources)  
(RD8)=
8. OpenMaint (CMMS) workflow user’s guide                [https://rubinobs.atlassian.net/wiki/spaces/CMMS/pages/309330317/OpenMAINT+User+s+Guide](https://rubinobs.atlassian.net/wiki/spaces/CMMS/pages/309330317/OpenMAINT+User+s+Guide)   
(RD9)=
9. The nightly plans  
      [https://rubinobs.atlassian.net/projects/BLOCK?selectedItem=com.atlassian.plugins.atlassian-connect-plugin:com.kanoah.test-manager\_\_main-project-page\#\!/v2/testCycles](https://rubinobs.atlassian.net/projects/BLOCK?selectedItem=com.atlassian.plugins.atlassian-connect-plugin:com.kanoah.test-manager__main-project-page#!/v2/testCycles)   
(RD10)=
10. Observatory Operations Documentation  
       [https://rubinobs.atlassian.net/wiki/spaces/OOD/overview?homepageId=39682050](https://rubinobs.atlassian.net/wiki/spaces/OOD/overview?homepageId=39682050)  
(RD11)=
11. The Unified Summit Schedule   
       [https://ls.st/summit-unified-sched](https://ls.st/summit-unified-sched)  
(RD12)=
12. The Rubin Baseline Calibration Plan  
       [https://sitcomtn-086.lsst.io/](https://sitcomtn-086.lsst.io/)  
(RD13)=
13. Plan for the operations of the Vera C. Rubin Observatory and Execution of its legacy survey of space and time  
       [https://ls.st/rdo-018](https://ls.st/rdo-018)  
(RD14)=
14. Summit control room usage and etiquette  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/77758494/Summit+Control+Room+Usage+and+Etiquette](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/77758494/Summit+Control+Room+Usage+and+Etiquette)  
(RD15)=
15. Summit software  
       [https://rtn-069.lsst.io/](https://rtn-069.lsst.io/)  
(RD16)=
16. R2A2s for On Sky Commissioning  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741822/R2A2+s+for+On+Sky+Commissioning](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741822/R2A2+s+for+On+Sky+Commissioning)  
(RD17)=
17. Night Planner Script  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/175407143/Night+Planner+Script](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/175407143/Night+Planner+Script)  
(RD18)=
18. Data Management Science Pipelines Design  
       [https://ls.st/ldm-151](https://ls.st/ldm-151)  
(RD19)=
19. Data Products Definition Document  
       [https://ls.st/lse-163](https://ls.st/lse-163)  
(RD20)=
20. The LSST Science Pipelines Software: Optical Survey Pipeline Reduction and Analysis Environment  
       [https://pstn-019.lsst.io/](https://pstn-019.lsst.io/)  
(RD21)=
21. LSST Science Pipelines website  
       [https://pipelines.lsst.io/](https://pipelines.lsst.io/)  
(RD22)=
22. The Rubin Observatory LSST Community Forum  
       [https://community.lsst.org/](https://community.lsst.org/)  
(RD23)=
23. Management and Execution Plan for Data Management Operations  
       [http://ls.st/rtn-046](http://ls.st/rtn-046)   
(RD24)=
24. EPO Design  
       [http://ls.st/lep-31](http://ls.st/lep-31)  
(RD25)=
25. Science Data Model Schemas  
       [https://sdm-schemas.lsst.io/](https://sdm-schemas.lsst.io/)  
(RD26)=
26. ConsDB Usage  
       [https://rubinobs.atlassian.net/wiki/spaces/\~ktl/pages/55377993/ConsDB+Usage](https://rubinobs.atlassian.net/wiki/spaces/~ktl/pages/55377993/ConsDB+Usage)  
(RD27)=
27. Telescope and Auxiliary Instrumentation Calibration Acceptance Board (TAXICAB)  
       [https://rubinobs.atlassian.net/jira/software/c/projects/TAXICAB/summary](https://rubinobs.atlassian.net/jira/software/c/projects/TAXICAB/summary)  
(RD28)=
28. Model for Community Science  
       [http://ls.st/rtn-006](http://ls.st/rtn-006)  
(RD29)=
29. Guidelines for User Support with the Rubin Community Forum  
       [http://ls.st/rtn-097](http://ls.st/rtn-097)  
(RD30)=
30. Rubin Operations Work Management and Budget Planning  
       [http://ls.st/rtn-005](http://ls.st/rtn-005)  
(RD31)=
31. TAXICAB Tracking Page  
       [https://rubinobs.atlassian.net/wiki/spaces/DM/pages/281673762/TAXICAB+Tracking+Page](https://rubinobs.atlassian.net/wiki/spaces/DM/pages/281673762/TAXICAB+Tracking+Page)  
(RD32)=
32. TMA Daytime Checkout for Nighttime Operations  
       [https://rubinobs.atlassian.net/wiki/spaces/OOD/pages/39682052/TMA+Daytime+Checkout+for+Nighttime+Operations](https://rubinobs.atlassian.net/wiki/spaces/OOD/pages/39682052/TMA+Daytime+Checkout+for+Nighttime+Operations)  
(RD33)=
33.  Checklist for start of system integration tests  
       [https://rubinobs.atlassian.net/wiki/spaces/OOD/pages/39690281/Checklist+for+start+of+system+integration+tests](https://rubinobs.atlassian.net/wiki/spaces/OOD/pages/39690281/Checklist+for+start+of+system+integration+tests)  
(RD34)=
34.  Target-of-Opportunity Operations During the Science Verification Surveys  
       [https://rtn-098.lsst.io/](https://rtn-098.lsst.io/)  
(RD35)=
35.  Observing Task Management Workflow Summary  
       [https://sitcomtn-019.lsst.io/](https://sitcomtn-019.lsst.io/)  
(RD36)=
36.  Shift Manager Roles (Operations)  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/1318354949/Shift+Manager+Roles+Operations](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/1318354949/Shift+Manager+Roles+Operations)  
(RD37)=
37.  Decision Making on Cerro Pachón [https://www.google.com/url?q=https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/702840924/Decision%2BMaking%2Bon%2BCerro%2BPach%2Bn%2BDraft\&sa=D\&source=docs\&ust=1765225616013568\&usg=AOvVaw2GCvKfT51Tx8OtZ\_-T8cxS](https://www.google.com/url?q=https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/702840924/Decision%2BMaking%2Bon%2BCerro%2BPach%2Bn%2BDraft&sa=D&source=docs&ust=1765225616013568&usg=AOvVaw2GCvKfT51Tx8OtZ_-T8cxS)  
(RD38)=
38.  Voluntary Out-of-Hours Support Call List  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTPO/pages/43242474/Voluntary+Out-of-Hours+Support+Call+List](https://rubinobs.atlassian.net/wiki/spaces/LSSTPO/pages/43242474/Voluntary+Out-of-Hours+Support+Call+List)  
(RD39)=
39.  DevOps Emergency Support Form  
       [https://webforms.squadcast.com/vera-c-rubin-observatory/Run-Support](https://webforms.squadcast.com/vera-c-rubin-observatory/Run-Support)  
(RD40)=
40. Emergency Response Guide   
       [https://obs-ops.lsst.io/Safety/emergency-response-guide.html](https://obs-ops.lsst.io/Safety/emergency-response-guide.html)  
(RD41)=
41. Summit Emergency Form  
       [https://webforms.squadcast.com/vera-c-rubin-observatory/Summit-Emergency](https://webforms.squadcast.com/vera-c-rubin-observatory/Summit-Emergency)  
(RD42)=
42.  Remote Control Room Display Setup Policies  
       [https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/585040063/Remote+Control+Room+Display+Setup+Policies](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/585040063/Remote+Control+Room+Display+Setup+Policies)  
(RD43)=
43.  Rubin Night Log mailing list  
       [https://lists.lsst.org/mailman/listinfo/rubin-night-log](https://lists.lsst.org/mailman/listinfo/rubin-night-log)  
(RD44)=
44.  Slack Channel Communication with Summit Personnel  
        [https://obs-ops.lsst.io/Daytime-Nighttime-Interactions/slack-channel-usage.html](https://obs-ops.lsst.io/Daytime-Nighttime-Interactions/slack-channel-usage.html)  
(RD45)=
45.  DevOps Notifications  
       [https://ittn-083.lsst.io/](https://ittn-083.lsst.io/)  
(RD46)=
46.  The Scheduler Dashboard  
       [https://usdf-rsp-dev.slac.stanford.edu/schedview-snapshot/dashboard](https://usdf-rsp-dev.slac.stanford.edu/schedview-snapshot/dashboard)  
(RD47)=
47.  FBS prenight simulations  
       [https://usdf-rsp-dev.slac.stanford.edu/times-square/github/lsst/schedview\_notebooks/prenight/prenight\_sims](https://usdf-rsp-dev.slac.stanford.edu/times-square/github/lsst/schedview_notebooks/prenight/prenight_sims)  
(RD48)=
48.  Vera C. Rubin Observatory Survey Strategy page  
       [https://survey-strategy.lsst.io/](https://survey-strategy.lsst.io/)  
(RD49)=
49.  Safety Policy  
       [https://ls.st/lpm-18](https://ls.st/lpm-18)  
(RD50)=
50.  Environmental, Health and Safety Plan  
       [https://docushare.lsst.org/docushare/dsweb/Get/Document-61265/LPM%20114%20EHS%20plan%20-%20Rubin%20-%20ENG.pdf](https://docushare.lsst.org/docushare/dsweb/Get/Document-61265/LPM%20114%20EHS%20plan%20-%20Rubin%20-%20ENG.pdf)  
(RD51)=
51.  Local Safety Health and Environmental Plans for  Each Site  
       [https://project.lsst.org/safety/local\_plan](https://project.lsst.org/safety/local_plans)  
(RD52)=
52.  EHS LPM Safety Standards   
         [https://docushare.lsst.org/docushare/dsweb/View/Collection-16607](https://docushare.lsst.org/docushare/dsweb/View/Collection-16607)  
(RD53)=
53.  Rubin Observatory Mirrors System Protocols  
       [https://docushare.lsst.org/docushare/dsweb/View/Collection-16200/Document-61335](https://docushare.lsst.org/docushare/dsweb/View/Collection-16200/Document-61335)  
(RD54)=
54.  LOTO Procedures \- All Systems  
       [https://docushare.lsst.org/docushare/dsweb/View/Collection-16533](https://docushare.lsst.org/docushare/dsweb/View/Collection-16533)  
(RD55)=
55.  Lockout-Tagout Safety Standard  
       [https://ls.st/lpm-212](https://ls.st/lpm-212)  
(RD56)=
56.  Quick Safety Reference for Nighttime Personnel  
       [https://obs-ops.lsst.io/Safety/index.html](https://obs-ops.lsst.io/Safety/index.html)  
     


       

     

(introduction)=
2. # Introduction 

This document outlines the practical implementation of summit operations
for Vera C. Rubin Observatory. It details the planning and execution of
work for both engineering operations (eng-ops; daytime) and observatory
operations (obs-ops; daytime and nighttime). These activities encompass
scheduled milestones such as maintenance, emergent repairs, and general
level-of-effort tasks. Guided by the organizational structure in Figure
2-1, this document provides a clear roadmap for the various departments,
consisting of various teams, requesting, implementing, and monitoring
specific summit work.  For high-level planning context, refer to
[RD30](#RD30).

This document does not discuss the observatory’s mission or
vision, the key performance indicators of the survey, nor the survey
strategies. [RD13](#RD13) has this information
plus staffing levels, organization, data management systems and other
management items including the role of NOIRLab and SLAC.  It does not
discuss the transfer, processing, distribution, and storage of the data,
which are discussed in [RD13](#RD13).

(operations-organizational-chart)=
1. ## Operations organizational chart

![][image1] *Figure 2-1: The organizational chart for Rubin operations.
Outside of the Director’s office are four departments, each containing
teams.  Each department has an Associate Director as the head, and
each team has a team lead. As of this writing, the System Performance
department has gone away, with the teams moving to other departments as
indicated by the red arrows. Additionally, the RDM Data Acquisition area
of responsibility has changed its name to Chile Facilities and Long Haul
Network.  We’ll update the organizational chart in the next release.*

Figure 2-1 shows the organizational chart for Rubin operations.  The
Directorate office is headed by the Director of Operations and has Safety,
Program Operations, In-kind Program Coordination, and a Legacy Survey of
Space and Time (LSST) teams. The three departments (pending the removal
of the System Performance department; see the figure’s caption) below
the Directorate are headed by an associate (AD) and a deputy director,
except for the Education and Public Outreach, which is led by a head of
program. Each team below the *Management* box has a lead.  The people
in these roles (at the time of this writing) are mentioned in Appendix A.

We discuss the departments in this order: Director’s Office
(RDO), Data Management Operations (RDM) and Summit Operations (RSO).
Data Management deals with the processing and publication of the data
we are taking. Conflicts in the plans of each are dealt with by the
Director’s office, and they each produce work packages that need to
be carried out at the summit, usually by Summit Operations.  Here,
we don’t discuss the EPO department; their design is discussed in
[RD24](#RD24) and [RD13](#RD13).

(director’s-office)=
3. #  Director’s office

The Vera C. Rubin Observatory Director’s office is responsible for
overall management of the observatory and the survey as well as fulfilling
the mission of the observatory and realizing its vision.

(the-director’s-office-teams)=
1. ## The Director’s office teams 

The **Directorate** team contains the director, deputy director and
together with the head of program operations and the head of science
for LSST, they form the senior leadership team for the observatory.
Together they are responsible for the observatory staff and facilities
at the highest level, ensuring the effective deployment of resources to
support them and answering to AURA, SLAC, NSF, and DOE for the execution
of operations.

The **Safety** team will collectively manage oversight of personnel
and equipment safety issues across the observatory geographic sites.
They work with RSO to ensure all summit work considers safety of both
personnel and equipment.  We discuss safety in section 8\.

**Program Operations** is responsible for administrative and program
management operations for Rubin Observatory. They are responsible for
preparing both the budget and the annual Program Operations Plan document
and the enduring Operations Plan document.

The **In-Kind Program Coordination** team accepts and manages the in-kind
contribution program from international (not U.S. and Chile) teams.
These contributions either offset operations costs (e.g. by providing
staff effort in operations roles, or computing resources for Rubin data
processing) or expand the resources available to the U.S. and Chilean
science community.

The **Legacy Survey of Space and Time** (LSST) team is the principal
custodian of the LSST Science Requirements Document and supports the
Rubin Observatory Directorate with a focus on the survey progress and
overall science goals of the LSST. The lead of this team is the head of
science, who has a science team that helps answer questions that concern
LSST science.

The **Survey Scheduling** team, reporting to the head of LSST, ensures
the strategy implemented by the scheduler software achieves the survey
science requirements. Achieving this goal involves simulating the
remaining survey time, folding in an evolving understanding of the
observatory system, and ascertaining whether a change to the scheduling
algorithm or configuration may be warranted.

# 

(data-management-in-operations)=
4. #  Data management in operations

The Rubin Data Management (RDM) department is responsible for the
development, maintenance, and operation of the networks, hardware, and
software infrastructure comprising the Rubin Observatory Data Management
System (see [RD23](#RD23)).  They are responsible for the generation
and archiving of prompt data products and periodic data releases.
They work with RSO to develop and deliver new software products that
affect summit operations and assess the quality of the data produced.


(the-dm-teams)=
1. ## The DM teams

Within the DM department staff are organized into areas of
responsibilities  Within those areas are the teams.  The teams are
sometimes split into groups, responsible for the different framework
and cadences involved in data management. For example, the *Calibration
Products Production* group sits in the **Algorithms and Pipelines**
team along with two other groups *Alert Production* and *Data Release
Production*.  The **Algorithms and Pipelines** team sits in the **Data
Production** area of responsibility.  The organizational chart in figure
2-1 shows the areas of expertise and the teams within them; it does not
show the groups.

The **Data Facilities** (DF) teams oversee the data facilities performance
and strategy.  This includes wide-area networking connecting the site,
supporting databases, providing managed physical resources for the data,
supporting users via the Rubin Science Platform.  The teams within
this area are **United States Data Facility (USDF)**,  **France Data
Facility**, and **United Kingdom Data Facility**.

The **Chile Facilities and Long Haul Network** area maintains the summit
infrastructure and software deployments necessary to acquire images and
get them to the USDF in a timely manner. There is only one team in this
area called the **Chile DevOps** team.

The **Data Abstraction** teams maintain and evolve the data butler,
workflow management, campaign management tooling, and other data
processing support.  They also support the build and packaging system
inherited from construction.  Teams in this area are **Pipeline
Middleware,** **Build Engineering** and **Data Engineering**.

The **Data Production** teams develop and maintain scientific
algorithms and pipelines to be capable of generating data products
which meet requirements and are ready for community use, based on the
guidance provided by the **Community Science** and **Verification
and Validation** teams.  Teams in this area are **Algorithms and
Pipelines,** **Campaign Management,** and the **Verification and
Validation** team. The **Verification and Validation** team will lead the
specification, development, verification, and validation of the survey
data products. They will be the ones building the tools that will monitor
data quality.

The **Data Services** teams maintain and evolve several cross cutting
services and platforms, one of the most important of which is the
Rubin Science Platform.  Teams in this area are the **Science Quality and
Reliability Engineering (SQuaRE)** and the **Query Server (Qserv)** teams.

DM retains a DM lead scientist who owns many topics around products,
quality and trade offs.  Under the DM lead scientist, the **Community
Science** team facilitates the community's use of the survey data
products.  They ingest the feedback needed to ensure scientific
productivity and robustness of the survey, coordinate expertise from
across the project and the community to assess risks and opportunities
for science, and enact change when needed.  [RD28](#RD28) describes the model
for community science within the observatory.

In addition the interaction with **NOIRLab’s Data Management and
Software** (DMS) services is unclear, AURA team leads in DM are
administratively in DMS functionally reporting to the AD of DM.

(handling-a-problem)=
2. ## Handling a problem

With the exception of prompt processing, DM is mostly not responsible
for critical systems. Thus, they work during the day and make requests
for summit activities per the procedures described in section 6\.
They also get called into the problem groups on sky performance or issues.

For prompt processing even one night of the alerts not going out with the
required latency is a significant portion of its 98% reliability target,
so they do respond during the night to problems with alert production and
prompt processing.  Eventually there will be automated tools which look at
the alerts (*are there any,* *are there too many?*) which will alert the
observers who would then call someone for support.  Until that exists,
USDF will recognize issues with the alerts and resolve issues as they
arise. In all cases while the alerts are being worked on, the observers
continue observing.  The work to automate this happens in the first year
of operations, remembering that alerts are not required in the first year.

In some cases the problem may be due to something changing in the camera,
calibration system,  etc.  There are two solutions here, one to fix alert
production stream to work with these data (handled by DM) and one with RSO
examining and fixing the problem.  In some cases, the project may want the
first solution put in place while RSO works on the problem.  In this case,
the problem may be handled with the data problem handling described below.

(data-problem-handling)=
1. ### Data problem handling

In addition to their own monitoring, the **Community Science** team
(CST) runs the Rubin Observatory Community Forums ([RD22](#RD22)).  They encourage
community scientists to post their questions to these forums.  If all goes
well, the community answers the questions themselves, but the **Community
Science** team watches the forums and ensures each person gets a response
within a working day.  ([RD29](#RD29) has guidelines for user support through the
community forum.)  One **Community Science** team member (per shift) is
responsible for monitoring the community forum.  This person then ensures
each question gets answered, files a Jira ticket for ones that need more
research, and keeps the submitter informed as the team progresses.

The problem/question may not come from the community forums, but could
come from  staff members as well.  They’ll likely do this by raising
the issue at an appropriate Slack channel.

In some cases, the question can be answered directly and closed.
Although the person responding may decide to issue a Jira ticket to get
documentation edited to avoid these questions in the future.  In other
cases, the respondent may need to ask someone else in Rubin for the
answer, in which case she tells the submitter that she is working on
the problem.  The problem may need to be reproduced so the respondent
works with the submitter to do this.  In some cases, the problem is not
answerable without some more research as to what caused the problem and
what the solution is.  Figure 4-1 outlines the process the CST uses to
address a problem.

Once a problem is discovered that requires research to figure out (whether
the problem comes from the Community Forums, the monitoring of metrics of
the survey, or other input), a group is formed, by the DM lead scientist,
to solve the problem.  It may be necessary for additional expertise
from other groups to be involved in solving the problem.  The associate
director (AD) of DM may ask the other ADs for support staff as needed.
This means, though, that those asked for expert help must stop at least
some of the other work they are doing to work on the problem.  If the
ADs themselves cannot agree to allocate people to work on the problem,
the AD of DM raises the issue with the director of operations and the
chief scientist.

![][image2]  
*Figure 4-1: A diagram of how problems are solved within the RDM CST.*

The DM/CST is staffed with members who have a direct interest in the
problem’s solution.   Since solutions often have cross-disciplinary
effects, CST includes or recruits representatives with the authority
to evaluate and approve work across all affected areas. In some cases
where the work affects the survey strategy or another survey metric,  the
AD of DM will often take it to the head of science for final approval.
The head of science may consult with his team and/or the Survey Cadence
Optimization Committee (SCOC), depending upon the nature of the request.


(summit-operations)=
5. # Summit operations 

This chapter will divide the summit operations work into engineering
operations (eng-ops) and observatory operations (obs-ops). The eng-ops
work is usually done during the daytime while the obs-ops work is largely
done at night, although during the day there is work done for calibrations
and preparing for the nighttime observations.

(the-rso-teams)=
1. ## The RSO teams

The RSO consists of 7 teams: **Science Operations**, **Summit Software**,
**Summit Facility**, **Nighttime Operations**, **Summit Engineering**,
**Camera, and Systems Engineering**. Together they are responsible for
operating and maintaining the telescope, camera systems, and summit
facilities in order to collect the raw imaging, housekeeping, and
environmental data needed by the Legacy Survey of Space and Time. The
primary tasks include maintaining the operating facilities, conducting
the nighttime survey operations, real-time assessment of image quality
and observing efficiency, performing the daily calibration, and collecting
and analyzing engineering data.

The **Science Operations** team includes senior scientists responsible
for each of the main Cerro Pachón facility elements including: the
observatory, the Simonyi telescope, the camera, the auxiliary telescope,
as well as other supporting environmental awareness systems needed to
support survey observing. These scientists are the primary liaisons to
the other Rubin Observatory operation departments to direct system wide
optimizations and adjustments into the nightly observing program.

The **Summit Software** team is responsible for maintaining and
optimizing the control software that operates all subsystems in the
observatory including the dome, summit facility, telescope, camera,
and auxiliary telescope.  This team is also responsible for managing
the overall software version and configuration and validating software
systems prior to any changes at the summit facility.

The **Summit Facility** team includes the site manager and all
technical staff charged with operating and maintaining Rubin Observatory
installation on Cerro Pachón on a daily basis.

The **Nighttime Operations** team performs survey observations, carries
out real-time trouble-shooting investigations of the observatory hardware,
observatory software, and the prompt data processing.  They operate the
telescope and camera to collect survey images and telescope-specific
calibration data and provide first technical analysis of on-site
performance and emergent issues.

The **Summit Engineering** team provides engineering support for
observatory hardware, including scheduled and unscheduled corrective
and preventive maintenance and servicing.

The **Camera** team is responsible for the LSSTCam maintenance
and engineering.  The camera software group is part of the **Summit
Software** team.

The **Systems Engineering** team’s responsibilities for the
observatory-wide systems *at the summit* include:

* Systems performance optimization  
* System quality assurance management  
* System monitoring using the FRACAS  
* Failure mode, effects, and criticality analysis   
* Maintenance and configuration management  
* System (re-)verification and (re-)validation 

(planning-for-eng-ops-summit-work)=
  2. ## Planning for eng-ops summit work 

The eng-ops tasks consist of troubleshooting, fixing problems,
maintenance, and upgrades.  Planning for eng–ops work happens in four
phases (figure 5-1 and table 5-1): the yearly/quarterly, the monthly,
weekly, and daily planning. The yearly/quarterly planning is the
responsibility of the chief engineer and informs the monthly planning,
which in turn informs the weekly and then the daily plans. Each planning
level also considers other inputs that are not necessarily addressed at
higher levels. Table 5-1 has the chair of each meeting along with other
relevant details.

*Table 5-1: A table of the core meetings that go into the daily eng-ops plan.*  

| TImescale | Meeting | Frequency | Chair | Output |
| ----- | ----- | ----- | ----- | ----- |
| **Year– Quarter** | Daytime Quarterly Review | Quarterly (currently doesn’t happen)    | Chief engineer |  |
| **Month – Week** | Summit Monthly Planning | Bi-weekly  | Deputy AD of RSO | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTPO/pages/43244380/Strategic+Planning+Meeting) |
|  | Weekly Summit Performance Status  | Weekly   | Summit support scientist  | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741775/SITCOM+Test+Planning+STP) |
| **Week** | Daytime Weekly Integration | Weekly   | Summit engineering team lead | [Summit weekly calendars](https://rubinobs.atlassian.net/plugins/servlet/ac/doitbetter.calendar/calendar-page?project.key=SUMMIT&project.id=10053) |
| **Day** | Daytime Briefing | Daily | Deputy head of summit facilities | A thread in [**\#summit-announce**](https://rubin-obs.slack.com/archives/C07QCJ7F962) |

*![][image3]*

*Figure 5-1: A summary of the eng-ops planning.*

(yearly/quarterly-planning-meeting)=
1. ### Yearly/quarterly planning meeting

The *Daytime Quarterly Review* reviews the tasks that need to be
completed each quarter.  The group ensures the plan aligns with the
science vision/goals and progress of the observatory. These agenda
includes upgrades and maintenance tasks, addressing failure reports
and their corrective actions, and reporting on failure mode, effect
and criticality analysis (FMECA), systems performance optimization,
system quality assurance management, and system reverification and
revalidation tasks.

The maintenance tasks are generated by the Computerized Maintenance
Management System (CMMS). The CMMS product is OpenMAINT. It is populated
with calendar-based maintenance procedures to facilitate the execution
of preventive maintenance activities.  Eventually, it will also
have maintenance that has triggers other than the date, allowing for
predictive maintenance. It will also be used to capture information
about corrective maintenance activities. OpenMAINT integrates with
Jira, allowing us to schedule maintenance tasks directly within Jira.
The workflow of maintenance tasks is provided in [RD8](#RD8).

During commissioning, the work of this meeting happened during scheduling
workshops; these will continue during the first year of operations as
construction comes to a close.   We expect a meeting of this nature to
occur during operations.

(monthly/weekly-planning-meeting:-the-summit-monthly-planning-meeting)=
2. ### Monthly/weekly planning meeting: the Summit Monthly Planning meeting

The *Summit Monthly Planning* meeting is held every week and looks at
the next week to month timescale of what engineering work needs to be
done at the telescope. This meeting looks at the calendar prepared in the
*Daytime Quarterly Review*  to see about scheduling tasks. In addition,
the attendees discuss how things are going, what work needs more time,
and what new work is coming up. This meeting does not provide an agenda,
but does provide notes for the meeting chair to use when scheduling the
work in the weekly/daily planning meetings, particularly the *Daytime
Weekly Integration* and *Weekly Summit Performance Status* meetings.

Notes are distributed via a Confluence page. This meeting is run by
the head of the **Summit** **Science** team and attendees include the
heads from various eng-ops groups. This is the meeting to go to bring
an activity that needs to be planned before the next *Daytime Quarterly
Review*.

* Confluence page: [Strategic Planning Meeting](https://rubinobs.atlassian.net/wiki/spaces/LSSTPO/pages/43244380/Strategic+Planning+Meeting) which includes meeting notes  
* Meetings currently happen weekly (see [RD1](#RD1)), but may switch to bi-weekly

(weekly-planning-meetings)=
  3. ### Weekly planning meetings

(the-daytime-weekly-integration-meeting)=
     1. #### The Daytime Weekly Integration Meeting

The *Daytime* *Weekly Integration* meeting happens once a week (see
[RD1](#RD1)) to go over what engineering work goes on at the telescope
the next week. It is run by the head of the **Summit Engineering** group,
with all technical day crew attending. This is the meeting where daytime
tasks are scheduled based on input from the *Weekly Test Planning* and
the *Summit Monthly Planning* meetings.  You can see the results by the
*Summit weekly planner* calendar on the Jira *summit* calendar. Other
calendars also show actions on a specific system: *Optical, Mechanical,
Electronics, Maintenance, Auxtel, Dome.* Such events usually overlap the
ones in the *Summit weekly planner* calendar, but not always. They do,
however, contain the Jira ticket the work is responding to. So for now,
if you want to know the eng-ops activities that happen at the telescope,
you’ll need to load the *Summit weekly planner* calendar plus the ones
for all the subsystems.

* Output: [Summit weekly calendars](https://rubinobs.atlassian.net/plugins/servlet/ac/doitbetter.calendar/calendar-page?project.key=SUMMIT&project.id=10053)  
* Meetings currently happen once a week (see [RD1](#RD1))


(the-weekly-summit-performance-status)=
  2. #### The Weekly Summit Performance Status 

The *Weekly Summit Performance Status* meeting occurs weekly and goes over
both daytime and nighttime tests.  The attendees are typically the summit
support and test scientists along with various department heads. They
have meeting notes which consist of the weekly plan on Confluence.
The meeting will likely evolve once there are less tests to be run and
the telescope is primarily run via the Feature Based Scheduler.

* Confluence page:  [Week Test Plan Meeting Notes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/68255748/Week+Test+Plan+Meeting+Notes)  
* Meetings currently happen once a week (see [RD1](#RD1))

(daily-planning-meeting:-daytime-briefing-meeting)=
  4. ### Daily planning meeting: Daytime Briefing meeting 

The *Daytime Briefing* meeting happens at the summit at the start of
every day. It is a 15–45 minute meeting, run by the deputy **Summit
Facility** head, where participants plan for that day’s work at the
summit. This meeting is principally conducted in Spanish.

The daily plan is informed by 

* The *Weekly Integration* meeting  
* The OBS Jira tickets from this week  
* The FRACAS Jira tickets with high criticality    
* How was work completed the day before  
* Systems performance optimization tasks

The operations triage manager doesn’t necessarily attend this
meeting. Still, the obs-ops representative (this is a role listed on [RD11](#RD11))
must attend with a summary of the triage tickets from the ongoing week
and an update on the events of the previous night.

Notes are distributed from this meeting at Slack
**\#summit-announce**. The Slack channel **\#rso-tailgate-coordination**
is used to organize which Operations representative will attend the
meeting and distribute the notes. This meeting is the handoff meeting
of the planning to the people implementing the work.

* Output: A thread in [**\#summit-announce**](https://rubin-obs.slack.com/archives/C07QCJ7F962)  
* This meeting happens at the start of each workday (see [RD1](#RD1))

(observatory-software-and-devops)=
  5. ### Observatory software and DevOps 

During operations, **Base and Summit DFs,** **DevOps** (see section 4.1),
and **Summit Software** (see [RD15](#RD15)) tasks will get added in the meetings
above through their groups’ attendees. Their work gets scheduled by
the data management associate director and the head of summit software in
their own group meetings. Work is announced in the **\#summit-announce**
Slack channel.

This work gets brought up in the weekly *Rubin Extended Computing
Activities Planning* (RECAP) meeting. There this work is scheduled and
progress reported as stakeholders for each activity are present at the
meeting. In general, most of the work is outlined under Jira tickets. A
notification goes to the product owner whenever a Jira ticket is created.

(summary)=
6. ### Summary

* Responsible

  * Site manager: day crew engineering work at the summit

  * Associate director of RDM, Head of OSW and Devops: software work that happens at the summit

* Input

  * Your representative at the *Strategic Planning* meeting

  * Tickets for software/DevOps work

* Output

  * The Rubin Jira calendar Summit weekly calendars has the work that is going on

  * Work is announced on Slack channel **\#summit-announce**

* Resolving problems:

  * See the responsible parties / your representatives to the *Summit Monthly Planning* meeting

* Handing over

  * Eng-ops work is handed over to people implementing them at the *Daily Briefing* meeting

  * Other daytime work gets handed over/announced at **\#summit-announce**

(planning-for-obs-ops-summit-work)=
  3. ## Planning for obs-ops summit work 

Daytime obs-ops summit activities consist of calibrations and preparing
for the nighttime obs-ops activities. This work includes getting the
telescope ready for nighttime observations (checking out the telescope
mount assembly, warming up the hexapods, opening the louvers, …).
Nighttime obs-ops activities will be guided by the feature-based planning
of the scheduler to meet LSST scientific goals. Early operations requires
tests and other observations to be performed during the night, requiring
significant preparation and planning for each night.

Each day the test planner (see [RD17](#RD17), currently the summit science support,
[RD11](#RD11)) produces a daily obs-ops plan that is published by 10:00 AM. This
plan has both the daytime and nighttime obs-ops activities in it. Because
it is published at the start of the day, this means the majority of it
is prepared the day before.

As the survey progresses and there are less tests to be performed during
the night and the daily calibrations are well-known, the project may
move away from the Zephyr Scale based workflow that produces the daily
obs-ops plan presented here. It will likely be replaced with a standard
daily plan.

(forming-the-daily-observatory-operations-plan)=
1. ### Forming the daily observatory operations plan 

The daily observatory operations (obs-ops) plan encompasses both
daytime and nighttime activities. This plan is a single **Zephyr Scale
Test Cycle** (see [RD3](#RD3), [RD35](#RD35)), which has all summit tasks broken into
individual Test Cases. This includes execution blocks for the Feature
Based Scheduler (FBS). As defined in [RD9](#RD9), this Test Cycle serves as the
authoritative obs-ops plan for the day.

There will be times when there are nighttime tests to be run or
maintenance to do on the telescope that can happen any time within a
certain window. The feature based scheduler will at times have something
to be said about when to schedule these tasks. For now, though, tests
aren’t run via the FBS, but in the future,  the test planner may enter
them into a scheduler configuration file. This file can be run all night,
meaning the scheduler will decide when to do the tests contained within
the configuration file. Right now, the FBS is not equipped to handle this.

So for now,  the scheduler can be disabled, then starting the scheduler
with a different configuration file for the test read in, then going
back to the normal scheduler when the test has been completed.  Or the
scheduler can be disabled, the test performed, then reenabling the
scheduler. The test planner decides which of these two mechanisms to use.

Targets of opportunity (ToOs) are handled in the Feature Based
Scheduler. The **Survey** **Scheduling** team updates the FBS with
the ToOs configurations.  The ToO advisory committee determines what
ToOs/triggers get observed. [RD34](#RD34) has the ToO processes documented.

The test planner must monitor relevant Slack channels, review meeting
notes, and often attend the meetings where nighttime activities are
discussed (see table 5-2). Most of the planning for the daily obs-ops
plan comes from the day before.  In the morning the test planner reviews
logs and optionally contacts the test and summit support scientists to
confirm which tests were completed successfully the previous night. Using
information from the **\#rso-test-planning** channel and the weekly
coordination meetings, the test planner assembles the daily obs-ops
plan. The triage manager also communicates pending triage tasks to the
test planner for inclusion into the daily obs-ops plan.

(calibrations)=
2. ### Calibrations 

Calibrations are taken every day.  They serve as a check on the camera
and the viability of the calibrations used.  The calibration system
has a dome-mounted screen and a flat field projector that has a common
beam projector that can illuminate the screen with white LED lights or
monochromatic light fed by a tunable laser.  The screen gets illuminated
by a reflector on the telescope that then reflects the light source to
the screen.  The system will also be used to obtain photon transfer curves
for the camera as well as the flats.  [RD13](#RD13) has the baseline
calibration plan, but it is undergoing revision in early operations.
It’s worth noting here that the calibration collimated beam projector
needs \~1 week of maintenance every half year. This work goes through
the CMMS system described above (section 5.2.1).

Calibrations need to be taken when the dome is dark.  For early
operations, calibrations are usually taken at the end of the night, before
the eng-ops work starts for the day.  Eventually, the dome will be dark
enough to take calibrations after the eng-ops work has been done before
nighttime observations start.  Calibration observations are specified
in a block of the daily obs-ops plan.  The daily calibrations currently
are three biases, three darks at different exposure times, three flats
for each filter, and a portion of a photon transfer curve (PTC). The PTC
takes hours to do, so that’s why it will be broken up into \~7 chunks
so it gets done in one week.  Ideally, each daily calibration will take
\~30 minutes to run and they will be taken at the same time every day.
Section 9.3 discusses how these data are used.

In addition to these daily calibrations, there will be more calibrations
(like monochromatic flats and collimated beam projector scans) taken on
a longer timescale. It is not yet sure what that timescale is: months,
quarters, or yearly.  These tasks take 4–6 hours to run, so could
likely be scheduled when the conditions at night make it impossible to
observe the sky.  There may be additional need for calibration data to
be taken. These requests get discussed in the normal planning obs-ops
scenario (discussed here) coming from the Calibration Products and
Production (CPP) group within RDM team **Algorithms and Pipelines**.
When weather conditions prevent dome opening, the observers can take
extra calibrations during the night.

The camera team tells the CPP when something changed on the camera that
may warrant new calibrations be taken. The CPP, when it determines a new
set of calibrations is needed, issues a Jira ticket and presents it at
the TAXICAB meeting, where the request is approved or not.  The TAXICAB
meeting has representatives from CPP,  RDM, and **Camera** teams.  The CPP
scientists investigate and issue a Jira ticket when a new calibration
set needs to be obtained, which is discussed at the usual nighttime
planning meetings (the weekly and the daily; see the next section).
[RD31](#RD31) has the list of the TAXICAB Jira tickets and their current status.

(meetings)=
3. ### Meetings

The daily obs-ops plan is the result of input from numerous meetings.
They each deal with different timescales: the quarterly to monthly,
the monthly to weekly, the weekly, and the daily. See table 5-2 below
and the flowchart figure 5-2.  If you have an obs-ops test you want
to get done, it’s best to raise it at the *Summit Monthly Planning*
meeting. If you need it done in the next couple of days, then post to
the **\#rso-test-planning** channel.

The test planner will generally overload the daily obs-ops plan with
more Test Cases than can be done on a given day. This is because the
amount of time needed to carry out each test, with errors and faults,
is not known, plus different tests may need different conditions. The
obs-ops plan is not necessarily meant to be done in order, although
there are blocks defined in daytime and nighttime. The OSs on shift
determine which Test Case to do next, sometimes contacting the remote
summit support scientist if needed.  In some cases, the obs-ops plan
contains low-priority tests that need to be done if the conditions do
not allow for adequate science exposures. This list is maintained by
the test planner, but it is up to the OSs to decide when to do a test.

You can observe the daily obs-ops plans at [RD9](#RD9). Documents [RD3](#RD3) and
[RD35](#RD35) show how you can create a Test Case for your test and have it
approved before it enters a Test Cycle. The Slack channels to discuss
a proposed and planned Test Case are: **\#rso-test-planning** and
**\#rso-observing-blocks**.  When a Test Case is submitted, a reviewer
is assigned to it.  When it’s approved, its status update gets changed
to *ready*.

*Table 5-2: A table of the core meetings that go into the nightly plan.  There are often other system sub-meetings that go into the weekly test meetings that are not included here.*

| TImescale | Meeting | Frequency | Chair | Output |
| ----- | ----- | ----- | ----- | ----- |
| **Quarter – Month** | Summit Monthly Planning Meeting | Weekly     | Deputy AD of RSO | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTPO/pages/43244380/Strategic+Planning+Meeting) |
| **Month – Week** | Rubin Extended Computing Activities Planning (RECAP) | Weekly | Calibration Consultant | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53739741/Weekly+Meetings) |
| **Week** | Weekly Summit Performance Status | Weekly  | Summit support scientist | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/68255748/Week+Test+Plan+Meeting+Notes) |
| **Week – Day** | Nighttime Plan Coordination | Weekly   | Summit support scientist | [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/53741775/SITCOM+Test+Planning+STP) |
| **Day** | Data Production Review | Daily | Head of RDM Data Production teams | Jira tickets, plus [Meeting minutes](https://rubinobs.atlassian.net/wiki/spaces/LSSTOps/pages/267223066/Weekly+On-sky+Issue+Summaries)  |
|  | **\#rso-test-planning** (Slack channel) | Daily | Test planner | Nightly plan: [RD9](#RD9) |
|  | Nighttime Briefing | Daily   | Test planner | Handover |

The test planner goes over the nightly part of the daily obs-ops plan
Test Cycle with the shift manager ([RD36](#RD36)) at the *Nighttime Briefing*
meeting. They in turn go over the nightly plan when the nighttime
observing specialists arrive. The test planner is not on call during
the night; the shift manager is responsible for the plan during the night.

![][image4]

*Figure 5-2: A summary of the obs-ops planning.*

If there is a call to cancel the nightly operations because of work
being done on the telescope / camera, that call happens at the *Nighttime
Briefing*, with input from RSO management.  The shift manager can cancel
the night after the *Nighttime Briefing* meeting, often consulting
with the remote summit support scientists and sometimes the subsystem
expert and RSO management in making the decision. Anyone can close the
telescope for safety reasons. If it’s a risk-balancing decision,
the shift manager refers to the subsystem expert for advice. If the
decision is a balance between risk and progress, the shift manager may
then call RSO management for the decision on whether to close or not.
[RD37](#RD37) has the procedure for who makes the call.

Each day after the daily obs-ops plan is handed over to the night crew an
automated message appears on **\#rso-test-planning** asking for requests
for the next night plan.


(summary-1)=
4. ### Summary

* Responsible

  * The test planner/ scheduler team

* Input

  * All the meetings in Table 5-2

* Output

  * The daily obs-ops plan is available at [RD9](#RD9)

* Resolving problems:

  * Test planner during the day, the shift manager during the night

* Handing over

  * *Nighttime Briefing* meeting

(implementing-eng-ops-summit-work)=
4. ## Implementing eng-ops summit work 

The deputy head of **Summit Facilities** runs the *Daytime Briefing*
at the start of the workday, where all the work for the day is being
discussed. Some daytime work gets handled remotely: software engineers
working on telescope and site software, who report their work via
**\#summit-announce**. Larger software efforts are discussed in the
*Daytime Briefing* meeting.

The shift manager ([RD36](#RD36)) is responsible for those at the telescope. During
the daytime, the shift manager is the **Summit Engineering** team lead.

The summit team includes the daytime engineering staff whose shift
is defined by the bus schedule, which arrives at the summit at 08:30
and departs 16:30 (see [RD2](#RD2)). They usually eat breakfast and start work
at 09:00.  Other summit teams are the operations team. These teams have
one daytime shift from 9:00 to 21:00 (see [RD2](#RD2)), although others working
on a specific project may adopt the same routine as the engineering staff.

Once the daily briefing completes at the start of the day, people go
about their work. The people doing the work will announce the start
of their work in the **\#summit-** channels of Slack if they believe
others will be affected by their work that day. This means not all work
is announced in the **\#summit-**  channels. If there is conflict within
the work being done that day, it is usually resolved by the person in
charge of the system, the head of **Summit Engineering,** or the summit
support scientist. You can reach them on the **\#\[subsystem\]-worklog**
Slack accounts and/or **\#summit-announce** if there’s a conflict that
needs resolving.

(version-control)=
1. ### Version control 

It’s important to capture the work that’s been done to maintain an
up to date look at the status of the hardware. Most work is recorded in
SUMMIT Jira tickets (see [RD4](#RD4)) and some of it makes its way to the CMMS,
to allow for maintenance, spare parts, and other updates. You can search
Jira tickets based on the subsystem to find the history of work on it.

Software version control is GitHub for source code and Argo CD
for tracking deployments. Argo CD is the system used to deploy and
maintain the configuration of many control system components and summit
services. Observers do not use Argo CD, so if a new software release has
to be deprecated during the night, they must go to the summit support
scientists or the appropriate observatory software (OSW) expert to do so.

(output)=
2. ### Output

The output of the *Daytime Briefing* is posted as notes in a thread of
**\#summit-announce**. This is where you can see what each day crew member
is working on that day.  As stated, most daytime activities are announced
on **\#summit-announce**. Some work on a given subsystem are reported on
the **\#worklog** Slack channels, although **\#daytime-tasks-worklog** is
not used in this capacity. It’s left as a future endeavor to have each
daytime activity mentioned in the Zephyr scale for notes/feedback from the
daytime/nighttime work. The best way to know what was worked on during
the day, which may help if there is troubleshooting during the night,
is to look at the daily tailgate notes in **\#summit-announce**. Work
on a Jira ticket (see [RD4](#RD4) and [RD5](#RD5)) gets acknowledged in Jira, as well.

(handover)=
3. ### Handover 

Handover occurs during the day. It occurs, nominally at a given time (see
[RD2](#RD2)) by the day crew. This is announced in **\#summit-announce**. During
the handover, the day crew ensures that everything is in working order
for the night time operations. The dome handover happens later to ensure
the dome is ready to operate for the night. The handover usually but does
not necessarily involve a member of the observing team; it is a check by
the day crew that things are ready to support night operations. There
is a Confluence checklist for the TMA handover ([RD32](#RD32)) and one for the
start of tests ([RD33](#RD33)). The daytime handover does not go over the work
done that day. See 5.4.2 for how to find out what work got done that day.

(summary-2)=
4. ###  Summary 

* Responsible

  * Deputy head of **Summit Facility** team

* Input

  * *Daytime Briefing* meeting

* Output

  * **\#summit-announce** has the results of the plan in a thread

* Resolving problems:

  * **\#summit-announce**

* Handing over

  * Occurs at the daily handover to the obs-ops crew

(implementing-obs-ops-summit-work)=
5. ## Implementing obs-ops summit work

This section describes the people involved in obs-ops summit work at
the summit.  It does not describe the work of operations; see [RD10](#RD10) for
a list of obs-ops procedures and documentation for telescope operations.

(who’s-at-the-summit)=
1. ### Who’s at the summit

The observing specialists (OS; discussed in [RD13](#RD13)) are those
responsible for executing the obs-ops daily plan. During the daytime,
the daytime OSs execute the plan, starting when the test planner releases
the plan at the start of their shift. They can contact the test planner
if there are any questions about the tasks within it.

At nighttime, the OS late shift executes the plan, as briefed by the
daytime OS shift manager when they start their shift. They are generally
the only ones at the summit at night, although sometimes there will be
engineering staff, summit support scientists, test scientists, or other
team members available. These additional staff will be on the summit,
based in La Serena control room, or remote. The shift manager is the
one who is aware of who is up at the summit and what they are doing there.

The Unified Summit Shift Schedule ([RD11](#RD11)) is a Google spreadsheet
that has the roles and their assigned schedules over a course of \~3
months. Each team leader maintains their respective tab, with team
members filling out their availability and the team leader assigning
shifts. When there’s not enough room at the summit the RSO associate /
deputy associate director will determine how many people for each group
(commissioning scientists, other subsystem teams) will be allowed at the
summit. The groups themselves self-organize to see which will go to the
summit and who will be remote. This allocation is subject to the RSO
AD’s approval. The guidelines for summit control room etiquette are
given in [RD14](#RD14). There are also policies for those supporting from remote
control rooms (La Serena, SLAC, Tucson; [RD42](#RD42)). The shift manager can
enforce guidelines if they aren't followed.

The observing specialists fill two shifts per day, each with two
OSs. First is the OS day shift role which starts at 9:00 and goes to
21:00.  One of the OSs is designated as the shift manager.  The second
late shift begins at 20:00 and goes to sunrise. These shift hours may
change with time. See [RD2](#RD2) for the current details.

(who’s-responsible)=
2. ### Who’s responsible 

Observing specialists oversee the execution of the daily obs-ops plan,
ensuring the system’s safe operations and stable performance. They
address any anomalies that occur during execution, calling for help as
needed. The roles, responsibilities, authority, and accountability are
given in [RD16](#RD16).  Their detailed logs are vital, offering debuggers the
necessary context to troubleshoot and implement solutions efficiently.

For nighttime operations, the de-facto model is to turn on the feature
based scheduler and then observe what it says. The feature based
scheduler page ([RD48](#RD48)) has links to dashboards ([RD46](#RD46)) describing why it
chose the next target. There is a pre-night simulation ([RD47](#RD47)) and links
to notebooks describing what happened any given night. Some of these
tools are still being developed during early operations.

As for other observations, not part of the survey, the scheduler can be
stopped and re-configured to execute them, or the tests can be executed
manually by the OSs, outside of FBS control (see section 5.3.1).  The OSs
use the guidance given in the obs-ops plan to decide when to do each
observation.  The summit support scientist offers technical advice if
need be.  If there is a need to deviate from the plan, they need to refer
to the Early Operations System Optimization Lead, who has the authority
to change the nightly plan.  Later on, the shift manager will have this
responsibility, often consulting with Slack channels or a manager on call.

The shift manager deals with any troubles implementing the plan or
conflict at the summit. The shift manager may consult with others in
making the decision, but has final decision-making authority while on
the summit. If any of the observing specialists can’t make it to the
summit, the shift manager makes a call in conjunction with the OS manager
(if available): see the shift manager and workflows responsibility page
([RD36](#RD36)). The OSs have a person designated as backup, so they’ll get
the call first.

(who’s-on-call)=
3. ### Who’s on call 

Section 6.5 discusses the call tree when something goes wrong.   

(handover-1)=
4. ### Handover

The observing specialists produce a detailed logging of what happens
over the night via OLE (the Observatory Logging Environment) and at
the end of the night produce a nightlog summary. You can get via the
**\#nightlog-bot** Slack channel and/or signing up on the email list at
[RD43](#RD43), or you can review it at the Nightly Digest that currently is at [RD6](#RD6).

Jira OBS tickets ([RD5](#RD5)) are filed for any faults found during the night.

The handover to the day crew occurs via the nightlog, updates in
Zephyr Scale, and end-of-night status messages posted to Slack channels
**\#summit-announce, \#summit-simonyi,** and **\#summit-auxtel**.

(summary-3)=
5. ### Summary

* Responsible

  * The shift manager

* Input

  * The daily obs-ops plan

* Output

  * The night log

* Resolving problems:

  * Observing Specialists, test scientists, shift manager, on-call support

* Handing over

  * The night log / summary

  ### 

(handling-a-problem-1)=
  6. ## Handling a problem

(system-problem-handling)=
     1. ### System problem handling

Problems related to the system are captured in FRACAS. Besides handling
issues as part of the corrective action process associated with
FRACAS, some problems demand more analysis so that's when the **Systems
Engineering** (SE) team does a more comprehensive failure mode, effects,
and criticality analysis (FMECA). The corrective actions that result
from FMECA are recorded as corrective maintenance activities in the
maintenance management system (see 5.2.1).

(doing-a-summit-test)=
2. ### Doing a summit test 

In the course of the problems’ analyses there may be a need for
some tests to be performed to help determine the cause of what they are
seeing. In some cases, these tests can be done on the data the observatory
is already collecting, so there is no need to go through the planning
for daytime or planning for nighttime procedures; they simply do their
tests with the data already collected.

Tests that require new data taken in a way that would not otherwise be
taken, could be day or night tests. When they have a test they want
to perform, they go through the planning for daytime and nighttime
procedures (see section 6\) to get it approved and put the test(s) into
the schedule. Typically, their tests are not highly time critical so
could be scheduled when the nighttime weather is not good for scientific
operations or when the dome is closed at night, or when there’s a
break in the daytime work. Critical tests get scheduled in the daytime
or nightly plan.

For non-critical nighttime tests, the observing specialists (OSs)
will have a list of tests that need to be done (as provided by the
test planner; see section 5.3), along with their priorities and required
conditions. OSs can then schedule them as they see fit. The test orgainzer
will configure the tests and bring them up through the planning for
nighttime observations process.  The test planner owns the list of
approved tests and lets the submitter know when the test has been done.

It is important for the time for on-sky nighttime tests to be done
consistent with what the scheduler allows for in its simulation.  One way
the survey scheduling team looks at this is by plotting metrics vs. time
(see figure 5-3).  So that way they can see if the survey is ahead or
behind schedule,  meaning more or less time for tests.

![][image5]

*FIgure 5-3: A simulated plot of g depth versus date (the black dots) plotted against a simulation. Here, you can see the survey is slightly ahead of where it should be.*

(communications)=
6. #  Communications

   

(communication-channels-and-etiquette)=
   1. ## Communication channels and etiquette 

Slack serves as the primary platform for internal communication at the
observatory. However, some of the groups of the extended family are not
as familiar with Slack as they are with other forms of communication:
email and WhatsApp being the other ones most commonly used.  To that end,
most important general announcements go both to email and Slack. Nothing
for general audiences go through WhatsApp.

Slack is very good for quick discussions, but other tools exist for
other purposes.  Formal requests should usually become Jira tickets
while formal guidelines/procedures should become Confluence pages or
other formal documentation.  Slack is not good at recording information
for posterity.

In general for all communication, please be kind with your
messages. Everyone is always working to do the right thing for the
observatory.  Do not send angry messages or complaints (direct such
complaints privately to a manager).  Also remember that many people
are not native English or Spanish speakers and come from all different
cultures.  Another reason to be kind; always assume the best of intentions
in the messages.

In some cases, people actually talk about things\!  Usually, if the
result of that conversation is something that concerns others, the talkers
should summarize the results of the conversation in a Slack channel.

(slack-channels)=
2. ## Slack channels

Although Slack also has a direct messaging capability, the observatory
encourages people to use the public channels instead. In that way, the
information being communicated is available to all who are interested
in it.  You can tag people in the channel message if you want them
to notice it directly, but please refrain from using @here or @channel
unless absolutely necessary to do so.  Almost every channel has bookmarks
and pins at the top. And clicking on the channel name will give you
information about the channel that usually includes what the topic of the
channel is.  These offer a quick solution to find relevant information
about the channel and its topic.

Because Slack is an important means for realtime communication, there is
a responsibility matrix for monitoring the slack channels, as shown in
figure 7-1 and 7-2.  By adhering to this, the Observatory ensures that
people who need to know what’s going on in Slack, do.

![][image6]*Figure 7-1: Who is responsible for monitoring what Slack channels. This figure can be found at [RD44](#RD44). The tiers are discussed in figure 7-2.*

![][image7]*Figure 7-2: A discussion of the tiers in the Slack channel referred to in figure 7-1.*

(squadcast)=
3. ## SquadCast

Problems involving systems not being worked on can occur during the day
and many systems have automated alarms through the Watcher service. A
visible notification of the error occurs in the control room in the
summit, but this room is not monitored by the engineering staff. So
such alarms are often first dealt with the RSO operations staff present
and/or the notifications that go out via SquadCast.  SquadCast is quite
configurable and there will be a manual that is being developed now
([RD45](#RD45)). SquadCast has a list of people to call during an emergency. It
can also be configured to create Jira tickets, create a slack channel,
send email, all with configurable messages.

(zoom)=
4. ## Zoom

Those working remotely connect to the summit control room with Zoom (the
link is available in the bookmarks of **\#summit-simonyi** channel). This
happens both day and night.  However, too many people talking at the Zoom
main channel at once can be disconcerting. In general, test scientists
discussing the data / what to do next, should use a breakout room and go
to another location if the noise will be a distraction to others in the
room. The main channel should be used for debugging / troubleshooting
discussions that involve the observing specialists.

(calling-for-help)=
5. ## Calling for help

   1. In emergencies

Any summit emergency not related to observing and summit operations
should be handled per the [RD40](#RD40) guide. This is to be used  for medical
emergencies, earthquakes, etc.  [RD40](#RD40) also has a link to [RD41](#RD41) form
that initiates a SquadCast calls for summit observing emergencies, but
should not be used for camera emergencies as the time limit for response
is greater than what can be gotten from SuadCast (\>2m).  For camera
emergencies, please contact the camera person as per the next section.

2. In non-emergencies

The Unified Summit Schedule ([RD11](#RD11)) has a list of remote people on call
for some topics. You can find this on the *Summary* tab for engineering
support during the night and the *Weekend* tab for the manager to call
on the weekends.

[RD38](#RD38) is a list of voluntary out-of-hours support contacts. The numbers
/ contact information for these people are in a 1Password vault that
the OSs have access to. Before calling someone on this list, the shift
manager is consulted first. Summit calls for DevOps are handled via a
work form at [RD39](#RD39).

(safety)=
7. #  Safety 

The Vera C. Rubin Observatory is committed to achieving the highest
performance in safety, health, and environmental management practices.
Its aim is to  create and maintain a safe and healthy working and
operating environment. The safety team, led by a dedicated safety manager
who is a member of the Directorate, implements and oversees the Rubin
Safety Policy ([RD49](#RD49)). The safety team also interacts with NOIRLab safety
as well, guaranteeing a uniform approach to safety.  The site specific
Safety, Health and Environmental (SHE) Plans ([RD50](#RD50), [RD51](#RD51)) contain
detailed guidelines for safe working conditions.  All people working on
Rubin Observatory are responsible for safe operations and should know
the Rubin Safety Policy ([RD49](#RD49)) and the local SHE for the site they are
operating at. **All personnel have the authority and obligation to report
hazards or pause work if safety is compromised (**[RD49](#RD49), section 6.5).

The safety standards are all stored in Docushare, both in English and
Spanish ([RD52](#RD52)). Similarly, there is a collection of procedures
for working with the mirrors ([RD53](#RD53)) and one with lockout-tagout
(LOTO) procedures ([RD54](#RD54)) with [RD55](#RD55) being the global
LOTO procedure..

During the night, the shift manager plays a safety role as well. They can
make the decision to evacuate the summit in case of inclement weather,
to close the telescope and dome in case of hazards to equipment or staff,
and are familiar with the emergency procedures outlined in observatory
operations documentation ([RD56](#RD56)). They are also responsible for
facilitating communication with the paramedics on summit and mountain
assistant in case of medical emergency.

Section 6.5 has the discussion of how to call when there is an emergency
at the summit.

# 

(understanding-data-quality)=
8. #  Understanding data quality 

This section deals with people and systems understanding data quality
to determine what actions, if any, need to happen in the coming daytime
or nighttime as a result. For example, it could mean data from a given
visit are bad and need to be re-taken or possibly an engineering test
or maintenance task must be performed to ensure data quality for the
next night.

(the-different-steps-of-understanding-data-quality)=
1. ## The different steps of understanding data quality

There are tools we use to assess data quality:

* The **ExposureLog**: Observers have the option to declare an exposure
good or bad in LOVE/OLE during the night.

* **Rapid analysis** (RA): RubinTV allows the user to see a rapid
reduction of the data as they are taken and assess for value. RubinTV
runs at the summit and USDF. See [RD7](#RD7) for a link.  The output of
RA is logged in ConsDB, but no assessment of the data is logged there.

* **Prompt processing** (PP): Prompt processing runs on the data
immediately after they are taken and is used to generate alerts.

* **Data release processing** (DRP): DRP does the long-term processing
of the data including the deep co-added imaging.

* **RDM** monitors data quality on a daily basis. See chapter 4\.

* **User input**: throughout the survey, users will look at the data
and may find some bad data. There is also the Exposure Checker which
outsources people looking at the data for artifacts. This is not yet
active, but a prototype with limited exposures was developed for LSSTCam
data.  The idea is to store the data from that into the ExposureLog.

(what-to-do-with-quality-assessments)=
  2. ## What to do with quality assessments

The scheduler automatically will retake bad data. The **Survey
Scheduling** team (under the Director’s Office **LSST** team) will
coordinate identification of bad data with DM, looking at the outputs
of RA/PP and DRP to determine if the data are bad or not.

Data that are bad that means something must be fixed during the day will
come from the observers via Jira obs- tickets and processed at the Daily
*Data Production Review* meeting. In addition, they may also identify
things that are going wrong that require system maintenance. Such work
will proceed along the lines of planning the eng-ops work (section 5.2).

At least for now, every user of quality assessments has their own
way of looking at the data and their assessments of the data are not
recorded anywhere. Additionally, a user looking at the data has no way
of informing everyone of a different assessment. The ExposureLog could
serve this purpose, but it’s not being used for this right now. The
ExposureLog keeps all entries for each exposure, but only the most recent
comment is declared active. So, it could be the source that has the one
official data assessment along with the full history of data assessments
by looking at the inactive comments.

(using-the-tools)=
3. ## Using the tools 

Data pipeline and its products are the face of Rubin Observatory the
public/scientists see. Here we discuss how they impact daily routines at
the summit. (For more information see [RD18](#RD18) and [RD19](#RD19) for
the design and definition document, [RD20](#RD20) for the paper on the
LSST science pipeline software, and [RD21](#RD21) for a practical getting
started with the pipeline website.)  Intra-night quick look analysis
happens in Rapid Analysis (real time, single frame measurement), Prompt
Processing which does the differential image analysis to generate alerts,
and the data pipeline processing that does the co-adds.

Additionally, cp\_verify  (alternatively called the Calibration Products
Production pipelines) will reduce daily calibrations and will tell
us if anything is wrong with the daily calibrations (6.3.2) which
could mean something from the camera has changed. Sometimes this is
normal and new master calibrations will need to be made; other times
it could highlight something changing non-accidentally, in which case
it needs to be addressed before the nighttime observations start. If
the camera changed purposefully, such changes follow the TAXICAB (the
Telescope and Auxiliary Instrumentation Calibration Acceptance Board; see
[RD27](#RD27)) process, so RDM should know about it. It’s also announced
on Slack **\#summit-simonyi**, **\#summit-auxtel.** During commissioning,
cp\_verify was run by hand every day. During the transition to operations,
it will be made to run automatically and alert the observers with Watcher
alarms when it notices a problem.

Rapid analysis provides quick single frame measurement reductions at
the summit and displays them via RubinTV. It is here OSs will look to
see the quality of the data they just took. In general, when the data
look bad, and there’s nothing the observers can do to fix it, they
keep on observing, as conditions allow. If there's a hardware item that
has gone wrong that could get worse if observing more, then they will
stop. Otherwise they keep on going and the scheduler and test planner
make the adjustments to future plans as needed. If the data are obviously
bad for all frames, then the OSs may stop observing and debug. If it’s
one or a few visits that are bad, the OSs may not even notice it (nor
are they required to) and will keep on taking data.

Quality control of data was done by hand during commissioning.
In operations, quality assessment will eventually be automated during
the night through rapid analysis, which will alert the OSs via Watcher
alarms when it notices something.  As part of this effort, these alarms
will be documented along with steps the OSs can take to see if they need
to stop taking data and fix something (like focusing the telescope).
Eventually, this documentation will handle all Watcher alarms.

Prompt processing prepares the alerts, in real time. OSs don’t
look at the results and if it fails, the default action is to keep on
observing. The RDM folks analyze prompt processing and feedback from it
generally means an action in RDM or occasionally, RDM will bring it to
RSO if an action is needed at the summit.

If prompt processing fails to complete in the required 60 s, the
observatory is not fulfilling its objective. The night crew continues
taking data, contacting the USDF alerts person if they note the problem,
while the USDF alerts person notices the problem and works on the
situation. This is discussed in section 4.2.

Data pipeline processing may signal slow, small effects of the system
that may need to be rectified before they turn into large effects. They
go through the standard implementing procedures to invoke action in
the end-ops or obs-ops plans. This is usually monitored by **CST**;
see section 4.2.

The Consolidated database (ConsDB) is a schema that contains information
for each exposure and visit (and each detector within those) taken
by the instrument. These data include observatory data from the FITS
image header metadata and measurements and metrics from Rapid Analysis
and other data processing.  It also includes telemetry data from the
telescope mount assembly for each visit/exposure that it gets from the
time-series engineering facilities database.  The ConsDB is maintained
by RDM and has a slack channel **\#consolidated-database** for questions
on using it or if you want new information to be added to it. The schema
is given by [RD25](#RD25) and a short tutorial and using it is provided in
[RD26](#RD26).

(people-in-roles)=
1. # People in roles

The staffing plan is given in [[RD13](#RD13)](#[RD13](#RD13)).  This
appendix has the people in some levels of the org chart as of the time
of this writing.

*Table A-1: The leads of the orgchart as of the time of this writing.*

| Role | Person |
| ----- | ----- |
| **Directorate** | Director of Operations: Bob Blum Deputy Director of Operations: Phil Marshall |
|   Safety | Sandra Romero Zenteno |
|   Program operations | Ranpal Gill |
|   In-kind program coordination | Aprajita Verma |
|   Legacy Survey of Space and TIme (LSST) | Zeljko Ivezic |
|   Survey scheduling | Lyyne Jones |
| **RSO** | Associate Director of Summit Operations: Sandrine Thomas Deputy: Kevin Reil |
|   Summit science | Kevin Reil Deputy: Bruno Quint |
|   Summit software | Michael Reuter |
|   Summit facility | Eduardo Serrano Deputy: Oscar Nuñez |
|   Nighttime operations | Eric Christensen |
|   Summit engineering | Roberto Tighe (interim) |
|   Camera | Travis Lange |
|   Systems engineering | Holger Drass |
| **RDM** | Associate Director of Data Management: Wil O’MullaneDeputy: Yusra AlSayyad Deputy: Frossie Economou |
|   U.S. data facilities | Adam Bolton |
|   France data facilities | Fabio Hernandez |
|   UK data facilities | George Beckett |
|   Chile facilities and long haul network | Cristian Silva |
|   Data abstraction | Tim Jenness |
|   Data production | Yusra AlSayyad |
|   Data services | Frossie Economou |
|   Verification and validation | Colin Slater |
|   Community science | Melissa Graham |
|   Lead Scientist | Leanne Guy |
| **EPO** | Head of Rubin Education and Public Outreach: Alan Strauss |
|   Technical | Group lead: Eric Rosas |
|   Education | Group lead: Ardis Herrold |
|   Outreach | Group lead: Kristen Metzger |
|   Citizen science | Group lead: Clare Higgs |

*Table A-2: People with various roles mentioned here as of the time of this writing.*

| Role | Person |
| ----- | ----- |
| Calibration Scientist | Eli Rykoff |
| Calibration Consultant | Robert Lupton |
| Chief Engineer | Doug Neill |
| Early Operations System Optimization Lead | Ketih Bechtol |
| SquadCast Lead | Cristian Silva |

[image1]: pix/orgchart.png

[image2]: <data:image/png;base64,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>

[image3]: <data:image/png;base64,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>

[image4]: <data:image/png;base64,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>

[image5]: pix/gdepthVStime.png

[image6]: pix/slackusage.png

[image7]: pix/slacktiers.png
