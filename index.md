# Summit Facility ConOps

```{toctree}
:maxdepth: 6
:numbered:
```

```{contents} Table of Contents
:depth: 5
```

(introduction)=
## Introduction 

This document outlines the practical implementation of summit operations
for Vera C. Rubin Observatory. It details the planning and execution of
work for both engineering operations (eng-ops; daytime) and observatory
operations (obs-ops; daytime and nighttime). These activities encompass
scheduled milestones such as maintenance, emergent repairs, and general
level-of-effort tasks. Guided by the organizational structure in {numref}`orgchart`,
this document provides a clear roadmap for the various departments,
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
### Operations organizational chart

```{figure} pix/orgchart.png
---
name: orgchart
align: center
---
*The organizational chart for Rubin operations.
Outside of the Director’s office are four departments, each containing
teams.  Each department has an Associate Director as the head, and
each team has a team lead. As of this writing, the System Performance
department has gone away, with the teams moving to other departments as
indicated by the red arrows. Additionally, the RDM Data Acquisition area
of responsibility has changed its name to Chile Facilities and Long Haul
Network.  We’ll update the organizational chart in the next release.*

```
{numref}`orgchart` shows the organizational chart for Rubin operations.  The
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
##  Director’s office

The Vera C. Rubin Observatory Director’s office is responsible for
overall management of the observatory and the survey as well as fulfilling
the mission of the observatory and realizing its vision.

(the-director’s-office-teams)=
### The Director’s office teams 

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


(data-management-in-operations)=
##  Data management in operations

The Rubin Data Management (RDM) department is responsible for the
development, maintenance, and operation of the networks, hardware, and
software infrastructure comprising the Rubin Observatory Data Management
System (see [RD23](#RD23)).  They are responsible for the generation
and archiving of prompt data products and periodic data releases.
They work with RSO to develop and deliver new software products that
affect summit operations and assess the quality of the data produced.


(the-dm-teams)=
### The DM teams

Within the DM department staff are organized into areas of
responsibilities  Within those areas are the teams.  The teams are
sometimes split into groups, responsible for the different framework
and cadences involved in data management. For example, the *Calibration
Products Production* group sits in the **Algorithms and Pipelines**
team along with two other groups *Alert Production* and *Data Release
Production*.  The **Algorithms and Pipelines** team sits in the **Data
Production** area of responsibility.  The organizational chart in {numref}`orgchart`
shows the areas of expertise and the teams within them; it does not
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
### Handling a problem

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
#### Data problem handling

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
what the solution is.  {numref}`problem-solve` outlines the process the CST uses to
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



```{mermaid} mermaid/community-problem-solving.md
---
caption: *A diagram of how problems are solved within the RDM CST.*
name: problem-solve
---
```

The DM/CST is staffed with members who have a direct interest in the
problem’s solution.   Since solutions often have cross-disciplinary
effects, CST includes or recruits representatives with the authority
to evaluate and approve work across all affected areas. In some cases
where the work affects the survey strategy or another survey metric,  the
AD of DM will often take it to the head of science for final approval.
The head of science may consult with his team and/or the Survey Cadence
Optimization Committee (SCOC), depending upon the nature of the request.


(summit-operations)=
## Summit operations 

This chapter will divide the summit operations work into engineering
operations (eng-ops) and observatory operations (obs-ops). The eng-ops
work is usually done during the daytime while the obs-ops work is largely
done at night, although during the day there is work done for calibrations
and preparing for the nighttime observations.

(the-rso-teams)=
### The RSO teams

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
### Planning for eng-ops summit work 

The eng-ops tasks consist of troubleshooting, fixing problems,
maintenance, and upgrades.  Planning for eng–ops work happens in four
phases ({numref}`daytime-planning` and table 5-1): the yearly/quarterly, the monthly,
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

```{mermaid} mermaid/daytime-planning.mmd
--- 
caption: *A summary of the eng-ops planning.*
name: daytime-planning
---
```

(yearly/quarterly-planning-meeting)=
#### Yearly/quarterly planning meeting

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
#### Monthly/weekly planning meeting: the Summit Monthly Planning meeting

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
#### Weekly planning meetings

(the-daytime-weekly-integration-meeting)=
##### The Daytime Weekly Integration Meeting

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
##### The Weekly Summit Performance Status 

The *Weekly Summit Performance Status* meeting occurs weekly and goes over
both daytime and nighttime tests.  The attendees are typically the summit
support and test scientists along with various department heads. They
have meeting notes which consist of the weekly plan on Confluence.
The meeting will likely evolve once there are less tests to be run and
the telescope is primarily run via the Feature Based Scheduler.

* Confluence page:  [Week Test Plan Meeting Notes](https://rubinobs.atlassian.net/wiki/spaces/LSSTCOM/pages/68255748/Week+Test+Plan+Meeting+Notes)  
* Meetings currently happen once a week (see [RD1](#RD1))

(daily-planning-meeting:-daytime-briefing-meeting)=
#### Daily planning meeting: Daytime Briefing meeting 

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
#### Observatory software and DevOps 

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
#### Summary

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
### Planning for obs-ops summit work 

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
#### Forming the daily observatory operations plan 

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
#### Calibrations 

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
#### Meetings

The daily obs-ops plan is the result of input from numerous meetings.
They each deal with different timescales: the quarterly to monthly,
the monthly to weekly, the weekly, and the daily. See table 5-2 below
and the flowchart {numref}`night-planning`.  If you have an obs-ops test you want
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

```{mermaid} mermaid/night-planning.mmd
---
caption: *A summary of the obs-ops planning.*
name: night-planning
---
```


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
#### Summary

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
### Implementing eng-ops summit work 

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
#### Version control 

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
#### Output

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
#### Handover 

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
####  Summary 

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
### Implementing obs-ops summit work

This section describes the people involved in obs-ops summit work at
the summit.  It does not describe the work of operations; see [RD10](#RD10) for
a list of obs-ops procedures and documentation for telescope operations.

(who’s-at-the-summit)=
#### Who’s at the summit

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
#### Who’s responsible 

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
#### Who’s on call 

Section 6.5 discusses the call tree when something goes wrong.   

(handover-1)=
#### Handover

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
#### Summary

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
### Handling a problem

(system-problem-handling)=
#### System problem handling

Problems related to the system are captured in FRACAS. Besides handling
issues as part of the corrective action process associated with
FRACAS, some problems demand more analysis so that's when the **Systems
Engineering** (SE) team does a more comprehensive failure mode, effects,
and criticality analysis (FMECA). The corrective actions that result
from FMECA are recorded as corrective maintenance activities in the
maintenance management system (see 5.2.1).

(doing-a-summit-test)=
#### Doing a summit test 

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
(see {numref}`gdepthvstime`).  So that way they can see if the survey is ahead or
behind schedule,  meaning more or less time for tests.

```{figure} pix/gdepthVStime.png
---
name: gdepthvstime
align: center
---
*A simulated plot of g depth versus date (the black dots) plotted against a simulation. Here, you can see the survey is slightly ahead of where it should be.*
```

(communications)=
##  Communications


(communication-channels-and-etiquette)=
### Communication channels and etiquette 

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
### Slack channels

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
{numref}`slackusage` and {numref}`slacktiers`.  By adhering to this, the Observatory ensures that
people who need to know what’s going on in Slack, do.

```{figure} pix/slackusage.png
---
name: slackusage
align: center
---
*Who is responsible for monitoring what Slack
channels. This figure can be found at [RD44](#RD44). The tiers are
discussed in {numref}`slacktiers`.*
```

```{figure} pix/slacktiers.png
---
name: slacktiers
align: center
---
*A discussion of the tiers in the Slack channel
referred to in {numref}`slackusage`.*
```

(squadcast)=
### SquadCast

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
### Zoom

Those working remotely connect to the summit control room with Zoom (the
link is available in the bookmarks of **\#summit-simonyi** channel). This
happens both day and night.  However, too many people talking at the Zoom
main channel at once can be disconcerting. In general, test scientists
discussing the data / what to do next, should use a breakout room and go
to another location if the noise will be a distraction to others in the
room. The main channel should be used for debugging / troubleshooting
discussions that involve the observing specialists.

(calling-for-help)=
### Calling for help

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
##  Safety 

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

(understanding-data-quality)=
##  Understanding data quality 

This section deals with people and systems understanding data quality
to determine what actions, if any, need to happen in the coming daytime
or nighttime as a result. For example, it could mean data from a given
visit are bad and need to be re-taken or possibly an engineering test
or maintenance task must be performed to ensure data quality for the
next night.

(the-different-steps-of-understanding-data-quality)=
### The different steps of understanding data quality

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
### What to do with quality assessments

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
### Using the tools 

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
## People in roles

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

(reference-documents)=
## Reference documents 

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

