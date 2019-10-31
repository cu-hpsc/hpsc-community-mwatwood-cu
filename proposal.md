# Community Software Analysis Proposal

## Software: MOM6 (CESM)

CESM is fully coupled climate model including ocean, atmosphere land ice, and sea ice. Useful to climate scientists and climate interested programmers. The MOM6 ocean model will be used in the upcoming version of CESM and the group at NCAR is working on the integration.

### Stats

| Description | Your answer |
|---------|-----------|
| Repository URL |  https://github.com/NCAR/MOM6  |
| Main/documentation website |  https://www.gfdl.noaa.gov/mom-ocean-model/   |
| Year project was started | 1990 MOM / 2012 MOM6?  |
| Number of contributors in the past year | ~10 for NCAR MOM6 |
| Number of contributors in the lifetime of the project | 41 |
| Number of distinct affiliations | ? |
| Where do development discussions take place? | Github |
| Typical number of emails/comments per week? | Recently few   |
| Typical number of commits per week? | Recently few, usally ~20 |
| Typical commit size | ? |
| How does the project accept contributions? | pull requests   |
| Does the project have an automated test suite? | ? |
| Does the project use continuous integration? | ? |
| Are any legal/licensing steps required to contribute? | no |

### Install and run

Check the following boxes when complete or add a note below if you
encountered a problem.
- [ ] I have installed the software (MPAS-O Previously)
- [ ] I have run at least one example
- [ ] I have run the test suite
- [ ] The test suite passes

### Notes/concerns/risks

I am in personal contact with two developers at NCAR and will be using there help and guidance

#### Note on copyright
Students retain copyright on any work done in completion of a CU
course, so you are authorized to sign a [contributor license
agreement (CLA)](https://en.wikipedia.org/wiki/Contributor_License_Agreement),
affirm a [developer's certificate of
origin (DCO)](https://en.wikipedia.org/wiki/Developer_Certificate_of_Origin),
etc.  If you have concerns about this, please note them and/or reach
out to Jed directly.


# Follow-up for Specific Project
After making contact with the developers at NCAR ths seemed like a good project and particularly useful and appropriate to our class studies.

https://github.com/NCAR/MOM6/issues/129

Email correspondence idea:

OpenMP profiling: MOM6 can be run in parallel with (1) MPI or  (2) both MPI and OpenMP. Within CESM, we have been running MOM6 with MPI only. Currently, about 30% of runtime is spent on message passing, so I think hybrid parallelism (MPI+OpenMP) may be considerably more efficient. I've recently been working on debugging our OpenMP directives and was able to compile and run with MPI+OpenMP last week. The future tasks that need to be undertaken are (1) the assessment of performance benefits of MPI+OpenMP,  (2) optimizing MPI+OpenMP and looking for more opportunities for multithreading in the code, and (3) the assessment of correctness (e.g, verifying that no race condition exists among threads, etc. 