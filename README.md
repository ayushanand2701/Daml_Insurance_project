# 🛠️ Daml_Insurance_company 🛠️ 
DamlMeetup is an application built on DAML that offers a platform for Insurance management and diffe policy rent organization.

### I. Overview 
This project was created by using the `empty-skeleton` template. Invite/Accept design pattern is used to create this DAML application.
The insurance application system is designed to facilitate the management of insurance policies between customers (policy applicants) and insurers (insurance companies). It provides a structured workflow for applying for, accepting, renewing, canceling, and managing insurance policies.
              


### II. Workflow
1.	Customer (policy applicant):
2.	Submit an insurance application.
3.	Accept or reject an insurance proposal.
4.	Renew an existing insurance policy.
5.	Cancel an insurance policy during the free period.
6.	Insurer (insurance company):
7.	Provide a quote for an insurance application.
8.	Initiate a medical checkup request for the customer.
9.	Terminate an insurance policy.
10.	Approve the cancellation of an insurance policy.
11.	Confirm payments made by the customer.

### III. Challenge(s)
* The project was created by using `empty-skeleton` and the following was removed from `daml.yaml`:
```
sandbox-options:
   - --wall-clock-time
```
and the following was added:

```
exposed-modules:
  - Main
```
For more info, check out [this post](https://discuss.daml.com/t/sandbox-options-wall-clock-time/5692/16?u=cathy_jung) on Daml Forum and [Daml Doc](https://docs.daml.com/tools/navigator/index.html?&_ga=2.48248804.337210607.1673989679-241632404.1672853064&_gac=1.17025355.1673455980.CjwKCAiA2fmdBhBpEiwA4CcHzfI2w1_D95zAr3_d6QTypOMXGTpUxtS06c55inucNwZvUZn4AebsJxoCZEgQAvD_BwE&_gl=1*elem6v*_ga*MjQxNjMyNDA0LjE2NzI4NTMwNjQ.*_ga_GVK9ZHZSMR*MTY3Mzk5NDQzOS4zMS4xLjE2NzM5OTQ3MDcuMC4wLjA.#logging-in-as-a-party).


### IV. Compiling & Testing
To compile and test, run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```

Test coverage report
```
$ daml test --show-coverage



Test Summary:-------

daml/Test.daml:setup: ok, 0 active contracts, 0 transactions.
daml/Test.daml:enquiry: ok, 2 active contracts, 23 transactions.
Modules internal to this package:
- Internal templates
  6 defined
  6 (100.0%) created
  internal templates never created: 0
- Internal template choices
  17 defined
  9 ( 52.9%) exercised
  internal template choices never exercised: 8
    Insurance:InsruancePolicy:Archive
    Insurance:InsruanceProposal:Archive
    Insurance:InsuranceApplication:Archive
    Insurance:MedicalRequisition:Archive
    Insurance:Payment:Archive
    Insurance:RefundProposal:Archive
    Insurance:InsuranceApplication:SubmitApplication
    Insurance:InsruancePolicy:TerminatePolicy
- Internal interface implementations
  0 defined
    0 internal interfaces
    0 external interfaces
- Internal interface choices
  0 defined
  0 (100.0%) exercised
  internal interface choices never exercised: 0
Modules external to this package:
- External templates
  0 defined
  0 (100.0%) created in any tests
  0 (100.0%) created in internal tests
  0 (100.0%) created in external tests
  external templates never created: 0
- External template choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external template choices never exercised: 0
- External interface implementations
  0 defined
- External interface choices
  0 defined
  0 (100.0%) exercised in any tests
  0 (100.0%) exercised in internal tests
  0 (100.0%) exercised in external tests
  external interface choices never exercised: 0
